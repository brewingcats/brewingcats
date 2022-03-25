---
title: "Tableau Embed Parser"
date: 2020-08-20T17:05:15-07:00
draft: false
featured_image: '/images/content/projects/software/tableau.jpg'
author: Hugo Belin
description: Basic utility to extract the required fields from a given Tableau share code in order for it to work with our custom Tableau embed shortcode
lang: en
---

{{< big W >}}e've created a {{< link "https://gist.github.com/hobelinm/de089f99c3543e2a16f8f24fee4d958e" "shortcode for embedding Tableau Vizzes" >}} into Hugo Framework based websites, 
it is quite simple to use and very convenient, however before being able to use it you need to know few fields which have to be retrieved from the share code provided by Tableau. Below are 
the steps to retrieve the code

{{< head 2 "Adding the ShortCode to your Hugo Site" >}}

{{< big T >}}o add support for embedding Tableau Public vizzes simply copy {{< link "https://gist.github.com/hobelinm/de089f99c3543e2a16f8f24fee4d958e" "our shortcode" >}} into the following 
path `/layouts/shortcodes/tableau.html`. To embed a viz to your website on your markdown post you need to add the following code wherever you want to embed your viz. The next section 
will show how to get the code from Tableau Public and then we can use that code to parse out the parameters

`{{` `< tableau "viz1595830498772" "Hi" "HikeCollection" "Hikes">` `}}`
{{< caption "Code used to embed a Tableau Public viz" >}}

The code above will create the following result:

{{< tableau "viz1595830498772" "Hi" "HikeCollection" "Hikes" >}}
{{< caption "Rendered Viz from the code above" >}}
{{< break >}}


{{< head 2 "Obtaining the Share Code" >}}

{{< big T >}}o obtain the sharing code from Tableau Public simply go to the viz you want to embed. From the toolbar on the bottom right there is a share button

{{< customimg src="/images/content/projects/software/tableauparser/sharebtn.jpg" caption="Tableau Public Share Button" >}}

Clicking on the share button brings the share dialog which has two fields, the first one labelled `Embed Code` is the one we'll be using, copy this field's data since you will need it 
for the form below (more on this later)

{{< customimg src="/images/content/projects/software/tableauparser/embedcode.jpg" caption="Sample code to embed a viz" >}}

The code copied will look like the sample below

{{< gist hobelinm 67b27751b6d1a6373f1ae09d4e8a3eb3 >}}
{{< caption "Sample Code to Embed a Tableau Viz" >}}

{{< head 2 "Extracting Data for our ShortCode" >}}

{{< big W >}}ith the embed code copied we can now use it to extract the info we need for our shortcode, simply paste the code into the input box below. This form will extract four fields from 
the shared code:
- Viz ID
- Viz Prefix Field
- Workbook Name
- Worksheet Name

These are used for our shortcode, alternatively you can simply copy the code in the last field and use it directly in our markdown

{{< tableauparser >}}
{{< caption "Embedded Viz" >}}

{{< unsplash "no2blvVYoJw" "claybanks" "Unsplash: Tableau Viz" >}}
{{< scrolltop >}}

{{< pageStats >}}
