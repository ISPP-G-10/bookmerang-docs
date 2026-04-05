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
- [3. Métricas de Solución y Umbrales](#3-métricas-de-solución-y-umbrales)
  - [3.1. Métricas Técnicas y de Desarrollo](#31-métricas-técnicas-y-de-desarrollo)
  - [3.2. Métricas Organizativas y de Gestión](#32-métricas-organizativas-y-de-gestión)
  - [3.3. Métricas de Infraestructura y Costes](#33-métricas-de-infraestructura-y-costes)
- [4. Validación y Verificación](#4-validación-y-verificación)
  - [4.1. Verificación de Calidad Técnica y Desarrollo](#41-verificación-de-calidad-técnica-y-desarrollo)
  - [4.2. Verificación de Gestión y Cohesión](#42-verificación-de-gestión-y-cohesión)
  - [4.3. Verificación de Infraestructura y Viabilidad](#43-verificación-de-infraestructura-y-viabilidad)

---

## 1. Historial de Versiones

| Versión | Fecha      | Participantes | Resumen de los cambios |
|:-------:|:----------:|---------------|------------------------|
| v1.0    | 01/04/2026 | Peter Carter  | Primera versión |
| v1.1    | 04/04/2026 | Peter Carter  | Adición de riesgos y asociación de riesgos con las métricas |
| v1.2    | 05/04/2026 | Peter Carter  | Reformulación de P-TEC-09 con métricas binarias de control de ramas y revisión por pares. Renombrado P-ORG-04 a Scope Creep con métrica y validación específica mediante auditoría de Backlog. Añadida evidencia de integración Git en sección 4.1. |

---

## 2. Cuadro de Mando Unificado: Problemas, Soluciones y Métricas

Este panel integra la evolución desde las medidas de urgencia hacia las soluciones estructurales, vinculando cada riesgo con su indicador de éxito.

| ID | Riesgo | Medida de Urgencia (Parche Rápido) | Solución Estructural (Mitigación) | Métrica / KPI | Umbral de Éxito | Estado |
|:---:|---|---|---|---|---|:---:|
| **P-TEC-01** | Curva .NET / C# | Refactorización reactiva. | Sesiones técnicas y revisión de código. | Tasa éxito Pull Requests. | > 90% aprobadas (1ª rev). | En ejecución |
| **P-TEC-02** | Curva Aprendizaje Expo | Consultas rápidas doc. | Formación interna y prototipo básico. | Tasa de errores de sintaxis. | < 15% en fase de desarrollo. | Completado |
| **P-TEC-03** | Dificultad Supabase | Consultas rápidas doc. | Tutoriales y soporte dedicado. | Consumo de recursos. | No superar plan gratuito. | Completado |
| **P-TEC-04** | PostGIS / Matching | Lógica simplificada. | Formación PostGIS y test de carga. | Latencia de Matching. | Consultas en < 500 ms. | En ejecución |
| **P-TEC-05** | Conocimiento Requisitos | Consultas puntuales. | Q&A de requisitos y lectura profunda. | Tasa de retrabajo (Rework). | < 10% tareas devueltas. | Completado |
| **P-TEC-06** | Arq. Distribuida | Consultas ad-hoc. | Diagramas de arq. y tutorías. | Éxito en Integración. | 100% módulos integrados. | Completado |
| **P-TEC-07** | Foco en MVP | Corrección al vuelo. | MoSCoW y definición estricta. | Puntos dedicados al Core. | > 80% de puntos del Sprint. | En ejecución |
| **P-TEC-08** | Límites Técnicos Expo | Parches por ritmo exigido. | Definición de módulos y GPS nativo. | Disponibilidad GPS/Mapas. | 100% operativos. | Completado |
| **P-TEC-09** | Conflictos y falta de revisión en Git | Resolución manual crisis. | Prohibición de commits directos / Revisión por pares. | Commits directos / PRs sin revisar. | 0 commits directos / 100% PRs revisadas. | En ejecución |
| **P-ORG-01** | Tensiones / Malos rollos | Aislamiento temporal. | Team Building y compañerismo. | Bloqueos por falta de cohesión. | 0 (en retrospectivas). | Completado |
| **P-ORG-02** | Sobrecarga / Sprint | Esfuerzo agónico. | Planning Poker y Burndown Chart. | Variación de Velocidad. | Desviación < 15% y 0 retrasos. | En observación |
| **P-ORG-03** | Comunicación F/B | Sincronización verbal. | Documentación Swagger/OpenAPI. | Errores integración API. | < 5% fallos de interface. | Completado |
| **P-ORG-04** | Scope Creep (Alcance) | Recorte de tareas no críticas. | Derivación de ideas al Backlog y foco MVP. | Funciones extra en desarrollo. | 0 funciones fuera del MVP. | En ejecución |
| **P-ORG-05** | Disponibilidad equipo | Reasignación tareas. | Avisos de antelación y rotación. | Tareas bloqueadas. | 0 tareas críticas bloqueadas. | En ejecución |
| **P-INF-01** | Complejidad Azure | Despliegue manual. | Despliegue temprano cloud. | Incidencias despliegue. | 0 tras puesta en marcha. | Mitigado |
| **P-INF-02** | Interrupciones | Uso entornos alternativos. | Alertas y monitorización Azure. | Tiempo de actividad (Uptime). | Disponibilidad >= 99%. | En ejecución |
| **P-INF-03** | Créditos Azure | Entornos gratuitos. | Solo prod. y uso de 3 cuentas. | Saldo de créditos. | Saldo > 0 euros fin proyecto. | Mitigado |

---

## 3. Métricas de Solución y Umbrales

Este apartado detalla los indicadores clave de desempeño (KPI) utilizados para monitorizar la efectividad de las mitigaciones aplicadas. Cada riesgo cuenta con una métrica unívoca que permite validar objetivamente el éxito del proyecto.

### 3.1. Métricas Técnicas y de Desarrollo

- **P-TEC-01 (Aprendizaje .NET / C#):** Se mide mediante la Tasa de éxito en Pull Requests (PRs). El umbral se establece en más del 90% de PRs aprobadas sin refactorización crítica tras la primera revisión.
- **P-TEC-02 (Curva Aprendizaje Expo):** Se utiliza la Tasa de errores de sintaxis en el desarrollo inicial. El umbral es una incidencia inferior al 15% en el código subido.
- **P-TEC-03 (Dificultad con Supabase):** Se monitoriza el consumo de recursos de plataforma. El umbral es no superar los límites del plan gratuito.
- **P-TEC-04 (PostGIS y Matching Geográfico):** Se mide por la Latencia del algoritmo de Matching. El umbral es una respuesta en menos de 500 ms.
- **P-TEC-05 (Conocimiento de Requisitos):** Se utiliza la Tasa de retrabajo (Rework). El umbral es mantener menos del 10% de tareas devueltas a desarrollo.
- **P-TEC-06 (Arquitectura Distribuida):** Se mide por el Éxito en la integración de módulos. El umbral es del 100% de integración técnica.
- **P-TEC-07 (Foco en el MVP):** Se monitoriza el porcentaje de puntos del Sprint dedicados al Core. El umbral debe ser superior al 80%.
- **P-TEC-08 (Límites Técnicos de Expo):** Se valida mediante la Disponibilidad operativa de servicios GPS y Mapas. El umbral es del 100%.
- **P-TEC-09 (Conflictos y falta de revisión en Git):** La métrica es binaria. Se busca un 0% de commits directos en la rama principal y un 100% de cumplimiento en revisiones por pares. Esto garantiza que ningún código llegue a producción sin el visto bueno de otro desarrollador.

### 3.2. Métricas Organizativas y de Gestión

- **P-ORG-01 (Cohesión y Salud del Equipo):** Se cuantifica por el Número de bloqueos interpersonales registrados. El umbral es 0.
- **P-ORG-02 (Sobrecarga y Velocity):** Una variación menor al 15% valida que las estimaciones eliminan los sprints agónicos.
- **P-ORG-03 (Comunicación Front vs Back):** Se utiliza la Tasa de errores en la integración de la API. El umbral es inferior al 5%.
- **P-ORG-04 (Control de Alcance):** Se mide mediante el conteo de funcionalidades "extra" en desarrollo activo. El umbral de éxito es 0, validando que cualquier idea nueva ha sido derivada al Backlog para proteger la entrega del MVP.
- **P-ORG-05 (Disponibilidad del equipo):** Se monitoriza el Número de tareas bloqueadas por ausencias. El umbral es de 0 tareas críticas bloqueadas.

### 3.3. Métricas de Infraestructura y Costes

- **P-INF-01 (Complejidad Azure Ops):** Se mide por las Incidencias técnicas tras el despliegue. El umbral es de 0 incidencias críticas.
- **P-INF-02 (Interrupciones de servicio):** Se utiliza el Tiempo de actividad del servicio (Uptime). El umbral es una disponibilidad igual o superior al 99%.
- **P-INF-03 (Créditos Azure):** Se controla el saldo de créditos disponibles. El umbral es mantener un saldo mayor a 0 euros hasta el despliegue final.

---

## 4. Validación y Verificación

Para asegurar que las mitigaciones han sido efectivas, se han establecido los siguientes métodos de verificación para cada punto de control.

### 4.1. Verificación de Calidad Técnica y Desarrollo

- **Validación de Código (.NET, Arquitectura y Git):** Se verifica mediante el Historial de Pull Requests en el repositorio. El cumplimiento del umbral se demuestra con el registro de aprobaciones por parte de los revisores y la ausencia de conflictos mayores en las ramas de integración.
- **Verificación de Aprendizaje (Expo y Sintaxis):** Se valida a través de los Logs de compilación y la reducción progresiva de errores técnicos reportados en el canal de desarrollo durante los primeros Sprints.
- **Validación de Supabase:** Se verifica consultando directamente el Panel de cuotas de Supabase, confirmando que el uso de filas y almacenamiento se mantiene dentro del Tier gratuito.
- **Prueba de Rendimiento (PostGIS):** Se valida mediante la ejecución de Tests de carga y latencia. La evidencia es un tiempo medio de respuesta inferior a 500 ms en las consultas de búsqueda por proximidad.
- **Verificación de Requisitos y Foco:** Se demuestra mediante el Acta de aceptación del MVP, donde se comprueba que el 80% de los puntos de historia completados corresponden al núcleo funcional del sistema.
- **Evidencia de Integración:** Auditoría del historial de Git en el que se verifique que todos los cambios en Main provienen de una Pull Request aprobada por un compañero distinto al autor.

### 4.2. Verificación de Gestión y Cohesión

- **Validación Social y del Equipo:** Se verifica mediante las Weekly Retrospectives. La ausencia de bloqueos críticos registrados en estas actas confirma la efectividad de las dinámicas de grupo.
- **Control de Planificación (Velocity y Planificación Realista):** Se valida a través del Gráfico de Velocidad (Velocity Chart) y el Burndown Chart. La prueba de éxito es la estabilidad de la pendiente en el Burndown, demostrando que el uso de Planning Poker ha eliminado la necesidad de esfuerzos agónicos en las 24 horas previas a la entrega.
- **Verificación de la Comunicación (Swagger):** Se demuestra mediante el Contrato Swagger UI operativo y accesible. La validación se realiza comparando las interfaces del Frontend y el Backend en las pruebas de integración; un fallo inferior al 5% confirma que Swagger actúa como fuente de verdad única.
- **Control de Alcance (Scope Creep):** Se verifica mediante una auditoría del Backlog de Producto. La evidencia de que esta mitigación funciona es que todas las funcionalidades detectadas fuera del núcleo funcional (MVP) están correctamente etiquetadas como "Post-MVP" o "Backlog" y no presentan actividad en el historial de desarrollo, garantizando que el equipo no ha desviado recursos del objetivo principal.
- **Control de Disponibilidad:** Se verifica mediante el Registro de asistencia y horas del equipo. La ausencia de tareas críticas bloqueadas demuestra que la rotación de conocimiento ha sido efectiva.

### 4.3. Verificación de Infraestructura y Viabilidad

- **Validación de Estabilidad Cloud (Azure):** Se verifica mediante los Informes de disponibilidad (Uptime) de Azure. Un registro del 99% o superior garantiza la operatividad de la infraestructura cloud.
- **Control de Incidencias:** Se valida mediante el Log de errores en producción, donde el objetivo es mantener un registro de cero incidencias críticas tras los despliegues estables.
- **Verificación Económica (Créditos):** Se demuestra mediante capturas del Dashboard de Facturación de Azure. El saldo positivo de las 3 cuentas redundantes asegura la continuidad del servicio hasta el cierre del proyecto.
