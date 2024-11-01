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
 
 - title: Redundancia
   slide-data: El concepto central para detectar o corregir errores es la redundancia. Para poder detectar o corregir errores, necesitamos enviar algunos bits extra con nuestros datos. Estos bits redundantes los agrega el remitente y el receptor los elimina. Su presencia permite al receptor detectar o corregir bits corruptos.

 - title: Detección vs corrección
   slide-data: La corrección de errores es más dificil que la detección. En la detección de errores, solo buscamos si se ha producido algún error. La respuesta es un simple sí o no. En la corrección de errores, necesitamos saber la cantidad exacta de bits que están dañados y lo que es más importante, su ubicación en el mensaje. El número de errores y el tamaño del mensaje son factores importantes.
 - title: Corrección de errores directos vs retransmisión
   slide-data:  La corrección de errores hacia adelante es el proceso en el que el receptor intenta adivinar el mensaje utilizando bits redundantes. Esto es posible, como veremos más adelante, si el número de errores es pequeño.  La corrección por retransmisión es una técnica en la que el receptor detecta la aparición de un error y solicita al remitente que reenvie el mensaje. EI reenvio se repite hasta que llega un mensaje que el receptor considera libre de errores (por lo general, no se pueden detectar todos los errores).
   
   - title: Codificación
   slide-data: La redundancia se logra mediante varios esquemas de codificación. El remitente agrega bits redundantes mediante un proceso que crea una relación entre los bits redundantes y los bits de datos reales. El receptor comprueba las relaciones entre los dos conjuntos de bits para detectar o corregir los errores.

 - title: 10.2 CODIFICACIÓN DE BLOQUES
   slide-data: En la codificación de bloques, dividimos nuestro mensaje en bloques, cada uno de k bits, lamados palabras de datos. Agregamos r bits redundantes a cada bloque para hacer que la longitud n = k+ r. Los bloques de n bits resultantes se denominan palabras de código. Cómo se eligen o calculan los r bits adicionales es algo que discutiremos más adelante. El proceso de codificación de bloques es uno a uno; la misma palabra de datos es siempre codificado como la misma palabra de código. 

 - title: Distancia de Hamming
   slide-data: . La distancia de Hamming entre dos palabras (del mismo tamaño) es el número de diferencias entre los bits correspondientes. Mostramos la distancia de Hamming entre dos palabras xey como d(x, y). La distancia de Hamming se puede encontrar fácilmente si aplicamos la operación XOR (4) a las dos palabras y contamos el número de Is en el resultado. Tenga en cuenta que la distancia de Hamming es un valor mayor que cero
   
   - title: Distancia mínima de Hamming
   slide-data: Aunque el concepto de distancia de Hamming es el punto central al tratar con códigos de detección y corrección de errores, la medida que se utiliza para diseñar un código es la distancia mínima de Hamming. En pocas palabras, la distancia minima de Hamming es la distancia de Hamming más pequeña entre todos los pares posibles. Usamos dimin para definir la distancia mínima de Hamming en un esquema de codificación.

 - title: 10.3 CÓDIGOS DE BLOQUE LINEALES
   slide-data: La definición formal de códigos de bloques lineales requiere el conocimiento de álgebra abstracta (particularmente campos de Calois). Por lo tanto damos una definición informal. Para nuestros propósitos, un código de bloque lineal es un código en el que el OR exclusivo (adición módulo-2) de dos palabras de código válidas crea otra palabra de código valida

 - title: CÓDIGOS CÍCLICOS
   slide-data: Los códigos ciclicos son códigos de bloques lineales especiales con una propiedad adicional. En un código cíclico, si una palabra de código se desplaza (rota) ciclicamente, el resultado es otra palabra de código. Por ejemplo, si 1011000 es una palabra en código y desplazamos ciclicamente hacia la izquierda, entonces 0110001 también es una palabra en código.
  
 - title: SUMA DE VERIFICACIÓN
   slide-data: La suma de comprobación se utiliza en Internet mediante varios protocolos, aunque no en la capa de enlace de datos. Sin embargo, lo analizamos brevemente aquí para completar nuestra discusión sobre la verificación de errores. Al igual que los códigos lineales y cíclicos, la suma de comprobación se basa en el concepto de redundancia.
  
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
    
