---
title: Detención y corrección de errores
layout: post
permalink: /presentation-1/
background: '#0a5'
slides:
 - title: Capitulo 10 Detención y corrección de errores
   slide-data: Ingeniería en sistemas computacionales
   slide-data: Fundamentos de telecomunicaciones
   slide-data: Alumna Texna Reyes Ivania Gpe.
     
 - title: Introducción
   slide-data: Los datos pueden corromperse durante la transmisión. Algunas aplicaciones requieren que se detecten y corrijan los errores.

 - title: Tipos de errores
   slide-data: Error de un solo bit significa que solo 1 bit de una unidad de datos determinada (como un byte, un carácter o un paquete) cambia de 1 a 0 o de 0 a 1., Error de ráfaga significa que 2 o más bits en la unidad de datos han cambiado de 1 a 0 o de 0 a 1.
 
 - title: Slide 3
   slide-data: This is third slide

 - title: Slide 3
   slide-data: This is third slide

 - title: Slide 3
   slide-data: This is third slide
  
  
---

{% for slide in page.slides %}
                    
<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}"><h1>{{slide.title}}</h1>{{ slide.slide-data }}</section>
                    
{% endfor %}
    
