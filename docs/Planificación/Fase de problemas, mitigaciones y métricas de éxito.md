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
| v1.2    | 05/04/2026 | Peter Carter  | Reformulación de P-TEC-09 con métricas binarias de control de ramas y revisión por pares. Renombrado P-ORG-03 a Scope Creep con métrica y validación específica mediante auditoría de Backlog. Añadida evidencia de integración Git en sección 4.1. |
| v1.3    | 07/04/2026 | Peter Carter  | Clarificación de los umbrales  y cambios en riesgo de créditos de Azure|

---

## 2. Cuadro de Mando Unificado: Problemas, Soluciones y Métricas

Este panel integra la evolución desde las medidas de urgencia hacia las soluciones estructurales, vinculando cada riesgo con su indicador de éxito.

| ID | Riesgo | Medida de Urgencia (Parche Rápido) | Solución Estructural (Mitigación) | Métrica / KPI | Umbral de Éxito | Estado |
|:---:|---|---|---|---|---|:---:|
| **P-TEC-01** | Curva .NET / C# | Refactorización reactiva. | Sesiones técnicas y revisión de código. | Tasa éxito Pull Requests. | > 90% aprobadas (1ª rev). | En ejecución |
| **P-TEC-02** | Curva Aprendizaje Expo | Consultas rápidas doc. | Formación interna y prototipo básico. | Tasa de errores de sintaxis. | < 15% de builds fallidos por Sprint. | Completado |
| **P-TEC-03** | Dificultad Supabase | Consultas rápidas doc. | Tutoriales y soporte dedicado. | Consumo de recursos. | No superar plan gratuito. | Completado |
| **P-TEC-04** | PostGIS / Matching | Lógica simplificada. | Formación PostGIS y test de carga. | Latencia de Matching. | Consultas en < 500 ms. | En ejecución |
| **P-TEC-05** | Conocimiento Requisitos | Consultas puntuales. | Q&A de requisitos y lectura profunda. | Tasa de retrabajo (Rework). | < 10% tareas devueltas. | Completado |
| **P-TEC-06** | Arq. Distribuida | Consultas ad-hoc. | Diagramas de arq. y tutorías. | Éxito en Integración. | 100% módulos integrados. | Completado |
| **P-TEC-07** | Foco en MVP | Corrección al vuelo. | MoSCoW y definición estricta. | Puntos dedicados al Core. | > 80% de puntos del Sprint. | En ejecución |
| **P-TEC-08** | Límites Técnicos Expo | Parches por ritmo exigido. | Definición de módulos y GPS nativo. | Disponibilidad GPS/Mapas. | 100% operativos. | Completado |
| **P-TEC-09** | Conflictos y falta de revisión en Git | Resolución manual crisis. | Prohibición de commits directos / Revisión por pares. | Commits directos / PRs sin revisar. | 0 commits directos / 100% PRs revisadas. | En ejecución |
| **P-ORG-01** | Sobrecarga / Sprint | Esfuerzo agónico. | Planning Poker y Burndown Chart. | Variación de Velocidad / Distribución Burndown. | Desviación < 15% y < 30% puntos en últimas 48h. | En observación |
| **P-ORG-02** | Comunicación F/B | Sincronización verbal. | Documentación Swagger/OpenAPI. | Errores integración API. | < 5% fallos de interface. | Completado |
| **P-ORG-03** | Scope Creep (Alcance) | Recorte de tareas no críticas. | Derivación de ideas al Backlog y foco MVP. | Funciones extra en desarrollo. | 0 funciones fuera del MVP. | En ejecución |
| **P-ORG-04** | Disponibilidad equipo | Reasignación tareas. | Avisos de antelación y rotación. | Tareas bloqueadas. | 0 tareas críticas bloqueadas. | En ejecución |
| **P-INF-01** | Complejidad Azure | Despliegue manual. | Despliegue temprano cloud. | Incidencias despliegue. | 0 tras puesta en marcha. | Mitigado |
| **P-INF-02** | Interrupciones | Uso entornos alternativos. | Alertas y monitorización Azure. | Tiempo de actividad (Uptime). | Disponibilidad >= 99%. | En ejecución |
| **P-INF-03** | Créditos Azure | Entornos gratuitos. | Solo prod. y uso de 3 cuentas. | Saldo de créditos por cuenta. | Gasto < 100 € por cuenta. | Mitigado |

