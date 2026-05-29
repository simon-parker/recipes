# Recipes

Personal recipe archive published with GitHub Pages.

Site: https://simon-parker.github.io/recipes/

## Project structure

- `_recipes/` — recipe Markdown files
- `_layouts/` — Jekyll layouts
- `index.html` — recipe index, search, tag filtering UI
- `assets/styles.css` — local CSS overrides
- `_config.yml` — Jekyll/GitHub Pages config

## Features

- Recipes are stored as Markdown.
- The index lists every recipe alphabetically.
- Search filters titles, tags, ingredients, and recipe text.
- Tags can be selected from a pill-style multi-select dropdown.
- Search and tag filters are stored in the URL, so refresh/share preserves them.
- Some recipes include English/Russian language toggles.

## Add a recipe

Create a Markdown file in `_recipes/` with front matter:

```md
---
title: Recipe Title
description: Short summary.
tags:
  - tag
---

## Ingredients

## Recipe
```

## Bilingual recipes

For recipes with multiple languages, add `languages` front matter and wrap each language in a section:

```md
---
title: Recipe Title
languages:
  - code: en
    label: English
  - code: ru
    label: Русский
---

<section data-language="en" markdown="1">

## Ingredients

</section>

<section data-language="ru" markdown="1" hidden>

## Ингредиенты

</section>
```

## CSS

The site uses the CSSBed Tufte theme: https://www.cssbed.com/tufte/

Local CSS in `assets/styles.css` handles layout details for the recipe index, filters, compact listing, and language toggle.
