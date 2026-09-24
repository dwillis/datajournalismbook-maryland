# Data Journalism with R and the Tidyverse

Course site for data journalism at the University of Maryland, built with [Quarto](https://quarto.org).

## How publishing works

- The site is a Quarto **website**. Only the pages listed under `project: render:` in `_quarto.yml` are built. When you add or remove a chapter, update that list *and* the `website: sidebar:` list.
- `execute: freeze: auto` means R code runs only when you render locally and only for pages whose source changed. The results are stored in `_freeze/`, which **must be committed**.
- Pushing to `main` runs `.github/workflows/publish.yml`, which renders from `_freeze/` (no R needed) and deploys to GitHub Pages.

## Editing a chapter

1. Edit the `.qmd` file.
2. Render locally, either with the RStudio **Render** button or with `quarto render chapter.qmd` (`quarto preview` for live reload).
3. Commit the `.qmd` **and** the updated files in `_freeze/`.

If you push a changed `.qmd` without its updated `_freeze/`, the CI build will fail, because it can't run R.

## API keys

Chapters that call the Census and Groq APIs read keys from environment variables. Put these in `~/.Renviron`; never write keys into a chapter:

```
CENSUS_API_KEY=...
GROQ_API_KEY=...
```

## Labs

`labs/` and `pre_labs/` hold class assignments. They are not part of the website build.
