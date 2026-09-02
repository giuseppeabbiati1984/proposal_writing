# CEBE Interdisciplinary Fellowship — LaTeX templates

Matches the formatting and structure required by the CEBE Interdisciplinary
Fellowship Programme call (PhD/Postdoc), call closes **30 Sept 2026**.

This folder holds the *templates* only. The actual proposal and CVs being
submitted live in `../application/` — see `../application/README.md` to
get started, and `../AGENTS.md` for the full naming convention and the
"please update all templates" workflow that keeps files in `application/`
in sync with these templates.

## Files

- `main-template.tex` — the project proposal template: frontpage, table
  of contents, Project Summary, Project Description (with the exact
  required subheadings), Project relevance to CEBE research fields,
  Sustainability goals.
- `cv-template.tex` — the CV template.
- `references.bib` — a minimal stub bibliography, only so this template
  compiles standalone for testing. The real, growing bibliography lives
  at `../application/references.bib`.

## Formatting compliance

- 12 pt, single-spaced, 2.5 cm margins — set in the preamble of both
  `.tex` files, do not change.
- Font: uses `mathptmx`, a Times-metric-compatible font bundled with every
  TeX distribution, so it compiles identically on Windows/MiKTeX,
  Overleaf, and Linux without needing font files. If you specifically
  want the literal Times New Roman TTF (available on this Windows
  machine), compile with **XeLaTeX** instead and swap in `fontspec` +
  `\setmainfont{Times New Roman}` — see the comment block at the top of
  `main-template.tex`.

## Building (to preview/test the template itself)

With `latexmk` (recommended — handles the bibtex re-run automatically):

```
latexmk -pdf main-template.tex
latexmk -pdf cv-template.tex
```

Or manually:

```
pdflatex main-template.tex
bibtex main-template
pdflatex main-template.tex
pdflatex main-template.tex
```

The same commands apply in `application/`, just run against the real
file names there (e.g. `latexmk -pdf main-cebe2026.tex`).

## Checking page limits

Each page-limited section also shows a small `[Target length: ...]` note
in the compiled PDF itself, right under its heading, so the limit is
visible while drafting. These notes are template scaffolding, not
proposal content — before the final submission build, hide them by
setting `\templatenotesfalse` near the top of each `.tex` file's
preamble (default is `\templatenotestrue`).

The call enforces hard maxima per section:

| Section | Limit |
|---|---|
| Project Summary | 1/2 page |
| Project Description | 4 pages (excluding references) |
| Project relevance to CEBE research fields | 1/2 page |
| Sustainability goals | 1/2 page |
| Each CV | 2 pages |

Each section in `main-template.tex` and `cv-template.tex` is bracketed by
a `\pagemark{...}` marker that prints to the compile log. After building,
check where each section starts/ends:

```
grep PAGEMARK main-template.log
grep PAGEMARK cv-template.log
```

## Build artifacts

LaTeX build byproducts (`.aux`, `.log`, `.bbl`, `.fls`, `.fdb_latexmk`,
`.toc`, ...) are already covered by the repo's root `.gitignore`.
