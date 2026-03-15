<div align="center">

<h1>Análisis de coste del proyecto</h1>

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
- [2. Introducción](#2-introducción)
- [3. Estimación de Costes](#3-estimación-de-costes)
  - [3.1 Costes del personal](#31-costes-del-personal)
  - [3.2 Costes de infraestructura](#32-costes-de-infraestructura)
  - [3.3 Costes de herramientas de desarrollo](#33-costes-de-herramientas-de-desarrollo)
  - [3.4 Costes de hardware y dispositivos](#34-costes-de-hardware-y-dispositivos)
  - [3.5 Costes de Distribución y Publicación](#35-costes-de-distribución-y-publicación)
  - [3.6 Costes totales](#36-costes-totales)

---

<!-- pagebreak -->

## 1. Historial de Versiones

<table>
  <thead>
    <tr>
      <th>Versión</th>
      <th>Fecha</th>
      <th>Participantes</th>
      <th>Resumen de los cambios</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>v1.0</td>
      <td>21/02/2026</td>
      <td>Javier Ulecia García</td>
      <td>Rellenar documento</td>
    </tr>
    <tr>
      <td>v1.1</td>
      <td>23/02/2026</td>
      <td>Javier Ulecia García</td>
      <td>Documento terminado</td>
    </tr>
    <tr>
      <td>v1.2</td>
      <td>24/02/2026</td>
      <td>Antonio Luis Jiménez de la Fuente</td>
      <td>Modificaciones en costes e infraestructura</td>
    </tr>
    <tr>
      <td>v1.3</td>
      <td>02/03/2026</td>
      <td>Antonio Luis Jiménez de la Fuente</td>
      <td>Añadir costes asociados a dispositivos del personal</td>
    </tr>
    <tr>
      <td>v1.4</td>
      <td>09/03/2026</td>
      <td>Antonio Luis Jiménez de la Fuente</td>
      <td>Actualización de costes de Seguridad Social y amortización de hardware según tablas fiscales</td>
    </tr>
  </tbody>
</table>

<!-- pagebreak -->

## 2. Introducción

Este documento tiene como objetivo analizar los costes asociados al desarrollo y mantenimiento de la aplicación Bookmerang. El análisis de costes se basa en la metodología PMBOK, considerando tanto los gastos de personal, infraestructura, herramientas de desarrollo, hardware y distribución, como una reserva de contingencia de un 10% sobre el total estimado. Además, se presenta una estimación de beneficios basada en el modelo de suscripción premium de la aplicación junto con un sistema de publicidad.

## 3. Estimación de Costes

### 3.1 Costes del personal

En la tabla 1 se puede ver el desglose de costes asociados a tener trabajadores en nómina según el rol que tengan asociado. Los datos de los salarios han sido extraídos de la página `https://www.getmanfred.com` donde miles de trabajadores reflejan de manera activa sus condiciones salariales. Los datos mostrados son la media que la página proporciona para cada perfil. En el caso de que algún empleado tenga asignados dos roles distintos el coste se calculará como la media aritmética de ambos roles.

Las contribuciones a la Seguridad Social a cargo de la empresa para el año 2026 se componen de los siguientes conceptos:

**Contribución social = (cc + pd + cp + f + F) * sueldo bruto**

- **cc** = Contingencias comunes (23,6%)
- **d** = Desempleo (5,5%)
- **mei** = Mecanismo de Equidad Intergeneracional (0,75%)
- **f** = Formación (0,6%)
- **F** = FOGASA (0,2%)

**cc + pd + cp + f + F = 30,65% (0,3065)**

<table>
  <thead>
    <tr>
      <th>Rol</th>
      <th>Criterio de búsqueda en manfred</th>
      <th>Estimación salario bruto anual</th>
      <th>Estimación salario bruto por hora</th>
      <th>Contribuciones sociales (30,9%)</th>
      <th>Coste total por hora</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Jefe de proyecto</td>
      <td>Rol: Project Manager &amp; Delivery Manager<br/>Experiencia: menos de 2 años<br/>Tecnología: .net8, React Native, Microsoft Project</td>
      <td>30.000€</td>
      <td>17,34€</td>
      <td>5,32€</td>
      <td>22,66€</td>
    </tr>
    <tr>
      <td>Fullstack</td>
      <td>Rol: Fullstack developer<br/>Experiencia: menos de 2 años<br/>Tecnología: .net8, React Native</td>
      <td>28.000€</td>
      <td>16,18€</td>
      <td>4,96€</td>
      <td>21,14€</td>
    </tr>
    <tr>
      <td>QA y tester</td>
      <td>Rol: QA &amp; Testing Engineer<br/>Experiencia: menos de 2 años<br/>Tecnología: xUnit, Selenium</td>
      <td>23.000€</td>
      <td>13,29€</td>
      <td>4,07€</td>
      <td>17,36€</td>
    </tr>
    <tr>
      <td>Documentador</td>
      <td>Rol: Administration<br/>Experiencia: menos de 2 años</td>
      <td>23.000€</td>
      <td>13,29€</td>
      <td>4,07€</td>
      <td>17,36€</td>
    </tr>
    <tr>
      <td>Analista</td>
      <td>Rol: Data Analyst<br/>Experiencia: menos de 2 años</td>
      <td>24.000€</td>
      <td>13,87€</td>
      <td>4,25€</td>
      <td>18,12€</td>
    </tr>
  </tbody>
</table>

**Tabla 1:** Desglose de costes por rol (incluyendo Seguridad Social)

Para los trabajadores se espera un tiempo de dedicación semanal de 10 horas, puesto que el proyecto tiene una duración de 15 semanas se espera una dedicación de 150 horas totales. En la tabla 2 se reflejan los costes de cada empleado según su asignación de roles. Los costes por hora se han redondeado al alza a dos decimales.

<table>
  <thead>
    <tr>
      <th>Empleado</th>
      <th>Roles</th>
      <th>Coste por hora</th>
      <th>Coste total</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Adolfo Agustín Borrego González</td><td>Scrum Master / Programador</td><td>21,94€</td><td>3.290€</td></tr>
    <tr><td>Alejandro Carmona Reina</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Peter Philip Carter González</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Alejandro Castilla Barbadillo</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Pablo Castrillón Mora</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>David Escudero Aldana</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>José Manuel García Rosa</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Samuel Granado Oliva</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Jianwu Hu</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Antonio Luis Jiménez de la Fuente</td><td>Scrum Master / Analista / Programador</td><td>21,94€</td><td>3.290€</td></tr>
    <tr><td>Adrián Ramírez Gil</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Antonio Rodríguez Calderón</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Francisco Rodríguez-Carretero Roldán</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Darío Román Jiménez</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Julián Romero Parejo</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Germán Sánchez Carmona</td><td>Scrum Master / Analista / Programador</td><td>21,94€</td><td>3.290€</td></tr>
    <tr><td>Jesús Sánchez Quirós</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Fernando Triguero Caballo</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Javier Ulecia García</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td>Alejandro Vela Molina</td><td>Analista / Programador</td><td>19,67€</td><td>2.951€</td></tr>
    <tr><td colspan="3"><strong>Total (Incluye Seguridad Social)</strong></td><td><strong>60.037€</strong></td></tr>
  </tbody>
</table>

**Tabla 2:** Desglose de costes por empleado (incluye contribuciones a la Seguridad Social)

<!-- pagebreak -->

### 3.2 Costes de infraestructura

Los costes de infraestructura para 15 semanas se han calculado en función de los precios oficiales de Microsoft Azure para los servicios utilizados. Para el despliegue del backend se ha considerado una instancia en Azure Container Apps con 0,5 vCPU y 1 GB de memoria en ejecución continua, estimando un coste mensual de ~18€ acorde a la carga prevista del proyecto.

Para la gestión y almacenamiento de las imágenes Docker se ha incluido Azure Container Registry. Todos los cálculos se han realizado prorrateando los importes mensuales al período total de 15 semanas (3,75 meses) de ejecución del proyecto.

<table>
  <thead>
    <tr>
      <th>Elemento</th>
      <th>Detalle</th>
      <th>Precio unitario</th>
      <th>Uso estimado</th>
      <th>Coste total (15 semanas)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Azure Container Apps</td>
      <td>0,25 vCPU - 1GB RAM - 1 réplica always-on</td>
      <td>~10€/mes</td>
      <td>15 semanas</td>
      <td>37,5€</td>
    </tr>
    <tr>
      <td>Azure Container Registry</td>
      <td>Almacenamiento de imágenes Docker</td>
      <td>~5€/mes</td>
      <td>15 semanas</td>
      <td>18,8€</td>
    </tr>
    <tr>
      <td colspan="4"><strong>Total</strong></td>
      <td><strong>56€</strong></td>
    </tr>
  </tbody>
</table>

**Tabla 3:** Desglose de coste de infraestructura

### 3.3 Costes de herramientas de desarrollo

Para el desarrollo del proyecto se han seleccionado herramientas ampliamente usadas en la industria.

<table>
  <thead>
    <tr>
      <th>Elemento</th>
      <th>Proveedor</th>
      <th>Detalle</th>
      <th>Coste total 15 semanas</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>GitHub (Github Team)</td><td>Microsoft</td><td>Plan Team para 20 usuarios</td><td>320€</td></tr>
    <tr><td>VS Code</td><td>Microsoft</td><td>Gratuito</td><td>0€</td></tr>
    <tr><td>GitHub Actions</td><td>Microsoft</td><td>Uso limitado 2000 min/mes *</td><td>0€</td></tr>
    <tr><td>.Net8</td><td>Microsoft</td><td>Gratuito</td><td>0€</td></tr>
    <tr><td>React Native</td><td>Meta</td><td>Gratuito</td><td>0€</td></tr>
    <tr><td>PostGreSQL</td><td>PostGreSQL Global Development</td><td>Gratuito</td><td>0€</td></tr>
    <tr><td>SonarCloud</td><td>SonarSource</td><td>Plan Team</td><td>105€</td></tr>
    <tr><td colspan="3"><strong>Total</strong></td><td><strong>425€</strong></td></tr>
  </tbody>
</table>

**Tabla 4:** Desglose de costes de herramientas de desarrollo

\* El plan GitHub Team/Free da 2.000 minutos de Actions al mes para repos privados de una organización.

En 15 semanas son unas 3,75 mensualidades, es decir, 7.500 minutos gratuitos. Para un proyecto académico con 20 personas, compilaciones moderadas (por ejemplo, unas decenas de pipelines al día) es muy difícil que lleguéis a 7.500 minutos; por tanto, el coste realista es 0 € para esas 15 semanas.

### 3.4 Costes de hardware y dispositivos

#### Adquisición de equipos

Se establece así los costes de una máquina estándar por cada uno de los usuarios / desarrolladores que se encuentran dentro del proyecto.

<table>
  <thead>
    <tr>
      <th>Elemento</th>
      <th>Proveedor</th>
      <th>Cantidad</th>
      <th>Coste total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Portátil estándar tipo Lenovo V15 G4, i5, 16 GB RAM, 512 GB SSD, 15,6’’ FHD</td>
      <td>Lenovo</td>
      <td>20</td>
      <td>11.000 €</td>
    </tr>
  </tbody>
</table>

**Tabla 4.1:** Adquisición de hardware

<!-- pagebreak -->

#### Amortización del hardware

Según las tablas oficiales de amortización de la Agencia Tributaria española, los equipos informáticos tienen un coeficiente lineal máximo del 25% anual (período máximo de 8 años). Esto significa que el valor de los equipos se amortiza en un 25% cada año.

Para el proyecto con una duración de 15 semanas (3,75 meses), la amortización correspondiente se calcula de la siguiente manera:

- **Valor total del hardware:** 11.000€
- **Amortización anual (25%):** 2.750€/año
- **Amortización para 15 semanas:** 2.750€ × (15 semanas / 52 semanas) = 793,27€

Esta amortización representa el coste de depreciación del hardware durante el período del proyecto y debe incluirse en los costes operacionales del mismo.

<table>
  <thead>
    <tr>
      <th>Concepto</th>
      <th>Valor</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Valor total del hardware</td><td>11.000€</td></tr>
    <tr><td>Coeficiente de amortización anual</td><td>25%</td></tr>
    <tr><td>Amortización anual</td><td>2.750€</td></tr>
    <tr><td>Amortización para 15 semanas del proyecto</td><td>793,27€</td></tr>
  </tbody>
</table>

**Tabla 4.1:** Amortización del hardware del proyecto

### 3.5 Costes de Distribución y Publicación

Para distribuir la aplicación se ha elegido Google Play Store y App Store, debido a su amplio alcance y facilidad de acceso en dispositivos Android e IOS.

Para publicar una aplicación en Google Play Store requiere de un pago único de 21,18€ (25 USD), que permite gestionar la aplicación durante todo el periodo del proyecto.

Para Apple App Store, se requiere de un pago anual al programa de desarrolladores de Apple, costando 83,87€ (99 USD) anuales.

<table>
  <thead>
    <tr>
      <th>Elemento</th>
      <th>Proveedor</th>
      <th>Detalle</th>
      <th>Coste total</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Google Play Store</td><td>Google</td><td>Registro de desarrollador</td><td>21.18€</td></tr>
    <tr><td>Apple App Store</td><td>Apple</td><td>Apple Developer Program</td><td>83.87€</td></tr>
    <tr><td colspan="3"><strong>Total</strong></td><td><strong>105.05€</strong></td></tr>
  </tbody>
</table>

**Tabla 5:** Desglose de coste de distribución y publicación

### 3.6 Costes totales

En la siguiente tabla se recogen los costes totales del proyecto, incluyendo las contribuciones a la Seguridad Social en los costes del personal y la amortización del hardware, además del 10% de reservas de contingencia.

<table>
  <thead>
    <tr>
      <th>Categoría</th>
      <th>Costes</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Costes de personal</td><td>60.037€</td></tr>
    <tr><td>Costes de infraestructura</td><td>56€</td></tr>
    <tr><td>Costes de Herramientas de Desarrollo</td><td>425€</td></tr>
    <tr><td>Amortización del hardware (15 semanas)</td><td>793,27€</td></tr>
    <tr><td>Costes de hardware y dispositivos</td><td>11.000€</td></tr>
    <tr><td>Costes de publicacion y distribucion</td><td>105,05€</td></tr>
    <tr><td>Total</td><td>70.829,78€</td></tr>
    <tr><td>Coste del proyecto (total + 10% de reservas de contingencia)</td><td>77.912,76€</td></tr>
  </tbody>
</table>

**Tabla 6:** Costes totales