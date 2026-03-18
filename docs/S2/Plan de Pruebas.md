<div align="center">

<h1>Plan de Pruebas</h1>

<p style="font-size: 1.2em; margin-top: -10px;">
  <strong>Bookmerang</strong>
</p>

<br/>

<picture>
  <source media="(prefers-color-scheme: dark )"
          srcset="../assets/img/logo-bookmerang-dark.png">
  <source media="(prefers-color-scheme: light )"
          srcset="../assets/img/logo-bookmerang-light.png">
  <img
    src="../assets/img/logo-bookmerang-light.png"
    alt="Bookmerang logo"
    width="320"
  />
</picture>

<br/><br/>

<hr style="width: 60%;"/>

<br/>

<div style="
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 20px;
  text-align: center;
">

  <div>
    <picture>
      <source media="(prefers-color-scheme: dark )"
              srcset="../assets/img/us-etsi-inf-dark.png">
      <source media="(prefers-color-scheme: light )"
              srcset="../assets/img/us-etsi-inf-light.png">
      <img
        src="../assets/img/us-etsi-inf-light.png"
        alt="ETSII – Universidad de Sevilla"
        width="180"
      />
    </picture>
  </div>

  <div style="max-width: 360px;">
    <p style="margin: 0; line-height: 1.6;">
      <strong>Asignatura:</strong> ISPP (Curso 2025/26)<br/>
      <strong>Grupo:</strong> C Tarde — <em>Bookmerang</em><br/>
      <strong>Grado:</strong> Ingeniería del Software<br/>
      <strong>Centro:</strong> ETSII — Universidad de Sevilla
    </p>
  </div>

</div>

</div>

<hr/>

## Índice

