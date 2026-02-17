<h1 style="text-align: center;">Plan de Mitigación de Riesgos</h1>

<p style="text-align: center; font-size: 1.2em; margin-top: -10px;">
  <strong>Bookmerang</strong>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)"
            srcset="assets/img/logo-bookmerang-light.png">
    <source media="(prefers-color-scheme: light)"
            srcset="assets/img/logo-bookmerang-dark.png">
    <img alt="Bookmerang logo"
         src="assets/img/logo-bookmerang-light.png"
         width="320">
  </picture>
</p>

---

<div style="
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 16px;
  text-align: center;
">

  <div>
    <picture>
      <source media="(prefers-color-scheme: light)"
              srcset="assets/img/us-etsi-inf-dark.png">
      <source media="(prefers-color-scheme: dark)"
              srcset="assets/img/us-etsi-inf-light.png">
      <img alt="ETSII – Universidad de Sevilla"
           src="assets/img/us-etsi-inf-light.png"
           width="200">
    </picture>
  </div>

  <div>
    <p style="margin: 0;">
      <strong>Asignatura:</strong> ISPP (Curso 2025/26)<br>
      <strong>Grupo:</strong> C Tarde — <em>Bookmerang</em><br>
      <strong>Grado:</strong> Ingeniería del Software<br>
      <strong>Centro:</strong> ETSII — Universidad de Sevilla
    </p>
  </div>

</div>

---

## Índice

