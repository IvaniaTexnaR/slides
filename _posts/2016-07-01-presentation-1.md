---
title: Detención y corrección de errores
layout: post
permalink: /presentation-1/
background: '#0a5'
slides:
 - title: Presentación
   slide-data:
   Instituto tecnológico de Cancún
   Materia: Fundamentos de telecomunicaciones
   Alumna: Texna Reyes Ivania Gpe.
   Tema: Capítulo 10 Detención y correción de errores
     
 - title: Slide 2
   slide-data: This is second slide

 - title: Slide 3
   slide-data: This is third slide
  
---

{% for slide in page.slides %}
                    
<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}"><h1>{{slide.title}}</h1>{{ slide.slide-data }}</section>
                    
{% endfor %}
    
