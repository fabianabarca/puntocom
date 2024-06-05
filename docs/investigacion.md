# Investigación

> Hago investigación en sistemas inteligentes y análisis de datos, con aplicación específica en transporte público y movilidad. Trabajo en el diseño y la implementación de arquitecturas tecnológicas adaptadas a Costa Rica y, además, en el desarrollo de métodos de aprendizaje automático para análisis de series temporales, útiles en tareas como la predicción o la detección de anomalías en el servicio de transporte público.

## Sistemas inteligentes de transporte público

El transporte público complementado con tecnologías de información y comunicación (TIC) es un *sistema inteligente de transporte público*. Es capaz de ofrecer información oportuna a las personas usuarias y también facilita la operación, la gestión administrativa, la planificación y la regulación del servicio. Esto es parte del concepto más amplio de las *ciudades inteligentes*.

Los sistemas modernos de transporte público son una *industria de alta tecnología*, que operan sobre la base de sistemas de telecomunicaciones y redes, sistemas de información, análisis de datos, sensores y otras tecnologías.

### Subtemas de interés

<div class="annotate" markdown>
- Modelos de arquitecturas tecnológicas (1) 
- Tecnologías y estándares de datos (2)
- Sistemas de información del servicio (3)
- Sistemas de datos en tiempo real (4)
- Análisis de series temporales (5)
- Bases de datos geoespaciales (6)
- Gobernanza digital y datos abiertos (7)
</div>

