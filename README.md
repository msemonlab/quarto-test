# MS Emon — Quarto Preview

This directory is an isolated Quarto conversion of the current MS Emon Jekyll site. It is prepared for review only; it has not been pushed or deployed.

## Project structure

The shared header and responsive navigation live in `_includes/header.html`. The shared footer and theme/menu behavior live in `_includes/footer.html`. The visual system was extracted into `assets/styles.css`. Homepage and static sections are represented by `index.qmd`, `about.qmd`, `research.qmd`, `analytics.qmd`, and `search.qmd`.

## Local preview

Install [Quarto](https://quarto.org/docs/get-started/) and run:

```bash
quarto preview
```

To generate static output:

```bash
quarto render
```

The generated site will be placed in `_site/`.

## Current limitation

The Jekyll source contained Liquid-based post loops. Since the repository currently has no research or article posts, this first conversion keeps those sections static and ready for future content. A later content-model decision is needed before implementing Quarto listings, RSS, search indexing, or legacy URL redirects.

Preview workflow trigger: this repository is configured to render and deploy through GitHub Actions when `main` changes.
