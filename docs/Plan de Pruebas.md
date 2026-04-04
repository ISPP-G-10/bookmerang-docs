# Plan de Pruebas de Software: Bookmerang

## 1. Objetivos y Alcance

### 1.1. Objetivos

El propósito de este documento es definir la estrategia y el plan de pruebas para el proyecto Bookmerang, con el fin de garantizar la máxima calidad, fiabilidad y robustez de la aplicación antes de su despliegue.

Los objetivos principales son:
- **Validar la Correctitud Funcional:** Asegurar que todas las características de la aplicación operan según los requisitos especificados.
- **Garantizar la Integridad del Sistema:** Verificar que los componentes del frontend y el backend se comunican de manera fluida y sin errores.
- **Asegurar una Experiencia de Usuario Óptima:** Identificar y eliminar cuellos de botella, errores de usabilidad y fallos que puedan afectar negativamente al usuario.
- **Establecer un Marco para la Regresión:** Crear una suite de pruebas automatizadas que prevenga la introducción de nuevos errores en futuras actualizaciones.

### 1.2. Alcance

Este plan cubre los siguientes niveles de prueba:

- **Pruebas de Integración (Backend):** Enfocadas en la interacción entre los servicios, la lógica de negocio, los controladores de la API y la capa de persistencia de datos.
- **Pruebas End-to-End (E2E):** Enfocadas en la validación de flujos de usuario completos desde la interfaz gráfica (frontend) hasta la base de datos (backend).
- **Pruebas No Funcionales:** Consideraciones iniciales sobre rendimiento y seguridad.

**Fuera del Alcance:** Las pruebas unitarias de componentes aislados y las pruebas de aceptación de usuario (UAT) se gestionan en documentos o procesos separados.

---

## 2. Estrategia General de Pruebas

### 2.1. Pirámide de Pruebas Aplicada

Bookmerang adopta el modelo de la pirámide de pruebas para optimizar el esfuerzo y la eficacia. La base de la pirámide (no cubierta en este documento) son las **pruebas unitarias**, rápidas y numerosas. El centro lo ocupan las **pruebas de integración**, que validan la colaboración entre componentes. La cima la forman las **pruebas E2E**, menos numerosas pero cruciales para validar el sistema completo.

### 2.2. Entornos de Prueba

- **Entorno de Desarrollo Local:** Los desarrolladores ejecutan pruebas unitarias y de integración en sus máquinas locales. Las pruebas de integración utilizan **Testcontainers** para levantar servicios (ej. PostgreSQL) en contenedores Docker, garantizando un entorno limpio y aislado.
- **Entorno de Integración Continua (CI):** En cada Pull Request, un pipeline automatizado (ej. GitHub Actions) ejecuta la totalidad de las pruebas unitarias y de integración para asegurar que los nuevos cambios no rompen la funcionalidad existente.
- **Entorno de Staging/Pre-producción:** Un entorno idéntico a producción donde se ejecutarán las pruebas E2E y las pruebas no funcionales antes de cada despliegue.

---

## 3. Pruebas de Integración (Backend)

Estas pruebas son fundamentales para garantizar que la lógica de negocio y la infraestructura del backend funcionan como un sistema cohesivo.

### 3.1. Arquitectura y Herramientas

- **Framework de Pruebas:** **xUnit** es el estándar para la definición y ejecución de tests en el ecosistema .NET del proyecto.
- **Base de Datos de Prueba:** Se utiliza **Testcontainers con PostgreSQL**. Esta elección es crítica, ya que permite probar contra una base de datos real y efímera. El proveedor de base de datos **Npgsql** es utilizado por Entity Framework Core para traducir las consultas de LINQ a SQL compatible con PostgreSQL, validando no solo la lógica de la aplicación, sino también el SQL generado y la correcta configuración de los mapeos.
- **Simulaciones (Mocks):** La librería **Moq** se emplea para aislar las dependencias externas (ej. servicios de terceros) que no son objeto de la prueba de integración.

### 3.2. Cobertura de Pruebas por Módulo Funcional

#### 3.2.1. Módulo de Autenticación y Usuarios (`Auth`)
- **Objetivo:** Validar el registro, inicio de sesión y la gestión de perfiles de usuario.
- **Flujos Validados:**
    - Creación de un usuario y su correspondiente persistencia en la base de datos.
    - Verificación de que un usuario con un Supabase ID duplicado no puede ser creado.
    - Correcta gestión del estado del perfil (activo, incompleto).
- **Ubicación:** `Bookmerang.Tests/Auth/`

#### 3.2.2. Módulo de Libros (`Books`)
- **Objetivo:** Asegurar la correcta gestión del ciclo de vida de un libro.
- **Flujos Validados:**
    - Persistencia de un libro con todos sus atributos (ISBN, título, estado, etc.).
    - Correcto mapeo de tipos `Enum` como `BookStatus` y `BookCondition`.
    - Asociación de un libro con sus géneros e idiomas correspondientes en las tablas intermedias.
    - Validación a nivel de API de que solo el propietario de un libro puede modificarlo o eliminarlo.
- **Ubicación:** `Bookmerang.Tests/Books/`

#### 3.2.3. Módulo de Intercambios (`Exchanges` y `Matcher`)
- **Objetivo:** Probar la lógica central de la aplicación: el sistema de matching y la formalización de intercambios.
- **Flujos Validados:**
    - El servicio de `Matcher` devuelve correctamente los libros candidatos basándose en las preferencias y la geolocalización del usuario.
    - Creación de un `Match` cuando dos usuarios muestran interés mutuo.
    - El sistema gestiona correctamente la creación de un `Exchange` a partir de un `Match`.
    - Validación de los cambios de estado de los libros (`PUBLISHED` -> `RESERVED` -> `EXCHANGED`) durante el proceso de intercambio.
