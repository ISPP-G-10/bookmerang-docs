<div align="center">

<h1>Definición del Stack Tecnológico</h1>

<p style="font-size: 1.2em; margin-top: -10px;">
<strong>Bookmerang</strong>
</p>

<br/>

<picture>
<source media="(prefers-color-scheme: dark)"
srcset="../assets/img/logo-bookmerang-dark.png">
<source media="(prefers-color-scheme: light)"
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
<source media="(prefers-color-scheme: dark)"
srcset="../assets/img/us-etsi-inf-dark.png">
<source media="(prefers-color-scheme: light)"
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
- [2. Introducción](#2-introducción)
- [3. Backend](#3-backend)
- [4. Frontend](#4-frontend)
- [5. Infraestructura](#5-infraestructura)
- [6. Estado en adopción del stack](#6-estado-en-adopción-del-stack)

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
      <td>08/02/2026</td>
      <td>Antonio Luis Jiménez de la Fuente</td>
      <td>Primera versión del documento</td>
    </tr>
    <tr>
      <td>v1.2</td>
      <td>16/02/2026</td>
      <td>Alejandro Castilla</td>
      <td>Segunda versión especificando más en detalle las tecnologías</td>
    </tr>
    <tr>
      <td>v1.3</td>
      <td>21/02/2026</td>
      <td>Antonio Luis Jiménez de la Fuente</td>
      <td>Incorporación de estado en adopción del stack</td>
    </tr>
  </tbody>
</table>

<!-- pagebreak -->

## 2. Introducción

Este documento presenta una definición completa del stack tecnológico propuesto, analizando cada componente de la arquitectura y evaluando sus ventajas y desventajas. El stack está diseñado para desarrollar aplicaciones móviles multiplataforma con un backend robusto y una infraestructura escalable en la nube.

## 3. Backend

**Tecnologías:**

- .NET 8 (C#) para APIs y lógica de negocio.
- PostgreSQL como base de datos principal.
- Supabase.
- PostGIS para capacidades geoespaciales (matching por cercanía).

**Ventajas**

- .NET 8 ofrece alto rendimiento, buena documentación y un ecosistema maduro para APIs REST y servicios de negocio.
- Supabase proporciona autenticación, almacenamiento y APIs sobre PostgreSQL, reduciendo tiempo de desarrollo y gestión de infraestructura.
- PostgreSQL + PostGIS permiten consultas geoespaciales avanzadas (distancias, contención, intersecciones) de forma eficiente.

**Inconvenientes / retos**

- Requiere conocer C# y el ecosistema .NET; si el equipo viene de JavaScript solo, la curva de aprendizaje puede ser moderada.
- Supabase añade cierta dependencia de plataforma (vendor lock-in ligero) y hay que entender bien sus límites de cuotas y rendimiento.
- PostGIS añade complejidad: hay que aprender tipos y funciones geoespaciales para sacarle partido.

<!-- pagebreak -->

## 4. Frontend

**Tecnologías:**

- React Native con Expo.
- TypeScript.

**Ventajas**

- Un solo código para Android, iOS y PWA web, reduciendo esfuerzo de desarrollo y mantenimiento.
- Expo simplifica el acceso a cámara, GPS y otras capacidades nativas, además de facilitar compilaciones en la nube y actualizaciones OTA.
- TypeScript mejora la calidad del código y el autocompletado, reduciendo errores en el tiempo de ejecución.
- Curva de aprendizaje razonable para equipos que ya conocen React/JavaScript.

**Inconvenientes / retos**

- Algunas funcionalidades muy nativas o específicas pueden requerir ejectuar “eject” de Expo o crear módulos nativos, lo que complica el proyecto.
- El rendimiento, aunque bueno, puede ser inferior a una app nativa pura en casos muy exigentes (gráficos intensivos, animaciones muy complejas).
- TypeScript añade una capa extra de tipado que al principio puede ralentizar a perfiles sin experiencia previa.

## 5. Infraestructura

**Tecnologías:**

- Docker para contenerización del backend y servicios auxiliares.
- Azure Container Apps para despliegue escalable sin gestionar Kubernetes directamente.
- GitHub Actions para CI/CD (build, test, lint, despliegue automatizado).

**Ventajas**

- Docker permite empaquetar el backend y otros servicios en contenedores reproducibles, facilitando despliegues consistentes entre entornos.
- Azure Container Apps ofrece escalado automático por carga, HTTPS integrado y observabilidad sin tener que gestionar Kubernetes directamente.
- Buen ajuste para arquitecturas desacopladas y microservicios, con potencial de reducción de costes frente a App Service tradicional.

**Inconvenientes / retos**

- Es necesario entender conceptos de contenedores (Dockerfiles, imágenes, redes), lo que añade una curva de aprendizaje inicial al equipo.
- La configuración avanzada de Azure Container Apps (escalado, secretos, redes virtuales) puede resultar compleja si no se tienen conocimientos previos de Azure.

<!-- pagebreak -->

## 6. Estado en adopción del stack

Durante el Sprint 1 se ha completado la puesta en marcha inicial del stack tecnológico en ambos repositorios principales del proyecto.

**Backend**

Se ha creado y estructurado el repositorio de backend siguiendo la arquitectura MVC definida para el proyecto, con la organización de carpetas y configuración del proyecto .NET 8. El repositorio ha sido desplegado correctamente en Azure Container Apps, quedando el entorno de pre-producción operativo y accesible.

**Frontend**

Se ha inicializado el repositorio de frontend con la estructura base del proyecto en React Native con Expo y TypeScript. Al igual que el backend, el despliegue en Azure ha concluido sin incidencias, con la PWA accesible desde el entorno de pre-producción.
