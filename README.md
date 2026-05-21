# Chibi planner

Editable LaTeX recreation of the **Chibi Cat Digital Planner** layout for Overleaf and other LaTeX editors.

## What this repo contains

- `main.tex` — complete planner document.
- `tex/planner-style.tex` — reusable TikZ/LaTeX layout macros, colors, grids, headers, and section boxes.
- `tex/planner-pages.tex` — page sequence and page-specific content.
- `.github/workflows/build.yml` — GitHub Actions PDF build.

## Build locally

Install a reasonably complete LaTeX distribution, then run:

```bash
latexmk -pdf main.tex
```

If `latexmk` is unavailable:

```bash
pdflatex main.tex
pdflatex main.tex
```

The compiled PDF will be `main.pdf`.

## Use on Overleaf

1. Create a new Overleaf project.
2. Upload `main.tex` and the `tex/` folder.
3. Set the compiler to **pdfLaTeX**.
4. Compile.

## Editing guide

- Change colors in `tex/planner-style.tex` under `\definecolor`.
- Add/remove planner pages in `tex/planner-pages.tex`.
- Most page templates are built from reusable commands such as:
  - `\weeklyplannerpage`
  - `\mealplannerpage`
  - `\selfcarepage`
  - `\medicationpage`
  - `\dailyplannerpage{Monday}`
  - `\trackerpage{Water Tracker}`

## Notes

This is a clean editable LaTeX reconstruction, not a pixel-perfect PDF trace. The structure, pastel chibi style, planner sections, tables, and editable text are recreated with LaTeX/TikZ so the planner can be maintained as source code.