1.  Como, por ejemplo, la [Referencia de Arquitectura para Transporte Cooperativo e Inteligente](https://www.arc-it.net/) (ARC-IT) del Departamento de Transporte de Estados Unidos.
2.  Siguiendo, por ejemplo, los [Principios de Interoperabilidad de Datos de Mobilidad](https://www.interoperablemobility.org/) (MDIP).
3.  Como el plan piloto del sistema de información del servicio del bus interno de la UCR, que incluye datos GTFS *Schedule* y *Realtime*, pantallas informativas y una campaña de comunicación.
4.  Específicamente sistemas de recolección y análisis de datos abiertos de transporte público GTFS *Realtime*.
5.  Con la aplicación de métodos de aprendizaje automático (ML) y profundo (DL).
6.  Particularmente con el uso de PostGIS, GeoDjango y GeoPandas, y en menor medida con QGIS.
7.  Según, por ejemplo, las definiciones de la [Comisión Económica para América Latina y el Caribe](https://biblioguias.cepal.org/gobierno-digital/concepto-gobernanza) (CEPAL) y la [Alianza para el Gobierno Abierto](https://www.opengovpartnership.org/es/about/approach/) (OGP).

### Proyectos

En esta área de investigación estoy coordinando o dirigiendo los siguientes proyectos.

!!! abstract "Proyecto de Investigación 322-C3-184 (2023 - 2026) <small>EN DESARROLLO</small>"
    **Análisis de datos abiertos de sistemas inteligentes de transporte público con herramientas de aprendizaje automático**

    ---

    Principales resultados en desarrollo:

    - Una propuesta de arquitectura tecnológica de un sistema inteligente de transporte público para Costa Rica.
    - Una plataforma de recolección de datos abiertos en tiempo real de transporte público.
    - Estrategias *en tiempo real* (*online*) y *adaptativas* de aprendizaje automático (ML) para la predicción de series temporales.

!!! abstract "Trabajo final de graduación de licenciatura modalidad seminario (2022 - 2025) <small>EN DESARROLLO</small>"
    **Diseño de una arquitectura de referencia para un sistema inteligente de transporte público en Costa Rica**

    ---

    Principales resultados del proyecto con estudiantes de licenciatura en ingeniería eléctrica:
    
    - Una propuesta concreta de una arquitectura tecnológica de un sistema inteligente de transporte público en Costa Rica.
    - La implementación del plan piloto de un sistema de información en el campus de la Universidad de Costa Rica.

!!! abstract "Proyecto de Investigación C1749 (2021 - 2022) <small>CONCLUIDO</small>"
    **Investigación del estado de la cuestión para la aplicación de aprendizaje automático en el análisis de datos espacio-temporales**

    ---

    Principales resultados del proyecto de apoyo a la investigación:
    
    - La identificación de la problemática del análisis de datos espacio-temporales en el transporte público en Costa Rica.
    - Propuesta de un nuevo proyecto de investigación y un trabajo final de graduación.

### Repositorios

A partir de estos proyectos y en conjunto con el trabajo comunal universitario TC-691 "Tropicalización de la tecnología" y otras instancias dentro y fuera de la universidad, estoy coordinando el desarrollo de los siguientes proyectos de software.

<div class="grid cards" markdown>

-  :material-bus-sign:{ .lg .middle } **gtfs2series**
    
    ---
    
    Una plataforma de recolección de datos de **GTFS Realtime** para su visualización y transformación en series temporales multivariadas y el análisis con aprendizaje automático.

    [:material-github: fabianabarca/gtfs2series](https://github.com/fabianabarca/gtfs2series)

    <small>Django | Python | Celery | PostgreSQL | PostGIS</small>

-  :material-chart-line:{ .lg .middle } **g2s**
    
    ---
    
    Un paquete de Python, complementario a **gtfs2series**, para la transformación de datos **GTFS Realtime** en series temporales multivariadas. 
    
    [:material-github: fabianabarca/g2s](https://github.com/fabianabarca/g2s)

    <small>Python | Pandas | GeoPandas</small>

-  :material-bus-clock:{ .lg .middle } **realtime**
    
    ---
    
    Un servidor para la recolección de datos en tiempo real de vehículos de transporte público y creación del suministro de datos **GTFS Realtime**.

    [:material-github: fabianabarca/realtime](https://github.com/fabianabarca/realtime)

    <small>Django | Python | Celery | Web API | PostgreSQL | PostGIS</small>

-  :material-database:{ .lg .middle } **datahub**
    
    ---
    
    Un servidor para la recolección de datos **GTFS Realtime** y otros datos complementarios para la distribución a sistemas de información.

    [:material-github: fabianabarca/datahub](https://github.com/fabianabarca/datahub)

    <small>Django | Python | Celery | Web API | PostgreSQL | PostGIS</small>

-  :material-fit-to-screen:{ .lg .middle } **screens**
    
    ---
    
    Un servidor para la recolección de datos **GTFS Realtime** y la distribución de información del servicio a pantallas en paradas de buses. 
    
    [:material-github: fabianabarca/screens](https://github.com/fabianabarca/screens)

    <small>Django | Python | Celery | WebSockets | PostgreSQL | PostGIS</small>

-  :material-calendar-edit:{ .lg .middle } **editor**
    
    ---
    
    Una plataforma web para la creación y edición del suministro de datos **GTFS Schedule**, diseñado para el contexto de Costa Rica. 
    
    [:material-github: fabianabarca/editor](https://github.com/fabianabarca/editor)

    <small>Django | Python | Celery | Web API | React | Material UI</small>

-  :material-calendar-clock:{ .lg .middle } **editor-stoptimes**
    
    ---
    
    Un paquete de Python, complementario a **editor**, con algoritmos de estimación de los tiempos de llegada a las paradas en **GTFS Schedule** para `stop_times.txt`. 
    
    [:material-github: fabianabarca/editor-stoptimes](https://github.com/fabianabarca/editor-stoptimes)

    <small>Python | Pandas | GeoPandas | SciPy</small>

-  :material-map-marker-distance:{ .lg .middle } **gdf2shapes**
    
    ---
    
    Un paquete de Python, complementario a **editor**, que transforma datos geoespaciales tipo GeoDataFrame en el formato `shapes.txt` de **GTFS Schedule**. 
    
    [:material-github: fabianabarca/gdf2shapes](https://github.com/fabianabarca/gdf2shapes)

    <small>Python | GeoPandas</small>

-  :material-cellphone-cog:{ .lg .middle } **databus**
    
    ---
    
    Una aplicación móvil operativa como alternativa de bajo costo para un equipo de telemetría y rastreo de vehículos de transporte público con funcionalidad limitada. 
    
    [:material-github: fabianabarca/databus](https://github.com/fabianabarca/databus)

    <small>React Native | Material UI</small>

</div>

## Movilidad activa

Realizo también, y en menor medida, investigación en temas de movilidad activa[^1], específicamente ciclismo urbano. 

[^1]:
    Según la [Comisión Europea](https://transport.ec.europa.eu/transport-themes/urban-transport/active-mobility-walking-and-cycling_en?prefLang=es&etrans=es), "son formas de movilidad de bajo costo y cero emisiones como caminar y andar en bicicleta".

### Análisis de factores ambientales en el uso de la bicicleta

En su fase inicial, este proyecto pretende explorar la hipótesis de que ciertas condiciones ambientales tienen un efecto significativo en la decisión de las personas de usar la bicicleta como medio de transporte. 

??? note "Más detalles de la investigación"
    Si bien es conocido que la infraestructura vial (como ciclovías y otros) es el factor que más influye en la decisión de utilizar la bicicleta, es necesario explorar también otras causas que puedan ser relevantes y que puedan orientar la política pública en ese sentido. 

    La literatura existente está centrada mayormente en estudios hechos en ciudades norteamericanas y europeas, cuyas condiciones son relativamente homogéneas y no capturan necesariamente estos factores. Por ejemplo, la topografía y el clima son factores distintivos en un país como Costa Rica. 

    El paquete de Python en desarrollo ya arrojó algunos resultados preliminares que muestran una correlación positiva entre la popularidad del uso de la bicicleta y qué tan "plana" es una ciudad, aplicado a más de 90 ciudades en un área de varios kilómetros cuadrados.

### Repositorio

<div class="grid cards" markdown>

-  :material-bike-fast:{ .lg .middle } **bikenv**
    
    ---
    
    Un paquete de Python para analizar el efecto de los factores ambientales (por ejemplo, topográficos y climáticos) en el uso de la bicicleta como medio de transporte en ciudades, por medio del análisis de la red vial y otros datos complementarios.

    [:material-github: fabianabarca/bikenv](https://github.com/fabianabarca/bikenv)

    <small>Python | GeoPandas | OSMnx</small>

</div>
