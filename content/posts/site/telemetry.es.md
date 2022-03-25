---
title: "Telemetría"
date: 2021-02-03T21:38:12-08:00
draft: false
author: "Hugo Belin"
type: page
featured_image: '/images/content/site/chart.jpg'
categories: [site]
tags: [site]
description: Datos de Telemetry, estadísticas de uso
lang: es
---
{{< big P >}}ara poder medir nuestro criterio de exito en nuestro website (prover una experiencia deleitable a nuestros usuarios) necesitamos conocer y entender como es este sitio usado. 
Planeamos lograrlo mediante el uso de datos de telemetría, esta información nos proveerá detalles sobre problemas de usabilidad, el tipo de contenido que los usuarios gustan más así como 
otro tipo de problemas

{{< big E >}}l uso de telemetría es una práctica común en la mayoría de sitios web, hoy en día ni siquiera se informa a los usuarios sobre esta práctica, mucho menos se les deja saber el 
uso que se da a esta información (por ejemplo el análisis que se da y si se vende para su uso en publicidad, o si se utiliza para generar un perfil individual y recolectar comportamiento 
sobre el usurio). En nuestro caso hemos tomado pasos adicionales para asegurarnos de que {{< link "/" "BrewingCats.com" >}} y sus sitios derivados sigan siendo confiables

{{< big C >}}omo se menciona en nuestra {{< link "/es/posts/site/policy/" "Política de Uso" >}} deseamos ser un ejemplo de comportamiento de la visión que deseamos para todos los sitios 
web sobre recolección y uso de información generada por los usuarios. Para lograr lo anterior, hemos tomado las siguientes acciones:

{{< big 1 >}} Construímos un sistema de recolección y almacenamiento personalizado. No quisimos usar proveedores de telemetría externos para evitar la tentación de que usen la información 
de los usuarios con otros propósitos. Como bono adicional aprendimos aprendimos a hacerlo y disfrutamos del proceso :smiley:

{{< big 2 >}} Estamos haciendo la información recolectada disponible a todo mundo. La información es recolectada por nuestros usuarios y para nuestros usuarios. Todo mundo tiene el derecho 
de saber que sucede con la información generada por ellos mismos. Por lo mismo estamos haciendo disponible el último mes de datos recolectados por nuestra telemetría los cuales pueden ser 
analizados por el Viz embebido abajo

{{< big 3>}} Los usuarios deben de saber que información específica es generada por su uso de nuestro sitio web. Por lo mismo nuestros vizzes tienen la habilidad de filtrar por `ClientId`. 
Este valor se muestra abajo también, al ingresar estos datos en los filtros del viz se puede saber la información especifica que el usuario generó al usuar nuestro sitio

{{< big 4 >}} Usted, como usuario tiene el derecho de no compartir la información de uso con nosotros, lo mismo aplica a nuestros sitios relacionados. Entendemos y promovemos el derecho a la 
completa privacidad a pesar de las medidas de transparencia anunciadas en este artículo, si el usuario no desea compartir la información de telemetría con nosotros apoyamos la decisión y le 
damos la facilidad de hacerlo fácilmente. Para ello puede usar los controles de abajo para deshabilitar la generación de información de telemetría

{{< head 3 "Datos de Telemetría del Último Mes" >}}
{{< telemetrybrs >}}
Tu Client ID: {{< clientid >}}

{{< tableautelemetry >}}

{{< break >}}
{{< unsplash "6EnTPvPPL6I" "isaacmsmith" "Unsplash: Charting Goals" >}}

{{< pageStats >}}
