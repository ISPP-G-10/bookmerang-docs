<div align="center">

<h1>Planes de gestión</h1>

<p style="font-size: 1.2em; margin-top: -10px;">
  <strong>Bookmerang</strong>
</p>

<br/>

<picture>
  <source media="(prefers-color-scheme: dark )"
          srcset="assets/img/logo-bookmerang-dark.png">
  <source media="(prefers-color-scheme: light )"
          srcset="assets/img/logo-bookmerang-light.png">
  <img
    src="assets/img/logo-bookmerang-light.png"
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

  <!-- Logo ETSII -->
  <div>
    <picture>
      <source media="(prefers-color-scheme: dark )"
              srcset="assets/img/us-etsi-inf-dark.png">
      <source media="(prefers-color-scheme: light )"
              srcset="assets/img/us-etsi-inf-light.png">
      <img
        src="assets/img/us-etsi-inf-light.png"
        alt="ETSII – Universidad de Sevilla"
        width="180"
      />
    </picture>
  </div>

  <!-- Texto académico -->
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
- [2. Gestión de los repositorios](#2-gestión-de-los-repositorios)
- [3. Gestión de las ramas](#3-gestión-de-las-ramas)
- [4. Gestión de los commits](#4-gestión-de-los-commits)
- [5. Gestión de tareas](#5-gestión-de-tareas)
  - [5.1 Estados del tablero (Workflow)](#51-estados-del-tablero-workflow)
- [6. Gestión del tiempo](#6-gestión-del-tiempo)
  - [6.1 Convención de entradas](#61-convención-de-entradas)
  - [6.2 Distribución de la carga semanal](#62-distribución-de-la-carga-semanal)
- [7. Gestión de conflictos](#7-gestión-de-conflictos)
  - [7.1 Prevención](#71-prevención)
  - [7.2 Identificación de conflictos](#72-identificación-de-conflictos)
  - [7.3 Protocolo de actuación](#73-protocolo-de-actuación)
  - [7.4 Compromiso de responsabilidad](#74-compromiso-de-responsabilidad)
- [8. Integración continua y despliegue continuo](#8-integración-continua-y-despliegue-continuo)
  - [8.1 Integración continua (CI)](#81-integración-continua-ci)
  - [8.2 Despliegue continuo (CD)](#82-despliegue-continuo-cd)
- [9. Herramientas y entornos](#9-herramientas-y-entornos)
- [10. Versionado](#10-versionado)
- [11. Gestión de las comunicaciones](#11-gestión-de-las-comunicaciones)
- [12. Gestión de riesgos](#12-gestión-de-riesgos)


---

## 1.  **Historial de Versiones** 

| Versión | Fecha | Participantes | Resumen de los cambios |
| :---: | :---: | ----- | ----- |
| v1.0 | 02/02/2026 | Alejandro Vela, Peter Carter, Fernando Triguero | Gestión de repositorios, ramas, commits, tareas, tiempo, conflictos, CI/CD, herramientas y versionado. |
| v1.1 | 03/02/2026 | Alejandro Vela, Peter Carter, Fernando Triguero, Julián Romero | Corrección de puntos y stack acabado. Gestión de comunicación, riesgos y roles. |
| v1.2   | 04/02/2026  | Alejandro Castilla  | Corrección de la portada y corrección de estilo. |

---

## 2.  **Gestión de los repositorios** 

Para mantener la autonomía de los 18 desarrolladores y minimizar los conflictos, hemos optado por una arquitectura de repositorios desacoplados. El repositorio de Backend centraliza la lógica de negocio, servicios y acceso a datos. El de Frontend se enfoca exclusivamente en la experiencia de usuario. Finalmente, el repositorio de Documentation alberga toda la documentación de planificación estratégica, hojas de ruta (roadmaps), actas de decisión arquitectónica y guías de gestión de equipo. Esta separación permite que cada equipo escale su infraestructura de despliegue de forma independiente y que un cambio estético en el frontend no requiera disparar innecesariamente los tests de integración de la base de datos.

## 3. **Gestión de las ramas** 

Para la correcta gestión de las ramas en los repositorios de desarrollo ("frontend" y "backend") que tendrá el proyecto nos hemos decantado por una estructura “git-flow” basada en las siguientes ramas:

  * Rama “main”: rama que contendrá el código estable y finalizado luego de cada release. El entorno de producción apuntará a esta rama.  
      
  * Rama “release”: rama que contendrá las releases del proyecto, con su versión correspondiente. Las ramas de este tipo se nombran de la siguiente manera: “release/vX.Y.Z”.  
      
  * Rama “trunk”: rama que contendrá código de las funcionalidades terminadas, listas para que, una vez estén todas las funcionalidades del sprint, pasar a la rama “release”. El entorno de pre-producción apuntará a esta rama.  
      
  * Ramas “feature”: son las ramas de cada una de las funcionalidades del proyecto. En ellas se desarrollarán todas las funcionalidades para, posterior a su desarrollo, subir dichas features a la rama “trunk”. Las ramas de este tipo se nombran de la siguiente manera: “feat/*numeroDeIssue*”, una vez se encuentre la tarea de la feature finalizada se borrará la rama con el fin de mantener limpio el entorno de trabajo.  
      
  * Ramas “hotfix”: son las ramas para corregir errores de última hora. Las ramas de este tipo se nombran: “hotfix/*numeroDeIssue*”, al igual que con la rama anterior se borrará la rama con el fin de la issue.

Mientras que el repositorio de documentación seguirá un git-flow simplificado. Tendrá únicamente ramas tipo docs y una rama main.

## 4. **Gestión de los commits** 

Para el desarrollo de este proyecto se va a usar el estándar Conventional Commit, una convención que define diversas reglas que consiguen que haya legibilidad en el histórico del repositorio.

Dicha convención hace uso de la siguiente estructura:

\<type\>(opcional: scope): \<descripción\>

Se destacan lo siguientes tipos de commits para el primer elemento:

* Feat : se usa cuando se añade una funcionalidad.   
* Fix: para arreglar un error.  
* Test: para añadido o arreglo de tests.  
* Docs: para añadido o arreglo de documentos.  
* Style: modificaciones de legibilidad o formateo de código sin afectar a la funcionalidad  
* Refactor: mejora del código sin añadido de funcionalidades.

Los commits pasarán de ramas a través de Pull Requests, las cuales deberán estar supervisadas antes de realizar el merge a la rama destino. Dicha revisión deberá ser realizada por, al menos, 2 integrantes.

## 5. **Gestión de tareas** 

Para centralizar el flujo de trabajo del equipo se usará GitHub Projects. Todas las tareas (issues) deberán estar etiquetadas según su tipo (frontend, backend, docs, testing, etc), lo que nos permitirá visualizar rápidamente el equilibrio de carga de trabajo, y su prioridad (alta, media o baja) para dictar el orden de ejecución en el tablero. Las métricas de esfuerzo se basarán en la metodología de Planning Poker, asignando valores de complejidad de forma consensuada; sin embargo, para mantener el dinamismo, se establecerá un tiempo límite de un día para esta dinámica: si algún miembro no puede participar en la sesión, el responsable de la tarea cerrará la estimación con los votos presentes para evitar que el proceso se convierta en un cuello de botella, garantizando que el equipo pase de la planificación a la acción de manera inmediata y fluida.

### 5.1. Estados del tablero (Workflow) 

Utilizaremos un flujo de 5 columnas para mantener el control total sobre el ciclo de vida de cada tarea:

* **Backlog**: Ideas, requerimientos brutos y tareas futuras que aún no han sido priorizadas para el ciclo actual.  
    
* **Todo**: Tareas priorizadas y con descripción clara que están listas para ser tomadas por un miembro del equipo.  
    
* **In Progress**: Tareas que están siendo ejecutadas activamente. **No más de 2 tareas por persona** para evitar la dispersión.  
    
* **In Review**: Significa que un documento está en revisión o que un PR está abierto esperando aprobaciones.  
    
* **Done**: Tarea finalizada y revisada. Ya en la rama “trunk”.

## 6. **Gestión del tiempo** 

Se seguirá un registro mediante el uso de Clockify. Esta herramienta permitirá hacer un seguimiento del tiempo empleado por cada miembro del equipo en las diversas tareas del proyecto.

### 6.1. Convención de entradas 

Usaremos el siguiente formato para definir en qué se ha estado trabajando:

**\[Categoría \- Subcategoría\] \- Acción \+ Entregable/Tarea**

Ejemplos de Aplicación por Áreas:

* \[Docs \- Plan\] \- Redactar planes de gestión  
* \[Docs \- Roadmap\] \- Definición de hitos del primer Sprint  
* \[Docs \- Riesgos\] \- Identificación de dependencias críticas entre equipos  
* \[Arch \- DB\] \- Diseño del esquema relacional para el microservicio de pagos  
* \[Setup \- Repo\] \- Configuración de permisos y ramas protegidas

### 6.2. Distribución de la Carga Semanal 

Cada miembro del equipo debe certificar un total de 10 horas semanales de dedicación al proyecto. Esta carga se divide de forma estándar de la siguiente manera:

* 4 Horas Presenciales (Sesiones de Clase): Tiempo destinado a la asistencia a las clases de Ingeniería del Software y Práctica Profesional. Será necesario incluir estas horas de asistencia en Clockify para llevar un control formal de quien asiste a las clases, ya sean las 4 horas completas o de manera parcial.  
    
* 6 Horas de Trabajo Autónomo: Tiempo dedicado a la ejecución de tareas específicas (redacción de documentos, desarrollo, configuración de entornos, despliegue, etc.).

Si un miembro no puede asistir a las 4 horas de clase, debe compensarlas obligatoriamente con 4 horas adicionales de trabajo individual esa misma semana. Las horas recuperadas deben registrarse en Clockify bajo el formato estándar, especificando en la descripción que se trata de una recuperación por ausencia.  
Será obligatorio avisar con antelación esta ausencia para poder llevar a cabo una reorganización de las tareas, asegurando que no haya cuellos de botella y el avance del equipo no se detenga.

## 7. **Gestión de conflictos** 

  ### 7.1. Prevención 

Se realizarán las siguientes acciones con el fin de prevenir conflictos:

* Revisión semanal: Se harán un contraste de las horas registradas en Clockify con el fin de asegurarse de que cada miembro cumple las 10 horas de trabajo acordadas en el agreement (6 en el caso de las asistencias a las clases de la asignatura).  
    
* Avisos tempranos: si un miembro observa que sus tareas no pueden ser cumplidas en el plazo acordado debe comunicarlo antes de obligar a sus compañeros a realizar más trabajo del acordado.  
  

### 7.2. Identificación de conflictos 

Se considerarán como graves los siguientes conflictos:

* Falta de horas de más del 50% de las requeridas.  
* Absentismo injustificado a las reuniones.  
* Faltas de respeto hacia otros miembros del equipo.  
* Actitud desinteresada tras avisos previos.


### 7.3. Protocolo de actuación              

Ante un conflicto por falta de compromiso o resultados, se seguirá este orden:

1. Mediación Interna: Reunión privada con el miembro afectado para identificar causas y buscar soluciones que permitan retomar la senda de las 10 horas semanales.  
2. Aplicación de Calificación Asimétrica: Si el retraso o la falta de dedicación persiste y obliga a otros a asumir su carga, el grupo solicitará formalmente una distribución asimétrica de la nota del entregable. Esta nota reflejará la contribución real y compensará el esfuerzo extra de quienes asumieron el trabajo faltante.  
3. Salida Voluntaria del Grupo: En última instancia, si el esfuerzo no alcanza el umbral mínimo del 50%, el miembro se compromete a abandonar voluntariamente el grupo para no obstaculizar el progreso general.  
   

  ### 7.4. Compromiso de responsabilidad             

Todos los miembros aceptan que la entrega a tiempo es una responsabilidad compartida. El incumplimiento de estas normas se considera una ruptura del acuerdo firmado, activando automáticamente los mecanismos de compensación mencionados.	

         


## 8. **Integración Continua/Despliegue continuo** 

   ### 8.1. Integración Continua (CI) 

En este proyecto aplicaremos distintos flujos de trabajo relacionados con la integración para automatizar tareas del proyecto. Los diferentes flujos de trabajo que aplicaremos en el proyecto serán las siguientes:

* Formateo automático: Se verifica que el código cumple con las reglas de estilo. Si el código está "sucio", el pipeline arregla automáticamente todo aquello mejorable en el formateo del código. 

* Ejecución de pruebas unitarias: Ejecución de tests automáticos. Para que el pipeline se dé por completado deberán pasar todos los tests. Dicho resultado se mandará a un canal de discord de la organización con el resultado de los tests.

### 8.2. Despliegue Continuo (CD) 

Para aplicar despliegue contínuo, usaremos las siguientes estrategias:

* El despliegue “pre-producción”: Estará apuntando a la rama “trunk” y se desplegará en AWS/Azure (aún debate) y se desplegará automáticamente con cada push a dicha rama.  
* El despliegue “producción”: Apuntará a la rama “main”, se hará en AWS/Azure y se desplegará con cada push a la rama principal.  
* Estrategia de versionado: Para mantener un correcto versionado del proyecto, se creará un pipeline que generará para cada push a la rama “release” un tag en git con la versión del proyecto.  
  


## 9. **Herramientas y entornos** 

* **Backend:** Se utilizará .NET8 como *framework* principal. La contenerización se gestionará con Docker, y el despliegue se realizará en Azure Container Apps. La base de datos será PostgreSQL a través de Supabase con SSL, que también gestionará autenticaciones y almacenamiento de archivos. Los *pipelines* integrarán las llamadas al servicio de Supabase tanto para la integración continua para validar las migraciones como para el despliegue para aplicar las nuevas migraciones a la rama “main”.  

* **Frontend:** Se desarrollará con Expo (utilizando React Native TypeScript \+ web). El despliegue web se realizará como PWA (Progressive Web App), y el *build* móvil será opcional.

## 10. **Versionado** 

Seguiremos el esquema de Versionado Semántico (X.Y.Z):

* X (Major): Cambios que rompen la compatibilidad hacia atrás.  
* Y (Minor): Nuevas funcionalidades (ej. añadir búsqueda de libros).  
* Z (Patch): Corrección de errores (ej. arreglar un bug en el login).

## 11. **Gestión de las comunicaciones** 

Establecemos un marco de comunicación claro para asegurar la transparencia, la toma de decisiones ágil y la documentación de hitos.

* Canales y Propósito:  
  * Discord: Canal principal para avisos de CI/CD (resultado de *tests*), consultas técnicas rápidas, y coordinación diaria. Se usará un canal específico para los avisos automatizados del *pipeline*.  
  * Reuniones en clase: se realizará un warm-up previo a las presentaciones estipuladas por la asignatura.  
  * Documentación (Drive/Repositorio Docs): Único lugar para actas de decisión arquitectónica, informes de progreso formales y cambios en los planes de gestión.  

* Frecuencia de Reuniones:  
  * Revisión de Tareas (*Stand-up*): Al inicio de cada sesión presencial.  
  * Actas de reunión: Un documento de resumen del progreso (horas registradas en Clockify, estado del tablero en GitHub Projects, y cumplimiento de objetivos) se genera semanalmente.

## 12. **Gestión de riesgos** 

Se identifican y se establecen planes de mitigación para los riesgos más críticos.

* **Riesgos Técnicos**  
  * **Riesgo:** Alta curva de aprendizaje o problemas de compatibilidad con .NET8 o Expo/React Native.  
  * **Mitigación:** Asignación de tiempo extra al inicio del proyecto para *spikes* (pequeños proyectos de prueba) y formación en las tecnologías clave.  
  * **Riesgo:** Fallos en la infraestructura de Supabase o Azure Container Apps.  
  * **Mitigación:** Documentación detallada del proceso de *setup* y configuración en el repositorio de Documentation para una rápida reconstrucción del entorno.  
* **Riesgos de Equipo y Alcance**  
  * **Riesgo:** Desviación del alcance (*Scope Creep*) por adición no planificada de funcionalidades.  
  * **Mitigación:** Todas las nuevas ideas deben entrar en el **Backlog** de GitHub Projects y ser priorizadas y estimadas antes de pasar a **Todo**. No se aceptan funcionalidades fuera de la planificación del *sprint* en curso.  
  * **Riesgo:** *Bus Factor* alto (dependencia crítica de un solo miembro en un componente).  
  * **Mitigación:** Asegurar que cada funcionalidad crítica tenga una revisión (*In Review*) realizada por al menos dos integrantes, garantizando el conocimiento compartido.

