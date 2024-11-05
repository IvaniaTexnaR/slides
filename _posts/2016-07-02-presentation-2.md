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
   
 - title: Guiados
   slide-data: Los medios guiados, que son aquellos que proporcionan un conducto de un dispositivo a otro. Una señal puede viajar a través de estos medios siendo limitado por los limites físicos de los cables. Par trenzado, Cable Coaxial y Fibra óptica
   background: '#3498db'
   
 - title: Par trenzado
   slide-data: Un par trenzado consta de dos conductores (normalmente de cobre), cada uno con su propio aislamiento plástico, trenzados entre sí. Uno de los cables se utiliza para llevar señales al receptor y el otro se utiliza solo como referencia de tierra. Además de la señal enviada por el transmisor en uno de los cables, la interferencia y la diafonía pueden afectar a ambos cables y crear señales no deseadas.
   background: '#2ecc71'
   
 - title: Cable Coaxial
   slide-data: El cable coaxial transporta señales de rangos de frecuencia más altos que los del cable de par trenzado. El cable coaxial tiene un conductor central de cable sólido o trenzado encerrado en una funda aislante, que, a su vez, está revestida de un conductor exterior de lámina metálica, trenza o una combinación de las dos. La envoltura metálica exterior sirve tanto como escudo contra el ruido como como segundo conductor. Este conductor exterior también está encerrado en una funda aislante y todo el cable está protegido por una cubierta de plástico.
   background: '#1abc9c'

 - title: Slide 7
   slide-data: This is seventh slide
   background: '#e67e22'
 
 - title: Slide 8
   slide-data: This is seventh slide
   background: "#e74c3c"

 - title: Slide 9
   slide-data: This is seventh slide
   background: '#f1c40f'
 
 - title: Slide 10
   slide-data: This is seventh slide
   background: '#9b59b6'
---

{% for slide in page.slides %}

<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}"><h1>{{slide.title}}</h1>{{ slide.slide-data }}</section>

{% endfor %}
