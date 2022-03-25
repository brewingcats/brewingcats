---
title: "Legend of Zelda: Breath of the Wild"
date: 2020-11-28T22:40:56-08:00
draft: false
featured_image: '/images/content/projects/gaming/botw/botw.jpg'
author: Hugo Belin
description: 'Alphabets, maps, and more about Legend of Zelda: BOTW '
lang: en
---

# LoZ: BOTW - Custom Alphabet #
If you played __Legend of Zelda: Breath of the Wild__ you might have noticed it has its own alphabet system. Looking online for answers I found an equivalency 
for the characters in it and I built an online message generator based on the game character set. It's simple, just select the style (blue/golden) type your 
message and get the equivalency. Supported characters are `a-z`, `0-9`, `-`, `.`, `!`, `?` other characters will be ignored

{{< botwtranslator "botw-translator" >}}

# LoZ: BOTW - Interactive Map #
If you happen to be playing the game still you may find the following interactive map useful. This map contains all the interest points and I based on the interactive map provided by 
{{< link "https://www.zeldadungeon.net/breath-of-the-wild-interactive-map/" "ZeldaDungeon.net" >}}. Since there's a lot of information initially on the viz I recommend to reduce the 
scope by region or by type of items. All items have reference links as well as its name in Zelda's BOTW alphabet style

{{< tableau "viz1610177864652" "Ze" "ZeldaBreathoftheWildInteractiveMap" "InteractiveMap" >}}

{{< break >}}

This interactive map can be viewed directly in {{< link "https://public.tableau.com/profile/hugo.belin#!/vizhome/ZeldaBreathoftheWildInteractiveMap/InteractiveMap" "Tableau Public" >}}

## Interactive Map. Behind the Scenes ##
In order to make possible this interactive map, I had to do the following:
- Obtained an empty image of the whole playable map, used {{< link "https://imgur.com/gaCjFoi" "this giganting 150MB 24k by 20k pixels image" >}}
- Started mapping all the items from the map found in {{< link "https://www.zeldadungeon.net/breath-of-the-wild-interactive-map/" "this Zelda interactive map" >}}
- In ordert to speed the process up I created {{< link "/posts/projects/software/polygonmaker/" "this page" >}} which helped by capturing clicks' coordinates and tags which where used to note regions
- After mapping more than 6k items I build the dual axis custom map shown above

{{< scrolltop >}}
{{< pageStats >}}
