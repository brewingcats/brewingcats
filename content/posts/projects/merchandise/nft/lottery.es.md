---
title: "Lotería Mexicana en NFT Primera Edición"
date: 2021-09-23T15:43:50-07:00
draft: false
featured_image: '/images/content/projects/merchandise/nft/mexico.jpg'
description: Vamos a jugar el juego de Lotería Mexicana en su version NFT
lang: es
---

{{< head 2 "¡Bienvenido al Juego de Lotería Mexicana en su version NFT!" >}}
{{< big E >}}l juego de la lotería, ampliamente difundido en México, es un juego de azar que consta de un mazo de 54 o 56 cartas y un número indefinido de tarjetas, por lo 
regular de 2 a 30 o 
más si participan muchas personas, llamadas "tablas" con 16 de dichas cartas escogidas aleatoriamente en una tabla de 4x4, aunque también existen más pequeñas de 3x3 para los niños o más 
grandes de 5x5. Cada vez que se extraiga al azar una carta de la baraja, esta se anuncia y solo los participantes que la tengan deben marcarla en su tabla. El ganador será el primero que 
forme en su tabla la alineación que se haya especificado al inicio del juego, por lo general la tabla completa con las cartas marcadas y grite "Lotería" en señal de victoria. Para las 
tablas de 4x4, existen combinaciones de 54 eligiendo 16 : C(54,16) = 21 094923 659355 es decir : 21 billones 94 923 millones 659 355 formas posibles de hacer tableros diferentes de lotería 
de 4x4 sin repetición de figuras con las 54 cartas estándar. {{< link src="https://en.wikipedia.org/wiki/Loter%C3%ADa" label="Léa la definición completa en Wikipedia." >}}

{{< big E >}}sta edición de lotería en su version NFT contiene tarjetas coleccionables y varios tableros de juego

{{< head 4 "Reglas Básicas" >}}
- Existen: `54 figuras` (tarjetas) basadas en el juego de mesa original Lotería Mexicana (acuñadas de forma única como collecionables NFT)
- El juego comienza con `4 tableros` (acuñados como coleccionables NFT). Para acuñar tableros adicionales la comunidad puede votar en la forma al final de este artículo
- Cada tablero tiene `16 figuras aleatorias` de las 54 de la colección original. Cada tablero contiene una combinación única de figuras

{{< head 4 "Tableros de Juego">}}
La colección actual (Edición: Pixel) presenta los siguientes tableros de juego NFT coleccionables, puedes encontrarlos en 
{{< link src="https://opensea.io/collection/mexican-lottery-game" label="OpenSea" >}} "gas free"

{{< carousel-rich data="loterianftboards" width="50%" >}}

{{< head 4 "Tarjetas Seleccionadas" >}}
La colección actual (Edición: Pixel) presenta las siguientes tarjetas NFT coleccionables, puedes encontrarlas en 
{{< link src="https://opensea.io/collection/mexican-lottery-game" label="OpenSea" >}} y ¡gana el juego!

{{< carousel-rich data="loterianftcards" width="50%" dropdown="yes" >}}

{{< head 4 "Mecánica del Juego" >}}
1. Creación de una nueva edicion (incluye un diseño actualizado)
2. Generación de 4 tableros de juego, cada uno acuñado como coleccionable NFT. Para entrar al juego deberás comprar un tablero
3. Selección de una tarjeta aleatoria (acuñada como coleccionable NFT)
4. ¿Existe un tablero ganador? (Lotería!)
    - No: De vuelta al paso 3
    - Si: Se acuñará una tarjeta especial de ganador para la edición actual que contendrá la lista de tarjetas, el tablero ganador asi como sus códigos unicos respectivamente
5. Se añadirán el resto de las 54 tarjetas a la colección NFT
6. Serás el ganador de la edición si tienes:
    - 16 tarjetas contenidas en el tablero de juego ganador
    - El tablero ganador con las 16 figuras ganadoras
    - La tarjeta especial del ganador
    - Todas las tarjetas y el tablero pertenecen a la misma edición (actualmente la primera edición)
    - ¡Felicidades! Eres el ganador de esta edición del juego de Lotería Mexicana
7. También te puedes convertir en ganador una vez que el juego se ha acabado si logras conseguir todos los requerimientos del paso 7 con la excepción de la tarjeta especial del ganador al comprar 
los coleccionables. Una vez conseguidos todos estos coleccionables {{<link src="https://twitter.com/brewingcats" label="déjanos saber">}} para acuñar una nueva tarjeta ganadora con la combinación 
que has adquirido. Las tarjetas ganadoras serán acuñadas en el orden pedido y van a tener un conteo del ganador
8. Si esta edición tuvo exito ¡podrás esperar una segunda edición del juego con un diseño actualizado!

