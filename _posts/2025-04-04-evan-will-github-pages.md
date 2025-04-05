---
date: 2025-04-04
title: Evan Will's Go Go Github Pages
published: true
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Jekyll
  - blog
  - Minima
  - Evan Will
  - tutorial
---

Evan Will's instructions [Introduction to Creating Websites with GitHub Pages and Jekyll](https://evanwill.github.io/go-go-ghpages-b/)
are comprehensive. There are videos on Youtube as well but I prefer texts over videos. 

I won't repeat what can be read on Evan's website, just make a few notes:

1. Typo error: Evan did a very good job with his website. However, it's noticed that there is one typo error in the name of the .csv file. It should have been plural animal**s**.csv. 

> ### Create _data
> To add some example data to our blog, let’s manually create a CSV:

> On your repository’s home page, click the “Add file” button and select “Create new file”.
> Type your new data filename: _data/animal.csv

Later on, there a pieces of code refering to animals.csv as seen below. These pieces of code didn't work until the error is fixed.

> ``` 
> {% for animal in site.data.animals %}
> {% endfor %} 
> ```