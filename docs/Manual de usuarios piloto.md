<div align="center">

<h1>Manual de Usuarios Piloto</h1>

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

- [Manual de Usuarios Piloto](#manual-de-usuarios-piloto)
- [1. Historial de Versiones](#1-historial-de-versiones)
- [2. Introducción y objetivos](#2-introducción-y-objetivos)
  - [2.1 Objetivos de la Prueba Piloto](#21-objetivos-de-la-prueba-piloto)
- [3. Perfil y captación de usuarios piloto](#3-perfil-y-captación-de-usuarios-piloto)
  - [3.1 Estrategia de Captación (Sistema de Tiers)](#31-estrategia-de-captación-sistema-de-tiers)
  - [3.2 Segmentación de los Usuarios Piloto actuales](#32-segmentación-de-los-usuarios-piloto-actuales)
- [4. Escenarios de Prueba](#4-escenarios-de-prueba)
- [5. Plan de Pruebas y Encuesta](#5-plan-de-pruebas-y-encuesta)
  - [Métricas de Éxito (KPIs)](#métricas-de-éxito-kpis)
  - [Bloque A: Usabilidad](#bloque-a-usabilidad)
  - [Bloque B: Valor Diferencial](#bloque-b-valor-diferencial)
  - [Bloque C: Bugs Técnicos](#bloque-c-bugs-técnicos)
- [6. Plan de Comunicaciones](#6-plan-de-comunicaciones)
- [7. Ejecución del Piloto](#7-ejecución-del-piloto)
- [8. Evaluación de Aprendizajes](#8-evaluación-de-aprendizajes)

---

## 1. Historial de Versiones

| Versión | Fecha      | Participantes                                     | Resumen de los cambios                                  |
|:------:|:----------:|---------------------------------------------------|--------------------------------------------------------|
| v1.0   | 15/02/2026 | Fernando Triguero                                 | Creación de la versión inicial del documento           |
| v1.1   | 16/02/2026 | Fernando Triguero, David Escudero, Peter Carter   | Añadidos usuarios y modificación de apartados          |
| v1.2   | 17/02/2026 | Samuel Granado  | Conversión a markdown

---

## 2. Introducción y objetivos

El objetivo de este manual es definir el protocolo de pruebas para la fase inicial de validación de Bookmerang, centrado en las funcionalidades CORE del MVP y en el flujo principal de intercambio físico de libros antes de escalar a funcionalidades sociales más complejas.

### 2.1 Objetivos de la Prueba Piloto

1. **Validar el Flujo de Intercambio:** Verificar que un usuario puede subir un libro, hacer match, chatear y cerrar un acuerdo sin errores.
2. **Testear el Algoritmo de Matching:** Comprobar que la geolocalización y las preferencias de género muestran resultados relevantes.
3. **Detectar Fricción:** Identificar puntos donde el usuario se pierde o frustra (ej. escaneo de ISBN, coordinación en chat).

---

## 3. Perfil y captación de usuarios piloto

Siguiendo la estrategia de captación definida y el feedback recibido, los usuarios se clasifican en dos niveles (Tiers) para una captación controlada, contando actualmente con 20 usuarios confirmados para el Tier 1 y 0 usuarios para el Tier 2.

### 3.1 Estrategia de Captación (Sistema de Tiers)

- Tier 1: Círculo cercano (amigos y compañeros).
    - Objetivo: Feedback rápido, alta tolerancia a fallos y pruebas de estrés iniciales.
    - Canal: Contacto directo y redes sociales personales.

- Tier 2: Familiares y conocidos con negocios locales.
    - Objetivo: Validar la usabilidad con usuarios de rangos de edad más amplios, así como integrar algunos BookSpots dispuestos a apoyar la aplicación.


### 3.2 Segmentación de los Usuarios Piloto actuales

Para asegurar una prueba efectiva, se han seleccionado usuarios que cumplen con los diferentes perfiles identificados en el estudio de mercado, siguiendo los siguientes tipos de usuario:

- Usuario A (Lector Estudiante/Económico): Busca libros académicos, además de best-sellers. Sensible al ahorro económico y de espacio.
- Usuario B (Lector Ecológico): Quiere dar una segunda vida a sus libros, motivado por la sostenibilidad. No le importa leer libros usados.
- Usuario C (Lector Económico): Quiere leer libros populares pero sin pagar el precio completo de un libro nuevo.
- Usuario D (Lector Social): Interesado en la gamificación y en el descubrimiento de nuevas historias.


| Nombre                          | Tipo de Usuario | Correo                                            |
|---------------------------------|-----------------|---------------------------------------------------|
| Andrés Triguero Soberá          | A               | ats0019@alu.medac.es                              |
| Raúl Martín Torrabadella Mendoza| C               | raul2.martin.torrabadella@gmail.com              |
| Ismael Pagés Domínguez          | C               | aipages20@iesvcntenario.org                      |
| Alberto Martín Puertas          | D               | murchero88@gmail.com                              |
| Antonio Del Can Segovia         | C               | delkyjr@hotmail.com                               |
| Ricardo Rodriguez Gonzalez      | B               | ricardorodriguezgonzalez15@gmail.com             |
| Ana Jimeno Carvajal             | D               | anajimeno279@gmail.com                            |
| Miguel Ángel Doval Romero       | D               | miguedr66@gmail.com                               |
| Irene Atencia Silva             | A               | atencia190604@gmail.com                           |
| Andrés Díaz Camacho             | A               | andresdiazcamacho@gmail.com                       |
| Carlos Díaz Boza                | C               | cadibo10@gmail.com                                |
| Fernando Cobos García           | A               | fernandodeportivo6@gmail.com                      |
| Adrián Robles Borrego           | A               | adrrobbor@alum.us.es                              |
| Andrés Dominguez Hidalgo        | A               | anddomhid@alum.us.es                              |
| Lucía Jimeno Carvajal           | B               | lujimeno7@gmail.com                               |
| Óscar Martín Leal               | C               | oscar10ml@gmail.com                               |
| Roberto Almendros Rodríguez     | A               | robertoar2004@gmail.com                           |
| Jorge Cabezas Grillo            | A               | jorgecabezas2004@gmail.com                        |
| Rosa García Monterrubio         | D               | garciamonterrubiorosa@gmail.com                   |
| Roberto Cordero Brenes          | D               | eustaquiofernandezambrosio@gmail.com             |

---

## 4. Escenarios de Prueba

Se han diseñado 4 escenarios CORE obligatorios para cada usuario.

- **Escenario A: Onboarding y Configuración**  
  - *Acción:* Registro de usuario y configuración de preferencias (distancia y géneros).  
  - *Objetivo:* Asegurar que el algoritmo de matching tenga datos para trabajar.

- **Escenario B: Digitalización (Subir Libro)**  
  - *Acción:* Subida de al menos 2 libros usando escaneo de ISBN y cámara.  
  - *Objetivo:* Validar la ausencia de fricción en la carga de inventario y el correcto funcionamiento del escaneo con la cámara.

- **Escenario C: Discovery (El Match)**  
  - *Acción:* Navegación en el Matcher, swipes izquierda/derecha y logro de “Match recíproco”.  
  - *Objetivo:* Validar la geolocalización y la visualización de tarjetas.

- **Escenario D: Cierre del Ciclo (Chat & Intercambio)**  
  - *Acción:* Negociación de lugar/hora y pulsación de “Aceptar Intercambio”.  
  - *Objetivo:* Confirmar el cambio de estado del libro y la finalización del flujo.

---

## 5. Plan de Pruebas y Encuesta

### Métricas de Éxito (KPIs)

Para medir la satisfacción, utilizaremos el Net Promoter Score **(NPS)** en la encuesta final:
- **Promotores** (9-10): El flujo es excelente.
- **Pasivos** (7-8): Funciona, pero falta "magia" o hay fricción leve.
- **Detractores** (0-6): Fallos críticos o propuesta de valor no entendida. **Cuestionario de Feedback**

### Bloque A: Usabilidad

- ¿Te resultó sencillo configurar tus géneros literarios y tu ubicación al registrarte?  
- Al usar el escáner de ISBN, ¿el sistema reconoció el libro a la primera o tuviste que introducir los datos manualmente?  
- ¿El proceso de subir las fotos del libro te pareció rápido o tedioso? ¿Pudiste usar la cámara directamente sin problemas?  
- ¿Dudaste en algún momento sobre qué "Estado" seleccionar para tu libro?  
- En la pantalla de Matcher, ¿la información de la tarjeta fue suficiente para decidir el swipe o echaste en falta algún dato?  
- ¿Te quedó claro cuándo el intercambio estaba oficialmente "Aceptado" por ambas partes?

### Bloque B: Valor Diferencial

- Al usar el Matcher, ¿sentiste que el proceso fue más ágil y menos estresante que negociar un precio en apps de segunda mano?  
- ¿El sistema de swipe te resultó efectivo para descubrir libros cercanos o preferirías un buscador tradicional?  
- Durante el chat, ¿sentiste solo coordinación de entrega o conexión con otro lector con gustos afines?  
- ¿Te motivó más liberar espacio en tu estantería o conseguir un libro nuevo gratis?

### Bloque C: Bugs Técnicos

- Reporte libre de fallos (cierres inesperados, fotos que no cargan, ubicación errónea, etc.).

---

## 6. Plan de Comunicaciones

Dado que estamos en la fase de Tier 1 (Círculo Cercano), la comunicación se basará en la confianza y la proximidad para reducir la fricción del usuario.

Modelo de Enlace Directo:

- Cada usuario piloto se comunicará exclusivamente con el miembro del equipo que lo invitó/reclutó.
- No se utilizarán grupos generales para evitar el "efecto espectador" y asegurar respuestas personalizadas.

Responsabilidad del Miembro del Equipo:

- Actuar como filtro y soporte de primer nivel.
- Recopilar el feedback informal (audios de WhatsApp, comentarios en persona) y transcribirlo a las herramientas de gestión del proyecto.
- Reportar los bugs bloqueantes inmediatamente al equipo de desarrollo.

Canales Habilitados:

- WhatsApp personal (contacto directo).
- Comunicación presencial.


---

## 7. Ejecución del Piloto

Cronograma de Ejecución (4 Días):

- **Día 1: Preparación** (Escenarios A y B)
  - Usuarios descargan la app.
  - Completan registro y suben inventario (mínimo 2 libros).
- **Día 2: Sincronización** (Escenario C)
    - Todos los usuarios entran al Matcher.
    - Se fuerza el ajuste de distancia en preferencias para asegurar visibilidad entre ellos.
    - Generación de Matches.

- **Día 3: Interacción** (Escenario D)
    - Uso del Chat.
    - Simulación física del encuentro (o real si es posible).
    - Cierre del intercambio en la app.
- **Día 4: Feedback**
    - Envío y cumplimentación de la encuesta a través de su enlace directo del equipo.

---

## 8. Evaluación de Aprendizajes

Al finalizar el Día 4, el equipo realizará una sesión de "Review" para procesar los datos:
1. **Cálculo de NPS**: Clasificar la recepción general del MVP.
2. **Análisis de Fricción**: Identificar en qué paso de la ejecución hubo más dudas (basado en Bloque A de la encuesta).
3. **Validación de Hipótesis**: Confirmar si se cumple la premisa de "Océano Azul" (basado en Bloque B).
4. **Priorización de Bugs**: Clasificar los errores técnicos del Bloque C para el siguiente Sprint de corrección.