- [1. Historial de Versiones](#1-historial-de-versiones)
- [2. Introducción](#2-introducción)
- [3. Riesgos asociados al Frontend](#3-riesgos-asociados-al-frontend)
  - [R1 — Curva de aprendizaje en Expo](#r1--curva-de-aprendizaje-en-expo)
  - [R2 — Limitaciones técnicas del entorno Expo](#r2--limitaciones-técnicas-del-entorno-expo)
- [4. Riesgos asociados al Backend](#4-riesgos-asociados-al-backend)
  - [R3 — Curva de aprendizaje en .NET y C#](#r3--curva-de-aprendizaje-en-net-y-c)
- [5. Riesgos asociados a PostGIS y Matching Geográfico](#5-riesgos-asociados-a-postgis-y-matching-geográfico)
  - [R4 — Complejidad técnica del modelado geográfico](#r4--complejidad-técnica-del-modelado-geográfico)
- [6. Riesgos asociados a Supabase](#6-riesgos-asociados-a-supabase)
  - [R5 — Dependencia de proveedor externo](#r5--dependencia-de-proveedor-externo)
  - [R6 — Escalabilidad futura del plan gratuito](#r6--escalabilidad-futura-del-plan-gratuito)
- [7. Riesgos asociados a la arquitectura híbrida](#7-riesgos-asociados-a-la-arquitectura-híbrida)
  - [R7 — Complejidad conceptual de arquitectura distribuida](#r7--complejidad-conceptual-de-arquitectura-distribuida)
- [8. Riesgo transversal principal](#8-riesgo-transversal-principal)
  - [R8 — Dispersión del foco técnico](#r8--dispersión-del-foco-técnico)
- [9. Conclusión](#9-conclusión)

---

## 1. Historial de Versiones

| Versión | Fecha | Participantes | Resumen de los cambios |
|:---:|:---:|---|---|
| v1.0 | 16/02/2026 | Alejandro Castilla |  |

---

## 2. Introducción

El plan de mitigación identifica los riesgos técnicos asociados al stack tecnológico seleccionado para Bookmerang y establece medidas de mitigación orientadas a reducir la incertidumbre, asegurar la viabilidad del desarrollo y proteger el núcleo funcional del proyecto (matching geográfico y módulo social).

---

## 3. Riesgos asociados al Frontend

### R1 — Curva de aprendizaje en Expo

**Descripción:**  
Aunque el equipo posee experiencia previa en React, Expo introduce particularidades en la gestión de permisos, compilación nativa y despliegue como PWA que requieren aprendizaje específico.

**Impacto:** Medio  
**Probabilidad:** Media  

**Mitigación:**
- Realizar un prototipo temprano que incluya:
  - Obtención de ubicación GPS.
  - Integración con mapa.
  - Comunicación con backend.
- Documentar buenas prácticas internas de uso de Expo.
- Evitar dependencias nativas avanzadas durante el MVP.

---

### R2 — Limitaciones técnicas del entorno Expo

**Descripción:**  
Algunas funcionalidades avanzadas pueden requerir abandonar el entorno “managed” de Expo (eject), aumentando la complejidad del proyecto.

**Impacto:** Medio  
**Probabilidad:** Baja–Media  

**Mitigación:**
- Validar desde el inicio las librerías necesarias (mapas, cámara, notificaciones).
- Priorizar soluciones compatibles con Expo managed.
- Evitar introducir funcionalidades nativas no esenciales en fases tempranas.

---

## 4. Riesgos asociados al Backend

### R3 — Curva de aprendizaje en .NET y C#

**Descripción:**  
Aunque algunos miembros conocen .NET, es cierto que la mayoría del equipo carece de experiencia con C#, lo que puede generar una dependencia técnica concentrada.

**Impacto:** Medio  
**Probabilidad:** Media  

**Mitigación:**
- Establecer una arquitectura clara desde el inicio.
- Documentar convenciones internas.
- Repartir conocimiento mediante sesiones internas de transferencia técnica.
- Evitar patrones arquitectónicos excesivamente complejos en el MVP.

---

## 5. Riesgos asociados a PostGIS y Matching Geográfico

### R4 — Complejidad técnica del modelado geográfico

**Descripción:**  
El sistema de matching se basa en consultas geoespaciales. Si por nuestra inexperiencia lleváramos a cabo un diseño inadecuado del modelo de datos o de los índices, podría afectar al rendimiento y precisión del algoritmo.

**Impacto:** Alto  
**Probabilidad:** Media  

**Mitigación:**
- Definir correctamente el tipo geography.
- Crear índices GiST.
- Limitar el radio máximo de búsqueda.
- Realizar pruebas de rendimiento con datos simulados.
- Documentar el modelo espacial.

---

## 6. Riesgos asociados a Supabase

### R5 — Dependencia de proveedor externo

**Impacto:** Medio  
**Probabilidad:** Media  

**Mitigación:**
- Utilizar únicamente funcionalidades estándar de PostgreSQL.
- Centralizar la lógica de negocio en el backend.
- Mantener el esquema documentado.
- Evaluar periódicamente límites del plan utilizado.

---

### R6 — Escalabilidad futura del plan gratuito

**Impacto:** Bajo en el primer Sprint  
**Probabilidad:** Media  

**Mitigación:**
- Diseñar consultas eficientes.
- Implementar paginación.
- Monitorizar consumo de recursos.
- Planificar migración a plan superior si fuera necesario.

---

## 7. Riesgos asociados a la arquitectura híbrida

### R7 — Complejidad conceptual de arquitectura distribuida

**Impacto:** Medio  
**Probabilidad:** Media  

**Mitigación:**
- Definir un diagrama arquitectónico.
- Documentar claramente responsabilidades de cada plataforma.
- Establecer convenciones de configuración por entorno.

---

## 8. Riesgo transversal principal

### R8 — Dispersión del foco técnico

**Impacto:** Alto  
**Probabilidad:** Media  

**Mitigación:**
- Repartir conocimiento mediante sesiones internas.
- Evitar alta complejidad en el MVP.
- Introducir complejidad progresivamente.
- Revisar periódicamente que desarrollo técnico y objetivos de negocio estén coordinados.

---

## 9. Conclusión

El principal riesgo tecnológico del proyecto no reside en la infraestructura de despliegue, sino en:

- La correcta implementación del matching geoespacial.
- La gestión de la curva de aprendizaje en Expo y .NET.
- La coordinación en la arquitectura híbrida (Azure + Supabase).

La estrategia de mitigación se centra en validación temprana del núcleo funcional, documentación clara y transferencia interna de conocimiento.

---

# Tabla Resumen

| ID | Área | Riesgo | Nivel | Qué puede provocar | Prevención (Mitigación) | Plan de contingencia | Responsable |
|:---:|---|---|:---:|---|---|---|:---:|
| R-01 | Frontend (Expo) | Curva de aprendizaje en Expo y gestión de permisos GPS/mapas | Medio | Retrasos en integración del mapa y geolocalización | Prototipo técnico en Sprint 1 con GPS + mapa + llamada real al backend | Reducir funcionalidades avanzadas y mantener solo mapa básico en MVP | SMs |
| R-02 | Backend (.NET) | Dependencia de pocos miembros con experiencia en .NET | Medio | Bloqueos técnicos o sobrecarga de desarrolladores | Documentar arquitectura y realizar sesiones internas de transferencia de conocimiento | Simplificar arquitectura (monolito modular) y redistribuir tareas | SMs |
| R-03 | Base de Datos (PostGIS) | Diseño incorrecto del modelo geoespacial | Alto | Matching lento o impreciso | Definir tipo geography, crear índices GiST y testear consultas | Reducir radio de búsqueda o simplificar algoritmo temporalmente | SMs |
| R-04 | Supabase | Dependencia de servicio externo y límites del plan | Medio | Restricciones de uso o rendimiento en crecimiento | Monitorizar consumo y diseñar consultas eficientes | Escalar plan o migrar a PostgreSQL alternativo | SMs |
| R-05 | Arquitectura híbrida | Confusión sobre qué se despliega en Azure y qué vive en Supabase | Medio | Errores de configuración o decisiones inconsistentes | Crear diagrama oficial y documentar responsabilidades | Revisión técnica interna antes de despliegues | SMs |
| R-06 | Enfoque técnico | Dedicación excesiva a infraestructura en lugar del núcleo funcional | Alto | Retraso en desarrollo del Matcher y módulo social | Priorizar roadmap: primero matching y chat | Posponer mejoras infra no críticas | SMs |