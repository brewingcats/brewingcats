---
title: "Extractor de Código de Tableau Share"
date: 2020-08-20T17:05:47-07:00
draft: false
featured_image: '/images/content/projects/software/tableau.jpg'
author: Hugo Belin
description: Utilidad básica para extraer los campos necesarios del código para compartir de Tableau con el objetivo de usarlos con nuestro shortcode para embeber Tableau
lang: es
---

{{< big A >}}nteriormente creamos un {{< link "https://gist.github.com/hobelinm/de089f99c3543e2a16f8f24fee4d958e" "shortcode para embeber Vizzes de Tableau" >}} en sitios web basados en el 
Framework de Hugo, el uso de este es bastante simple y conveniente, sin embargo para poder hacer uso de el necesitamos saber de antemano ciertos campos que extraemos manualmente del
código para compartir que nos da Tableau. Abajo los pasos para obtener este código

{{< head 2 "Añadiendo el ShortCode a tu Sitio Basado en Hugo" >}}

{{< big P>}}ara agregar soporte para embeber vizzes de Tableau sencillamente copia {{< link "https://gist.github.com/hobelinm/de089f99c3543e2a16f8f24fee4d958e" "nuestro shortcode" >}} en el 
siguiente directorio dentro de tu sitio `/layouts/shortcodes/tableau.html`. Para embeber un viz en tu sitio web en tu código de markdown agregue el siguiente código donde quieras embeber tu viz. 
La siguiente sección mostrará como obtener el código para compartir desde Tableau Public y a partir de ahi podremos usarlo para obtener los parámetros que necesitamos

`{{` `< tableau "viz1595830498772" "Hi" "HikeCollection" "Hikes">` `}}`
{{< caption "Código usado para embeber un viz de Tabelau Public" >}}

El código de arriba producirá el siguiente resultado:

{{< tableau "viz1595830498772" "Hi" "HikeCollection" "Hikes" >}}
{{< caption "Viz generada a partir del código de arriba" >}}
{{< break >}}


{{< head 2 "Cómo Obtener el Código para Compartir" >}}

{{< big P >}}ara obtener el código para compartir de un viz de Tableau Public sencillamente vaya al viz que desea embeber. En la barra de herramientas de la parte inferior derecha se encuentra 
un botón para compartir

{{< customimg src="/images/content/projects/software/tableauparser/sharebtn.jpg" caption="Botón para Compartir un Viz de Tableau Public" >}}

Al hacer click en el botón de compartir se despliega el dialogo para compartir que tiene dos campos, el primero etiquetado `Embed Code` será el que usaremos, copie el contenido de este campo 
ya que será el que usaremos para la forma de abajo (siga leyendo para más detalles)

{{< customimg src="/images/content/projects/software/tableauparser/embedcode.jpg" caption="Código de Ejemplo para Embeber un Viz" >}}

El código copiado será similar al ejemplo de abajo

{{< gist hobelinm 67b27751b6d1a6373f1ae09d4e8a3eb3 >}}
{{< caption "Código de Ejemplo para Embeber un Viz de Tableau" >}}

{{< head 2 "Extrayendo la Información Necesaria para Nuestro ShortCode" >}}

{{< big C >}}on el código para embeber el viz copiado podemos hacer uso de el para extraer la información necesaria para nuestro ShortCode, sencillamente péguela en la caja de texto en la forma. 
La forma extraerá cuatro campos necesarios a partir del código pegado:
- Viz ID
- Prefijo del Viz
- Nombre del Workbook (libro de trabajo)
- Nombre del Worksheet (hoja de trabajo)

Estos campos se utilizan en nuestro ShortCode, otra opción es sencillamente copiar el código del último campo y pegarlo directamente en nuestro markdown

{{< tableauparser >}}
{{< caption "Viz Embebida" >}}

{{< unsplash "no2blvVYoJw" "claybanks" "Unsplash: Tableau Viz" >}}
{{< scrolltop >}}

{{< pageStats >}}
