---
title: jekyll-journy
layout: post
date: 2016-12-28
categories: [tools]
tags:
  - 
---
This post is used to collect all Q&A during I'm using jekyll in in github pages.

# Q: how to embed image in post?
In here, it suggests to put images in folder like /_assets_, then do add the line like:
```
... which is shown in the screenshot below:
![My helpful screenshot]({{ site.url }}/assets/screenshot.jpg)

OR
<img src="{{ site.url }}/assets/something.png">

OR provide a link for downloading something

... you can [get the PDF]({{ site.url }}/assets/mydoc.pdf) directly.

```