---

## 3. Métricas de Solución y Umbrales

Este apartado detalla los indicadores clave de desempeño (KPI) utilizados para monitorizar la efectividad de las mitigaciones aplicadas. Cada riesgo cuenta con una métrica unívoca que permite validar objetivamente el éxito del proyecto.

### 3.1. Métricas Técnicas y de Desarrollo

- **P-TEC-01 (Aprendizaje .NET / C#):** Se mide mediante la Tasa de éxito en Pull Requests (PRs). El umbral es que más del 90% de las PRs sean aprobadas en la primera revisión sin requerir cambios estructurales, entendidos como la reescritura de lógica de negocio, el rediseño de clases o la modificación de contratos de interfaz. Los comentarios cosméticos o de estilo no invalidan la aprobación.
- **P-TEC-02 (Curva Aprendizaje Expo):** Se mide mediante el número de builds fallidos por causa de errores de sintaxis en cada Sprint. El umbral es que estos builds fallidos no superen el 15% del total de builds ejecutados en el Sprint, calculado como: (builds fallidos por sintaxis / total de builds) × 100. Esta métrica se obtiene directamente de los logs de compilación del pipeline de CI/CD.
- **P-TEC-03 (Dificultad con Supabase):** Se monitoriza el consumo de recursos de la plataforma frente a los límites del plan gratuito de Supabase, que establece un máximo de 500 MB de base de datos, 1 GB de almacenamiento de archivos y 2 GB de transferencia de datos mensual. El umbral de éxito es no superar ninguno de estos tres límites, verificable directamente en el panel de cuotas de Supabase.
- **P-TEC-04 (PostGIS y Matching Geográfico):** Se mide por la latencia media del algoritmo de Matching, calculada como el tiempo medio de respuesta de las consultas de búsqueda por proximidad ejecutadas durante las pruebas de carga. El umbral es un tiempo medio de respuesta inferior a 500 ms.
- **P-TEC-05 (Conocimiento de Requisitos):** Se utiliza la Tasa de retrabajo (Rework), calculada como el porcentaje de tareas completadas en un Sprint que son devueltas a desarrollo por no cumplir los criterios de aceptación definidos, sobre el total de tareas completadas en ese mismo Sprint: (tareas devueltas / tareas completadas) × 100. El umbral es mantener este porcentaje por debajo del 10% en cada Sprint.
- **P-TEC-06 (Arquitectura Distribuida):** Se mide por el éxito en la integración de los módulos definidos en la arquitectura del sistema (frontend, backend, base de datos y servicios externos). Un módulo se considera integrado cuando supera satisfactoriamente las pruebas de integración automatizadas con el resto del sistema y está desplegado en el entorno correspondiente. El umbral es que el 100% de los módulos definidos alcancen este estado antes de la entrega final.
- **P-TEC-07 (Foco en el MVP):** Se monitoriza el porcentaje de puntos de historia completados en cada Sprint que corresponden a funcionalidades clasificadas como "Must Have" según la priorización MoSCoW acordada al inicio del proyecto. La clasificación de cada historia de usuario como Core o no-Core queda fijada en el Backlog antes del inicio del Sprint y no puede modificarse durante el mismo. El umbral es que más del 80% de los puntos completados pertenezcan a esta categoría.
- **P-TEC-08 (Límites Técnicos de Expo):** Se valida comprobando que el 100% de las funcionalidades del MVP que dependen de GPS o mapas responden correctamente en los dispositivos de prueba definidos por el equipo. Una funcionalidad se considera operativa si completa su flujo completo sin errores de permisos, de renderizado o de geolocalización en al menos 3 ejecuciones consecutivas. Este umbral se verifica antes de cada entrega.
- **P-TEC-09 (Conflictos y falta de revisión en Git):** La métrica es binaria y aplica exclusivamente sobre las ramas protegidas del repositorio (main y develop). Se busca un 0% de commits directos sobre estas ramas y un 100% de Pull Requests aprobadas por al menos un compañero distinto al autor antes de su fusión. Ambas condiciones deben cumplirse simultáneamente; el incumplimiento de cualquiera de ellas invalida el umbral. Esto garantiza que ningún código llegue a producción sin revisión por pares.

### 3.2. Métricas Organizativas y de Gestión

- **P-ORG-01 (Sobrecarga y Velocity):** Se utilizan dos indicadores complementarios. El primero es la Variación de Velocity, calculada como la diferencia porcentual entre los puntos comprometidos al inicio del Sprint y los puntos completados al cierre; el umbral es una desviación inferior al 15%. El segundo es la Distribución del trabajo, verificada mediante el Burndown Chart: se considera exitoso si menos del 30% de los puntos totales del Sprint se completan en las últimas 48 horas previas a la entrega, lo que evidencia que el Planning Poker ha generado estimaciones realistas y sostenibles.
- **P-ORG-02 (Comunicación Front vs Back):** Se utiliza la Tasa de errores en la integración de la API, calculada como el porcentaje de endpoints que producen respuestas inesperadas (tipos de datos incorrectos, campos ausentes o códigos de error no contemplados en el contrato Swagger) sobre el total de endpoints probados en cada ciclo de integración: (endpoints con error / total endpoints probados) × 100. El umbral es inferior al 5%.
- **P-ORG-03 (Control de Alcance):** Se mide mediante el conteo de funcionalidades en desarrollo activo que no figuren en la lista de requisitos "Must Have" del MVP, definida y congelada al inicio del proyecto en el Product Backlog. Una funcionalidad se considera "fuera del MVP" si tiene tareas activas en el tablero y no está incluida en dicha lista de referencia. El umbral de éxito es 0 funcionalidades en ese estado, validando que cualquier idea nueva ha sido derivada correctamente al Backlog como ítem "Post-MVP".
- **P-ORG-04 (Disponibilidad del equipo):** Se monitoriza el número de tareas bloqueadas por ausencias no previstas. A efectos de esta métrica, una tarea se considera **crítica** si está en el Sprint activo, tiene dependencias directas con otras tareas en curso y su bloqueo impide el avance de al menos otro miembro del equipo. El umbral es de 0 tareas críticas bloqueadas según esta definición.

### 3.3. Métricas de Infraestructura y Costes

- **P-INF-01 (Complejidad Azure Ops):** Se mide por el número de incidencias técnicas tras el despliegue. A efectos de esta métrica, una incidencia se considera **crítica** si provoca una caída total del servicio, pérdida o corrupción de datos, o impide el acceso de los usuarios a las funcionalidades del MVP. El umbral es de 0 incidencias críticas según esta definición tras cada despliegue estable.
- **P-INF-02 (Interrupciones de servicio):** Se utiliza el Tiempo de actividad del servicio (Uptime) medido por Azure Monitor durante los periodos de evaluación y demostración del proyecto. El umbral es una disponibilidad igual o superior al 99% en dichos periodos, lo que equivale a un máximo de aproximadamente 7 minutos de caída por cada 12 horas de ventana de evaluación. Fuera de estos periodos, se acepta una disponibilidad menor derivada del uso de entornos de bajo coste.
- **P-INF-03 (Créditos Azure):** Se controla el saldo de créditos disponibles en cada una de las tres cuentas de Azure habilitadas para el despliegue. El umbral de éxito es que ninguna de las cuentas supere un gasto de 100 €, garantizando así la continuidad del servicio hasta el cierre del proyecto sin agotar los créditos disponibles.

---

## 4. Validación y Verificación

Para asegurar que las mitigaciones han sido efectivas, se han establecido los siguientes métodos de verificación para cada punto de control.

### 4.1. Verificación de Calidad Técnica y Desarrollo

- **Validación de Código (.NET y C#):** Se verifica mediante el Historial de Pull Requests en el repositorio, calculando el porcentaje de PRs aprobadas en la primera revisión sin requerir cambios estructurales sobre el total de PRs abiertas en el Sprint. El umbral se cumple si dicho porcentaje supera el 90%.
- **Verificación de Aprendizaje (Expo y Sintaxis):** Se valida a través de los Logs de compilación del pipeline de CI/CD, calculando el porcentaje de builds fallidos por errores de sintaxis sobre el total de builds del Sprint. El umbral se cumple si dicho porcentaje es inferior al 15%.
- **Validación de Supabase:** Se verifica consultando directamente el Panel de cuotas de Supabase, confirmando que el uso se mantiene por debajo de los tres límites definidos: 500 MB de base de datos, 1 GB de almacenamiento de archivos y 2 GB de transferencia de datos mensual.
- **Prueba de Rendimiento (PostGIS):** Se valida mediante la ejecución de Tests de carga y latencia. La evidencia es un tiempo medio de respuesta inferior a 500 ms en las consultas de búsqueda por proximidad.
- **Verificación de Requisitos y Foco (P-TEC-05):** Se verifica revisando el tablero de tareas al cierre de cada Sprint y calculando el porcentaje de tareas completadas que fueron devueltas a desarrollo por no cumplir los criterios de aceptación. El umbral se cumple si dicho porcentaje es inferior al 10%.
- **Verificación de Foco en MVP (P-TEC-07):** Se demuestra mediante el Acta de aceptación del MVP, donde se comprueba que más del 80% de los puntos de historia completados corresponden al núcleo funcional del sistema clasificado como "Must Have".
- **Verificación de Integración de Módulos (P-TEC-06):** Se verifica comprobando que cada módulo definido en la arquitectura (frontend, backend, base de datos y servicios externos) supera las pruebas de integración automatizadas y está correctamente desplegado en el entorno correspondiente. La evidencia es el informe de resultados del pipeline de integración continua.
- **Verificación GPS y Mapas (P-TEC-08):** Se valida ejecutando cada funcionalidad del MVP que dependa de GPS o mapas en los dispositivos de prueba definidos por el equipo. El umbral se cumple si el 100% de dichas funcionalidades completan su flujo sin errores de permisos, renderizado o geolocalización en al menos 3 ejecuciones consecutivas antes de cada entrega.
- **Evidencia de Revisión en Git (P-TEC-09):** Auditoría del historial de Git en el que se verifique que todos los cambios en main y develop provienen de una Pull Request aprobada por un compañero distinto al autor, y que no existe ningún commit directo sobre dichas ramas.

### 4.2. Verificación de Gestión y Cohesión

- **Validación Social y del Equipo:** Se verifica mediante las Weekly Retrospectives. La ausencia de bloqueos interpersonales registrados en estas actas confirma la efectividad de las dinámicas de grupo.
- **Control de Planificación (Velocity y Planificación Realista):** Se valida mediante dos comprobaciones. Primera: el Gráfico de Velocidad, verificando que la diferencia entre puntos comprometidos y completados al cierre del Sprint no supera el 15%. Segunda: el Burndown Chart, verificando que menos del 30% de los puntos del Sprint se completen en las últimas 48 horas previas a la entrega. Ambas condiciones deben cumplirse para considerar el indicador satisfecho.
- **Verificación de la Comunicación (Swagger):** Se demuestra mediante el Contrato Swagger UI operativo y accesible. La validación se realiza comparando las interfaces del Frontend y el Backend en las pruebas de integración; un fallo inferior al 5% confirma que Swagger actúa como fuente de verdad única.
- **Control de Alcance (Scope Creep):** Se verifica mediante una auditoría del Backlog de Producto. La evidencia de que esta mitigación funciona es que todas las funcionalidades detectadas fuera del núcleo funcional (MVP) están correctamente etiquetadas como "Post-MVP" o "Backlog" y no presentan actividad en el historial de desarrollo, garantizando que el equipo no ha desviado recursos del objetivo principal.
- **Control de Disponibilidad:** Se verifica mediante el Registro de asistencia y horas del equipo. La ausencia de tareas críticas bloqueadas demuestra que la rotación de conocimiento ha sido efectiva.

### 4.3. Verificación de Infraestructura y Viabilidad

- **Validación de Estabilidad Cloud (Azure):** Se verifica mediante los Informes de disponibilidad (Uptime) de Azure. Un registro del 99% o superior garantiza la operatividad de la infraestructura cloud.
- **Control de Incidencias:** Se valida mediante el Log de errores en producción, donde el objetivo es mantener un registro de cero incidencias críticas tras los despliegues estables.
- **Verificación Económica (Créditos):** Se demuestra mediante capturas del Dashboard de Facturación de Azure de cada una de las tres cuentas. El umbral se cumple si ninguna de las cuentas registra un gasto acumulado superior a 300 €, garantizando la continuidad del servicio hasta el cierre del proyecto.