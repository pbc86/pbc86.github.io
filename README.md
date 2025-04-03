# My notes

This is my notes taken while following instructions from [Build your professional webpage - Tutorial](https://www.youtube.com/watch?v=Pof342wGt78&t=605s) by MathQuantum.

### Step 1: Creating page and copy template 

- Create your GitHub account
- Then go to https://github.com/mmistakes
- Click on "Use this template"
- Name your repo as <your_account.github.io>

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

### Step 5:
- Mathematical expressions: he mentioned it but did not explain how to do it. I found a solution:
  - Create `_includes/head/custom.html`
  - Add relevant scripts. See my `custom.html` for script.
- Favico:
  - Create and download favico images at <https://realfavicongenerator.net/> into `assets/images`
  - Copy code from the above into `_includes/head/custom.html`

---
Notes:
1. How to hide a post: add `published: false` to the front matter


---
# Minimal Mistakes remote theme starter

Click [**Use this template**](https://github.com/mmistakes/mm-github-pages-starter/generate) button above for the quickest method of getting started with the [Minimal Mistakes Jekyll theme](https://github.com/mmistakes/minimal-mistakes).

Contains basic configuration to get you a site with:

- Sample posts.
- Sample top navigation.
- Sample author sidebar with social links.
- Sample footer links.
- Paginated home page.
- Archive pages for posts grouped by year, category, and tag.
- Sample about page.
- Sample 404 page.
- Site wide search.

Replace sample content with your own and [configure as necessary](https://mmistakes.github.io/minimal-mistakes/docs/configuration/).

---

## Troubleshooting

If you have a question about using Jekyll, start a discussion on the [Jekyll Forum](https://talk.jekyllrb.com/) or [StackOverflow](https://stackoverflow.com/questions/tagged/jekyll). Other resources:

- [Ruby 101](https://jekyllrb.com/docs/ruby-101/)
- [Setting up a Jekyll site with GitHub Pages](https://jekyllrb.com/docs/github-pages/)
- [Configuring GitHub Metadata](https://github.com/jekyll/github-metadata/blob/master/docs/configuration.md#configuration) to work properly when developing locally and avoid `No GitHub API authentication could be found. Some fields may be missing or have incorrect data.` warnings.
