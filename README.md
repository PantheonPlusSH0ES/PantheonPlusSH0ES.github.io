# Simplest GitHub Page

Test of simplest GitHub page, leveraging Jekyll without Jekyll.

View at [https://christophera.github.io/simplest-github-page/](https://christophera.github.io/simplest-github-page/)

Repo at [https://github.com/ChristopherA/simplest-github-page/](https://github.com/ChristopherA/simplest-github-page/)

## Goals

* Without using Jekyll, Ruby or Gem, leverage the various files that allow you to use markdown directly within github pages.
* Pages should largely look the same when rendered from the GitHub repo page and from the git
* Leverage the default [Jekyll Primer](https://github.com/pages-themes/primer) theme's CSS without the using the full theme.
* Support internal anchor link tags

## Using This
* [ ]  Copy these files in this repo to your own github
* [ ]  In your repo, turn on github pages for 'master'
* [ ]  Do not select a theme.
* [ ]  Edit the `_config.yml` with your own info
* [ ]  Edit the `/assets/css/style.css` for your own styles
* [ ]  Edit the `/_layouts/default.html` file for the default html template.
## Notes
* This technique will force Github to default to the CSS used by the [Primer Theme](https://github.com/pages-themes/primer), which is is the default Github theme if you do not select a theme, however, note that this theme is not among GitHub's standard theme choices, so you can't return to it if you pick a different theme.
* Github will render raw URLs as links, but you must use proper markdown construction for it to work on pages
* I've not been able to get the `_posts` feature to work without using Jekyll itself. The supposedly should work, but doesn't.
* If you do a relative link to a markdown file without the extension, it will be rendered in html correctly, for example relative [./sample](./sample). Unfortunately, when rendered in Github the relative link will give a 404 error. To preserve compatiblity of both, if use use the `.md` extension in the relative link — it will render correctly in both html and gihub and both will function as links to the correct place, for example see [./sample.md](./sample.md). You do not need to do this with `/` which will render `README.md` as `index.html`
* You can create other `_layouts/` templates, and have pages use them by adding this yaml frontmatter to the top of the page:
  ```
  ---
  layout: templatename
  ---
  ```
* You can have pages that will not be rendered as web pages by adding this yaml frontmatter to the top of the page:
```
  ---
  published: false
  ---
  ```
* You can display a github avatar `\{% avatar [USERNAME] %}` {% avatar [ChristopherA] %}
