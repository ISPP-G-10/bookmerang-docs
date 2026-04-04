<div align="center">

<h1>Manual de Usuarios Piloto</h1>

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
- [2. Introducción y objetivos](#2-introducción-y-objetivos)
  - [2.1. Objetivos de la Prueba Piloto](#21-objetivos-de-la-prueba-piloto)
- [3. Perfil y captación de usuarios piloto](#3-perfil-y-captación-de-usuarios-piloto)
  - [3.1. Estrategia de Captación (Sistema de Tiers)](#31-estrategia-de-captación-sistema-de-tiers)
  - [3.2. Segmentación de los Usuarios Piloto actuales](#32-segmentación-de-los-usuarios-piloto-actuales)
- [4. Escenarios de Prueba](#4-escenarios-de-prueba)
- [5. Plan de Comunicaciones](#5-plan-de-comunicaciones)
- [6. Ejecución del Piloto](#6-ejecución-del-piloto)
- [7. Evaluación de Aprendizajes](#7-evaluación-de-aprendizajes)
- [8. Gestión, Expansión y Evolución de Usuarios Piloto](#8-gestión-expansión-y-evolución-de-usuarios-piloto)
  - [8.1. Gestión Continua de los Usuarios Piloto](#81-gestión-continua-de-los-usuarios-piloto)
  - [8.2. Expansión y Ampliación de la Lista de Usuarios](#82-expansión-y-ampliación-de-la-lista-de-usuarios)
  - [8.3. Continuidad más allá del MVP (Nuevas Funcionalidades)](#83-continuidad-más-allá-del-mvp-nuevas-funcionalidades)

---

<!-- pagebreak -->

## 1. Historial de Versiones

| Versión | Fecha | Participantes | Resumen de los cambios |
|---|---|---|---|
| v1.0 | 15/02/2026 | Fernando Triguero | Creación de la versión inicial del documento |
| v1.1 | 16/02/2026 | Fernando Triguero, David Escudero, Peter Carter | Añadidos usuarios y modificación de apartados |
| v1.2 | 02/03/2026 | Fernando Triguero Caballo | Añadido BookSpot y apartado 9 |

<!-- pagebreak -->

## 2. Introducción y objetivos

El objetivo de este manual es definir el protocolo de pruebas para la fase inicial de validación de Bookmerang. Esta fase se centra exclusivamente en las funcionalidades CORE del MVP, asegurando que el flujo principal de valor (el intercambio físico de libros) funciona correctamente antes de escalar a funcionalidades sociales complejas.

### 2.1. Objetivos de la Prueba Piloto

1. **Validar el Flujo de Intercambio:** Verificar que un usuario puede subir un libro, hacer match, chatear y cerrar un acuerdo sin errores.
2. **Testear el Algoritmo de Matching:** Comprobar que la geolocalización y las preferencias de género muestran resultados relevantes.
3. **Detectar Fricción:** Identificar puntos donde el usuario se pierde o frustra (ej. escaneo de ISBN, coordinación en chat).

## 3. Perfil y captación de usuarios piloto

Siguiendo la estrategia de captación definida y el feedback recibido, los usuarios se clasifican en dos niveles (Tiers) para una captación controlada. Actualmente, se cuenta con 99 usuarios confirmados para el Tier 1 y con 1 usuarios confirmados para el Tier 2.

### 3.1. Estrategia de Captación (Sistema de Tiers)

- **Tier 1: Círculo cercano (amigos y compañeros).**
  - **Objetivo:** Feedback rápido, alta tolerancia a fallos y pruebas de estrés iniciales.
  - **Canal:** Contacto directo y redes sociales personales.
- **Tier 2: Negocios locales.**
  - **Objetivo:** Integrar algunos BookSpots dispuestos a apoyar la aplicación. Comunicación mediante formulario con los familiares. Comunicación presencial con los BookSpots y una vez han aceptado mediante correo electrónico formal.

### 3.2. Segmentación de los Usuarios Piloto actuales

Para asegurar una prueba efectiva, se han seleccionado usuarios que cumplen con los diferentes perfiles identificados en el estudio de mercado, siendo identificados siguiendo los siguientes tipos de usuario:

- **Usuario A (Lector Estudiante/Económico):** Busca libros académicos, además de best-sellers. Sensible al ahorro económico y de espacio.
- **Usuario B (Lector Ecológico):** Quiere dar una segunda vida a sus libros, motivado por la sostenibilidad. No le importa leer libros usados.
- **Usuario C (Lector Económico):** Quiere leer libros populares pero sin pagar el precio completo de un libro nuevo.
- **Usuario D (Lector Social):** Interesado en la gamificación y en el descubrimiento de nuevas historias.
- **Bookspot:** Comercio o local con interés en ser promocionado en la aplicación como punto seguro de intercambio de libros.

| Nombre | Tipo de Usuario | Correo |
|---|---|---|
| Raúl Martín Torrabadella Mendoza | C | raul2.martin.torrabadella@gmail.com |
| Ismael Pagés Domínguez | C | aipages20@iesvcntenario.org |
| Alberto Martín Puertas | D | murchero88@gmail.com |
| Antonio Del Can Segovia | C | delkyjr@hotmail.com |
| Ricardo Rodriguez Gonzalez | B | ricardorodriguezgonzalez15@gmail.com |
| Ana Jimeno Carvajal | D | anajimeno279@gmail.com |
| Miguel Ángel Doval Romero | D | miguedr66@gmail.com |
| Irene Atencia Silva | A | atencia190604@gmail.com |
| Andrés Díaz Camacho | A | andresdiazcamacho@gmail.com |
| Carlos Díaz Boza | C | cadibo10@gmail.com |
| Fernando Cobos García | A | fernandodeportivo6@gmail.com |
| Adrián Robles Borrego | A | adrrobbor@alum.us.es |
| Andrés Dominguez Hidalgo | A | anddomhid@alum.us.es |
| Lucía Jimeno Carvajal | B | lujimeno7@gmail.com |
| Óscar Martín Leal | C | oscar10ml@gmail.com |
| Roberto Almendros Rodríguez | A | robertoar2004@gmail.com |
| Jorge Cabezas Grillo | A | jorgecabezas2004@gmail.com |
| Rosa García Monterrubio | D | garciamonterrubiorosa@gmail.com |
| Roberto Cordero Brenes | D | eustaquiofernandezambrosio@gmail.com |
| Massimo, Sito | D | sitomassimo01@gmail.com |
| Javier Arellano López | A | javiiarellanoo27@gmail.com |
| Alejandro Mauro Fernández | A | alemaurofernandez@gmail.com |
| Jorge García Rosa | A | jorgegarciarosa11@gmail.com |
| Rosa María Rosa Murillo | B | rosamrosamurillo@gmail.com |
| Jesús García Pérez | A | jesuxx4@gmail.com |
| Jesús Olmos Machado | D | j03olmos@gmail.com |
| Araceli Rosa | D | aracelirosaj@gmail.com |
| Francisco Javier González Cabrera | A | francisgcsfc04@gmail.com |
| Rafael Hidalgo Infante | A | xrafael101104x@gmail.com |
| Juan Gordo Vázquez | D | gordovazquezjuan@gmail.com |
| Elena Chaparro Méndez | A | elena2004julio@gmail.com |
| Inés Luengo Fermoselle | A | inesluengofer@outlook.com |
| Julio Manuel Silva Aranda | B | juliomsiar@gmail.com |
| Pilar Parejo Remedios | A | piilarr07@gmail.com |
| Luisa María Álvarez Estrada | D | lmag.971519@gmail.com |
| Rebeca Rodríguez Ortega | A | lpsrebeca@gmail.com |
| Alejandra Benítez Páez | A | abenez07@gmail.com |
| Natalia Egea García | A | nataliaeg2005@gmail.com |
| Marco Rico Domínguez | B | marcoricodominguez@gmail.com |
| David García Castilla | D | davidgarciacastilla888@gmail.com |
| Esther Sánchez Álvarez | D | esther.sanchez1994@hotmail.com |
| Francisco Sánchez Gallego | D | fsanchezg59@gmail.com |
| Alicia García Lavado | B | aliciaaaliciamacumacu@gmail.com |
| Álvaro Jiménez de la Fuente | A | donalvarojf88@gmail.com |
| Alejandro Tagua Hurtado | A | alejandrotaguahurtado@gmail.com |
| Pau Castillo Barbadillo | D | pcastillobarbadillo@gmail.com |
| Pedro Bermejo Pinto | A | pedroberpin@gmail.com |
| Laura González Villa | A | laugonvil2610@gmail.com |
| Hugo Fernández Alcántara | A | hugofdezalcan@gmail.com |
| Cristina Barbadillo | D | fraurank@hotmail.com |
| María de la Cruz Lerín | C | mardeler@alum.us.es |
| Alfredo Bolaños Sevillano | A | abolsevus@gmail.com |
| Ángela de la Fuente Moreno | D | am.delafuentemoreno@gmail.com |
| Amal F | A | amalfarhat2006@gmail.com |
| Katherine Carter González | D | katherinecartergonzalez@gmail.com |
| José de la Fuente | B | jadlf67@gmail.com |
| Carmen de Utrilla Martínez | B | cardeutmar@gmail.com |
| Javier Baile Núñez | D | javibaile23@gmail.com |
| Vadik Rebullida | D | vadikrebullida@gmail.com |
| Marisol Ramírez | C | teatrolalavanderia@gmail.com |
| Carolina Murillo Ruiz | A | caromuri2007@gmail.com |
| Elisa Linares | C | elisalfernandez@gmail.com |
| María Iluminada Jiménez Santana | D | iluminadajs@gmail.com |
| Nadia Coronel Correa | A | nadia.coronelcorrea@gmail.com |
| Joaquinsca | D | joaquinsca1522@gmail.com |
| Almudena Iturri Franco | B | almudenaiturri@gmail.com |
| Rafael Sánchez Guerrero | A | ganadosrsg@gmail.com |
| Rosendo Javier García Sánchez | D | rosendogarciasanchez@gmail.com |
| Carmen Peña Cáceres | D | carmenpcaceres@gmail.com |
| José María Sánchez Gallego | D | jmsanchezg46@gmail.com |
| Virginia Rodríguez Jiménez | A | virrodjim@gmail.com |
| Ramón Rosa Murillo | B | 3166rrm@gmail.com |
| Paula Parrado Díaz | A | paulaparradodiaz@hotmail.com |
| Alejandro Damián Contreras Vázquez | A | alejandroconva@gmail.com |
| Mar Castillo | A | mar.castillobarbadillo@gmail.com |
| Elena Martín Merelo | A | elenamm637@gmail.com |
| Pablo Partridge García | A | pablopablo@gmail.com |
| Ana Gema Sánchez Peña | D | anagema.sanchez@gmail.com |
| Carmen Sánchez | D | mcarmensanchezpena@hotmail.com |
| Manuel Holguin Sánchez | D | maholsan@gmail.com |
| Marta Parejo Remedios | A | martitaparejo2004@gmail.com |
| Cristina Castilla | B | cristinacastillab18@gmail.com |
| Andrés Triguero | A | ats0019@alu.medac.es |
| Pilar Utrera Cotán | D | utreracotan@gmail.com |
| Paco Sánchez Álvarez | D | fsanchezalvarez44@gmail.com |
| Alfonso Fernández Andujar | D | alfonofdezandujar@gmail.com |
| Raquel Romero Sierra | A | raquelromerosierra@gmail.com |
| Carmen Estrada Pérez | B | cestradaperez@yahoo.es |
| Juan Pedro Hernández | D | juanpedrohf@telefonica.net |
| Ana María Sánchez Gallego | C | amsanchezg03@gmail.com |
| Julia Barea | B | juliabarea1702@gmail.com |

### BookSpots Confirmados

| Nombre | Tipo de Usuario | Correo |
|---|---|---|
| Miranda’s Coffee | Bookspot | paulamirandagonz@gmail.com |

<!-- pagebreak -->

## 4. Escenarios de Prueba

Se han diseñado 4 escenarios CORE obligatorios para cada usuario:

- **Escenario A: Onboarding y Configuración**
  - **Acción:** Registro de usuario y configuración de preferencias (distancia y géneros).
  - **Objetivo:** Asegurar que el algoritmo de matching tenga datos para trabajar.
- **Escenario B: Digitalización (Subir Libro)**
  - **Acción:** Subida de al menos 2 libros usando escaneo de ISBN y cámara.
  - **Objetivo:** Validar la ausencia de fricción en la carga de inventario y el correcto funcionamiento del escaneo con la cámara.
- **Escenario C: Discovery (El Match)**
  - **Acción:** Navegación en el Matcher, Swipes (izquierda/derecha) y logro de "Match recíproco".
  - **Objetivo:** Validar la geolocalización y la visualización de tarjetas.
## 5. Plan de Comunicaciones

Dado que estamos en la fase de Tier 1 (Círculo Cercano), la comunicación se basará en la confianza y la proximidad para reducir la fricción del usuario.

### Modelo de Enlace Directo

- Cada usuario piloto se comunicará exclusivamente con el miembro del equipo que lo invitó/reclutó.
- No se utilizarán grupos generales para evitar el "efecto espectador" y asegurar respuestas personalizadas.
- Se usará un formulario para que los usuarios puedan dar feedback.

### Responsabilidad del Miembro del Equipo

- Actuar como filtro y soporte de primer nivel.
- Recopilar el feedback informal (audios de WhatsApp, comentarios en persona) y transcribirlo a las herramientas de gestión del proyecto.
- Reportar los bugs bloqueantes inmediatamente al equipo de desarrollo.

### Canales Habilitados

- WhatsApp personal (contacto directo).
- Comunicación presencial.
- Formulario de Google.

Para los usuarios de Tier 2, la comunicación se lleva a cabo de forma presencial la primera vez para establecer contacto con los negocios, y si estos deciden formar parte de los usuarios pilotos, se les solicita un correo electrónico con el que poder comunicarles todo lo necesario.

## 6. Ejecución del Piloto

### Cronograma de Ejecución (4 Días)

- **Día 1: Preparación (Escenarios A y B)**
  - Usuarios descargan la app.
  - Completan registro y suben inventario (mínimo 2 libros).
- **Día 2: Sincronización (Escenario C)**
  - Todos los usuarios entran al Matcher.
  - Se fuerza el ajuste de distancia en preferencias para asegurar visibilidad entre ellos.
  - Generación de Matches.
- **Día 3: Interacción (Escenario D)**
  - Uso del Chat.
  - Simulación física del encuentro (o real si es posible).
  - Cierre del intercambio en la app.
- **Día 4: Feedback**
  - Envío y cumplimentación de la encuesta a través de su enlace directo del equipo.

## 7. Evaluación de Aprendizajes

Al finalizar el Día 4, el equipo realizará una sesión de "Review" para procesar los datos:

1. **Cálculo de NPS:** Clasificar la recepción general del MVP.
2. **Análisis de Fricción:** Identificar en qué paso de la ejecución hubo más dudas (basado en Bloque A de la encuesta).
3. **Validación de Hipótesis:** Confirmar si se cumple la premisa de "Océano Azul" (basado en Bloque B).
4. **Priorización de Bugs:** Clasificar los errores técnicos del Bloque C para el siguiente Sprint de corrección.

## 8. Gestión, Expansión y Evolución de Usuarios Piloto

Este apartado define cómo se administrará el ciclo de vida de los usuarios piloto actuales, las estrategias para escalar la base de usuarios hacia nuevos Tiers y la hoja de ruta para el testeo de futuras funcionalidades una vez superada la fase inicial.

### 8.1. Gestión Continua de los Usuarios Piloto

Para asegurar un seguimiento efectivo de los 99 usuarios confirmados en el Tier 1, se implementarán las siguientes acciones de gestión:

- **Fidelización y Recompensas:** Los usuarios piloto fundadores (Tier 1 y Tier 2) recibirán un identificador especial en sus perfiles como agradecimiento por su alta tolerancia a fallos en esta fase inicial.
- **Transición de Canales:** Aunque en la fase actual la comunicación se basa en el WhatsApp personal de los miembros del equipo y un formulario de Google, progresivamente se canalizará a los usuarios hacia formularios de feedback integrados en la propia aplicación para automatizar la recolección de métricas.

### 8.2. Expansión y Ampliación de la Lista de Usuarios

Una vez validado el flujo principal de valor (intercambio físico de libros) sin errores, se procederá a escalar la captación de forma iterativa:

- **Activación del Tier 2:** Actualmente este nivel cuenta con 1 usuario confirmado. La expansión comenzará cerrando acuerdos presenciales (seguidos de correos formales) con negocios locales dispuestos a ser BookSpots.
- **Creación de un Tier 3 (Comunidad Universitaria):** Tras estabilizar la app con el Tier 2, se lanzará una campaña de captación en la ETSII y otras facultades. El objetivo será atraer masivamente a los perfiles de "Usuario A (Lector Estudiante/Económico)" y "Usuario C (Lector Económico)" mediante cartelería física y redes sociales.
- **Sistema de Referidos:** Se habilitará un sistema temporal de invitaciones exclusivas donde los usuarios actuales podrán invitar a 2 o 3 personas de su entorno, asegurando un crecimiento orgánico y controlado de la red.

### 8.3. Continuidad más allá del MVP (Nuevas Funcionalidades)

El objetivo de esta prueba piloto se centra exclusivamente en las funcionalidades CORE del MVP. A medida que el desarrollo avance hacia las funcionalidades sociales complejas, el protocolo de pruebas evolucionará de la siguiente manera:

- **Testeo de Funcionalidades Sociales y Gamificación:** Para validar los elementos diseñados para el "Usuario D (Lector Social)", se seleccionarán subgrupos específicos dentro de nuestra base de usuarios activos para realizar pruebas A/B.
- **Pruebas de funcionalidades concretas:** En lugar de probar la app entera de nuevo, las futuras actualizaciones se probarán mediante tests cortos (de 2 a 3 días) centrados en una única nueva característica.
- **Evolución de los KPIs:** El Net Promoter Score (NPS) utilizado para medir la satisfacción actual se complementará con métricas de retención (usuarios activos mensuales) y de Engagement (tiempo de uso y número de interacciones sociales por sesión).
