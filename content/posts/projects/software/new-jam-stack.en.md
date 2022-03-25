---
title: "New Jam Stack"
date: 2020-04-19T17:24:25-07:00
draft: false
author: Hugo Belin
featured_image: '/images/BrewingCatsMain.jpg'
categories: [software]
tags: [software,projects]
description: Thoughts on the migration from Gatsby into Hugo
lang: en
---

{{< big P>}}revious version of {{< link src="https://brewingcats.com" label="brewingcats.com" >}} was built on a different 
{{< link "https://jamstack.org/" "JAM Stack" >}}, in particular a different {{< link "https://www.staticgen.com/" "Static Site Generator" >}}. 
Building {{< link "https://brewingcats.com" "brewingcats.com" >}} on {{< link "https://www.gatsbyjs.org" "Gatsby" >}} on Gatsby brought us a lot of 
experience and allowed us to make use of our knowledge in {{< link "https://reactjs.org/" "React" >}} and apply it to the website. React is core to 
the structure of the site, we also had the opportunity of learning {{< link "https://graphql.org/" "GraphQL" >}} querying system to perform basic operations

{{< big U>}}nfortunatelly there were additional side effects that came with the adoption of Gatsby, I will try to summarize some of the learnings as well as describing 
why the decision of moving to {{< link "https://gohugo.io/" "Hugo" >}}
- Not supported by {{< link "https://www.typescriptlang.org" "TypeScript" >}} by default. Specific starters do support it, however your options are reduced a 
lot since there aren't many
- Site become absolutely dependent on the selected starter. No guarantee on the maintenance of it, while this is an issue that could happen in Hugo, using TypeScript reduced our options and increased the chances of starters with high number of defects or that fall way behind on dependencies
- Overly dependent on npm. While having a dependency management system is useful, having many dependencies increased the chances of having breaking changes 
which unfortunatelly happened often, we were resorted to either stay on potentially unsecure dependencies, or to manually dig around the problems and read 
non-useful console outputs (something greatly improved when we tried Hugo)
- Development comes first, content comes later. Any small customization required an investment, many scenarios were not covered by default. With the little time 
using Hugo we got out-of-the-box support for multiple languages and for Disqus and we got it running with little effort. As for Gatsby, using a TypeScript 
supported starter we had to design custom React components in the case of language we needed extensive layout updates to support it
- Modifications to the selected starter become your own responsibility. Since we had to make several changes to the layout files we ended up having to synchronize 
and resolve dependencies whenever the starter got updated. Hugo does this beautifully by allowing to override starter layout files and more without having to mess 
with the source files and allowing for a clean upgrade
- For this initial relase we are also dropping core TypeScript language (we are probably still going to design libraries in this language and the backend code). 
This relases the team to focus mostly on the contents and leaving code updates and design to be a nice add on for whenever this is required
- Gatsby is React based, everything revolves around React, therefore extending changes requires making your own components even if the changes are simple. That 
coupled with the starters mixing issue mentioned on the second bullet point made our life more difficult. Hugo's lookup order is greatly welcome in this regard, we 
can still use React if we want to by embedding it using a shortcode, we could have multiple react applications running in the same post as well

That being said, Gatsby is still excellent and starters are useful to focus on content given one that fits all your needs. Maintenance might still be an issue 
depending on the selected starter but without heavy modifications it should not be a major problem

![Gatsby vs Hugo](/images/content/New-JAM-Stack.jpg)

{{< big W >}}ith this change we're also taking the opportunity to improve the design of the website as well, in particular we're moving the storage of images. Previously we 
experienced long build times with Gatsby given the amount of images as these are optimized to be progressively loaded (very nice feature), to avoid this we decided 
to host them in a separate subdomain `media.*` which was the wrong decision because of the way we did this. Currently our site is hosted as a GitLab Page which has 
a `Node.js` server on the background, as the number of requests decrease GitLab puts the instance hosting the website to sleep. Getting back from sleeping can take 
up to several seconds. Hosting media content on a separate GitLab page instance caused an initial delay for loading, while the instance becomes warm, requesting 
media from other cold instance caused additional delays hence degrading the experience with posts containing multiple pictures. To address this we're including 
images along with the current website deployment again and we are leveraging Unsplash and Instagram where applicable

{{< head 3 "Next Steps" >}}
We are working on porting all the features as well as to moving all the content over to Hugo, stay tuned :smiley:

{{< scrolltop >}}
{{< pageStats >}}
