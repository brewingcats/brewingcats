---
title: "Nuevo Jam Stack"
date: 2020-04-19T17:24:32-07:00
draft: false
author: Hugo Belin
featured_image: '/images/BrewingCatsMain.jpg'
categories: [software]
tags: [software,proyectos]
description: Conclusiones sobre la migración de Gatsby a Hugo
lang: es
---

{{< big L >}}a versión anterior de {{< link src="https://brewingcats.com" label="brewingcats.com" >}} se construyó sobre un diferente 
{{< link "https://jamstack.org/" "JAM Stack" >}}, y en particular en un diferente {{< link "https://www.staticgen.com/" "Generador de Sitio Estático" >}}. 
Construir {{< link "https://brewingcats.com" "brewingcats.com" >}} sobre {{< link "https://www.gatsbyjs.org" "Gatsby" >}} nos permitió adquirir 
bastante experiencia y nos dejó hacer uso de nuestro conocimiento en {{< link "https://reactjs.org/" "React" >}} para aplicarlo al sitio. React es parte 
central de la estructura del sitio, además tuvimos la oportunidad de aprender el sistema de querying de {{< link "https://graphql.org/" "GraphQL" >}} 
para llevar a cabo operaciones básicas

Desafortunadamente tuvimos efectos colaterales como parte de la adopción de Gatsby, intentaré resumir algunas de las lecciones asi describir el porqué de 
nuestra decisión de movernos a {{< link "https://gohugo.io/" "Hugo" >}}
- {{< link "https://www.typescriptlang.org" "TypeScript" >}} no esta soportado por default. TypeScript esta soportado por ciertos "starters", eso reduce bastante 
las opciones disponibles ya que no hay muchos
- El sitio se vuelve completamente dependiente del "starter" seleccionado. No hay garantías de su mantenimiento, y aunque esto es un problema que también puede 
ocurrir con Hugo, el uso de TypeScript redujo las opciones e incremento las probabilidades de "starters" con un alto numero de defectos o que se retrasa mucho en actualizar las dependencias
- Sobre-dependiente de npm. Aunque tener un systema de manejo de dependencias es útil, tener muchas dependencias incrementó las probabilidades de cambios que 
rompieran la construcción del sitio, lo cual desafortunadamente ocurrió con frecuencia, lo cual nos llevó ya sea a quedarnos con dependencias inseguras 
potencialmente, o manualmente investigar los problemas y leer la salida de la consola sin mucho detalle (experiencia que mejoró bastante al usar Hugo)
- Desarrollo del sitio es primero, el contenido viene despues. Cualquier personalización, por pequeña que sea, requiere de cierta inversión, varios de los 
escenarios no se cubren por default. Al poco de usar Hugo pudimos usar con muy poco esfuerzo el soporte de múltiples idiomas así como incluir Disqus en los  
artículos. En cuanto a Gatsby, usando un "starter" que soportara TypeScript nos llevo a diseñar componentes de React personalizados y en el caso de soporte de 
múltiples idiomas nos tocó modificar extensivamente el diseño del sitio para tenerlo funcionando
- Modificaciones al "starter" seleccionado se volvieron responsabilidad del equipo. Debido a que tuvimos que hacer varios cambios a los archivos de diseño del 
sitio tuvimos que sincronizar y resolver dependencias cada vez que el "starter" era actualizado. Hugo logra lo mismo de manera maravillosa al tomar precedencia en 
los archivos locales sobre los del "starter" lo cual nos evita cambiar la fuente y actualizar sin problemas
- En este release inicial dejamos de usar de manera central el lenguaje TypeScript (aún consideramos usarlo en librerías y código del servidor). Esto permite a 
nuestro equipo concentrarse mayormente en generar contenido y deja las actualizaciones de código y diseño como algo adicional y solo cuando es requerido
- Gatsby se encuentra basado en React, por lo cual todo circula alrededor de React. Extender el sitio requiere crear componentes propios incluso si el cambio, 
es sencillo. Lo anterior junto con la mezcla con el starter mencionada en el segundo argumento hizo nuestra tarea más difícil. El orden de busqueda de Hugo es 
bastante bien recibido en este contexto, además si queremos usar React podemos incluir aplicaciones de React utilizando lo que se conoce como un 'shortcode', 
también podríamos usar varias aplicaciones de React dentro de un mismo artículo

Considerando lo anterior, creemos que Gatsby es un excelente sistema y los "starters" permiten concentrarse en el contenido cuando se encuentra uno que llene todas las necesidades. El mantenimiento es involucrado aun así dependiendo del "starter" que se haya seleccionado sin embargo sin modificaciones esto no debería ser 
mayor problema

![Gatsby vs Hugo](/images/content/New-JAM-Stack.jpg)

{{< big A >}}demás del cambio a Hugo hemos tomado la oportunidad de mejorar el diseño del sitio, en particular hemos movido el almacenamiento de imagenes. Anteriormente nos 
encontramos con tiempos largos de 'compilación' debidos a que Gatsby procesaba las imágenes optimizándolas para que fueran cargadas progresivamente (una 
característica bastante buena de cualquier sitio), para evitar aquellos largos tiempos movimos el almacenamiento de imagenes en un subdominio separado `media.*` 
lo cuál no fue la mejor decisión dada la implementación que escogimos. Actualmente el sitio se encuentra hosteado en GitLab Pages el cual tiene de fondo una 
instancia de `Node.js`, una vez que el numero de usuarios baja GitLab manda dormir la instancia. Despertar la instancia de nuevo es un proceso que puede llevar 
varios segundos. Hostear imágenes y otro contenido en una instancia separada de GitLab Pages ocasionó que al tiempo inicial de carga de la página se le sume el 
tiempo que toma despertar la instancia adicional lo cual degradó la experiencia para contenido con varias imágenes. Para resolverlo hemos incluido las imagenes 
de nuevo con el sitio actual así como haremos uso de Unsplash e Instagram cuando sea aplicable

{{< head 3 "Siguientes Pasos" >}}
Estaremos portando todos los features y moviendo todo el contenido a Hugo, esté al pendiente :smiley:

{{< scrolltop >}}
{{< pageStats >}}
