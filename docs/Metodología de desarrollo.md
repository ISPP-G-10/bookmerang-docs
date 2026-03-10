<div align="center">

<h1>Metodología de desarrollo empleada</h1>

<p style="font-size: 1.2em; margin-top: -10px;">
  <strong>Bookmerang</strong>
</p>

<br/>

<picture>
  <source media="(prefers-color-scheme: dark)"
          srcset="assets/img/logo-bookmerang-dark.png">
  <source media="(prefers-color-scheme: light)"
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

  <div>
    <picture>
      <source media="(prefers-color-scheme: dark)"
              srcset="assets/img/us-etsi-inf-dark.png">
      <source media="(prefers-color-scheme: light)"
              srcset="assets/img/us-etsi-inf-light.png">
      <img
        src="assets/img/us-etsi-inf-light.png"
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

# Índice

- [1. Historial de Versiones](#1-historial-de-versiones)
- [2. Visión general](#2-visión-general)
- [3. Roles del equipo](#3-roles-del-equipo)
- [4. Estructura de los Sprints](#4-estructura-de-los-sprints)
- [5. Ceremonias del equipo](#5-ceremonias-del-equipo)
  - [Reunión de Scrum Masters — Jueves tras clase](#reunión-de-scrum-masters--jueves-tras-clase)
  - [Revisión de Sprint — Miércoles previo a la defensa](#revisión-de-sprint--miércoles-previo-a-la-defensa)
  - [Reunión conjunta de puesta a punto — Fin de semana](#reunión-conjunta-de-puesta-a-punto--fin-de-semana)
  - [Trabajo autónomo por subequipos — Lunes a jueves](#trabajo-autónomo-por-subequipos--lunes-a-jueves)
- [6. Gestión del backlog y el tablero](#6-gestión-del-backlog-y-el-tablero)
- [7. Estimación de tareas](#7-estimación-de-tareas)
- [8. Definición de hecho](#8-definición-de-hecho)

---

# 1. Historial de Versiones

| Versión | Fecha | Participantes | Resumen de los cambios |
|--------|------|--------------|-----------------------|
| v1.0 | 21/02/2026 | Antonio Luis Jiménez de la Fuente | Primera versión del documento |

---

# 2. Visión general

El equipo de **Bookmerang** trabaja con una metodología **Scrum adaptada al contexto académico de la asignatura**.

El trabajo se organiza en **tres sprints de duración fija**, alineados con los entregables principales del proyecto:

- Core / MVP  
- Módulo social y espacios físicos  
- Gamificación y monetización  

El equipo está formado por **20 integrantes**, cada uno con una dedicación aproximada de **10 horas semanales**, distribuidas en:

- **4 horas presenciales en clase**
- **6 horas de trabajo autónomo**

---

# 3. Roles del equipo

El equipo se divide en **tres subequipos**, organizados alrededor de dos roles principales.

## Scrum Master

Cada subequipo cuenta con un Scrum Master cuya función es:

- Facilitar las reuniones y la distribución de tareas.
- Eliminar bloqueos que impidan el avance del equipo.
- Garantizar que el tablero de **GitHub Projects** refleje el estado real del trabajo.

Además, supervisa el cumplimiento de las normas internas del equipo:

- convenciones de commits
- flujo de ramas
- registro de horas en Clockify
- límite de tareas activas por persona

Los Scrum Masters también participan activamente en el desarrollo del proyecto.

## Equipo de Desarrollo

Los **17 integrantes restantes** se organizan en tres subequipos siguiendo la arquitectura del proyecto.

Principios de trabajo:

- división por funcionalidades
- uso de **pair programming**
- cada funcionalidad incluye **backend y frontend**

El backend sigue una arquitectura **Modelo-Vista-Controlador (MVC)** como estándar obligatorio.

Cada subequipo trabaja de forma autónoma pero coordinada para garantizar la **integración continua**.

Regla organizativa:

- ningún miembro puede tener **más de 2 tareas activas simultáneamente**.

---

# 4. Estructura de los Sprints

El proyecto se divide en tres sprints alineados con el calendario académico.

| Sprint | Nombre | Alcance principal |
|------|------|----------------|
| Sprint 1 | Core / MVP | Registro, matcher, chats e intercambio completo de libros |
| Sprint 2 | Módulo social | Comunidades, quedadas presenciales y mapa de BookSpots |
| Sprint 3 | Gamificación y monetización | InkDrops, niveles, rachas, suscripción Premium y BookSpots Partners |

Al final de cada sprint se entrega un **incremento funcional desplegado** que se defiende en clase.

Solo se consideran parte del incremento las funcionalidades que cumplen la **Definición de Hecho**.

---

# 5. Ceremonias del equipo

El equipo mantiene un **ritmo semanal fijo** que combina coordinación entre Scrum Masters, trabajo autónomo por subequipos y reuniones de seguimiento.

---

## Reunión de Scrum Masters — Jueves tras clase

Cada jueves, tras la sesión presencial, los Scrum Masters de los tres subequipos se reúnen para organizar el trabajo de la semana siguiente.

Durante esta reunión:

- se revisa el estado del tablero de GitHub Projects
- se reasignan tareas bloqueadas
- se identifican dependencias entre subequipos
- se definen los objetivos para la semana siguiente

Cuando comienza un nuevo sprint, la reunión incluye además:

### Retrospectiva

El equipo analiza:

- qué funcionó bien
- qué problemas surgieron
- qué mejoras aplicar en el siguiente sprint

Se registran **hasta 3 acciones de mejora** en un acta almacenada en el repositorio de Documentation.

### Planificación del sprint

Los Scrum Masters presentan las **issues prioritarias del backlog** según el feedback del Product Owner (profesorado ISPP).

Las tareas se estiman mediante **Planning Poker** y las seleccionadas pasan de **Backlog → Todo** en GitHub Projects.

---

## Revisión de Sprint — Miércoles previo a la defensa

El miércoles previo a la defensa se realiza una revisión interna del sprint.

Durante esta sesión:

- se realiza una **demostración en vivo de las funcionalidades**
- se revisa el backlog
- las issues aceptadas pasan a estado **Done**

Esto permite llegar a la defensa con el incremento validado internamente.

---

## Reunión conjunta de puesta a punto — Fin de semana

Durante el fin de semana se celebra una breve reunión con todo el equipo para revisar:

- qué tareas se han completado
- cuáles están en progreso
- qué bloqueos existen

La coordinación y convocatoria se realiza a través de **Discord**.

---

## Trabajo autónomo por subequipos — Lunes a jueves

Entre lunes y jueves cada subequipo trabaja de forma independiente ejecutando las tareas asignadas.

La comunicación entre subequipos se canaliza a través de los **Scrum Masters**, que actúan como enlace para:

- resolver dependencias
- transmitir decisiones
- escalar bloqueos

---

# 6. Gestión del backlog y el tablero

Todo el trabajo del proyecto se gestiona mediante **GitHub Projects**, que actúa como tablero central del proyecto.

La organización dispone de **tres tableros**, uno por subequipo:

- E1
- E2
- E3

Estos tableros se sincronizan automáticamente con los repositorios:

- Backend
- Frontend
- Documentation

De esta forma cualquier **issue creada en un repositorio aparece automáticamente en el tablero central**.

### Estados del flujo de trabajo

| Estado | Descripción |
|------|-------------|
| Backlog | ideas y tareas futuras |
| Todo | tareas priorizadas para el sprint |
| In Progress | tareas en ejecución |
| In Review | Pull Request abierto |
| Done | tarea finalizada y fusionada |

Cada issue debe incluir:

- título descriptivo
- criterios de aceptación
- etiqueta de equipo (E1, E2, E3)
- tipo (frontend, backend, docs, testing, infra)
- prioridad
- estimación de tamaño
- asignación de responsable

---

# 7. Estimación de tareas

El equipo utiliza **Planning Poker** para estimar el esfuerzo relativo de cada tarea.

Escala utilizada:

```
 1, 2, 3, 5, 8, 13, 21 
```

Las tareas con estimación **mayor a 13 puntos** deben dividirse en subtareas antes de incorporarse al sprint.

Para evitar bloqueos en la estimación, se establece un **plazo máximo de un día** para cerrar la votación.

---

# 8. Definición de hecho

Una tarea se considera **Done** únicamente cuando cumple todos los criterios siguientes:

- El código ha sido revisado mediante **Pull Request** por al menos un miembro distinto del autor.
- Los commits siguen la convención **Conventional Commits**.
- La rama `feature/*` ha sido fusionada en `trunk` y eliminada.
- El pipeline de **GitHub Actions** ha ejecutado correctamente formateo y tests.
- La funcionalidad no ha sido rechazada por el Product Owner.
- La issue está marcada como **Done** en GitHub Projects.
- El tiempo invertido está registrado en **Clockify** con el formato estándar.