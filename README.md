# Leonardo Oña — academic website

A small GitHub Pages/Jekyll site with a local stylesheet and system fonts.

## Local preview

Install Ruby and Bundler, then run:

```sh
bundle install
bundle exec jekyll serve
```

Open the local address printed by Jekyll. To generate the static site:

```sh
bundle exec jekyll build
```

GitHub Pages continues to use the existing publishing configuration; this
redesign does not change the publishing branch or enable automatic merging.

## Editing

- Home, About and Contact are HTML pages with Jekyll front matter.
- The common header, navigation, footer and SEO integration are in
  `_layouts/default.html`.
- Colours, typography, spacing and responsive layouts are in
  `assets/css/site.css`.
- Contact email and academic profile URLs are in `_config.yml`.
- People are maintained in `_data/people.yml`, with portrait paths and
  dimensions in `_data/portraits.yml`.
- Update the dated Wiko affiliation in Home, Contact and People when the
  fellowship ends. The current dates were verified from Wiko's official profile.
- A page can opt into MathJax by adding `math: true` to its front matter.
  None of the current four pages needs it. There is no site-wide JavaScript
  dependency, remote font or icon library.

Original images remain at their existing repository paths. The displayed
portraits use smaller local derivatives; no profile or education entry has
been discarded. See `ASSETS.md` for the new photograph's licence and map source,
and `VALIDATION.md` for completed checks and remaining review work.
