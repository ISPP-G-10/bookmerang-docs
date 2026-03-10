<div align="center">

<h1>Casos de Uso</h1>

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
- [2. Pantalla de Inicio (Home)](#2-pantalla-de-inicio-home)
  - [2.1 Visualización y Navegación](#21-visualización-y-navegación)
  - [2.2 Interacción con Publicaciones](#22-interacción-con-publicaciones)
  - [2.3 Navegación Global](#23-navegación-global)
- [3. Pantalla de Matcher (Swipe)](#3-pantalla-de-matcher-swipe)
  - [3.1 Visualización del Modo Swipe](#31-visualización-del-modo-swipe)
  - [3.2 Interacción de Swipe](#32-interacción-de-swipe)
  - [3.3 Límites y Gamificación](#33-límites-y-gamificación)
  - [3.4 Funcionalidades Avanzadas](#34-funcionalidades-avanzadas)
- [4. Pantalla de Subir](#4-pantalla-de-subir)
  - [4.1 Información Básica del Libro](#41-información-básica-del-libro)
  - [4.2 Escaneo ISBN](#42-escaneo-isbn)
  - [4.3 Datos del Libro](#43-datos-del-libro)
  - [4.4 Observaciones y Publicación](#44-observaciones-y-publicación)
  - [4.5 Validación y Errores](#45-validación-y-errores)
- [5. Pantalla de Chats (Lista)](#5-pantalla-de-chats-lista)
  - [5.1 Visualización de Conversaciones](#51-visualización-de-conversaciones)
  - [5.2 Información de Cada Chat](#52-información-de-cada-chat)
  - [5.3 Interacción con Chats](#53-interacción-con-chats)
  - [5.4 Notificaciones](#54-notificaciones)
- [6. Pantalla de Chat Individual](#6-pantalla-de-chat-individual)
  - [6.1 Visualización del Chat](#61-visualización-del-chat)
  - [6.2 Propuesta de Intercambio](#62-propuesta-de-intercambio)
  - [6.3 Mensajes](#63-mensajes)
  - [6.4 Envío de Mensajes](#64-envío-de-mensajes)
  - [6.5 Coordinación del Intercambio](#65-coordinación-del-intercambio)
- [7. Pantalla de Perfil](#7-pantalla-de-perfil)
  - [7.1 Información Personal](#71-información-personal)
  - [7.2 Estadísticas](#72-estadísticas)
  - [7.3 Preferencias](#73-preferencias)
  - [7.4 Biblioteca Personal](#74-biblioteca-personal)
  - [7.5 Gamificación e InkDrops](#75-gamificación-e-inkdrops)

---

# 1. Historial de Versiones

| Versión | Fecha | Participantes | Resumen |
|-------|------|------|------|
| v1.0 | 09/02/2026 | Antonio Luis Jiménez, Peter Carter, Julián Romero, Alejandro Vela, Alejandro Castilla, Fernando Triguero | Creación del documento |

---

# 2. Pantalla de Inicio (Home)

## 2.1 Visualización y Navegación

Como usuario, quiero ver el logo de Bookmerang en la parte superior para identificar la aplicación

Como usuario, quiero ver una barra de búsqueda principal para buscar libros rápidamente

Como usuario, quiero acceder a un botón de filtros desde la barra de búsqueda para refinar mi búsqueda

Como usuario, quiero ver categorías de géneros literarios en formato de chips horizontales (Ficción, Misterio, Historia, Ciencia, Autoayuda, Romance, Fantasía) para navegar publicaciones por géneros

Como usuario, quiero poder hacer scroll horizontal en las categorías de géneros para ver más opciones

Como usuario, quiero ver una sección de "Publicaciones" para descubrir publicaciones cercanas

Como usuario, quiero ver las publicaciones en formato de tarjetas con foto, título, autor, estado y distancia

Como usuario, quiero ver el estado del libro (Como nuevo, Bueno, Excelente, Aceptable, Nuevo, Muy bueno) mediante etiquetas que determine el usuario

Como usuario, quiero ver la distancia aproximada del libro (ej. "A 1.2 km") para saber una estimación de la distancia entre el otro propietario y el usuario

Como usuario, quiero hacer scroll vertical para ver más publicaciones recomendadas

Como usuario, quiero ver una sección "¡Match a la vista!" con un llamado a la acción hacia el Matcher

## 2.2 Interacción con Publicaciones

Como usuario, quiero poder hacer clic en una publicación para ver en detalle 

Como usuario, quiero filtrar las publicaciones por categoría haciendo clic en los chips de género

Como usuario, quiero ver libros ordenados por proximidad geográfica para facilitar el intercambio

Como usuario, quiero poder hacer clic en "Explorar Matcher" para ir directamente al modo swipe

Como usuario, quiero poder dar me gusta a las publicaciones

## 2.3 Navegación Global

Como usuario, quiero ver una barra de navegación inferior con 5 opciones (Inicio, Matcher, Subir, Chats, Perfil)

Como usuario, quiero ver cuál pestaña está activa en la barra de navegación

Como usuario, quiero poder cambiar de sección tocando los iconos de la barra inferior

---

# 3. Pantalla de Matcher (Swipe)

## 3.1 Visualización del Modo Swipe

Como usuario, quiero ver un libro en formato grande ocupando la pantalla principal

Como usuario, quiero ver la foto del libro en primer plano

Como usuario, quiero ver la distancia al usuario que quiere intercambiar el libro en la esquina superior (ej. "A 2.5 km")

Como usuario, quiero ver el título del libro debajo de la imagen

Como usuario, quiero ver el nombre del autor debajo del título

Como usuario, quiero ver el avatar o inicial del propietario del libro

Como usuario, quiero ver el nombre del propietario

Como usuario, quiero ver una "NOTA DEL AUTOR" con un mensaje personalizado del propietario

Como usuario, quiero leer las observaciones del propietario sobre el libro (ej. "Te engancha desde la primera página. Cambio por algo de desarrollo personal.")

Como usuario, quiero ver el estado del libro (Como nuevo, Bueno, Excelente, Aceptable, Nuevo, Muy bueno) mediante etiquetas

Como usuario, quiero poder hacer clic en un libro para ver los detalles del mismo

## 3.2 Interacción de Swipe

Como usuario, quiero hacer swipe hacia la izquierda para descartar un libro

Como usuario, quiero hacer swipe hacia la derecha para indicar interés en un libro

Como usuario, quiero ver botones de navegación (flechas) para avanzar o retroceder entre libros

Como usuario, quiero que el sistema me muestre el siguiente libro automáticamente después de un swipe

Como usuario, quiero poder volver al libro anterior si cambié de opinión

## 3.3 Límites y Gamificación

Como usuario FREE, quiero saber cuántos swipes me quedan del límite diario (20 swipes)

Como usuario FREE, quiero ver un anuncio cada 5 swipes para mantener el modelo freemium

Como usuario FREE, quiero poder comprar swipes adicionales con InkDrops (20 puntos por cada 10 swipes)

Como usuario PREMIUM, quiero tener swipes ilimitados sin anuncios

Como usuario, quiero recibir una notificación cuando hago match con otro usuario

## 3.4 Funcionalidades Avanzadas

Como usuario, quiero poder reportar un libro inapropiado

Como usuario, quiero que el algoritmo aprenda de mis preferencias para mostrarme libros más relevantes

---

# 4. Pantalla de Subir

## 4.1 Información Básica del Libro

Como usuario, quiero ver un título claro "Sube un libro"

Como usuario, quiero ver un texto motivacional que explique que a más detalles, más rápido encontraré intercambio

Como usuario, quiero poder añadir hasta 4 fotos del libro mediante botones de "Añadir"

Como usuario, quiero poder usar la cámara del dispositivo para tomar fotos del libro (versión móvil). 

Como usuario, quiero poder seleccionar fotos de mi galería

Como usuario, quiero ver una vista previa de las fotos que he subido

Como usuario, quiero poder eliminar fotos que ya he añadido

## 4.2 Escaneo ISBN

Como usuario, quiero tener un campo de texto para ingresar el ISBN manualmente (formato: 978-84-XXXXX-XX-X)

Como usuario, quiero tener un botón "Escanear" para usar la cámara y escanear el código de barras del libro (versión móvil)

Como usuario, quiero que el sistema autocomplete los datos del libro (título, autor, páginas, editorial, género) después de escanear el ISBN

Como usuario, quiero poder editar los datos autocompletados si son incorrectos

## 4.3 Datos del Libro

Como usuario, quiero poder ingresar el autor del libro con un campo de texto (ej. Patrick Rothfuss)

Como usuario, quiero seleccionar uno o varios géneros mediante botones tipo chip (Ficción, No ficción, Fantasía, Romance, Misterio, Ciencia ficción, Biografía, Historia, Autoayuda, Infantil, Juvenil, Terror, Poesía, Ensayo)

Como usuario, quiero poder ingresar el número de páginas del libro

Como usuario, quiero seleccionar el tipo de cubierta (Tapa dura, Tapa blanda, Bolsillo) mediante un selector desplegable

Como usuario, quiero poder ingresar la editorial del libro (ej. Plaza & Janés)

Como usuario, quiero seleccionar el estado del libro (Como nuevo, Bueno, Aceptable, Malo, Muy malo) mediante un selector desplegable

Como usuario, quiero seleccionar el idioma del libro (Español, Inglés, Francés, Alemán, Italiano, Portugués, Catalán, Gallego, Euskera) mediante un selector desplegable

## 4.4 Observaciones y Publicación

Como usuario, quiero tener un campo de texto grande para añadir observaciones adicionales sobre el libro

Como usuario, quiero poder especificar qué tipo de libro busco a cambio

Como usuario, quiero poder añadir detalles sobre el estado de conservación que no cubran las opciones predefinidas

Como usuario, quiero tener un botón "Publicar libro" al final del formulario

Como usuario, quiero recibir una confirmación visual cuando el libro se ha publicado exitosamente

Como usuario, quiero poder guardar el libro como borrador si no tengo todos los datos

## 4.5 Validación y Errores

Como usuario, quiero ver mensajes de error si faltan campos obligatorios

Como usuario, quiero que los campos obligatorios estén claramente marcados

Como usuario, quiero poder cancelar la publicación y volver a la pantalla anterior

Como usuario, quiero que se guarden mis datos si salgo accidentalmente de la pantalla

---

# 5. Pantalla de Chats (Lista)

## 5.1 Visualización de Conversaciones

Como usuario, quiero ver una lista de todas mis conversaciones activas

Como usuario, quiero ver dos pestañas: "Activos" e "Historial" para organizar mis chats

Como usuario, quiero que los chats activos muestren conversaciones en curso

Como usuario, quiero que el historial muestre intercambios completados o archivados

Como usuario, quiero ver una barra de búsqueda para buscar chats específicos por nombre o libro

## 5.2 Información de Cada Chat

Como usuario, quiero ver el avatar o inicial del contacto

Como usuario, quiero ver el nombre del contacto

Como usuario, quiero ver el título del libro entre comillas debajo del nombre

Como usuario, quiero ver el último mensaje enviado o recibido

Como usuario, quiero ver la hora del último mensaje (ej. "HACE 2 MIN", "HACE 1 HORA", "AYER")

Como usuario, quiero ver un indicador visual si el mensaje es nuevo (punto rojo)

Como usuario, quiero ver si el contacto está en línea

## 5.3 Interacción con Chats

Como usuario, quiero poder hacer clic en un chat para abrirlo

Como usuario, quiero poder deslizar un chat hacia la izquierda para ver opciones (archivar, eliminar, silenciar)

Como usuario, quiero poder mantener presionado un chat para seleccionarlo

Como usuario, quiero poder filtrar chats por estado (pendiente, aceptado, rechazado)(??)

Como usuario, quiero poder ordenar chats por fecha o nombre(??)

## 5.4 Notificaciones

Como usuario, quiero recibir notificaciones push cuando reciba un mensaje nuevo

Como usuario, quiero ver un contador de mensajes no leídos en la pestaña de Chats de la barra inferior

Como usuario, quiero poder silenciar notificaciones de un chat específico

---

# 6. Pantalla de Chat Individual

## 6.1 Visualización del Chat

Como usuario, quiero ver el avatar y nombre del contacto en la cabecera

Como usuario, quiero ver si el contacto está "En línea ahora" o cuándo fue su última conexión

Como usuario, quiero ver un botón "Oferta" en la cabecera para revisar los detalles del intercambio

Como usuario, quiero poder hacer clic en el nombre del contacto para ver su perfil completo

Como usuario, quiero poder volver a la lista de chats con un botón atrás

## 6.2 Propuesta de Intercambio

Como usuario, quiero ver una sección destacada con "TU LIBRO" y "LIBRO DE [NOMBRE]"

Como usuario, quiero ver imágenes en miniatura de ambos libros

Como usuario, quiero ver los títulos de ambos libros

Como usuario, quiero ver tres botones de acción: "Aceptar", "Contraoferta", "Desestimar"

Como usuario, quiero poder hacer clic en "Aceptar" para confirmar el intercambio

Como usuario, quiero poder hacer clic en "Contraoferta" para proponer otro libro

Como usuario, quiero poder hacer clic en "Desestimar" para rechazar la oferta

## 6.3 Mensajes

Como usuario, quiero ver los mensajes organizados cronológicamente

Como usuario, quiero ver separadores de fecha (ej. "HOY", "AYER")

Como usuario, quiero ver mis mensajes alineados a la derecha con un color distintivo

Como usuario, quiero ver los mensajes del contacto alineados a la izquierda

Como usuario, quiero ver la hora de cada mensaje

Como usuario, quiero ver indicadores de lectura (enviado, entregado, leído)

## 6.4 Envío de Mensajes

Como usuario, quiero tener un campo de texto en la parte inferior para escribir mensajes

Como usuario, quiero tener un botón de envío (icono de avión de papel)

Como usuario, quiero que el botón de envío solo se active cuando haya texto

Como usuario, quiero poder adjuntar fotos del libro

Como usuario, quiero poder compartir mi ubicación para coordinar el encuentro

Como usuario, quiero poder usar emojis en mis mensajes

Como usuario, quiero que el texto se ajuste automáticamente en múltiples líneas

## 6.5 Coordinación del Intercambio

Como usuario, quiero poder proponer una fecha y hora para el intercambio por mensaje

Como usuario, quiero poder proponer un lugar de encuentro por mensaje

Como usuario, quiero recibir sugerencias de Bookmerang Spots cercanos

Como usuario, quiero poder marcar el intercambio como completado

Como usuario, quiero poder reportar un problema con el intercambio

---

# 7. Pantalla de Perfil

## 7.1 Información Personal

Como usuario, quiero ver mi foto de perfil grande y centrada

Como usuario, quiero poder hacer clic en mi foto para cambiarla

Como usuario, quiero ver mi nombre completo

Como usuario, quiero ver mi nombre de usuario (@username)

Como usuario, quiero ver mi ubicación (ciudad, país)

Como usuario, quiero tener un botón de configuración (engranaje) en la parte superior

Como usuario, quiero tener un botón de editar perfil (lápiz) en la parte superior

## 7.2 Estadísticas

Como usuario, quiero ver mi valoración promedio con estrellas (ej. 4.9)

Como usuario, quiero ver la palabra "Valoración" debajo del número

Como usuario, quiero ver el número total de intercambios realizados (ej. 28)

Como usuario, quiero ver cuántos intercambios he hecho este mes (ej. "+ 5 este mes")

Como usuario, quiero poder hacer clic en las estadísticas para ver detalles

## 7.3 Preferencias

Como usuario, quiero ver un botón "Editar Preferencias" destacado

Como usuario, quiero poder especificar mis géneros literarios favoritos

Como usuario, quiero poder establecer mi radio de búsqueda preferido

Como usuario, quiero poder indicar qué tipo de libros busco

## 7.4 Biblioteca Personal

Como usuario, quiero ver una sección "Tu Biblioteca" con todos mis libros publicados

Como usuario, quiero ver mis libros en formato de grid/cuadrícula

Como usuario, quiero ver la portada, título, autor y estado de cada libro

Como usuario, quiero poder hacer clic en un libro de mi biblioteca para ver sus detalles

Como usuario, quiero poder editar o eliminar libros de mi biblioteca

Como usuario, quiero poder ver qué libros están activos y cuáles ya fueron intercambiados

Como usuario, quiero poder filtrar mi biblioteca por estado (disponible, en negociación, intercambiado)

Como usuario, quiero poder marcar libros como "pausados" temporalmente. Llevar seguimiento de lo que estás leyendo (de momento opcional). 

## 7.5 Gamificación e InkDrops

Como usuario, quiero ver mi saldo de InkDrops (puntos)

Como usuario, quiero poder hacer clic en mis InkDrops para ver el historial de puntos

Como usuario, quiero ver logros desbloqueados

Como usuario, quiero ver mi progreso hacia el siguiente logro

Como usuario, quiero ver cuántos árboles he salvado con mis intercambios

Como usuario, quiero ver estadísticas de impacto ambiental (ligado al cliente ecológico). Un libro = 0.04 árboles (25 libros equivalen a un árbol) y entre 5-10 mililitros de tinta con 300 páginas(entre el 60-100% de 1 cartucho de tóner).