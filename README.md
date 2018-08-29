Test of simplest GitHub page, leveraging Jekyll without Jekyll.

View at https://christophera.github.io/simplest-github-page/

This technique will force Github to default to the [Primer Theme](https://github.com/pages-themes/primer), which is is the default if you do not select a theme, however, this theme is not among GitHub's standard theme choices.

## Goals

* Without using Jekyll, leverage the various files that allow you to use markdown directly with github pages.
* Pages should largely look the same when rendered from the GitHub repo page and from the git
* Leverage the default Jekyll Primer theme.

## Using This
* [ ] Copy these files in this repo to your own github
* [ ] In your repo, turn on github pages for 'master'
* [ ] Do not select a theme.
* [ ] Edit the `_config.yml` with your own info
* [ ] Edit the `/assets/css/style.css` for your own styles
* [ ] Edit the `/_layouts/default.html` file for the default html template.
* [ ] You can create other `_layouts/` templates, and have pages use them by adding this yaml frontmatter to the top of the page:
  ```
  ---
  layout: templatename
  ---
  ```

## Notes
* Github will render raw URLs as links, but you must use proper markdown construction for it to work on pages
* If you do a relative link to a markdown file without the extension, it will be rendered in html correctly, for example relative [./sample](./sample). Unfortunately, when rendered in Github the relative link will give a 404 error. To preserve compatiblity of both, if use use the `.md` extension in the relative link — it will render correctly in both html and gihub and both will function as links to the correct place, for example see [./sample.md](./sample.md). You do not need to do this with `/` which will render `README.md` as `index.html`
  


