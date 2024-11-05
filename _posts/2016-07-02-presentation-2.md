---
title: Capitulo 7 
layout: post
permalink: /presentation-2/

slides:
 - title: Capítulo 7 Medios de transmisión
   slide-data: Ingeniería en sistemas computacionales - Fundamentos de telecomunicaciones - Alumna Texna Reyes Ivania Gpe.
   background: "#e74c3c"
     
 - title: Definición
   slide-data: Un medio de transmisión puede definirse en términos generales como cualquier cosa que pueda llevar información desde una fuente a un destino. El medio de transmisión suele ser el espacio libre, un cable metálico o un cable de fibra óptica. La información suele ser una señal que es el resultado de la conversión de datos de otro formato.
   background: '#f1c40f'
   
 - title: Categorías de medios de transmisión
   slide-data: En telecomunicaciones, los medios de transmisión se pueden dividir en dos grandes categorías guiados y no guiados. A continuación se explicará más acerca de cada categoría.
   background: '#9b59b6'
   
 - title: GUIADOS
   slide-data: Los medios guiados, que son aquellos que proporcionan un conducto de un dispositivo a otro. Una señal puede viajar a través de estos medios siendo limitado por los limites físicos de los cables. Par trenzado, Cable Coaxial y Fibra óptica
   background: '#3498db'
   
 - title: Par trenzado
   slide-data: Un par trenzado consta de dos conductores (normalmente de cobre), cada uno con su propio aislamiento plástico, trenzados entre sí. Uno de los cables se utiliza para llevar señales al receptor y el otro se utiliza solo como referencia de tierra. Además de la señal enviada por el transmisor en uno de los cables, la interferencia y la diafonía pueden afectar a ambos cables y crear señales no deseadas.
   background: '#2ecc71'
   
 - title: Cable Coaxial
   slide-data: El cable coaxial transporta señales de rangos de frecuencia más altos que los del cable de par trenzado. El cable coaxial tiene un conductor central de cable sólido o trenzado encerrado en una funda aislante, que, a su vez, está revestida de un conductor exterior de lámina metálica, trenza o una combinación de las dos. La envoltura metálica exterior sirve tanto como escudo contra el ruido como como segundo conductor. Este conductor exterior también está encerrado en una funda aislante y todo el cable está protegido por una cubierta de plástico.
   background: '#1abc9c'

 - title: Fibra óptica
   slide-data: Un cable de fibra óptica está hecho de vidrio o plástico y transmite señales en forma de luz. Las fibras ópticas utilizan la reflexión para guiar la luz a través de un canal. Un núcleo de vidrio o plástico está rodeado por un revestimiento de vidrio o plástico menos denso.
   background: '#e67e22'
 
 - title: NO GUIADOS
   slide-data: Los medios no guiados transportan ondas electromagnéticas sin utilizar un conductor físico. Este tipo de comunicación suele denominarse comunicación inalámbrica. Las señales se transmiten normalmente a través del espacio libre y, por lo tanto, están disponibles para cualquier persona que tenga un dispositivo capaz de recibirlas.
   background: "#e74c3c"

 - title: Propagación
   slide-data: Propagación por tierra Las señales de radio viajan a través de una posición más baja y cercana a la tierra.
   slide-data: Propagación por aire. Las señales son de una frecuencia más alta y estas viajan por la ionosfera y recorren más distancia sin requerir tanta potencia de salida
   slide-data:Línea de mira. Son señales de alta frecuencia que se transmiten de antena a antena
   background: '#f1c40f'
 
 - title: Ondas de radio
   slide-data: Las ondas de radio son en su mayoría omnidireccionales, esto hace que las antenas de transmisión y recepción no necesiten estar alineadas, pero puede provocar interferencias si otra antena sintoniza la misma frecuencia o banda.
   background: '#9b59b6'
   
 - title: Microondas
   slide-data: Las microondas son unidireccionales. Cuando una antena transmite ondas de microondas, estas pueden estar enfocadas de forma muy precisa. Esto significa que las antenas emisoras y receptoras deben estar alineadas.
   background: '#3498db'
 
 - title: Infrarrojo
   slide-data: Las ondas infrarrojas se pueden utilizar para comunicaciones de corto alcance. Las ondas infrarrojas, al tener frecuencias altas, no pueden atravesar paredes. Esta característica ventajosa evita las interferencias entre un sistema y otro; un sistema de comunicación de corto alcance en una habitación no puede verse afectado por otro sistema en la habitación contigua
   background: '#2ecc71'
---

{% for slide in page.slides %}

<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}"><h1>{{slide.title}}</h1>{{ slide.slide-data }}</section>

{% endfor %}
