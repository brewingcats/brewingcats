---
title: "Creador de Polígonos"
date: 2020-12-15T18:13:15-08:00
draft: false
featured_image: '/images/content/projects/software/polygonmaker/polygon.jpg'
author: Hugo Belin
description: 'Crea Polígonos sobre Imagenes'
lang: es
---

En este artículo encontrarás que puedes dibujar polígonos sobre la imagen de tu elección. Lo anterior tiene varias utilidades, en nuestro caso nos ha servido para obtener 
las coordenadas de los vértices para usarlas en visualizaciones de Tableau. Con las coordenadas de los vertices podemos dibujar polígonos sobre imagenes en Tableau con el propósito 
de crear zonas o áreas que pueden ser correlacionadas de distintas formas. {{< link "/es/posts/projects/gaming/botw/" "Este artículo" >}} muestra un ejemplo del uso de polígonos

### Instrucciones ###
Para hacer uso de esta herramienta siga estos pasos:
- Copie la URL de una imagen en la web (sirva de ejemplo {{< link "https://source.unsplash.com/WLUHO9A_xik/800x600" "esta imagen de Unsplash" >}})

{{< customimg src="https://source.unsplash.com/WLUHO9A_xik/800x600" caption="Volcanes" max-height="800" >}}

- Haga click en el botón `Load` para cargar la imagen en el canvas
- El sistema de coordenadas comienza de izquierda a derecha y de arriba a abajo (siendo la esquina superior izquierda `0,0`), puede cambiar las coordenadas usando _offsets_ o desplazamientos 
en los campos provistos
- Cada vértice (creado al hacer click en la imagen) se representa con un cuadrado (su tamaño por default es de `10` pixeles), el campo `size` premite cambiar el tamaño de los cuadrados
- El _checkbox_ funciona con etiquetas (_tags_), al agregar una etiqueta (haciendo click con el boton derecho del ratón), subsecuentes clicks usarán esa última etiqueta si el _checkbox_ esta activo
- Una vez cargada la imagen en el canvas, el botón `Start` comenzará a grabar los clicks hechos en la imagen y añadirá las coordenadas de cada click al final de esta página. Clicks con el botón 
derecho del ratón permiten usar y crear etiquetas, útiles para marcar regiones

{{< customimg src="/images/content/projects/software/polygonmaker/pathoutline.png" caption="Ruta Trazada" max-height="800" >}}

- Una vez que se han marcado las coordenadas deseadas use el enlace `Download` para descargar una copia de las coordenadas en formato `CSV`
- Si desea comenzar de nuevo use el botón `Clear`

{{< polygonmaker prompt >}}

{{< unsplash "WLUHO9A_xik" "apu889" "Unsplash: Volcanes" >}}
{{< unsplash "3pH7TxHU6gw" "callumlwale" "Unsplash: Polígonos" >}}
{{< scrolltop >}}

{{< pageStats >}}
