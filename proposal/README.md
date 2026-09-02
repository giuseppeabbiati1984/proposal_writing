# CEBE Interdisciplinary Fellowship — proposal LaTeX template

Matches the formatting and structure required by the CEBE Interdisciplinary
Fellowship Programme call (PhD/Postdoc), call closes **30 Sept 2026**.

## Files

- `main.tex` — the project proposal itself: frontpage, table of contents,
  Project Summary, Project Description (with the exact required
  subheadings), Project relevance to CEBE research fields, Sustainability
  goals.
- `cv-template.tex` — a single CV template. Copy it once per person
  (`cv-pi.tex`, `cv-cosupervisor1.tex`, `cv-candidate.tex`, ...) and fill
  each in separately — max 2 pages per the call.
- `references.bib` — bibliography for citations used in `main.tex`
  (via natbib: `\citep{key}` / `\citet{key}`).

## Formatting compliance

- 12 pt, single-spaced, 2.5 cm margins — set in the preamble of both
  `.tex` files, do not change.
- Font: uses `mathptmx`, a Times-metric-compatible font bundled with every
  TeX distribution, so it compiles identically on Windows/MiKTeX,
  Overleaf, and Linux without needing font files. If you specifically
  want the literal Times New Roman TTF (available on this Windows
  machine), compile with **XeLaTeX** instead and swap in `fontspec` +
  `\setmainfont{Times New Roman}` — see the comment block at the top of
  `main.tex`.

## Building

With `latexmk` (recommended — handles the bibtex re-run automatically):

```
latexmk -pdf main.tex
latexmk -pdf cv-template.tex   # repeat per CV copy
```

Or manually:

```
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

## Checking page limits

The call enforces hard maxima per section:

| Section | Limit |
|---|---|
| Project Summary | 1/2 page |
| Project Description | 4 pages (excluding references) |
| Project relevance to CEBE research fields | 1/2 page |
| Sustainability goals | 1/2 page |
| Each CV | 2 pages |

Each section in `main.tex` and `cv-template.tex` is bracketed by a
`\pagemark{...}` marker that prints to the compile log. After building,
check where each section starts/ends:

```
grep PAGEMARK main.log
grep PAGEMARK cv-template.log
```

## Assembling the submission PDF

The call requires **one single PDF**: frontpage + proposal + all CVs, in
that order. Once every file is compiled to its own PDF, merge them
(`pdfunite` on Linux/WSL, or `pdftk`):

```
pdfunite main.pdf cv-pi.pdf cv-cosupervisor1.pdf cv-candidate.pdf submission.pdf
```

Submit `submission.pdf` via the EasyChair portal linked from www.cebe.dk.

## Build artifacts

LaTeX build byproducts (`.aux`, `.log`, `.bbl`, `.fls`, `.fdb_latexmk`,
`.toc`, ...) are already covered by the repo's root `.gitignore`.
