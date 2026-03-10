<div align="center">

<h1>Planificación del proyecto en 3 Sprints</h1>

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

# Índice

- [1. Historial de Versiones](#1-historial-de-versiones)
- [2. Visión general](#2-visión-general)
- [3. Sprint 1 - Core / MVP](#3-sprint-1---core--mvp)
- [4. Sprint 2 - Módulo social y Espacios Físicos](#4-sprint-2---módulo-social-y-espacios-físicos)
- [5. Sprint 3 - Gamificación y Monetización](#5-sprint-3---gamificación-y-monetización)

---

# 1. Historial de Versiones

| Versión | Fecha | Participantes | Resumen de los cambios |
|--------|------|--------------|------------------------|
| v1.0 | 02/02/2026 | Antonio Luis Jiménez de la Fuente | Primera versión del proyecto |
| v1.1 | 09/02/2026 | Antonio Rodríguez Calderón | Revisión Ortográfica |
| v1.2 | 16/02/2026 | Francisco Rodríguez-Carretero Roldán | Adición de fechas. Ajuste para cuadrar con el plan de diseño y D. GANT |
| v1.3 | 17/02/2026 | Antonio Luis Jiménez de la Fuente | Adaptación a nuevo documento de diseño |
| v1.4 | 18/02/2026 | Darío Román Jiménez | Reordenación tareas del alcance de cada Sprint |

---

# 2. Visión general

El proyecto Bookmerang se ha reorientado para transformar el intercambio de libros en una experiencia social y física. El desarrollo se divide en tres fases: consolidación del Core (MVP), expansión del módulo social y comunidades, y finalmente, la implementación del sistema de gamificación avanzado y monetización.

---

# 3. Sprint 1 - Core / MVP (19/02 - 04/03)

## Objetivo principal

Establecer la infraestructura base y las funcionalidades críticas (Core) que permitan realizar un intercambio completo desde el descubrimiento hasta la entrega física.

## Alcance funcional

**Sistema de Identificación**

Registro, login y gestión de sesiones de usuario.

**Perfil de Usuario**

Visualización de datos básicos, preferencias de intercambio y puntos acumulados.

**Gestión de Biblioteca Personal**

Formulario de subida de libros (Título, Autor, ISBN, Género, Estado) y visualización de la biblioteca en el perfil.

**Módulo Matcher (Fase 1)**

Implementación de la interfaz tipo tarjeta, lógica de deslizamiento (derecha/izquierda) y algoritmo de recomendación básico por cercanía y géneros.

**Módulo de Chat (Fase 1)**

Creación automática de canales tras un match, gestión de mensajes 1 a 1 y visualización de la lista de chats activos.

**Gestión de Intercambios**

Flujo lógico de aceptación/rechazo de propuestas y confirmación final de entrega.

## Entregables clave

Backend con API REST para gestión de usuarios, libros y matches.

App móvil funcional con navegación mediante Footer (Matcher, Chats, Subir Libro, Perfil).

Base de datos desplegada con modelos de datos para libros, usuarios y transacciones.

---

# 4. Sprint 2 - Módulo social y Espacios Físicos

## Objetivo principal

Integrar la dimensión social de la aplicación mediante la creación de comunidades y la validación de espacios físicos (BookSpots).

## Alcance funcional

**Sistema de Mensajería Avanzado**

Implementación de estados de lectura, notificaciones push y adjuntos básicos en el chat.

**Mapa de BookSpots**

Visualización de cafeterías y librerías seguras, y sistema de validación comunitaria para nuevos puntos propuestos por usuarios.

**Módulo de Comunidades**

Creación de grupos reducidos, chat interno de comunidad y biblioteca compartida con sistema de "Likes" para optimizar intercambios.

**Gestión de Quedadas**

Herramienta para organizar eventos presenciales en BookSpots y asistente de selección de libros basado en la demanda del grupo.

## Entregables clave

Módulo de mapas integrado con geolocalización de BookSpots.

Lógica de negocio para comunidades activas (mínimo 3 miembros).

---

# 5. Sprint 3 - Gamificación y Monetización

## Objetivo principal

Implementar el sistema de incentivos para asegurar la retención y desplegar las vías de ingresos B2C y B2B.

## Alcance funcional

**Sistema de InkDrops**

Lógica de asignación de puntos por intercambios y asistencia a eventos, y reseteo mensual.

**Sistema de Rachas**

Multiplicadores de puntos por actividad semanal consecutiva.

**Niveles y Recompensas**

Curva de progresión (niveles 1-50) con desbloqueo de cosméticos (marcos, insignias, colores).

**Suscripción Premium (2,99€)**

Eliminación de publicidad, acceso al Ranking Mensual y funcionalidades avanzadas de comunidad.

**Módulo Business (BookSpots Partners)**

Funcionalidad de BookDrop (custodia asíncrona) y posicionamiento prioritario para locales de pago (4,99€/mes).

## Entregables clave

Pasarela de pagos integrada para suscripciones.

Panel de ranking dinámico para usuarios Premium dentro de comunidades.

Sistema de analítica de negocio (conversión a premium, recurrencia de usuarios).