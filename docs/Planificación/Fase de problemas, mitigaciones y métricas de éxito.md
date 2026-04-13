<div align="center">

<h1>Fase de problemas, mitigaciones y métricas de éxito</h1>

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
      <strong>Grupo:</strong> 8 — <em>Bookmerang</em><br/>
      <strong>Grado:</strong> Ingeniería del Software<br/>
      <strong>Centro:</strong> ETSII — Universidad de Sevilla
    </p>
  </div>

</div>

</div>

<hr/>

## Índice

- [1. Historial de Versiones](#1-historial-de-versiones)
- [2. Cuadro de Mando Unificado: Problemas, Soluciones y Métricas](#2-cuadro-de-mando-unificado-problemas-soluciones-y-métricas)
  - [2.1. Problemas Organizativos y de Gestión](#21-problemas-organizativos-y-de-gestión)
  - [2.2. Problemas de Comunicación Interpersonal y Cohesión de Equipo](#22-problemas-de-comunicación-interpersonal-y-cohesión-de-equipo)
  - [2.3. Problemas de Rendimiento Individual](#23-problemas-de-rendimiento-individual)
  - [2.4. Problemas Técnicos y de Calidad del Proyecto](#24-problemas-técnicos-y-de-calidad-del-proyecto)
- [3. Definiciones Previas](#3-definiciones-previas)
  - [3.1. Rúbrica de Calidad del Trabajo](#31-rúbrica-de-calidad-del-trabajo)
  - [3.2. Definición de Decisión Documentable](#32-definición-de-decisión-documentable)
  - [3.3. Definición de Conflicto Escalado](#33-definición-de-conflicto-escalado)
  - [3.4. Definición del Índice de Rendimiento Relativo (IRR)](#34-definición-del-índice-de-rendimiento-relativo-irr)
- [4. Métricas de Solución y Umbrales](#4-métricas-de-solución-y-umbrales)
  - [4.1. Métricas Organizativas y de Gestión](#41-métricas-organizativas-y-de-gestión)
  - [4.2. Métricas de Comunicación Interpersonal y Cohesión de Equipo](#42-métricas-de-comunicación-interpersonal-y-cohesión-de-equipo)
  - [4.3. Métricas de Rendimiento Individual](#43-métricas-de-rendimiento-individual)
  - [4.4. Métricas Técnicas y de Calidad del Proyecto](#44-métricas-técnicas-y-de-calidad-del-proyecto)
- [5. Validación y Verificación](#5-validación-y-verificación)
  - [5.1. Verificación de Gestión y Cohesión](#51-verificación-de-gestión-y-cohesión)
  - [5.2. Verificación de Comunicación y Convivencia](#52-verificación-de-comunicación-y-convivencia)
  - [5.3. Verificación de Rendimiento Individual](#53-verificación-de-rendimiento-individual)
  - [5.4. Verificación de Riesgos Técnicos y de Calidad](#54-verificación-de-riesgos-técnicos-y-de-calidad)

---

## 1. Historial de Versiones

| Versión | Fecha      | Participantes | Resumen de los cambios |
|:-------:|:----------:|---------------|------------------------|
| v1.0    | 01/04/2026 | Peter Carter  | Primera versión. |
| v1.1    | 04/04/2026 | Peter Carter  | Adición de riesgos y asociación de riesgos con las métricas. |
| v1.2    | 05/04/2026 | Peter Carter  | Reformulación de P-TEC-09 con métricas binarias de control de ramas y revisión por pares. Renombrado P-ORG-03 a Scope Creep con métrica y validación específica mediante auditoría de Backlog. Añadida evidencia de integración Git en sección 4.1. |
| v1.3    | 07/04/2026 | Peter Carter  | Clarificación de los umbrales de los problemas organizativos. |
| v1.4    | 12/04/2026 | Peter Carter  | Ampliación con problemas de comunicación interpersonal y rendimiento individual. |
| v1.5    | 12/04/2026 | Peter Carter  | Incorporación de definiciones previas para garantizar que todos los umbrales sean objetivamente cuantificables. |
| v1.6    | 13/04/2026 | Javier Ulecia García  | Incorporación nuevos problemas, metricas y validaciones. |
| v2.0    | 13/04/2026 | Peter Carter, Javier Ulecia García | Unificación del criterio IRR a rango fijo [0,60–1,60]; restauradas referencias en el cuadro de mando; actualización de métricas y validaciones. |

---

## 2. Cuadro de Mando Unificado: Problemas, Soluciones y Métricas

Este panel integra la evolución desde las medidas de urgencia hacia las soluciones estructurales, vinculando cada riesgo con su indicador de éxito. Los términos marcados con (x.y) quedan definidos con precisión en el apartado siguiente.

### 2.1. Problemas Organizativos y de Gestión

| ID | Riesgo | Medida de Urgencia (Parche Rápido) | Solución Estructural (Mitigación) | Métrica / KPI | Umbral de Éxito | Estado |
|:---:|---|---|---|---|---|:---:|
| **P-ORG-01** | Sobrecarga / Sprint | Esfuerzo agónico. | Planning Poker y Burndown Chart. | Variación de Velocity / Distribución Burndown. | Desviación < 15% y < 30% puntos completados en las últimas 48h del sprint. | En observación |
| **P-ORG-02** | Comunicación Front/Back | Sincronización verbal. | Documentación Swagger/OpenAPI. | Tasa de errores de integración API: (endpoints con error / total endpoints probados) × 100. | < 5%. | Completado |
| **P-ORG-03** | Scope Creep (Alcance) | Recorte de tareas no críticas. | Derivación de ideas al Backlog y foco MVP. | Número de funcionalidades con tareas activas en el tablero que no figuran en la lista "Must Have" del Product Backlog. | 0 funcionalidades fuera del MVP. | En ejecución |
| **P-ORG-04** | Disponibilidad equipo | Reasignación de tareas. | Avisos de antelación mínima de 24h y rotación de conocimiento. | Número de tareas críticas bloqueadas (4.1). | 0 tareas críticas bloqueadas. | En ejecución |

### 2.2. Problemas de Comunicación Interpersonal y Cohesión de Equipo

| ID | Riesgo | Medida de Urgencia (Parche Rápido) | Solución Estructural (Mitigación) | Métrica / KPI | Umbral de Éxito | Estado |
|:---:|---|---|---|---|---|:---:|
| **P-COM-01** | Discusiones y desacuerdos de rumbo | Mediación verbal inmediata por los Scrum Masters. | Weekly Retrospective estructurada para canalizar desacuerdos de forma constructiva. | Número de conflictos escalados por sprint (3.3). | ≤ 1 conflicto escalado por sprint. | Completado |
| **P-COM-02** | Tensiones intergrupales entre subequipos | Intervención directa de los SMs para restablecer el diálogo. | Actividades de Team Building y reuniones conjuntas entre subequipos. | Puntuación media de la encuesta interna de convivencia (escala 1–10, media aritmética de todos los miembros). | ≥ 7,0 / 10 en la medición posterior a cada actividad de Team Building. | Completado |
| **P-COM-03** | Falta de canal común de decisiones | Uso improvisado de mensajería directa. | Canal oficial de comunicación con registro de decisiones tras cada reunión. | Porcentaje de decisiones documentables registradas en el canal oficial (3.2): (decisiones registradas / decisiones documentables totales) × 100. | ≥ 90% por semana. | En ejecución |

### 2.3. Problemas de Rendimiento Individual

| ID | Riesgo | Medida de Urgencia (Parche Rápido) | Solución Estructural (Mitigación) | Métrica / KPI | Umbral de Éxito | Estado |
|:---:|---|---|---|---|---|:---:|
| **P-REN-01** | Ejecución tardía de tareas | Redistribución urgente de carga entre miembros disponibles. | Monitorización semanal de fechas de cierre de tareas en el tablero. | Porcentaje de tareas cerradas después de la fecha acordada en la planificación: (tareas fuera de plazo / total tareas del sprint) × 100. | ≤ 25% por sprint. | En observación |
| **P-REN-02** | Desequilibrio de carga entre miembros | Reasignación puntual de tareas detectada en la Weekly Review. | Planning Poker para estimación colectiva y revisión de distribución en el Weekend Meeting. | IRR individual por miembro y semana (3.4). | IRR de cada miembro en el rango [0,60 – 1,60] cada semana. | En observación |
| **P-REN-03** | Baja calidad del trabajo entregado | Revisión adicional por pares antes de merge. | Revisión obligatoria con la rúbrica de calidad (3.1) antes de integrar cualquier entrega. | Puntuación media de calidad según la rúbrica del punto 3.1 (media de los cuatro criterios). | ≥ 7,0 / 10 por entrega. | En ejecución |
| **P-REN-04** | Miembros con rendimiento fuera del rango esperado | Conversación directa del SM con el miembro afectado. | Seguimiento individualizado semanal por el SM de referencia. | Número de miembros con IRR < 0,60 o IRR > 1,60 en una misma semana (3.4). | ≤ 2 miembros fuera del rango [0,60 – 1,60] en cualquier semana del sprint. | En observación |

### 2.4. Problemas Técnicos y de Calidad del Proyecto

| ID | Riesgo | Medida de Urgencia (Parche Rápido) | Solución Estructural (Mitigación) | Métrica / KPI | Umbral de Éxito | Estado |
|:---:|---|---|---|---|---|:---:|
| **P-TEC-01** | Acumulación de deuda técnica | Corregir bugs críticos antes de nuevas tareas. | Reserva fija de capacidad del sprint para refactorización y mejora técnica. | Porcentaje de tareas técnicas completadas respecto a las planificadas (tareas técnicas completadas / tareas técnicas planificadas) × 100. | ≥ 80% por sprint. | En ejecución |
| **P-TEC-02** | Bloqueos por dependencias entre tareas o módulos  | Repriorización inmediata de tareas bloqueadas y reasignación temporal de apoyo. | Definición explícita de dependencias en el tablero y revisión anticipada en la planificación semanal. | Porcentaje de tareas bloqueadas por dependencias no detectadas en planificación: (tareas bloqueadas por dependencia imprevista / total tareas del sprint) × 100. | ≤ 10% por sprint. | En observación |
| **P-TEC-03** | Retrasos por errores en despliegue / entorno | Hotfix inmediato y rollback si es necesario. | Checklist de despliegue + entorno de preproducción estable. | Número de incidencias de despliegue por sprint. | ≤ 1 incidencia por sprint. | En ejecución |
| **P-TEC-04** | Baja cobertura de pruebas / errores en producción. | Test manual sobre los módulos afectados. | Política mínima de test automáticos en funcionalidades clave. | Porcentaje de historias críticas cubiertas por test: (historias críticas con test / total historias críticas) × 100. | ≥ 85%. | En ejecución |

---

## 3. Definiciones Previas

Esta sección establece las definiciones acordadas por el equipo que se usan de forma consistente en el resto del documento. Su propósito es eliminar cualquier ambigüedad en la medición de los umbrales presentados en el apartado anterior.

### 3.1. Rúbrica de Calidad del Trabajo

Toda entrega de trabajo (tarea, documento o pull request) se evalúa por el revisor asignado con la siguiente rúbrica de cuatro criterios, cada uno puntuado de 0 a 10. La **puntuación final** es la media aritmética de los cuatro:

| Criterio | 0–4 (Insuficiente) | 5–6 (Aceptable) | 7–8 (Bien) | 9–10 (Excelente) |
|---|---|---|---|---|
| **Completitud** | Faltan partes esenciales o requisitos sin cubrir. | Cubre lo mínimo pero con lagunas menores. | Cubre todos los requisitos acordados. | Cubre todos los requisitos y anticipa casos límite. |
| **Corrección** | Errores que impiden el funcionamiento o comprensión. | Errores menores que no bloquean pero requieren corrección. | Funciona correctamente sin errores observables. | Sin errores y con manejo explícito de casos de error. |
| **Claridad** | Sin documentación o comentarios; imposible de entender sin ayuda. | Documentación mínima; requiere explicación adicional. | Documentación suficiente para que otro miembro lo entienda. | Documentación clara, estructura autoexplicativa. |
| **Criterios de aceptación** | No cumple los criterios de aceptación definidos en la tarea. | Cumple parcialmente (≥ 50% de los criterios). | Cumple todos los criterios de aceptación definidos. | Cumple todos los criterios y añade evidencia de prueba. |

Una entrega se considera **aceptada** si su puntuación media es ≥ 7,0. Si es inferior, el revisor devuelve la tarea con los criterios suspendidos indicados y no se integra al sprint hasta su corrección.

### 3.2. Definición de Decisión Documentable

A efectos de la métrica P-COM-03, se entiende por **decisión documentable** cualquier acuerdo tomado en el marco del proyecto que afecte a una o más de las siguientes categorías:

- Cambio en el alcance del sprint o del MVP (añadir, eliminar o posponer funcionalidades).
- Cambio en la asignación de tareas entre miembros o subequipos.
- Resolución de un conflicto técnico con impacto en la arquitectura o la API.
- Resolución de un conflicto interpersonal que haya requerido mediación del SM.
- Cambio en una fecha de entrega interna acordada en la planificación.

Las conversaciones de trabajo cotidiano (dudas puntuales, aclaraciones de detalle) **no** cuentan como decisiones documentables. El SM de cada subequipo es responsable de identificar y registrar las decisiones de su ámbito en el canal oficial al finalizar cada reunión.

### 3.3. Definición de Conflicto Escalado

A efectos de la métrica P-COM-01, un **conflicto escalado** es aquel en el que se cumplen simultáneamente las dos condiciones siguientes:

1. Los miembros implicados no han podido resolverlo por sí mismos en el plazo de 24 horas.
2. El SM ha tenido que intervenir activamente (convocar una conversación, tomar una decisión de desempate o mediar formalmente) para restablecer el trabajo normal.

Las discusiones técnicas o de criterio que se resuelven en la misma reunión sin intervención del SM **no** cuentan como conflicto escalado. El SM registra cada conflicto escalado en el mismo documento de intervenciones donde constan las decisiones documentables.

### 3.4. Definición del Índice de Rendimiento Relativo (IRR)

El **IRR** de un miembro en una semana dada se calcula como:

```
IRR = (Horas dedicadas / Calidad media de sus entregas esa semana)
      dividido entre
      (Total de horas del equipo / Calidad media del equipo esa semana)
```

Un IRR igual a 1 indica que el miembro rinde exactamente igual que la media del equipo. Valores superiores a 1 indican más horas relativas por unidad de calidad (trabajo más lento o de mayor volumen); valores inferiores a 1 indican menos horas relativas por unidad de calidad (trabajo más rápido o de menor volumen). La **calidad media** empleada en el cálculo es la puntuación obtenida con la rúbrica del apartado 3.1, por lo que su medición es objetiva y reproducible.

Los umbrales fijos de alerta por IRR son:

- **IRR < 0,60**: el miembro está aportando significativamente por debajo de la media → el SM inicia seguimiento individualizado.
- **IRR > 1,60**: el miembro está absorbiendo una carga desproporcionada o trabajando con calidad muy baja → el SM revisa la asignación de tareas.

Estos límites fijos sustituyen al rango dinámico (media ± DT) usado en versiones previas, garantizando que el umbral sea independiente de la composición del equipo en cada semana.

---

## 4. Métricas de Solución y Umbrales

Este apartado detalla el procedimiento de cálculo de cada KPI y explica por qué el umbral fijado es suficiente para validar que la mitigación está siendo efectiva.

### 4.1. Métricas Organizativas y de Gestión

- **P-ORG-01 (Sobrecarga y Velocity):** Se utilizan dos indicadores complementarios. El primero es la Variación de Velocity, calculada como `|puntos comprometidos − puntos completados| / puntos comprometidos × 100`; el umbral es una desviación inferior al 15%. El segundo es la Distribución del trabajo en el Burndown Chart: se verifica qué porcentaje de los puntos totales del sprint se completaron en las últimas 48 horas antes de la entrega; el umbral es que ese porcentaje sea inferior al 30%. Ambas métricas se leen directamente del tablero de sprint sin necesidad de juicio subjetivo.

- **P-ORG-02 (Comunicación Front vs Back):** La Tasa de errores de integración se calcula como `(número de endpoints que producen respuesta inesperada / total de endpoints probados en el ciclo de integración) × 100`. Se entiende por "respuesta inesperada" cualquier tipo de dato incorrecto, campo ausente o código de error no contemplado en el contrato Swagger vigente. El umbral es inferior al 5%. El resultado es reproducible porque el contrato Swagger actúa como referencia objetiva.

- **P-ORG-03 (Control de Alcance):** Se cuenta el número de funcionalidades que tienen al menos una tarea activa en el tablero y no aparecen en la lista "Must Have" del Product Backlog congelada al inicio del proyecto. El recuento es directo: cualquier miembro puede realizarlo consultando el tablero y el Backlog. El umbral de éxito es 0.

- **P-ORG-04 (Disponibilidad del equipo):** Una tarea se considera **crítica** si cumple las tres condiciones siguientes: (1) pertenece al sprint activo, (2) tiene al menos una dependencia directa con otra tarea en curso, y (3) su bloqueo impide que al menos otro miembro avance en su propia tarea. El número de tareas en estado "bloqueada" que cumplen esas tres condiciones se consulta en el tablero. El umbral es 0.

### 4.2. Métricas de Comunicación Interpersonal y Cohesión de Equipo

- **P-COM-01 (Conflictos escalados):** Se cuenta el número de entradas en el registro de intervenciones del SM durante el sprint, aplicando la definición del punto 3.3. La fuente de datos es el propio registro, que el SM actualiza tras cada intervención con fecha, miembros implicados y resolución alcanzada. El umbral de ≤ 1 conflicto escalado por sprint refleja que la Weekly Retrospective está funcionando como espacio de resolución preventiva.

- **P-COM-02 (Convivencia y cohesión):** La puntuación de convivencia es la media aritmética de las valoraciones individuales recogidas en la encuesta interna (escala 1–10). La encuesta se pasa antes y después de cada actividad de Team Building, lo que permite medir el impacto de forma objetiva. Los datos del equipo muestran una mejora de 4,65 a 7,65, superando el umbral de ≥ 7,0. La encuesta se repetirá al inicio de cada sprint para detectar posibles regresiones.

- **P-COM-03 (Decisiones documentadas):** Al cierre de cada reunión (Weekly Review y Weekend Meeting), el SM de cada subequipo contrasta las decisiones tomadas con la definición del punto 3.2 y registra en el canal oficial las que correspondan. Al final de la semana se calcula `(decisiones registradas en el canal / decisiones documentables identificadas por el SM) × 100`. El denominador lo determina el SM en el momento de la reunión, anotando en el acta cuántas decisiones documentables se tomaron, lo que hace el cálculo trazable y verificable por cualquier miembro del equipo.

### 4.3. Métricas de Rendimiento Individual

- **P-REN-01 (Ejecución tardía):** Al cierre de cada sprint se extrae del tablero el listado de tareas con su fecha de cierre real y su fecha acordada en la planificación. El porcentaje se calcula automáticamente como `(tareas cerradas después de su fecha acordada / total de tareas del sprint) × 100`. El umbral de ≤ 25% está alineado con el valor actual registrado (22,3%), lo que indica que el sistema de seguimiento es efectivo aunque con margen de mejora.

- **P-REN-02 (Desequilibrio de carga — IRR individual):** El IRR de cada miembro se calcula semanalmente con la fórmula del punto 3.4, usando las horas registradas en el sistema de seguimiento del equipo y la puntuación media de calidad obtenida con la rúbrica del punto 3.1. El umbral fijo de [0,60 – 1,60] se aplica de forma directa: si el IRR de un miembro cae fuera de ese rango, el SM inicia el protocolo de seguimiento antes del siguiente Weekend Meeting. Al usar límites fijos en lugar de la desviación típica dinámica, el umbral es el mismo independientemente de la semana o de cuántos miembros haya activos.

- **P-REN-03 (Calidad del trabajo entregado):** Cada entrega se puntúa con la rúbrica del punto 3.1. La puntuación final es la media de los cuatro criterios (completitud, corrección, claridad y criterios de aceptación), cada uno valorado de 0 a 10. El revisor registra la puntuación de cada criterio individualmente en el sistema de revisiones, lo que hace el resultado auditable. El umbral de ≥ 7,0 significa que la entrega debe obtener al menos un "Bien" en todos los criterios o compensar algún criterio más bajo con excelencia en otro.

- **P-REN-04 (Miembros fuera del rango de rendimiento):** Se cuenta semanalmente el número de miembros con IRR < 0,60 o IRR > 1,60, usando los mismos valores calculados para P-REN-02. El umbral de ≤ 2 miembros fuera del rango en cualquier semana del sprint actúa como señal de alerta estructural: si se supera, el SM evalúa si la causa es puntual (ausencia, pico de dificultad técnica) o sistemática (mala distribución de tareas en el Planning), y actúa en consecuencia.

### 4.4. Métricas Técnicas y de Calidad del Proyecto

- **P-TEC-01 (Acumulación de deuda técnica):** Al inicio de cada sprint, los SM registran en el Product Backlog las tareas técnicas necesarias para mantener la calidad del proyecto (refactorización, limpieza de código, optimización de consultas, mejora de estructura o documentación técnica). Al cierre del sprint se calcula el porcentaje de tareas técnicas completadas respecto a las planificadas `(tareas técnicas completadas / total tareas técnicas planificadas) × 100`. La fuente de los datos es el tablero del sprint y el backlog técnico. El umbral de éxito es ≥ 80% por sprint, ya que un valor inferior indicaría acumulación de deuda técnica que podría comprometer la mantenibilidad futura del proyecto.

- **P-TEC-02 (Bloqueos por dependencias imprevistas):** Se calcula semanalmente el porcentaje de tareas del sprint que han quedado bloqueadas durante más de 24 horas por depender de otra tarea, módulo o entrega que no fue identificada como dependencia durante la planificación inicial, siendo la fórmula `(tareas bloqueadas por dependencia imprevista / total tareas del sprint) × 100`. Se considera dependencia imprevista aquella situación en la que:
  - La tarea estaba en la columna de "In progress" al inicio del sprint.
  - El miembro asignado no puede continuar por más de 24 horas.
  - La causa del bloqueo es falta de finalización de otra tarea o módulo necesario.

  El umbral de éxito es ≤ 10% de tareas bloqueadas por sprint, ya que un valor superior indicaría una mala detección de dependencias en la planificación.

- **P-TEC-03 (Retrasos por errores en despliegue o entorno):** Se registra cada incidencia ocurrida durante despliegues, pruebas en entorno o integración continua que impida validar o entregar una funcionalidad en el tiempo previsto.
Se consideran incidencias de despliegue: 
  - errores en configuración
  - fallos en la build
  - errores de migración en la base de datos
  - incompatibilidades entre entornos
  - necesidad de rollback

  La métrica es el número total de incidencias por sprint, siendo el umbral de éxito ≤ 1 incidencia por sprint, ya que un valor superior reflejaría inestabilidad en el proceso de integración y entrega.
  La fuente de datos son los logs del sistema, el historial de despliegues y el registro interno de incidencias.

- **P-TEC-04 (Baja cobertura de pruebas en funcionalidades críticas):** Al inicio de cada sprint se identifican las historias de usuario críticas para el funcionamiento del producto (autenticación, gestión de datos, endpoints principales, persistencia, flujos sensibles).
Al cierre del sprint se calcula el porcentaje de historias críticas que cuentan con pruebas funcionales o automáticas validadas: `(historias críticas con pruebas validadas / total historias críticas del sprint) × 100` 
Se considera que una historia está cubierta si:
  - existe evidencia de prueba manual o automática
  - la prueba ha sido ejecutada con resultado satisfactorio
  - el resultado ha quedado registrado

  La fuente de datos es el tablero del sprint y el backlog técnico. El umbral de éxito es ≥ 85% por sprint, ya que un valor inferior indicaría acumulación de deuda técnica que podría comprometer la mantenibilidad futura del proyecto.

---

## 5. Validación y Verificación

Para asegurar que las mitigaciones han sido efectivas, se han establecido los siguientes métodos de verificación para cada punto de control. En todos los casos se indica la fuente de datos y quién es responsable de la comprobación.

### 5.1. Verificación de Gestión y Cohesión

- **Control de Planificación (P-ORG-01):** Responsable: SM del subequipo. Fuente: tablero de sprint. Se verifica al cierre de cada sprint comprobando (1) que la variación de Velocity no supera el 15% y (2) que el Burndown Chart no muestra más del 30% de puntos completados en las últimas 48 horas. Ambas condiciones deben cumplirse simultáneamente.

- **Verificación de Integración (P-ORG-02):** Responsable: equipo de QA. Fuente: resultados del ciclo de pruebas de integración. Se verifica tras cada ciclo de integración comprobando que la tasa de errores de la API no supera el 5% respecto al contrato Swagger vigente.

- **Control de Alcance (P-ORG-03):** Responsable: SM del subequipo. Fuente: tablero de tareas y Product Backlog. Se verifica semanalmente mediante una auditoría cruzada entre las tareas activas del tablero y la lista "Must Have" congelada. Cualquier tarea sin correspondencia en dicha lista se marca como "fuera del MVP" y se traslada al Backlog o se elimina.

- **Control de Disponibilidad (P-ORG-04):** Responsable: SM del subequipo. Fuente: tablero de tareas. Se verifica en tiempo real: cuando una tarea pasa a estado "bloqueada", el SM aplica los tres criterios de criticidad definidos en el punto 4.1 para determinar si debe activarse el protocolo de reasignación.

### 5.2. Verificación de Comunicación y Convivencia

- **Control de Conflictos (P-COM-01):** Responsable: SM de cada subequipo. Fuente: registro de intervenciones del SM. Al cierre de cada sprint se consulta el número de entradas del registro. Si supera 1, el SM y los SMs de los otros subequipos revisan conjuntamente las causas en la Weekly Retrospective siguiente para reforzar el proceso de resolución preventiva.

- **Verificación de Cohesión (P-COM-02):** Responsable: SM global del equipo. Fuente: resultados de la encuesta interna de convivencia. Se valida comparando la puntuación media posterior a cada actividad de Team Building con el umbral de 7,0. Adicionalmente, los comentarios cualitativos del campo de texto libre se revisan para detectar señales de malestar no capturadas por la puntuación numérica.

- **Control del Canal de Decisiones (P-COM-03):** Responsable: SM de cada subequipo. Fuente: canal oficial de comunicación y actas de reunión. Al cierre de cada semana el SM calcula el porcentaje de decisiones documentables registradas. Si el resultado es inferior al 90%, actualiza el registro retroactivamente con los acuerdos pendientes y emite un recordatorio al equipo para la semana siguiente.

### 5.3. Verificación de Rendimiento Individual

- **Control de Ejecución Tardía (P-REN-01):** Responsable: SM del subequipo. Fuente: historial de cambios de estado del tablero. Se calcula automáticamente al cierre del sprint. Si supera el 25%, se convoca una retrospectiva específica para identificar las causas raíz (mala estimación, bloqueos técnicos, sobrecarga) y ajustar la planificación del sprint siguiente.

- **Control del Equilibrio de Carga (P-REN-02):** Responsable: SM del subequipo. Fuente: cuadro de rendimiento individual actualizado semanalmente. El SM calcula el IRR de cada miembro con la fórmula del punto 3.4 y lo compara con el rango [0,60 – 1,60]. Si algún miembro sale del rango, el SM inicia el seguimiento individualizado antes del siguiente Weekend Meeting.

- **Verificación de Calidad (P-REN-03):** Responsable: revisor asignado a cada tarea. Fuente: historial de revisiones con puntuación desglosada por criterio. El revisor registra la puntuación de cada uno de los cuatro criterios de la rúbrica del punto 3.1. Si la media es inferior a 7,0, la entrega se devuelve indicando los criterios suspendidos. Si un miembro acumula dos entregas consecutivas por debajo de 7,0, el SM acuerda con él un plan de mejora.

- **Control de Miembros Fuera de Rango (P-REN-04):** Responsable: SM del subequipo. Fuente: mismos valores de IRR calculados para P-REN-02. Se verifica semanalmente. Si más de 2 miembros presentan IRR fuera del rango [0,60 – 1,60], el SM determina si se trata de una anomalía puntual o de una desviación estructural que requiera replanificar la distribución de tareas del sprint en curso.

### 5.4. Verificación de Riesgos Técnicos y de Calidad

- **Control de la Deuda Técnica (P-TEC-01):** Responsable: SM de cada equipo. Fuente: Product Backlog. Al cerrar cada sprint se revisa el número de tareas técnicas planificadas y completadas. Si el porcentaje de resolución es menor del 80%, se priorizan tareas técnicas en el siguiente sprint, se revisa si la carga funcional ha sido excesiva y se ajusta la planificación para evitar acumulación.

- **Control de bloqueos por dependencias (P-TEC-02):** Responsable: SM del subequipo. Fuente: tablero de tareas y registro de incidencias. Se verifica semanalmente revisando las tareas bloqueadas, la duración del bloqueo y la causa de este. Si una tarea permanece bloqueada por más de 24 horas por una dependencia no prevista, se reprioriza la tarea y se reasigna apoyo temporal. Al cerrar cada sprint se calcula el porcentaje total de tareas afectadas. Si supera el 10%, el equipo revisa en la retrospectiva si falló la detección de dependencias, la división de tareas fue incorrecta o si hubo falta de coordinación entre subequipos.

- **Control de incidencias de despliegue (P-TEC-03):** Responsable: responsable de despliegue. Fuente: logs de integración continua y registro de incidencias. Se verifica tras cada despliegue, si se detecta alguna incidencia se documenta la causa raíz, se corrige el fallo y se actualiza el checklist de despliegue para prevenir recurrencias. Al cerrar el sprint, si se supera el umbral de 1 incidencia se revisa el proceso de integración, se añaden validaciones previas y se redefine el protocolo de despliegue.

- **Control de pruebas críticas (P-TEC-04):** Responsable: equipo de QA. Fuente: archivos de pruebas y análisis de SonarCloud. Al cierre de cada sprint se revisan las historias críticas identificadas, las pruebas ejecutadas y las evidencias registradas. Si la cobertura es menor del 85%, se priorizan las pruebas pendientes antes del cierre del sprint, se bloquea la integración de funcionalidades sensibles no validadas y se revisa la carga de QA para el próximo sprint. Esto garantiza que los módulos más relevantes mantengan un nivel de calidad aceptable y reduzcan el riesgo de fallos en producción.