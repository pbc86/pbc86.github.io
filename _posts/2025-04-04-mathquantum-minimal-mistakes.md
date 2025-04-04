---
date: 2025-04-04
title: MathQuantum's tutorial on Minimal Mistakes
published: true
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Jekyll
  - blog
  - Minimal Mistakes
  - MathQuantum
  - tutorial
---

This is my notes taken while following instructions from [Build your professional webpage - Tutorial](https://www.youtube.com/watch?v=Pof342wGt78&t=605s) by MathQuantum.

### Step 1: Creating page and copy template 

- Create your GitHub account
- Then go to https://github.com/mmistakes
- Click on "Use this template"
- Name your repo as `<your_account.github.io>`

### Step 2: Replace bio image
- Replace bio image: Upload a bio image into assets/images then update `avatar : "/assets/images/new_bio_image.jpg"` in _`config.yml`
- Update other values in `_config.yml`:
  ```
  title: Trumpian taxonomy
  email: # leave it blank 
  description: >- # this means to ignore newlines until "baseurl:"
  
  # twitter_username: username # comment it out
  github_username: pbc86
  minimal_mistakes_skin: dark

  author:
  name   : "Cau Pau"
  avatar : "/assets/images/cau.jpg"
  bio    : "Minimal mistakes theme on the most significant tariff mistakes"

  ```  
- MathQuantum suggests to update `index.html` to `index.md`. It's a good idea so you can update the index file easily without too much html.

### Step 3: Landing page and navigation menu
- Change `layout: single` in `index.md` from (`layout: home`) so it won't show the blog posts. (I skipped this step)
- Markdown syntax: **bold**, *italic*, heading, etc... For further reference, see [Markdown Guide](https://www.markdownguide.org),
- Update `_data/navigation.yml': 
- Change the `title` and `url` for instance:
  ```
  - title: "Presentations"
    url: /presentations/
  ```
- Create / rename file in `_pages` to match `url`, for instance: `presentations.md`.
- In the front matter, make sure that `permalink` is pointed to the `url`, for instance:
  ```
  ---
  permalink: /presentations/
  title: "Presentations"
  ---
  ```
  Note that the value of `url` key will be the same as `permalink` and there is no hyphen before the `title`.
 
### Step 4: Embed video and pdf file
- Insert Youtube video:
  - click Share button
  - select Embed
  - then just copy the code in `<iframe>` tag that Youtube created.
  <br>
- Insert pdf file in Google Drive.
  - open the pdf file and Share it.
  - click three dots and select  "Open in new window"
  - in new window, click the three dots again and select "Embeded item ..."
  - copy the code in `<iframe>` tag

> _Note: not to worry if Review doesn't show the embeded files properly._

See an example of the above [here:](https://pbc86.github.io/about/)

### Step 5: Beyond tutorials
- Mathematical expressions: MathQuantum mentioned it but did not explain how to do it.
  - Option 1: I found a solution that works for me:
    - Create `_includes/head/custom.html`
    - Add relevant scripts. See my `custom.html` for script.
  - Option 2: from MathQuantum's response to my comment on his video. I will test this later.
    - [How to render math equations on your Minimal Mistakes](https://www.cross-validated.com/How-to-render-math-on-Minimal-Mistakes/)
- Favico:
  - Favico should be square as svg file needs to be square.
  - Create and download favico images at <https://realfavicongenerator.net/> into `assets/images`
  - Copy code from the above into `_includes/head/custom.html`
  - Good reference [Adding a favicon to a Jekyll-based static website](https://peateasea.de/add-favicon-to-mm-jekyll-site/)
- How to hide a post: add `published: false` to the front matter

