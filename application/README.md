# CEBE Interdisciplinary Fellowship — application (proposal + CVs)

This folder holds the *actual* proposal and CVs being submitted for the
call (call closes **30 Sept 2026**). The reusable structure/formatting
templates live in `../templates/` — this folder is where real content
goes.

## Naming convention

- The proposal: `main-*.tex`, e.g. `main-cebe2026.tex` (any name other
  than `main-template.tex`, which stays in `../templates/`).
- CVs: `cv-*.tex`, one file per person, e.g. `cv-pi.tex`,
  `cv-cosupervisor-jhonattan.tex`, `cv-cosupervisor-carolin.tex`,
  `cv-cosupervisor-ueli.tex`, `cv-candidate-lorenzo.tex`.
- `references.bib` — the real, growing bibliography cited in the
  proposal (distinct from the stub bib in `../templates/`).

See `../AGENTS.md` for the full naming/role convention, including the
reviewer role and the standing "please update all templates" / "please
give me feedback on the application" commands.

## Getting started

To start the proposal or a CV, copy the corresponding template from
`../templates/` into this folder under one of the names above, e.g.:

```
cp ../templates/main-template.tex main-cebe2026.tex
cp ../templates/cv-template.tex cv-pi.tex
```

Once files exist here, "please update all templates" will keep their
structure/formatting in sync with `../templates/` as the templates
evolve, without touching the content you've written.

## Building

Same as the templates (see `../templates/README.md`), run against the
real file names here, e.g.:

```
latexmk -pdf main-cebe2026.tex
latexmk -pdf cv-pi.tex   # repeat per CV
```

## Checking page limits

Same mechanism as the templates — see `../templates/README.md` for the
`[Target length: ...]` annotations and the `\templatenotesfalse` toggle
to hide them before the final submission build. After compiling:

```
grep PAGEMARK main-cebe2026.log
grep PAGEMARK cv-pi.log
```

## Assembling the submission PDF

The call requires **one single PDF**: frontpage + proposal + all CVs, in
that order. Once every file is compiled to its own PDF, merge them
(`pdfunite` on Linux/WSL, or `pdftk`):

```
pdfunite main-cebe2026.pdf cv-pi.pdf cv-cosupervisor-jhonattan.pdf \
  cv-cosupervisor-carolin.pdf cv-cosupervisor-ueli.pdf \
  cv-candidate-lorenzo.pdf submission.pdf
```

Submit `submission.pdf` via the EasyChair portal linked from www.cebe.dk.

## Build artifacts

LaTeX build byproducts (`.aux`, `.log`, `.bbl`, `.fls`, `.fdb_latexmk`,
`.toc`, ...) are already covered by the repo's root `.gitignore`.
