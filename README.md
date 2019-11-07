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
* [ ]  Edit the `/_layouts/default.html` file to change default html template.
* [ ]  Add to `/_layouts/default.html` template any inline styles you wish to override.

## Notes
* This technique will force Github to default to the CSS used by the [Primer Theme](https://github.com/pages-themes/primer), which is is the default Github theme if you do not select a theme, however, note that this theme is not among GitHub's standard theme choices, so you can't return to it if you pick a different theme.
* I've not been able to get the `_posts` feature to work without using Jekyll itself. The supposedly should work, but doesn't.
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

### Displays correctly both Web View and in GitHub View

### Displays correctly both Web View and in GitHub View, but requires proper formatting
* Github will render raw URLs as links, but you must use proper markdown construction `[linkname](link)` for URLs to display propery in the Web View.
* If you do a relative link to a markdown file without the extension, it will be rendered in html correctly, for example relative [./sample](./sample). Unfortunately, when rendered in Github the relative link will give a 404 error. To preserve compatiblity of both, if use use the `.md` extension in the relative link — it will render correctly in both html and gihub and both will function as links to the correct place, for example see [./sample.md](./sample.md). You do not need to do this with `/` which will render `README.md` as `index.html`

### Displays correctly in Web View, but look different (but is acceptable) in GitHub View
* HTML Components such as Buttons (for instance <a class="btn mr2" href="#url" role="button">Link Button</a> & <a class="btn btn-sm" href="#url" role="button">Small Link Button</a> will render as buttons on in the WebView, but as links in the GitHub view. More information on other HTML components available at [https://primer.style/css/components](https://primer.style/css/utilities/box-shadow)
* HTML Divs such as boxes can be useful in Web View, but don't display in GitHub. The can be make to look acceptable in both using tricks like a blockquote tag. More information on other HTML divs such as boxes available at [https://primer.style/css/utilities/box-shadow](https://primer.style/css/utilities/box-shadow)
<blockquote>
<div class="col-6">
  <div class="Box box-shadow">
    <div class="Box-row">
      <h3 class="m-0">Box Header</h3>
    </div>
    <div class="Box-row">
      <p class="mb-0 text-gray">
        Box body text, such as the quick brown fox jumped over the lazy dog.
      </p>
    </div>
    <div class="Box-row">
      <a class="btn btn-primary btn-block" href="#url" role="button" name="Box Link Button">A Box Button Link</a>
    </div>
  </div>
</div>
</blockquote>

### Displays correctly in Web View, but on in GitHub View
* You can display a github avatar {% avatar ChristopherA %} in the Web View but is ugly in the Github View.



