# Quarto Conversion Report

## Scope

This isolated project converts the current MS Emon Jekyll presentation layer into a Quarto website. No files were pushed to GitHub and no deployment was performed.

## Converted structure

| Jekyll | Quarto | Notes |
|---|---|---|
| `_config.yml` | `_quarto.yml` | Site metadata, HTML output, stylesheet, and shared includes |
| `_layouts/default.html` | `_includes/header.html`, `_includes/footer.html`, `assets/styles.css` | Shared shell and visual system split into Quarto-compatible files |
| `index.md` | `index.qmd` | Homepage content converted to Quarto Markdown with raw HTML components |
| `about.md` | `about.qmd` | Static About page |
| `research.md` | `research.qmd` | Empty-ready Research archive page |
| `analytics.md` | `analytics.qmd` | Empty-ready Analytics page |
| `search.md` | `search.qmd` | Search landing page retained as an empty-ready Quarto page |
| `_data/navigation.yml` | Header/footer navigation markup | Quarto navigation is explicit in the shared includes |

## Important differences

Jekyll Liquid expressions such as `site.posts`, `where_exp`, and `jsonify` do not run in Quarto. Because the current repository has no published research posts, the conversion uses static empty-ready archive pages. Future posts can be added as Quarto documents and linked manually, or a Quarto listing can be introduced when the content model is finalized.

The extracted stylesheet preserves the current visual language, but Quarto adds its own document wrapper and generated HTML metadata. The site should therefore receive a visual review after rendering, especially around page title handling, code-generated wrappers, and responsive header behavior.

## Validation status

The file inventory, YAML/front-matter delimiters, shared include paths, links, and HTML structure were checked programmatically. A native Quarto render could not be run in this environment because the Quarto CLI is not installed. No GitHub push or deployment was attempted.

## Review questions

Before adopting this as the repository’s primary codebase, decide whether future content should use ordinary `.qmd` pages, a Quarto listing-based blog, or a hybrid of pages and computational documents. This choice affects search indexing, categories, navigation, and URL compatibility.