- [1. Historial de Versiones](#1-historial-de-versiones)
- [2. Alcance de las Pruebas](#2-alcance-de-las-pruebas)
- [3. Backend (.NET C# / Bookmerang.Api)](#3-backend-net-c--bookmerangapi)
  - [3.1 Módulo: Autenticación (Auth)](#31-módulo-autenticación-auth)
  - [3.2 Módulo: Gestión de Libros (Books & Genres)](#32-módulo-gestión-de-libros-books--genres)
  - [3.3 Módulo: Matcher (Sistema de Emparejamiento)](#33-módulo-matcher-sistema-de-emparejamiento)
  - [3.4 Módulo: Intercambios y Chats (Exchanges & Chats)](#34-módulo-intercambios-y-chats-exchanges--chats)
  - [3.5 Módulo: Preferencias de Usuario (UserPreferences)](#35-módulo-preferencias-de-usuario-userpreferences)
- [4. Frontend (React Native / Expo)](#4-frontend-react-native--expo)
  - [4.1 Módulo: Autenticación (AuthContext & authService)](#41-módulo-autenticación-authcontext--authservice)
  - [4.2 Módulo: Subida de Libros (Book Upload)](#42-módulo-subida-de-libros-book-upload)
  - [4.3 Módulo: Interfaz de Emparejamiento (Matcher)](#43-módulo-interfaz-de-emparejamiento-matcher)
  - [4.4 Módulo: Chats y Comunicación](#44-módulo-chats-y-comunicación)
  - [4.5 Módulo: Ajustes y Perfil](#45-módulo-ajustes-y-perfil)
- [5. Estrategia de Ejecución y Herramientas](#5-estrategia-de-ejecución-y-herramientas)
- [6. Resumen de Calidad (Criterios de Éxito)](#6-resumen-de-calidad-criterios-de-éxito)

---

## 1. Historial de Versiones

| Versión | Fecha       | Participantes | Resumen de los cambios |
|:------:|:-----------:|---------------|-----------------------|
| v1.0   | 18/03/2026  | Julián Romero Parejo, Alejandro Vela Molina | Creación inicial del documento a partir de TEST_PLAN.md |

---

Este documento define el plan de pruebas exhaustivo para la aplicación Bookmerang, enfocándose exclusivamente en **pruebas unitarias** e **integración**, basándose en los módulos existentes del backend y frontend.

---

## 2. Alcance de las Pruebas

El objetivo de este plan de pruebas es garantizar el correcto funcionamiento de la lógica de negocio, la integridad de los datos, el flujo de estado de la interfaz de usuario y la comunicación efectiva entre el cliente frontend (React Native/Expo) y la API backend (.NET).

---

## 3. Backend (.NET C# / Bookmerang.Api)

**Metodología y Arquitectura de Pruebas:**
El proyecto `Bookmerang.Tests` establece un estándar robusto mediante el uso de:
*   **xUnit:** Framework principal para la definición y ejecución de pruebas (uso de `[Fact]` y `[Theory]`).
*   **Moq:** Herramienta para crear mocks de dependencias, como `ILogger` o `IChatService`.
*   **Base de datos en Memoria (`Microsoft.EntityFrameworkCore.InMemory`):** Utilizada para pruebas puramente de lógica de negocio (ej. `MatcherServiceTests`), lo cual permite la ejecución rápida de tests aislados donde no se requieren extensiones específicas de base de datos.
*   **Testcontainers (`Testcontainers.PostgreSql`):** Empleado de manera crítica para **pruebas de integración avanzadas** (ej. `PostgresMatcherFixture.cs`). Se instancia dinámicamente una imagen de PostgreSQL con la extensión PostGIS (`postgis/postgis:16-3.4`).
*   **Ejecución de Migraciones de Supabase:** En lugar de depender de Entity Framework migrations de manera tradicional, la fixture de Testcontainers busca recursivamente y ejecuta los archivos `.sql` nativos desde la carpeta `supabase/migrations` (ej. `0001_extensions.sql`, `0002_schema.sql`).
*   **NetTopologySuite & Mapeo de Enums (Npgsql):** Configurado directamente en el `NpgsqlDataSource` de pruebas para asegurar una replicación exacta del entorno real de producción, vital para las funcionalidades geoespaciales (distancia entre usuarios) y los numerosos enums definidos (`ChatType`, `MatchStatus`, etc.).

### 3.1 Módulo: Autenticación (Auth)
**Pruebas Unitarias:**
*   **Validación de Credenciales:** Probar escenarios de inicio de sesión exitoso, contraseña incorrecta y usuario no existente.
*   **Registro de Usuarios:** Verificar la creación de la entidad usuario y fallos controlados ante duplicidad de correos (`ValidationException`).

**Pruebas de Integración:**
*   **Flujo Completo de Auth:** Enviar peticiones HTTP validando la persistencia real del usuario en la base de datos de Testcontainers (AppDbContext).

### 3.2 Módulo: Gestión de Libros (Books & Genres)
**Pruebas Unitarias:**
*   **Validación de Entidades:** Verificar que los modelos DTO de creación de libro rechacen datos incompletos.
*   **Obtención de Libros:** Mockear el repositorio con InMemoryDatabase para asegurar que `BookService` devuelve la lista correcta paginada.

**Pruebas de Integración:**
*   **CRUD de Libros:** Utilizar la fixture de Testcontainers para verificar que los libros insertados se asocian de manera correcta en la base de datos a sus respectivos propietarios y géneros. Se debe respetar el mapeo de Enums (ej. `BookStatus`, `BookCondition`).

### 3.3 Módulo: Matcher (Sistema de Emparejamiento)
**Pruebas Unitarias (Metodología actual en `MatcherServiceTests.cs`):**
*   **Lógica Matemática y de Negocio:** Evaluar que el `MatcherService` calcule correctamente fórmulas puras (ej. fórmula de distancia usando el componente de radio `Math.Max(0.0, 1.0 - distance / radioMeters)`).
*   **Prevención de Overflows:** Confirmar que no hay desbordamiento en la paginación (`skip`).
*   **Algoritmo de Intercalado:** Validar `MatcherService.InterleaveBooks` para comprobar que respeta el `PriorityToDiscoveryRatio` al mezclar listas de libros, incluso cuando una de las listas está vacía.

**Pruebas de Integración (Metodología actual en `PostgresMatcherFixture.cs`):**
*   **Cálculo de Distancia Geoespacial (PostGIS):** Verificar emparejamientos y distancias exactas instanciando el servicio `MatcherService` acoplado al `AppDbContext` respaldado por el Testcontainer con NetTopologySuite.
*   **Generación de Matches en DB:** Simular un escenario de doble "Like" entre usuarios y confirmar la transición de enums (`MatchStatus`).

### 3.4 Módulo: Intercambios y Chats (Exchanges & Chats)
**Pruebas Unitarias:**
*   **Creación de Intercambio:** Validar (usando Moq para dependencias externas) que no se pueda iniciar un intercambio si no existe previamente un "Match" válido.
*   **Transición de Estados:** Validar los cambios de estado (ej. `ExchangeStatus.Pending` a `ExchangeStatus.Accepted`).

**Pruebas de Integración:**
*   **Persistencia de Historial de Chat:** Insertar mensajes en la base de datos contenedorizada verificando el orden de recuperación. Validar el mapeo del enum `ChatType`.

### 3.5 Módulo: Preferencias de Usuario (UserPreferences)
**Pruebas Unitarias:**
*   **Actualización y Redistribución:** Como se ve en `MatcherServiceTests.cs`, asegurar que la redistribución de pesos (genre, extension, distance, recency) se calcule correctamente cuando el usuario no define preferencias de género.

**Pruebas de Integración:**
*   **Persistencia Geográfica:** Actualizar preferencias de distancia en la DB de pruebas y comprobar que PostGIS almacena y recupera las coordenadas y límites correctamente.

---

## 4. Frontend (React Native / Expo)

### 4.1 Módulo: Autenticación (AuthContext & authService)
**Pruebas Unitarias:**
*   **Flujo del AuthContext:** Usar `React Testing Library` para simular llamadas al método `login` del Contexto y verificar si el estado cambia a "autenticado".
*   **Gestión de Sesión:** Verificar (mockeando AsyncStorage/SecureStore) que el token JWT se guarda y se recupera correctamente al inicializar la app.
*   **Validaciones Visuales:** Validar que los formularios de Login (`app/login.tsx`) y Register (`app/register.tsx`) muestren errores visuales ante emails inválidos o contraseñas cortas.

**Pruebas de Integración:**
*   **Mockeo de API HTTP:** Interceptar llamadas a `authService.ts` mediante `MSW` (Mock Service Worker) y probar que al recibir un `200 OK` del backend mockeado, la aplicación navegue a `(tabs)`.

### 4.2 Módulo: Subida de Libros (Book Upload)
**Pruebas Unitarias:**
*   **Validaciones (bookUploadValidation.ts):** Llamar a las funciones de validación aisladamente con campos vacíos y campos llenos para confirmar que devuelven los mensajes de error adecuados (ej. "La imagen es obligatoria").
*   **Estados de Flujo (uploadFlowState.ts):** Verificar la correcta transición del gestor de estados multipaso del formulario de subida de libros.

**Pruebas de Integración:**
*   **Formulario de Creación (`app/books/create` o `app/(tabs)/subir.tsx`):** Llenar el formulario en un componente renderizado, simular un click de envío y comprobar que se invoca `lib/books.ts` (API Client) con el FormData / JSON esperado.

### 4.3 Módulo: Interfaz de Emparejamiento (Matcher)
**Pruebas Unitarias:**
*   **Renderizado de Tarjetas:** Asegurar que el componente UI del Matcher (`components/matcher/`) carga y muestra correctamente la portada, título y género de un libro en base a los props recibidos (`types/matcher.ts`).
*   **Eventos de Swipe:** Validar que la acción de deslizar a la derecha llama a la función "onLike" y deslizar a la izquierda llama a "onDislike".

**Pruebas de Integración:**
*   **Flujo de Matcher:** Mockear `matcherApi.ts` para que devuelva una lista de libros. Realizar "swipes" simulados y confirmar que, tras cada interacción, el estado elimina la tarjeta actual e invoca la API (POST `/like` o `/dislike`).
*   **Modal de Match:** Verificar que si la respuesta de la API de Matcher indica "It's a Match!", el componente renderiza el `<ConfirmationModal />` (o equivalente).

### 4.4 Módulo: Chats y Comunicación
**Pruebas Unitarias:**
*   **Renderizado de Lista (mockChats.ts):** Proveer datos falsos a la pantalla `app/(tabs)/chat.tsx` y comprobar que se renderiza el número correcto de elementos.
*   **Cifrado/Seguridad (crypto.ts):** Probar las funciones de utilidad de encriptación (si las hubiere) validando el output frente a un input conocido.

**Pruebas de Integración:**
*   **Sala de Chat (`app/chat/[id].tsx`):** Integrar la UI del chat con una implementación mock de `chatApi.ts`. Enviar un mensaje, verificar que la API fue llamada e inmediatamente comprobar que la UI actualiza la vista (append del mensaje) optimísticamente o tras recibir respuesta.

### 4.5 Módulo: Ajustes y Perfil
**Pruebas Unitarias:**
*   **Interacciones Básicas:** Validar los toggles y formularios de configuración (`app/settings.tsx`, `components/PreferencesModal.tsx`). Asegurar que los hooks de estado reflejan el cambio.

**Pruebas de Integración:**
*   **Sincronización de Preferencias:** Cambiar la distancia máxima de emparejamiento, pulsar guardar, y comprobar que la app llama al endpoint correspondiente para sincronizar con el backend, mostrando una alerta de éxito.

---

## 5. Estrategia de Ejecución y Herramientas

*   **Backend (.NET C#):**
    *   **Framework de Pruebas:** `xUnit` (Anotaciones `[Fact]`, `[Theory]`, `[InlineData]`).
    *   **Mocking:** `Moq` (Para simular dependencias como `ILogger`, `IChatService`).
    *   **Base de Datos en Memoria:** `Microsoft.EntityFrameworkCore.InMemory` (Exclusivo para pruebas unitarias de lógica pura y cálculos).
    *   **Pruebas de Integración de Base de Datos:** `Testcontainers.PostgreSql` implementado mediante la clase `PostgresMatcherFixture` (implementando `IAsyncLifetime`). Se levanta un contenedor de `postgis/postgis:16-3.4` para validar el comportamiento con NetTopologySuite y Enums nativos. Las migraciones se inyectan ejecutando directamente scripts de `supabase/migrations`.
    *   **Pruebas de Integración API:** `Microsoft.AspNetCore.Mvc.Testing` (`WebApplicationFactory`) para simular llamadas a endpoints.
*   **Frontend (React Native / Expo):**
    *   **Framework Unitario/Integración:** Jest + React Native Testing Library (La infraestructura debe configurarse ya que el `package.json` de frontend aún no posee las dependencias base implementadas activamente, aunque se asume este estándar para React Native).
    *   **Mocking HTTP:** MSW (Mock Service Worker) o Jest Mocks (`jest.mock('lib/api')`).

## 6. Resumen de Calidad (Criterios de Éxito)
*   **Cobertura:** Mantener un mínimo de 70-80% de cobertura en los módulos críticos de negocio (`MatcherService`, validaciones).
*   **Aislamiento:** Las pruebas unitarias que usan `InMemoryDatabase` no deben depender de la red externa; las pruebas de integración deben correr de manera paralela controlada levantando sus propios Testcontainers por clase (Fixture).
*   **Reproducibilidad:** Las pruebas de integración del backend ejecutan scripts nativos `.sql` desde `supabase/migrations`, por lo tanto, la base de datos generada por el Testcontainer es idéntica estructuralmente al estado actual de Supabase en producción.
