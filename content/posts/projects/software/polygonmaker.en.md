---
title: "Polygon Maker"
date: 2020-12-15T18:13:10-08:00
draft: false
featured_image: '/images/content/projects/software/polygonmaker/polygon.jpg'
author: Hugo Belin
description: 'Creates polygons on top of images'
lang: en
---

This post allows you to draw polygons on top of a picture of your choice. This comes handy for several scenarios, in our case we have used it to get path coordinates for 
Tableau visualizations. With the path coordinates we were able to draw the resulting polygons on top of the images in Tableau with the ability to correlate this data for 
zones or areas that we wanted. To view the usage sample check out {{< link "/posts/projects/gaming/botw/" "this post." >}}

### Usage ###
To make use of this utility follow these steps:
- Copy the path of the image on the web (we're using {{< link "https://source.unsplash.com/WLUHO9A_xik/800x600" "this sample from Unsplash" >}})

{{< customimg src="https://source.unsplash.com/WLUHO9A_xik/800x600" caption="Volcanoes" max-height="800" >}}

- Click the `Load` button to put it on the canvas
- The coordinate system start from left to right and top to bottom (upper left corner is `0,0`), if you want it to be different you can use the offset input fields provided
- Every vertex (where you click on the picture) is denoted by a square (default size is `10` pixels), the size field allows you to change the size of the squares
- Checkbox field works with tags, if you use right click you can use tags, if you add a tag and the checkbox is active further left clicks will use the last tag
- Once you loaded the image on the canvas `Start` button will start recording clicks on the image and the coordinates will be appended to the bottom of the image. Right clicks can be used 
to add tags to the points which can be used to denote regions

{{< customimg src="/images/content/projects/software/polygonmaker/pathoutline.png" caption="Path Outline" max-height="800" >}}

- Once the desired coordinates are recorded at the bottom use the `Download` link to get them via `CSV`
- If you desire to start over use the `Clear` button

{{< polygonmaker prompt >}}

{{< unsplash "WLUHO9A_xik" "apu889" "Unsplash: Volcanoes" >}}
{{< unsplash "3pH7TxHU6gw" "callumlwale" "Unsplash: Polygons" >}}
{{< scrolltop >}}

{{< pageStats >}}
