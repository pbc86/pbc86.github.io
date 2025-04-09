---
date: 2025-04-07
title: Jekyll tutorial on Happy Coding by Kevin Workman
published: true
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Jekyll
  - blog
  - Kevin Workman
  - tutorial
---

Kevin has a bunch of tutorials on his [website](https://happycoding.io/). For Jekyll tutorial, go to Tutorials tab, under HTML, you can find his [Jekyll Tutorial](https://happycoding.io/tutorials/html/jekyll).

Remember to add a **dot** (`.`) just before the / to indicate parent folder instead of root. For instance:

```
<link rel="stylesheet" type="text/css" href="./styles.css">
<a href="./index.html">Home</a>
<a href="./contact.html">Contact</a>
<a href="./beach.html">Beach</a>

```

### Timestamps:

24:34 - Creating Beach.html  
26:11 - Creating folder images  
28:03 - Update `css` as file not found when rendering beach.html due to relative path. _Note_: here Kevin use slash to go to "root" folder, but I have to use ./ to go to current folder instead.  
30:10 - Add `permalink` to `Beach.html`, but that isn't ideal.  
30:40 - update `permalink` using **Placeholders** (i.e. from `beach` to `:title`)  
32:30 - create _config.yml file and move the property `permalink`  
33:10 - something broke
35:10 - create `hike.html`  
36:58 - taking index of posts from Jekyll Docs `for post in site.posts` 
42:25 - convert `beach.html` to `beach.md`  
