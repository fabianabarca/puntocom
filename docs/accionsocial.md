# Acción Social

> Mi trabajo de acción social combina mis intereses de investigación y otros temas de interés personal para participar en la atención de necesidades comunitarias. Por ejemplo, con las ferias del agricultor aplicamos herramientas de desarrollo de sistemas de información para la creación de un sitio informativo junto con campañas de sensibilización en redes sociales. Esto acompañado de estudios de opinión, entrevistas, conversatorios y otras formas de acercamiento a la comunidad.

## Trabajo comunal universitario

Soy parte del proyecto de trabajo comunal universitario "Tropicalización de la tecnología" desde el 2018.

!!! abstract "Proyecto de Acción Social TC-691 (2018 - presente)"
    ![Logo TC-691 Tropicalización de la tecnología](assets/img/tropicalizacion_negro.png)

    Un trabajo comunal universitario dedicado a la aplicación de soluciones tecnológicas a problemas comunitarios.

Actualmente, los proyectos en los que estoy involucrado son sobre ferias del agricultor y transporte público, descritos a continuación.

## Ferias del agricultor

A partir de la pregunta **¿dónde está la feria y cuándo está abierta?** comenzamos a explorar un tema que nos pareció fascinante. De ahí nació el proyecto **deferia.cr**. Encontramos un vacío de información para el público en general sobre la operación de las ferias del agricultor, donde solo es posible encontrar información dispersa, desactualizada y en formatos poco accesibles.

![Logo DeFeria](assets/img/deferia_rojo.png)

??? note "Las consignas de nuestro proyecto"
    Promovemos las ferias del agricultor convencidos de las siguientes premisas:
    
    1. El mejor lugar para comprar productos frescos por precio, variedad y frescura es la feria del agricultor.
    2. La mejor dieta para la salud humana está basada en productos frescos.
    3. Las ferias benefician directamente a las familias comerciantes dedicadas a la producción agrícola.
    4. Las ferias benefician directamente a las familias consumidoras, y representan un instrumento efectivo para la seguridad alimentaria y nutricional. 
    5. Las ferias son espacios sociales y culturales relevantes para Costa Rica, con una tradición de muchas décadas. 

<div class="grid cards" markdown>