{{< head 3 "Código para Selección y Generación Aleatoria" >}}
{{< big P >}}ara asegurar la transparencia hemos hecho public el código de _selección aleatoria de tarjetas_ asi como el código de _generación aleatoria de tableros_. Si estás interesado en los 
detalles técnicos y quieres saber como se selecciona una tarjeta aleatoriamente o como se genera un tablero puedes encontrarlo en el
{{< link src="https://github.com/brewingcats/loteria" label="Módulo de PowerShell: Lotería" >}} hosteado en GitHub. Este repositorio contiene los cmdlets para cada operación así como una forma 
de simular un juego completo de principio a fin

{{< head 3 "Diseño de las Tarjetas de Lotería" >}}

{{< big C >}}ada tarjeta tiene un diseño único basado en el juego original de Lotería Mexicana. Adicionalmente las tarjetas tienen un diseño basado en el tema de la edición, con un marco específico 
y un número de carta asociado. Además del diseño cada tarjeta contiene un código único visible por el dueño, este código único es distinto a la clave única creada cuando se acuña la tarjeta. Vea 
la imágen abajo para más detalles del diseño de la tarjeta

{{< customimg src="/images/content/projects/merchandise/nft/loteriav1/carddesign.png" caption="Diseño de la Tarjeta: Primera Edición" >}}

{{< head 3 "Diseño del Tablero de Juego" >}}

{{< big E>}}l tablero de juego esta diseñado con 16 tarjetas (arregladas en 4x4) de acuerdo al diseño original del juego de mesa Lotería Mexicana, las tarjetas dentro son exactamente las tarjetas 
que serán acuñadas conforme el juego avance para su fácil identificación. La tarjeta tiene un marco conmemorativo correspondiente a su edición. Cada tablero tiene un código único separado de la 
clave única creada cuando se acuña el tablero ademas de los 16 códigos correspondientes a las tarjetas que representa, estos códigos son solo visibles por el dueño del tablero. Vea la imágen 
abajo para más detalles del diseño del tablero

{{< customimg src="/images/content/projects/merchandise/nft/loteriav1/boarddesign.png" caption="Diseño del Tablero: Primera Edición" >}}

{{< head 3 "Diseño de la Tarjeta Ganadora" >}}

{{< big L >}}a tarjeta ganadora, también conocida como la tarjeta de trofeo se utiliza para señalizar que el dueño es el ganador del juego. Existen dos tipos de tarjetas de trofeo, el primer tipo 
es cuando se emite la tarjeta de forma natural una vez que el juego termina cuando se detectó que alguno de los tableros de juego existente tiene una combinación ganadora de tarjetas, este tipo 
de tarjeta contiene la designación "`Winner`" además de los atributos regulares. Una vez que un nuevo dueño adquiere 16 tarjetas y un tablero de juego que las contiene (todas de la misma edición), 
este nuevo dueño puede {{<link src="https://twitter.com/brewingcats" label="solicitar">}} que se acuñe una nueva tarjeta de trofeo, esta tarjeta de trofeo contendrá la designación `### Winner` 
además de sus atributos regulares. Todas las tarjetas de trofeo contendrán la edición a la que pertenece y la combinación de códigos ganadores. Tú puedes declararte el orgulloso ganador de 
_¡Lotería!_ si posees las 16 tarjetas, el tablero que las contiene, y la tarjeta de trofeo que prueba que has ganado. El diseño de esta tarjeta es reservado hasta que se encuentre un ganador

{{< head 3 "¿Cómo Acuñar mas Tableros de Juego?" >}}

{{< big S >}}i existe una fuerte demanda es natural que más usuarios quieran participar en el juego, para satisfacer esta demanda hemos creado la siguiente forma para que la comunidad nos 
deje saber si hay interés de participar. Basado en las respuestas de esta forma acuñaremos mas tableros de juego de acuerdo a las siguientes reglas:

- Despues de `100` solicitudes `4` tableros adicionales serán acuñados y tendrás la oportunidad de comprar uno
- Al crear los tableros se revisará si alguno de ellos es ganador, lo cual finalizará el juego
- Para acuñar `4` tableros de juego adicionales el numero de respuestas tendrá que incrementarse de acuerdo a la formula `n = n * 2` donde `n` es el número de solicitudes por ejemplo 100, 200, 
400, 800, etc.


Número de solicitudes para acuñar mas tableros de juego: `100`

{{< iframe "https://docs.google.com/forms/d/e/1FAIpQLSc3tib1-iRlrTUeoN6fU3iRBnPMCfGz8gnxkluEUM6VGshnRQ/viewform?embedded=true" "640" "500" >}}


{{< unsplash "pelUkQqVVbA" "pinamessina" "Unsplash: Arte Mexicano" >}}
{{< scrolltop >}}

{{< pageStats >}}
