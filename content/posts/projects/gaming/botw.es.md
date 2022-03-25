---
title: "Legend of Zelda: Breath of the Wild"
date: 2020-11-28T22:41:02-08:00
draft: false
featured_image: '/images/content/projects/gaming/botw/botw.jpg'
author: Hugo Belin
description: 'Alfabetos, mapas y más de Legend of Zelda: BOTW'
lang: es
---

# LoZ: BOTW - Alfabeto personalizado #
Si has jugado __Legend of Zelda: Breath of the Wild__ habrás notado que el juego tiene su propio alfabeto. Al buscar por respuestas encontré la equivalencia de caracteres 
y construí un generador de mensajes basados en los caracteres usados en el juego. Es muy sencillo, solo selecciona el estilo (azul/dorado), escribe tu mensaje y obten la equivalencia. 
Caracteres permitidos son `a-z`, `0-9`, `-`, `.`, `!`, `?` (los demás caracteres serán ignorados)

{{< botwtranslator "botw-translator" >}}

# LoZ: BOTW - Mapa Interactivo #
Si aún te encuentras jugando `BOTW` encontrarás el siguiente mapa interactivo de utilidad. Este mapa contiene todos los puntos de interés y fué basado en el mapa interactivo provisto 
por {{< link "https://www.zeldadungeon.net/breath-of-the-wild-interactive-map/" "ZeldaDungeon.net" >}}. Debido a la gran cantidad de información del viz recomiendo reducir los datos mediante 
el uso de filtros por tipo de objetos o limitando por región. Todos los objetos tienen enlaces de referencia así como el nombre en alfabeto de BOTW

{{< tableau "viz1610177864652" "Ze" "ZeldaBreathoftheWildInteractiveMap" "InteractiveMap" >}}

{{< break >}}

El mapa interactivo completo puede ser visto directamente en {{< link "https://public.tableau.com/profile/hugo.belin#!/vizhome/ZeldaBreathoftheWildInteractiveMap/InteractiveMap" "Tableau Public" >}}

## Mapa Interactivo. Detalles de la creación ##
Para poder crear este mapa interactivo se tuvo que hacer lo siguiente:
- Obtener una imagen vacía de todo el mapa jugable, utilicé {{< link "https://imgur.com/gaCjFoi" "esta imagen gigantesca de 150MB y 24k por 20k pixeles" >}}
- Coloqué todos los objetos del mapa encontrados en {{< link "https://www.zeldadungeon.net/breath-of-the-wild-interactive-map/" "este mapa interactivo de Zelda" >}}
- Para acelerar el proceso cree {{< link "/es/posts/projects/software/polygonmaker/" "esta página" >}} que permite capturar las coordenadas de los clicks sobre imagenes junto con etiquetas que fueron 
usadas para denominar regiones
- Despues de colectar alrededor de 6 mil puntos construí el mapa con doble eje mostrado arriba

{{< scrolltop >}}
{{< pageStats >}}
