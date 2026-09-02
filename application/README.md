# CEBE Interdisciplinary Fellowship — application (proposal + CVs)

This folder holds the *actual* proposal and CVs being submitted for the
call (call closes **30 Sept 2026**). The reusable structure/formatting
templates live in `../templates/` — this folder is where real content
goes.

## Naming convention

- The proposal: `main-*.tex`, e.g. `main-cebe2026.tex` (any name other
  than `main-template.tex`, which stays in `../templates/`).
- CVs: `CV-<GivenName>.tex`, one file per person. The five expected
  files (already instantiated from `cv-template.tex`, see
  `../AGENTS.md`): `CV-Giuseppe.tex`, `CV-Jhonattan.tex`,
  `CV-Carolin.tex`, `CV-Ueli.tex`, `CV-Lorenzo.tex`.
- `references.bib` — the real, growing bibliography cited in the
  proposal (distinct from the stub bib in `../templates/`).

See `../AGENTS.md` for the full naming/role convention, including the
reviewer role and the standing "please update all templates" / "please
give me feedback on the application" commands.

## Getting started

To start the proposal, copy the template from `../templates/` into
this folder under a name of your own choosing, e.g.:

```
cp ../templates/main-template.tex main-cebe2026.tex
```

The five CVs already exist under the names above; to add a CV for
someone not yet on the team, copy the template the same way, e.g.:

```
cp ../templates/cv-template.tex CV-NewPerson.tex
```

Once files exist here, "please update all templates" will keep their
structure/formatting in sync with `../templates/` as the templates
evolve, without touching the content you've written.

## Building

Same as the templates (see `../templates/README.md`), run against the
real file names here, e.g.:

```
latexmk -pdf main-cebe2026.tex
latexmk -pdf CV-Giuseppe.tex   # repeat per CV
```

## Checking page limits

Same mechanism as the templates — see `../templates/README.md` for the
`[Target length: ...]` annotations and the `\templatenotesfalse` toggle
to hide them before the final submission build. After compiling:

```
grep PAGEMARK main-cebe2026.log
grep PAGEMARK CV-Giuseppe.log
```

## Assembling the submission PDF

The call requires **one single PDF**: frontpage + proposal + all CVs, in
that order. Once every file is compiled to its own PDF, merge them
(`pdfunite` on Linux/WSL, or `pdftk`):

```
pdfunite main-cebe2026.pdf CV-Giuseppe.pdf CV-Jhonattan.pdf \
  CV-Carolin.pdf CV-Ueli.pdf CV-Lorenzo.pdf submission.pdf
```

Submit `submission.pdf` via the EasyChair portal linked from www.cebe.dk.

## Build artifacts

LaTeX build byproducts (`.aux`, `.log`, `.bbl`, `.fls`, `.fdb_latexmk`,
`.toc`, ...) are already covered by the repo's root `.gitignore`.
