---
title: Detención y corrección de errores
layout: post
permalink: /presentation-1/
background: '#0a5'
slides:
 - title: Capitulo 10 Detención y corrección de errores
   slide-data: Ingeniería en sistemas computacionales - Fundamentos de telecomunicaciones - Alumna Texna Reyes Ivania Gpe.
     
 - title: Introducción
   slide-data: Los datos pueden corromperse durante la transmisión. Algunas aplicaciones requieren que se detecten y corrijan los errores.

 - title: Tipos de errores
   slide-data: Error de un solo bit significa que solo 1 bit de una unidad de datos determinada (como un byte, un carácter o un paquete) cambia de 1 a 0 o de 0 a 1. Error de ráfaga significa que 2 o más bits en la unidad de datos han cambiado de 1 a 0 o de 0 a 1.
 
 - title: Redundancia
   slide-data: El concepto central para detectar o corregir errores es la redundancia. Para poder detectar o corregir errores, necesitamos enviar algunos bits extra con nuestros datos. Estos bits redundantes los agrega el remitente y el receptor los elimina. Su presencia permite al receptor detectar o corregir bits corruptos.

 - title: Detección vs corrección
   slide-data: La corrección de errores es más difícil que la detección. En la detección de errores, solo buscamos si se ha producido algún error. La respuesta es un simple sí o no. En la corrección de errores, necesitamos saber la cantidad exacta de bits que están dañados y su ubicación en el mensaje. El número de errores y el tamaño del mensaje son factores importantes.
 
 - title: Corrección de errores directos vs retransmisión
   slide-data: La corrección de errores hacia adelante es el proceso en el que el receptor intenta adivinar el mensaje utilizando bits redundantes. Esto es posible si el número de errores es pequeño. La corrección por retransmisión es una técnica en la que el receptor detecta un error y solicita al remitente que reenvíe el mensaje. El reenvío se repite hasta que el receptor considera libre de errores el mensaje.
   
 - title: Codificación
   slide-data: La redundancia se logra mediante varios esquemas de codificación. El remitente agrega bits redundantes mediante un proceso que crea una relación entre los bits redundantes y los bits de datos reales. El receptor comprueba estas relaciones para detectar o corregir errores.

 - title: 10.2 Codificación de bloques
   slide-data: En la codificación de bloques, dividimos nuestro mensaje en bloques de k bits, llamados palabras de datos. Agregamos r bits redundantes para que la longitud total sea n = k + r. Estos bloques resultantes se denominan palabras de código. El proceso de codificación es uno a uno; la misma palabra de datos es siempre codificada de la misma manera.

 - title: Distancia de Hamming
   slide-data: La distancia de Hamming entre dos palabras (del mismo tamaño) es el número de diferencias entre los bits correspondientes. Se puede hallar aplicando la operación XOR a las dos palabras y contando los '1's en el resultado. La distancia de Hamming es siempre mayor que cero.
   
 - title: Distancia mínima de Hamming
   slide-data: La distancia mínima de Hamming es la distancia de Hamming más pequeña entre todos los pares posibles de palabras. Se utiliza para diseñar códigos de detección y corrección de errores.

 - title: 10.3 Códigos de bloque lineales
   slide-data: Los códigos de bloques lineales son códigos en los que el XOR de dos palabras de código válidas crea otra palabra de código válida. Para definirlos formalmente se requiere álgebra abstracta.

 - title: Códigos cíclicos
   slide-data: Los códigos cíclicos son códigos de bloques lineales con una propiedad adicional. En un código cíclico, si una palabra de código se desplaza cíclicamente, el resultado es otra palabra de código válida.

 - title: Suma de verificación
   slide-data: La suma de comprobación se utiliza en Internet mediante varios protocolos, aunque no en la capa de enlace de datos. Se basa en el concepto de redundancia.

 - title: 
   slide-data: 

 - title: 
   slide-data: 

 - title: 
   slide-data: 

 - title: 
   slide-data: 

---

{% for slide in page.slides %}

<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}"><h1>{{slide.title}}</h1>{{ slide.slide-data }}</section>

{% endfor %}
