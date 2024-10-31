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
   slide-data: Data can be corrupted during transmission.
Some applications require that errors be detected and corrected

 - title: Slide 3
   slide-data: This is third slide
  
---

{% for slide in page.slides %}
                    
<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}"><h1>{{slide.title}}</h1>{{ slide.slide-data }}</section>
                    
{% endfor %}
    
