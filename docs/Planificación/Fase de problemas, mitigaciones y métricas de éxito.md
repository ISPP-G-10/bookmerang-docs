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
- [2. Cuadro de Mando Unificado: Problemas, Soluciones y Métricas](#2-cuadro-de-mando-unificado-problemas-soluciones-y-métricas)
- [3. Métricas de Solución y Umbrales](#3-métricas-de-solución-y-umbrales)
- [4. Validación y Verificación](#4-validación-y-verificación)

---

## 1. Historial de Versiones

| Versión | Fecha       | Participantes | Resumen de los cambios |
|:------:|:-----------:|---------------|-----------------------|
| v1.0   | 01/04/2026  | Peter Carter  | Primera versión del documento de control |

---

## 2. Cuadro de Mando Unificado: Problemas, Soluciones y Métricas

Este panel integra la evolución desde las medidas de urgencia hacia las soluciones estructurales, vinculando cada riesgo con su indicador de éxito y umbral correspondiente.

| ID | Problema Detectado | Medida de Urgencia (Parche Rápido) | Solución Estructural (Mitigación) | Métrica / KPI Asociado | Umbral de Éxito | Estado |
|:---:|---|---|---|---|---|:---:|
| **P-TEC-01** | Curva de aprendizaje .NET / C# | Refactorización reactiva ante errores inmediatos. | Sesiones de transferencia técnica y revisión de código. | Tasa de éxito en Pull Requests (PRs). | > 90% aprobadas sin refactorización crítica. | En ejecución |
| **P-TEC-02** | Dependencias y GPS en Expo | Medidas de urgencia para mantener el ritmo inicial. | Definición de módulos y prototipo temprano de GPS. | Disponibilidad de servicios Core. | 100% de servicios GPS/Mapas operativos. | Completado |
| **P-TEC-03** | Dificultad con Supabase | Consultas rápidas a documentación externa. | Tutoriales internos y equipo de soporte dedicado. | Consumo de recursos de plataforma. | No superar los límites del plan gratuito. | Completado |
| **P-ORG-01** | Tensiones e intergrupales ("Malos rollos") | Aislamiento temporal para evitar discusiones. | Ejercicios de Team Building y fomento del compañerismo. | Bloqueos por falta de cohesión. | 0 bloqueos críticos (registrados en retrospectivas de Sprint). | Completado |
| **P-ORG-02** | Ejecución de tareas tardía (Sprint final) | Sobrecarga de trabajo y "sprints agónicos" para entregar. | Implementación de Planning Poker y división de historias. | Variación de la velocidad (Velocity). | Desviación < 15% entre puntos prometidos y hechos. | En observación |
| **P-ORG-03** | Comunicación deficiente (Front vs Back) | Sincronización verbal ad-hoc para parches rápidos. | Documentación de APIs mediante Swagger/OpenAPI. | Tasa de errores en integración API. | < 5% de fallos por desajuste de interfaces. | Completado |
| **P-INF-01** | Complejidad operativa en Azure | Pruebas locales y despliegue manual improvisado. | Despliegue temprano para eliminar incertidumbre técnica. | Incidencias de despliegue en producción. | 0 incidencias técnicas tras la puesta en marcha. | Mitigado |

---

## 3. Métricas de Solución y Umbrales

Se describe la lógica de verificación para los indicadores clave de desempeño.

### A. Calidad de la Integración (Software)
- **Métrica:** Tasa de éxito en la integración de código (Pull Requests).
- **Umbral:** Se requiere que más del 90% de las PRs sean aprobadas sin refactorización crítica tras la primera revisión.
- **Criterio de Éxito:** La reducción de "vueltas" en el código indica que el equipo ha asimilado las convenciones de .NET y Expo.
- **Estado:** Cumplido; el equipo domina actualmente la estructura de módulos.

### B. Rendimiento del Algoritmo (Matching)
- **Métrica:** Tiempo de respuesta del algoritmo PostGIS.
- **Umbral:** Las consultas de matching geográfico deben ejecutarse en menos de 500 ms.
- **Criterio de Éxito:** Validación mediante pruebas de rendimiento con datos simulados bajo carga.
- **Estado:** En validación.

### C. Eficiencia de Gestión (Velocity)
- **Métrica:** Variación de la velocidad del Sprint.
- **Umbral:** La desviación entre los puntos de historia comprometidos y los terminados debe ser inferior al 15%.
- **Criterio de Éxito:** La distribución uniforme del trabajo elimina la necesidad de ejecuciones tardías críticas al final del ciclo.
- **Estado:** En mejora tras la aplicación de parches de gestión.

---

## 4. Validación y Verificación

La efectividad de las soluciones se valida mediante las siguientes evidencias objetivas obtenidas durante el desarrollo:

* **Hito de Infraestructura:** Cierre del riesgo de complejidad operativa de Azure el **21 de febrero de 2026** tras un despliegue exitoso sin incidencias técnicas registradas.
* **Hito de Gestión de Tiempos:** La implementación del Planning Poker y la división de tareas han permitido realizar estimaciones más realistas, reduciendo la sobrecarga de trabajo. Se verifica mediante la eliminación de los "sprints agónicos" de última hora, logrando una distribución del trabajo mucho más uniforme.
* **Hito de Comunicación:** La adopción de **Swagger** ha centralizado la definición de datos, permitiendo que Frontend y Backend trabajen de forma síncrona y sin los bloqueos de integración detectados en fases tempranas.