- **Ubicación:** `Bookmerang.Tests/Matcher/`, `Bookmerang.Tests/Exchanges/`

#### 3.2.4. Módulo de Comunidades (`Communities`)
- **Objetivo:** Validar la gestión de comunidades, librerías y eventos.
- **Flujos Validados:**
    - Un usuario puede crear y unirse a una comunidad.
    - Creación y gestión de librerías dentro de una comunidad.
    - Programación y gestión de `Meetups` (eventos) asociados a una comunidad.
- **Ubicación:** `Bookmerang.Tests/Communities/`

---

## 4. Pruebas End-to-End (E2E)

Las pruebas E2E son la validación definitiva de la experiencia del usuario, simulando flujos completos a través de la interfaz gráfica.

### 4.1. Estado Actual y Estrategia de Implementación

**Estado Actual:** El proyecto carece de un framework de pruebas E2E. Las pruebas de frontend existentes se limitan a la validación de componentes individuales con Jest.

**Estrategia Propuesta:**
1.  **Selección de Herramienta:** Se recomienda la adopción de **Cypress** por su robustez, excelente documentación y capacidades de depuración visual ("time-travel").
2.  **Integración en CI/CD:** Las pruebas E2E se integrarán en el pipeline de CI/CD para ser ejecutadas automáticamente contra el entorno de `Staging` antes de cualquier despliegue a producción.
3.  **Desarrollo Iterativo:** Se comenzará por los flujos más críticos (happy paths) y se expandirá la cobertura iterativamente.

### 4.2. Casos de Prueba E2E Prioritarios

A continuación, se detallan los flujos de usuario críticos a ser automatizados, descritos en formato Gherkin.

#### Flujo 1: Registro y Onboarding de un Nuevo Usuario
```gherkin
Feature: Registro de Usuario

  Scenario: Un nuevo visitante se registra y completa su perfil
    Given un visitante anónimo en la página de inicio
    When hace clic en "Registrarse"
    And rellena el formulario de registro con datos válidos y lo envía
    Then es redirigido a la página de "Bienvenida" o "Configuración Inicial"
    When configura sus géneros literarios preferidos
    And establece su ubicación para el matching
    And guarda su configuración
    Then su perfil se muestra como completo y puede acceder a la funcionalidad principal
```

#### Flujo 2: Ciclo de Vida Completo de un Libro
```gherkin
Feature: Gestión de Libros

  Scenario: Un usuario sube, edita y finalmente elimina un libro
    Given un usuario autenticado en su panel de control
    When navega a la sección "Mis Libros" y hace clic en "Subir Libro"
    And completa el formulario con los detalles del libro (ISBN, título, fotos, estado)
    And guarda el libro
    Then el nuevo libro aparece en su lista de "Libros Publicados"
    When hace clic en "Editar" en el libro recién creado
    And cambia el campo "Observaciones" y guarda los cambios
    Then el campo "Observaciones" del libro se muestra actualizado
    When hace clic en "Eliminar" en el mismo libro y confirma la acción
    Then el libro ya no aparece en su lista
```

#### Flujo 3: El "Happy Path" del Intercambio
```gherkin
Feature: Intercambio de Libros

  Scenario: Dos usuarios hacen match y completan un intercambio
    Given "Usuario A" y "Usuario B" están autenticados y han subido libros
    And las preferencias y ubicaciones de ambos usuarios son compatibles

    When "Usuario A" navega al Matcher y ve un libro de "Usuario B"
    And desliza a la derecha (like) sobre el libro de "Usuario B"
    
    When "Usuario B" navega al Matcher y ve el libro de "Usuario A" por el que "Usuario A" mostró interés
    And desliza a la derecha (like) sobre el libro de "Usuario A"
    
    Then ambos usuarios reciben una notificación de "Nuevo Match"
    And se crea una nueva conversación en su sección de Chats

    When "Usuario A" abre el chat con "Usuario B"
    And envía un mensaje para coordinar la entrega
    And "Usuario B" responde al mensaje
    And ambos usuarios hacen clic en "Aceptar Intercambio" en el chat
    
    Then el estado de ambos libros cambia a "Intercambiado"
    And ya no aparecen disponibles en el Matcher para otros usuarios
```

---

## 5. Pruebas No Funcionales

Aunque el foco principal de esta fase son las pruebas funcionales, es vital establecer una base para las pruebas no funcionales.

### 5.1. Pruebas de Rendimiento
- **Objetivo:** Identificar cuellos de botella y asegurar que la aplicación responde de manera ágil bajo carga.
- **Estrategia Inicial:**
    - **Pruebas de Carga en API:** Utilizar herramientas como **k6** o **JMeter** para simular peticiones concurrentes a los endpoints más críticos de la API (ej. `GET /api/matcher`, `POST /api/exchanges`).
    - **Métricas Clave:** Tiempo de respuesta (latencia), peticiones por segundo (throughput), tasa de error.

### 5.2. Pruebas de Seguridad
- **Objetivo:** Identificar y mitigar vulnerabilidades de seguridad comunes.
- **Estrategia Inicial:**
    - **Análisis Estático (SAST):** Integrar herramientas en el pipeline de CI que analicen el código fuente en busca de patrones de vulnerabilidad conocidos (ej. **SonarCloud**, **Snyk**).
    - **Revisión de Dependencias:** Utilizar herramientas como **GitHub Dependabot** para detectar y alertar sobre vulnerabilidades en las librerías de terceros utilizadas en el proyecto.
    - **Validación de Autorización:** Asegurar mediante pruebas de integración que los endpoints de la API validan correctamente los permisos del usuario (ej. un usuario no puede editar o eliminar un libro que no le pertenece).
