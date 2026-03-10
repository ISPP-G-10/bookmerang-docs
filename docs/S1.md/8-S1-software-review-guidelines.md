<div align="center">

<h1>Grupo 8 - Sprint 1 - Software Review Guidelines</h1>

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

## 1. Entornos de Despliegue

- **Azure:**
  - Backend:  
    <https://bookmerang-back.jollytree-74260255.spaincentral.azurecontainerapps.io/>
  - Frontend:  
    <https://bookmerang-front.jollytree-74260255.spaincentral.azurecontainerapps.io/>

- **Render:**
  - Backend: <https://bookmerang-backend.onrender.com/>
  - Frontend: <https://bookmerang-frontend.onrender.com/>

---

## 2. Funcionalidades Implementadas (Casos de Uso)

En esta versión se han integrado y habilitado los siguientes módulos y flujos:

- **Autenticación de Usuarios:** Sistema completo de registro e inicio de sesión (Login).
- **Motor de Emparejamiento (Matcher):** Implementación del algoritmo principal para conectar usuarios compatibles.
- **Biblioteca Personal:** Espacio para que cada usuario gestione su inventario de libros.
- **Gestión de Intercambios:** Configuración de preferencias individuales y administración de solicitudes de intercambio.
- **Perfil y Estadísticas:** Panel de usuario enriquecido con métricas y estadísticas de actividad.
- **Sistema de Mensajería:** Módulo de chat en vivo para facilitar la comunicación tras un *match*.

---

## 3. Datos y Contexto para Pruebas

Para agilizar la validación del sistema, se ha precargado información en la base de datos de pruebas:

### 1. Credenciales de Acceso

<table>
  <thead>
    <tr>
      <th align="left">Correo Electrónico</th>
      <th align="left">Contraseña</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>alice@test.com</td>
      <td>Test1234</td>
    </tr>
    <tr>
      <td>bob@test.com</td>
      <td>Test1234</td>
    </tr>
    <tr>
      <td>carlos@test.com</td>
      <td>Test1234</td>
    </tr>
  </tbody>
</table>

<!-- pagebreak -->

### 2. Estado del Entorno

- **Inventario:** Existen **6 libros** en total registrados en la plataforma (distribuidos equitativamente, 2 por cada usuario).
- **Interacciones preconfiguradas:** Para poder probar el sistema de chat y visualización de emparejamientos de forma directa, la usuaria **Alice** ya cuenta con un *match* activo con otro usuario. En adición, el usuario **Bob** podrá hacer *match* con otros usuarios.
- **Correlación:** Para poder ver el despliegue, primero hay que entrar al enlace del backend y esperar a que salga en una pantalla un “Hello World!” antes de entrar al despliegue del Frontend.

---

## 4. Requisitos Potenciales y Consideraciones Técnicas

- **Gestión de la Ubicación:** Actualmente, el sistema requiere capturar la ubicación del usuario de forma puntual. Como requisito potencial para futuras versiones, se está evaluando la viabilidad de implementar acceso a la ubicación en tiempo real para optimizar la logística de los intercambios.
