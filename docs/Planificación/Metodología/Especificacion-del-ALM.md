<div align="center">

<h1>Especificación del ALM</h1>

<p style="font-size: 1.2em; margin-top: -10px;">
<strong>Bookmerang</strong>
</p>

<br/>

<picture>
<source media="(prefers-color-scheme: dark)"
srcset="../../assets/img/logo-bookmerang-dark.png">
<source media="(prefers-color-scheme: light)"
srcset="../../assets/img/logo-bookmerang-light.png">
<img
src="../../assets/img/logo-bookmerang-light.png"
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
<source media="(prefers-color-scheme: dark)"
srcset="../../assets/img/us-etsi-inf-dark.png">
<source media="(prefers-color-scheme: light)"
srcset="../../assets/img/us-etsi-inf-light.png">
<img
src="../../assets/img/us-etsi-inf-light.png"
alt="ETSII – Universidad de Sevilla"
width="180"
/>
</picture>
</div>

<div style="max-width: 360px;">
<p style="margin: 0; line-height: 1.6;">
<strong>Asignatura:</strong> ISPP (Curso 2025/26)<br/>
<strong>Grupo:</strong> 8 — <em>Bookmerang</em><br/>
<strong>Grado:</strong> Ingeniería del Software<br/>
<strong>Centro:</strong> ETSII — Universidad de Sevilla
</p>
</div>

</div>

</div>

<hr/>


<!-- pagebreak -->
## Índice

- [1. Historial de Versiones](#1-historial-de-versiones)
- [2. Gobernanza y organización del proyecto](#2-gobernanza-y-organización-del-proyecto)
- [3. Estrategia de Desarrollo e Integración](#3-estrategia-de-desarrollo-e-integración)
  - [3.1 Metodología de Trabajo](#31-metodología-de-trabajo)
  - [3.2 Herramientas de QA y Calidad](#32-herramientas-de-qa-y-calidad)
- [4. Estrategia de Despliegue (CD)](#4-estrategia-de-despliegue-cd)
- [5. Modelado y Gestión de Datos](#5-modelado-y-gestión-de-datos)

---

<!-- pagebreak -->

## 1. Historial de Versiones

<table>
  <thead>
    <tr>
      <th>Versión</th>
      <th>Fecha</th>
      <th>Participantes</th>
      <th>Resumen de los cambios</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>v1.0</td>
      <td>21/02/2026</td>
      <td>Peter Carter</td>
      <td>Primera versión del documento</td>
    </tr>
    <tr>
      <td>v1.1</td>
      <td>23/02/2026</td>
      <td>Peter Carter</td>
      <td>Cambio de metodología del trabajo y workflows de CI</td>
    </tr>
  </tbody>
</table>

<!-- pagebreak -->

## 2. Gobernanza y organización del proyecto

La gestión del ciclo de vida se centraliza en GitHub Projects, que actúa como la fuente de verdad única para el estado del proyecto y mantiene la estructura jerárquica para la coordinación de los equipos:

- **Estructura de Proyectos:**
  1. Se utiliza un tablero grande central para las funcionalidades principales (fuente de verdad).
  2. Se mantienen 3 GitHub Projects individuales (E1, E2, E3) para la gestión específica de tareas de cada subequipo, sincronizados automáticamente con las issues de los repositorios (Backend, Frontend, Documentation).
- **Nomenclatura de Equipos:** Los equipos se identificarán siguiendo el estándar ISPP-G8-E1/E2/E3, utilizado también como etiqueta obligatoria en el tablero.
- **Gestión de Tareas y Flujo de Trabajo:** El seguimiento se realiza exclusivamente a través de GitHub Projects. El flujo de trabajo cuenta con 5 estados que aseguran el orden y evitan solapamientos entre módulos:
  1. **Backlog:** Ideas, requisitos y tareas futuras sin priorizar para ningún sprint.
  2. **Todo:** Tareas priorizadas y listas para ser tomadas por un miembro en el sprint actual.
  3. **In Progress:** Tareas en ejecución activa (con un límite de máximo 2 por persona).
  4. **In Review:** Tarea cuyo Pull Request está abierto y pendiente de revisión por otros miembros.
  5. **Done:** Tarea finalizada, revisada y fusionada en trunk (cumpliendo la Definición de Hecho).

<!-- pagebreak -->

## 3. Estrategia de Desarrollo e Integración

La Integración Continua (CI) se centrará en la calidad del código y la sincronización del equipo.

### 3.1 Metodología de Trabajo

- **GitFlow:** Todo el desarrollo debe seguir el flujo de trabajo "GitFlow" y es obligatorio el uso de Pull Requests (PRs) para integrar código.

### 3.2 Herramientas de QA y Calidad

- **Sonarqube:** Se integrará como herramienta principal de QA para el análisis estático de código, asegurando que no se introduzca deuda técnica en las PRs.
- **Entorno .NET:** Se utilizarán las siguientes herramientas de calidad y estilo de código específicas para .NET:
  - **.NET:** workflow que realiza la construcción de un proyecto con el framework del mismo nombre y ejecuta los tests.
  - **SonarCloud analysis:** workflow que realiza un análisis de la calidad del código mediante Sonarcloud detectando bugs, vulnerabilidades, code smells, problemas de seguridad y métricas de calidad.
  - **Node.js CI:** workflow que compila un proyecto Node instalando previamente las dependencias para ejecutar los tests; dicho proceso se realiza en 3 versiones de Node, haciendo uso de caché para acelerar las instalaciones.

Estos workflows se ejecutarán cuando se den pull requests o commits a las ramas de producción (`main`) y preproducción (`develop`).

<!-- pagebreak -->

## 4. Estrategia de Despliegue (CD)

El despliegue está automatizado y segmentado para proteger la estabilidad del producto y el presupuesto, se harán uso de los siguientes entornos de despliegue:

<table>
  <thead>
    <tr>
      <th>Entorno</th>
      <th>Plataforma</th>
      <th>Propósito</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Preproducción (Prep)</td>
      <td>Render</td>
      <td>Pruebas de integración y validación de funcionalidades antes de producción.</td>
    </tr>
    <tr>
      <td>Producción (Prod)</td>
      <td>Azure</td>
      <td>Entorno final para el usuario. El despliegue por sprint se hace en cuentas distintas para optimizar costes.</td>
    </tr>
  </tbody>
</table>

A su vez, se va a usar el siguiente flujo de despliegue automatizado:

1. **Containerización:** Creación de un servicio de registro de imágenes de Docker (organización privada de Docker Desktop).
2. **Push al Registro:** Las imágenes se pushean al registro de Azure.
3. **Automatización de Releases:** Las releases deben estar totalmente automatizadas para evitar errores manuales.
4. **Guías de Soporte:** se proporcionan las guías de descarga de entornos y la guía específica de despliegue en Azure.

<!-- pagebreak -->

## 5. Modelado y Gestión de Datos

El núcleo de la persistencia se basa en la flexibilidad entre local y nube.

- **Tecnología:** Base de datos PostgreSQL gestionada a través de Supabase.
- **Sincronización:** El modelo debe poder exportarse tanto a Supabase como a local de forma íntegra.
- **Gestión de Chats:** Los chats se conservarán inicialmente en formato JSON y se integrarán en la BD mediante imports en .NET, usando tablas separadas para usuarios y conversaciones con índices complejos (**FALTA VERLO TODAVÍA**).
