# Chibi Planner

A LaTeX/Overleaf-managed reconstruction of the Chibi Cat Digital Planner.

## Build modes

This repo now contains two versions:

1. **Pixel-perfect source-backed planner** — `main.tex`
   - Uses the original PDF pages as full-page LaTeX backgrounds.
   - This is the closest possible visual recreation because it preserves the exported Canva artwork exactly.
   - Best for printing, sharing, and maintaining a faithful PDF from Overleaf/GitHub Actions.

2. **Editable TikZ reconstruction** — `editable-reconstruction.tex`
   - Rebuilds the planner with LaTeX/TikZ templates.
   - Easier to modify structurally, but not pixel-perfect.
   - Useful as a starting point for replacing page backgrounds with fully editable elements over time.

## Build on Overleaf

Upload/import the repository and compile `main.tex` for the pixel-perfect version.

To work on the editable approximation, set Overleaf's main document to:

```text
editable-reconstruction.tex
```

## Local build

With a full TeX installation:

```bash
latexmk -pdf main.tex
```

Or with Docker:

```bash
docker run --rm -v "$PWD:/work" -w /work ghcr.io/xu-cheng/texlive-full:latest \
  latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
```

## Files

- `main.tex` — pixel-perfect source-backed planner
- `editable-reconstruction.tex` — editable TikZ reconstruction
- `tex/planner-style.tex` — reusable TikZ styles/templates
- `tex/planner-pages.tex` — editable reconstruction page order
- `source/chibi-cat-digital-planner.pdf` — source page artwork used by `main.tex`
- `docs/page-map.md` — page structure notes

## Notes

The pixel-perfect version is faithful because it embeds the source pages. The editable reconstruction remains available for gradual conversion into editable LaTeX components.
