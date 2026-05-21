# Iron Planner

A masculine, editable LaTeX/TikZ redesign of the original Chibi Planner layout.

This repository was created as a separate GitHub project so the previous `chibi-planner` work remains untouched.

## Theme

The layout remains the same planner structure, but the visual language has been reforged:

- charcoal and gunmetal backgrounds
- brass/copper accent rules
- parchment writing panels
- sharper geometric ornaments instead of soft pastel decorations
- cleaner print-oriented panels with reduced visual noise
- stronger divider pages with plaque-style section titles
- wolf/shield crest cover art in place of the chibi cat motif

## Build

Compile the editable TeX planner:

```bash
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
```

Or with Docker:

```bash
docker run --rm -v "$PWD:/work" -w /work ghcr.io/xu-cheng/texlive-full:latest \
  latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
```

## Files

- `main.tex` — editable Iron Planner build
- `tex/planner-style.tex` — theme, drawing macros, panels, cover art, ornamentation
- `tex/planner-pages.tex` — page order and planner layout
- `editable-reconstruction.tex` — original editable reconstruction entrypoint retained for reference
- `source/chibi-cat-digital-planner.pdf` — original source PDF retained for comparison/reference

## Original work

Original repository: <https://github.com/alienvisa/chibi-planner>

This repository intentionally does not overwrite that work.