-  :material-fruit-watermelon:{ .lg .middle } **ferias**
    
    ---
    
    Un proyecto de difusión de las ferias del agricultor en Costa Rica con una página web informativa. 
    
    [:material-link-circle: deferia.cr](https://deferia.cr/)

    [:material-github: fabianabarca/ferias](https://github.com/fabianabarca/ferias)

    <small>Django | Python | API | PostgreSQL | PostGIS</small>

-  :material-share-variant:{ .lg .middle } **Redes sociales**
    
    ---
    
    Un proyecto de difusión de las ferias del agricultor en Costa Rica con una campaña de redes sociales. 
    
    [:material-instagram: instagram/deferia.cr](https://instagram/deferia.cr/)

    [:material-facebook: Facebook](https://web.facebook.com/deferia.costarica)

    [:simple-tiktok: tiktok/@deferia.cr](https://www.tiktok.com/@deferia.cr)

</div>

## Sistemas de información del transporte público

Desde el TCU hemos hecho nuestro aporte para paliar una de las carencias más evidentes de los sistemas de transporte público en Costa Rica: la falta de información clara sobre su operación.

### Plan piloto de los buses de la UCR

En conjunto con el proyecto de investigación 322-C3-184 y el seminario de graduación de licenciatura, el TCU está creando el primer sistema integral de información del servicio de transporte público en el país, para el bus interno de la Universidad de Costa Rica.

El nuevo logo del sistema *b***UCR** es:

![Logo bUCR](assets/img/b_azul.png)

Los trabajos en desarrollo en el proyecto son:

<div class="annotate" markdown>
- Una encuesta de satisfacción de las personas usuarias
- Levantamiento de datos **GTFS Schedule** (1) para Google Maps y Moovit
- Una propuesta de un sistema de señalética (rotulación)
- Un sistema de recolección de datos de los buses en tiempo real
- Publicación de **GTFS Realtime** (2) para aplicaciones y pantallas
- Pantallas informativas en paradas y espacios seleccionados
- Campaña de comunicación sobre el sistema y el transporte público
</div>

1. GTFS Schedule es la versión "estática" del estándar de datos abiertos, e incluye información como rutas, horarios, paradas, trayectorias y tarifas.
2. GTFS Realtime es la versión en tiempo real del estándar de datos abiertos, e incluye información como ubicación actual, porcentaje de ocupación del bus, actualización de tiempos de llegada y alertas del servicio.

El sistema de datos en tiempo real para las pantallas tiene la siguiente estructura[^1]:

[^1]:
    OSG es la Oficina de Servicios Generales, encargada de la administración del servicio.

```mermaid
flowchart TD
    B[Buses] 
    RT[Servidor en tiempo real]
    APP[Servidor de las pantallas]
    S[Pantallas]
    GTFS[Editor GTFS]
    OSG[OSG]

    B -->|datos vía API| RT
    RT -->|GTFS Realtime| APP
    APP -->|WebSockets| S
    GTFS -->|GTFS Schedule| RT
    GTFS -->|GTFS Schedule| APP
    OSG -->|administra| GTFS
```

<div class="grid cards" markdown>

-  :material-text-box:{ .lg .middle } **Informe de encuesta de satisfacción**
    
    ---
    
    Un reporte de la encuesta aplicada a más de 700 personas en el campus Rodrigo Facio con un instrumento desarrollado para evaluar el servicio del bus interno.

    [:material-link-circle: Repositorio Kérwá 10669/91076](https://kerwa.ucr.ac.cr/handle/10669/91076)

    <small>Canva</small>

-  :material-bus:{ .lg .middle } **bucr**
    
    ---
    
    Una página web con información del servicio de buses de la Universidad de Costa Rica, *b***UCR**. Primera versión estática.
    
    [:material-link-circle: bus.ucr.ac.cr](https://bus.ucr.ac.cr/).

    [:material-github: fabianabarca/bucr](https://github.com/fabianabarca/bucr)

    <small>HTML | Bootstrap</small>

-  :material-bus-sign:{ .lg .middle } **senaletica**
    
    ---
    
    Propuesta del sistema de señalética para el sistema de información del bus interno de la Universidad de Costa Rica.

    [:material-github: fabianabarca/senaletica](https://github.com/fabianabarca/senaletica)

    <small>Inkscape</small>

</div>

### Transportes San Gabriel

En 2020 comenzamos nuestro primer proyecto de transporte público, para facilitar la información del servicio de buses a las comunidades de San Gabriel de Aserrí, San Ignacio de Acosta y alrededores.

![Logo TSG](assets/img/tsg_negro.png)

!!! tip "¡Seguimos siendo visitados!"
    Hoy en día este sitio recibe en promedio 1000 visitantes diarios, lo cual confirma la utilidad que tiene para la comunidad.

!!! tip "¡Primeros en Google Maps!"
    Este es el primer servicio de buses en Costa Rica con presencia en Google Maps, gracias al uso de datos estandarizados [GTFS](https://gtfs.org/).

<blockquote class="twitter-tweet"><p lang="es" dir="ltr">¿Cómo hacen ustedes cuando necesitan información de los buses en Costa Rica? ¿Encuentran fácilmente lo que buscan, como horarios y tarifas? En nuestro TCU hicimos un sitio web con datos «estandarizados» para usuarixs de 🚍 de la región Caraigres y esto fue lo que resultó 🧵</p>&mdash; Fab (@fabianabarca) <a href="https://twitter.com/fabianabarca/status/1426194551597944835?ref_src=twsrc%5Etfw">August 13, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

El sitio está disponible como un proyecto de código abierto.

<div class="grid cards" markdown>

-  :material-bus-side:{ .lg .middle } **buses**
    
    ---
    
    Una página web con información de las rutas de buses San Luis de Acosta - San José, Turrujal - San José, San Gabriel - San José, incluyendo: próximos buses, horarios, tarifas, mapas y paradas. 
    
    [:material-link-circle: transportessangabriel.com](https://transportessangabriel.com/)

    [:material-github: fabianabarca/buses](https://github.com/fabianabarca/buses)

    <small>Django | Python | Vue</small>

</div>

## Otros trabajos

Como parte de este TCU decidimos resolver una necesidad que teníamos con el registro de horas de trabajo, y aprovechamos nuestro conocimiento en desarrollo web para crear el siguiente sistema.

<div class="grid cards" markdown>

-  :material-clock:{ .lg .middle } **horas**
    
    ---
    
    Una página web para el registro de horas de trabajo comunal universitario en TC-691 "Tropicalización de la tecnología". 
    
    [:material-link-circle: tropicalizacion.eie.ucr.ac.cr](https://tropicalizacion.eie.ucr.ac.cr/)

    [:material-github: fabianabarca/horas](https://github.com/fabianabarca/horas)

    <small>Django | Python</small>

</div>
