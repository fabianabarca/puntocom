# Investigación

> Mi investigación está centrada en arquitecturas tecnológicas y análisis de datos, con aplicación específica en sistemas inteligentes de transporte público. Estoy trabajando con docentes, estudiantes y organizaciones públicas y privadas en el planteamiento y la implementación de arquitecturas tecnológicas adaptadas a Costa Rica. Trabajo en el desarrollo de métodos de aprendizaje automático para análisis de series temporales, útiles en tareas como la predicción o la detección de anomalías en el servicio de buses.

## Sistemas inteligentes de transporte público

### Temas de interés

- Modelos de arquitecturas tecnológicas[^1]
- Tecnologías y estándares de datos[^2]
- Sistemas de información de servicios
- Sistemas de datos en tiempo real
- Bases de datos geoespaciales
- Gobernanza digital y datos abiertos[^3]

[^1]: 
    Por ejemplo, la [Referencia de Arquitectura para Transporte Cooperativo e Inteligente](https://www.arc-it.net/) (ARC-IT) del Departamento de Transporte de Estados Unidos
[^2]:
    Siguiendo, por ejemplo, los [Principios de Interoperabilidad de Datos de Mobilidad](https://www.interoperablemobility.org/)
[^3]:
    Según las definiciones de la [biblioteca](https://biblioguias.cepal.org/gobierno-digital/concepto-gobernanza) de la CEPAL

### Proyectos

En esta área de investigación estoy coordinando o dirigiendo los siguientes proyectos.

!!! abstract "Proyecto de Investigación 322-C3-184 (2023 - 2026)"
    **Análisis de datos abiertos de sistemas inteligentes de transporte público con herramientas de aprendizaje automático**

    ---

    Los resultados principales esperados incluyen una plataforma de recolección de datos abiertos de transporte público y estrategias de aprendizaje automático en tiempo real y adaptativas para la predicción de series temporales.

!!! abstract "Proyecto de Investigación C1749 (2021 - 2022)"
    **Investigación del estado de la cuestión para la aplicación de aprendizaje automático en el análisis de datos espacio-temporales**

    ---

    Este fue un proyecto de apoyo a la investigación que facilitó la identificación de la problemática del análisis de datos espacio-temporales en el transporte público como caso especial, y el vacío de investigación específica para Costa Rica.

!!! abstract "Trabajo final de graduación de licenciatura modalidad seminario (2022 - 2024)"
    **Diseño de una arquitectura de referencia para un sistema inteligente de transporte público en Costa Rica**

    ---

    Este es un proyecto con estudiantes de licenciatura en ingeniería eléctrica que busca hacer propuestas concretas para una arquitectura tecnológica de un sistema inteligente de transporte público en Costa Rica, junto con la implementación de un plan piloto en la UCR.

### Repositorios

A partir de estos proyectos y en conjunto con el trabajo comunal universitario TC-691 "Tropicalización de la tecnología" y otras instancias, estoy coordinando el desarrollo de los siguientes proyectos de software.

<div class="grid cards" markdown>

-  :material-bus-clock:{ .lg .middle } **gtfs2series**
    
    ---
    
    Una plataforma de recolección de datos de **GTFS Realtime** para su transformación en series temporales multivariadas para el análisis con aprendizaje automático.

    [:material-github: fabianabarca/gtfs2series](https://github.com/fabianabarca/gtfs2series)

    <small>Django | Python | Celery | PostgreSQL | PostGIS</small>

-  :material-chart-line:{ .lg .middle } **g2s**
    
    ---
    
    Un paquete de Python, complementario a **gtfs2series**, para la transformación de datos **GTFS Realtime** en series temporales multivariadas para el análisis con aprendizaje automático. 
    
    [:material-github: fabianabarca/g2s](https://github.com/fabianabarca/g2s)

    <small>Python | Pandas | GeoPandas</small>

-  :material-bus-clock:{ .lg .middle } **realtime**
    
    ---
    
    Un servidor para la recolección de datos en tiempo real de vehículos de transporte público y creación del suministro de datos **GTFS Realtime**.

    [:material-github: fabianabarca/realtime](https://github.com/fabianabarca/realtime)

    <small>Django | Python | Celery | RESTful API | PostgreSQL | PostGIS</small>

-  :material-fit-to-screen:{ .lg .middle } **screens**
    
    ---
    
    Un servidor para la recolección de datos **GTFS Realtime** y la distribución de información a pantallas del servicio en paradas de buses. 
    
    [:material-github: fabianabarca/screens](https://github.com/fabianabarca/screens)

    <small>Django | Python | Celery | WebSockets | PostgreSQL | PostGIS</small>

-  :material-calendar-edit:{ .lg .middle } **databus**
    
    ---
    
    Una plataforma con un editor web para la creación del suministro de datos **GTFS Schedule**, diseñado para el contexto de Costa Rica. 
    
    [:material-github: fabianabarca/databus](https://github.com/fabianabarca/databus)

    <small>Django | React</small>

-  :material-calendar-clock:{ .lg .middle } **databus-stoptimes**
    
    ---
    
    Un paquete de Python, complementario a **databus**, con algoritmos de estimación de los tiempos de llegada a las paradas en **GTFS Schedule**. 
    
    [:material-github: fabianabarca/databus-stoptimes](https://github.com/fabianabarca/databus-stoptimes)

    <small>Python | GeoPandas</small>

-  :material-calendar-clock:{ .lg .middle } **gdf2shapes**
    
    ---
    
    Un paquete de Python, complementario a **databus**, que transforma datos geoespaciales tipo GeoDataFrame en el formato `shapes.txt` de **GTFS Schedule**. 
    
    [:material-github: fabianabarca/gdf2shapes](https://github.com/fabianabarca/gdf2shapes)

    <small>Python | GeoPandas</small>

</div>

## Movilidad activa

### Análisis de factores ambientales en el uso de la bicicleta

En su fase inicial, este proyecto pretende explorar la hipótesis de que ciertas condiciones ambientales tienen un efecto significativo en la decisión de las personas de usar la bicicleta como medio de transporte. 

Si bien es conocido que la infraestructura vial (como ciclovías y otros) es el factor que más influye en esta decisión, es necesario explorar también otras causas que puedan ser relevantes y que puedan orientar la política pública en ese sentido. 

<div class="grid cards" markdown>

-  :material-bike-fast:{ .lg .middle } **bikenv**
    
    ---
    
    Un paquete de Python para analizar el efecto de los factores ambientales (por ejemplo, topográficos y climáticos) en el uso de la bicicleta como medio de transporte en ciudades, por medio del análisis de la red vial y otros datos complementarios.

    [:material-github: fabianabarca/bikenv](https://github.com/fabianabarca/bikenv)

</div>

La literatura existente está centrada mayormente en estudios hechos en ciudades norteamericanas y europeas, cuyas condiciones son relativamente homogéneas y no capturan necesariamente estos factores. Por ejemplo, la topografía y el clima son factores distintivos en un país como Costa Rica. 

El paquete de Python en desarrollo ya arrojó algunos resultados preliminares que muestran una correlación positiva entre la popularidad del uso de la bicicleta y qué tan "plana" es una ciudad, aplicado a más de 90 ciudades en un área de varios kilómetros cuadrados.
