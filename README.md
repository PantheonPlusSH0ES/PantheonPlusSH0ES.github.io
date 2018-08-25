Test of simplest GitHub page, leveraging Jekyll without Jekyll.

View at https://christophera.github.io/simplest-github-page/

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
* The H1 rendered the top of the html comes from the setting in `_config.yml` does not appear in the github rendered page.
* Github will render raw URLs as links, but you must use proper markdown construction for it to work on pages


