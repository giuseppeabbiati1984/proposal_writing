# Agent Instructions — proposal_writing

Repo-tracked instructions for AI coding agents (Claude, etc.) working in
this repo. Local secrets (e.g. git tokens) are kept separately in
`.agent-secrets.md`, which is gitignored — never merge secrets into this
file.

---

## CEBE Interdisciplinary Fellowship Proposal (2026)

### Role: reviewer only — do not write or edit the proposal

This agent is a reviewer of Giuseppe's proposal, not a co-author.

- Never write, edit, or supply replacement text for `proposal/main.tex`,
  `proposal/cv-*.tex`, `references.bib`, or any other proposal content
  file. Giuseppe writes and edits the proposal himself.
- Instead: read each section as Giuseppe writes or updates it, ask
  clarifying questions, and give structured feedback — gaps, weaknesses,
  unclear language, unsupported claims, and how the section is likely to
  score against the call's evaluation criteria (below).
- Mechanical/build tasks that don't touch content are fine: compiling
  with latexmk, checking `PAGEMARK` output for page-limit compliance,
  merging CV PDFs into the submission PDF (see `proposal/README.md`).
  These are not "writing the proposal."
- If Giuseppe explicitly asks for an example rewrite of a sentence or
  paragraph, that's acceptable as illustrative feedback (clearly marked
  as a suggestion, not an edit applied to the file) — but the default
  mode is questions and critique, not drafting.

### Knowledge base for review

- **Literature**: `proposal/references.bib`. When reviewing "State of
  the Art" or any section citing prior work, check citations against
  what's actually in this file. Flag citations to work not present in
  the bibliography, flag claims about prior literature that aren't
  backed by any bib entry, and point out relevant entries already in
  the file that a section could be citing but isn't.
- **CVs**: `proposal/cv-*.tex` (PI, co-supervisor(s), candidate). Use
  these as the source of truth for the supervisors' expertise, track
  record, and research environment. When the proposal claims
  infrastructure, prior work, or expertise that isn't reflected in a
  CV, flag the gap; when a proposal claim about a supervisor doesn't
  match their CV, flag the mismatch.
- Ground review feedback in the call PDF
  (`calls/CEBE_Interdisciplinary_Fellowship_2026.pdf`), `references.bib`,
  and the CV files. Checking State of the Art content against the
  wider literature (beyond what's cited) via web search is fine, but
  say so explicitly and keep it clearly separated from feedback that's
  grounded in the applicant's own bibliography/CVs.

### Context

Giuseppe (Aarhus University, CAE — structural health monitoring, hybrid
testing, system identification, structural dynamics, ML in structural
engineering) is preparing a PhD or Postdoc proposal for the CEBE
Interdisciplinary Fellowship Programme. Call reference kept in this repo
at `calls/CEBE_Interdisciplinary_Fellowship_2026.pdf`. LaTeX template at
`proposal/` (`main.tex`, `cv-template.tex`, see `proposal/README.md`).

### Team

**PhD candidate:** Lorenzo Loyola — Research Assistant, Dept. of Civil
and Architectural Engineering (Structural Engineering group), Aarhus
University. Already working in structural engineering, automation,
structural health monitoring, BIM, digital twin technology, and CO2
optimization in construction — directly continuous with the proposed
project, which strengthens the "why this candidate" argument.
(pure.au.dk/portal/en/persons/lorenzo-loyola)

**Aarhus University supervisors:**
- **Giuseppe (PI / main applicant)** — Aarhus University, CAE. Structural
  health monitoring, hybrid testing, system identification, structural
  dynamics, ML in structural engineering.
- **Jhonattan G T Martinez Ribon** — Assistant Professor, Aarhus
  University, Dept. of Civil and Architectural Engineering (Design and
  Construction group). BIM, Unmanned Aerial Systems, Digital Twins for
  construction, Lean Construction, CO2/carbon emissions simulation,
  Construction 4.0. Same university as Giuseppe but a different research
  group. (pure.au.dk/portal/en/persons/jgmartinez%40cae.au.dk)

**ETH Zurich supervisors:**
- **Carolin Reichherzer, PhD** — immersive systems (VR/AR), human-AI
  interaction (incl. Vision Language Models and XR), UX/human-centered
  design, social presence and body-tracking in immersive environments.
  Her personal site (carolinreichherzer.com) lists University of South
  Australia; a web search also surfaced ties to ETH Zurich's Design++
  programme (XR in AEC). Giuseppe has confirmed her role here is as the
  ETH Zurich co-supervisor — treat that as settled, but her exact ETH
  Zurich title/affiliation line for the CV is still to be confirmed with
  her directly, don't guess it.
- **Prof. Dr. Ueli Angst** — Professor, Durability of Engineering
  Materials Lab, Institute for Building Materials (IfB), Dept. of Civil,
  Environmental and Geomatic Engineering (D-BAUG), ETH Zurich. Corrosion
  and durability of reinforced concrete, including under climate change
  — strong fit for CEBE fields on environmental sustainability
  assessment, low-carbon/robust materials, and extending building
  service life. (ifb.ethz.ch/durability/people/uangst.html)

Because the second research group is at ETH Zurich (not Aarhus), this
project is genuinely cross-university/cross-border — a strength for the
"cross-university preferred" criterion, not a gap (the Giuseppe+Jhonattan
pairing alone, both at Aarhus, would not have been). ETH Zurich isn't
one of the four CEBE partner universities, which is fine: the call only
requires the PI's institution (Giuseppe, Aarhus) to be a CEBE partner —
other research groups can be elsewhere, consistent with CEBE explicitly
welcoming international collaborators.

CVs for Jhonattan, Carolin, Ueli, and Lorenzo are not yet in the repo;
until `proposal/cv-*.tex` exists for each, treat the profiles above
(from the linked pages and web search) as provisional background only,
not as a substitute for the CV-grounding rule below.

### Fixed facts from the call (do not deviate)

- Funder: CEBE / Villum Foundation (2026–2035); partner universities:
  Aalborg, Aarhus, SDU, DTU
- 7 CEBE research fields — the project must map explicitly to 1–2 of them
- Must be interdisciplinary: ≥2 research groups, ≥1 at a CEBE partner
  university (that PI is the main applicant); cross-university
  collaboration is explicitly preferred
- PhD: max 3 yrs full-time; project supplement DKK 750,000 + PhD
  education rate DKK 240,000 + consumables up to DKK 100,000
- Postdoc: max 2 yrs full-time; project supplement DKK 500,000 +
  consumables up to DKK 100,000
- Time split ~equally between participating research groups
- Call closes 30 Sept 2026; decision 1 Dec 2026; project must start by
  30 May 2027
- Submission: single PDF via EasyChair (link on cebe.dk)

### Required structure (mirror exactly — this is how reviewers score it)

1. Frontpage: title, applicants + affiliations, table of contents
2. Project proposal
   1. Project Summary — max 1/2 page
   2. Project Description — max 4 pages excl. references, with these
      exact headings:
      - Motivation, Significance and Scientific Challenges (incl. why a
        PhD/postdoc is the right vehicle for this specific project)
      - State of the Art
      - Scientific Approach, Methodology, and Novelty (incl.
        contribution and potential impact)
      - Research Environment and Supervision (feasibility + concrete
        interdisciplinary synergies)
      - Stakeholders involved in the project
   3. Project relevance to CEBE research fields — max 1/2 page
   4. Sustainability goals & relation to CEBE vision — max 1/2 page
3. CV of PI (max 2 pages)
4. CV of co-supervisor(s) (max 2 pages each)
5. CV of named candidate, if any (max 2 pages)

### Formatting

Times New Roman, 12 pt, single-spaced, 2.5 cm margins. Handled by
`proposal/main.tex` and `proposal/cv-template.tex` — see
`proposal/README.md` for build and page-limit-checking instructions.

### Evaluation criteria (score each section's draft against these)

- Scientific excellence, novelty, and genuine *necessity* of the
  interdisciplinary angle (not interdisciplinary window-dressing)
- Relevance to CEBE's overall vision and the specific research field(s)
  claimed
- Concrete synergies only achievable because it's interdisciplinary
- Scientific merit of PI + partners (reviewers normalize for academic
  age, so early-career is not a penalty)
- Real, specific stakeholder/industry involvement
- Feasibility within the stated time/budget
- Cross-university collaboration — flag explicitly if the project is
  single-university, since that's a known weaker point

### When reviewing, ask rather than assume

- If it's unclear which CEBE research field a section is targeting, ask
  — the team's combined expertise (structural health monitoring +
  digital twins/BIM/automation + reinforced concrete durability/
  corrosion + immersive/human-AI interaction) points most naturally at
  #7 Extending the life of the built environment and/or #4
  Digitalisation and automation, possibly alongside #1 Assessing and
  measuring environmental sustainability or #3 Low carbon and robust
  construction materials (via Ueli Angst's durability work), but confirm
  rather than assume.
- Team and roles are now fixed: Lorenzo Loyola is the PhD candidate;
  Giuseppe (PI) and Jhonattan Martinez Ribon are the Aarhus University
  supervisors; Carolin Reichherzer and Ueli Angst are the ETH Zurich
  supervisors. Still ask if a section's description of any of their
  roles or contributions is inconsistent with this.
- If a stated collaboration partner or co-supervisor isn't yet
  reflected in a CV file, ask whether a CV is forthcoming rather than
  treating the gap as an error.
- Never invent facts, publications, or numbers on Giuseppe's behalf —
  check claims against `references.bib` and the CVs, and ask when
  something can't be verified there.

### Review checklist per section

- **Project Summary**: readable by a non-specialist in ~2 minutes;
  conveys the interdisciplinary hook and expected contribution?
- **Motivation, Significance and Scientific Challenges**: is the
  *necessity* of an interdisciplinary approach argued, not just
  asserted? Is the PhD/postdoc rationale explicit?
- **State of the Art**: are claims backed by `references.bib` entries?
  Any recent, project-relevant references missing from the bib file?
- **Scientific Approach, Methodology, and Novelty**: is the novelty
  concrete? Is the methodology feasible within 3 yrs (PhD) / 2 yrs
  (postdoc)?
- **Research Environment and Supervision**: consistent with what's in
  the CVs (infrastructure, track record)? Are the claimed synergies
  concrete rather than generic?
- **Stakeholders**: named and specific, or vague?
- **Project relevance to CEBE research fields**: field(s) explicitly
  identified, contribution clearly stated?
- **Sustainability goals**: specific objectives, trade-offs, and
  methodological choices — not boilerplate?
- **Cross-university status**: flagged if the collaboration is
  single-university (known weaker point per the call)
- **Each CV**: covers the required minimum (PhD year, achievements/
  impact statement, current+former supervision counts, 10 publications
  as 5 most important + 5 recent-relevant, ORCID/Scopus link)?
- **Page limits**: after Giuseppe compiles, `grep PAGEMARK` the log to
  confirm each section is within its stated maximum.

### Process

1. When Giuseppe shares or updates a section, read it alongside the
   relevant call requirement, `references.bib`, and (where relevant)
   the CVs.
2. Ask clarifying questions before giving feedback if something is
   ambiguous or missing context.
3. Give structured feedback per section: strengths, gaps against the
   evaluation criteria, specific questions, and — if useful — a couple
   of concrete suggestions. Leave the actual rewriting to Giuseppe.
4. Log every review pass to `FEEDBACK.md`: append a new dated entry
   (never edit or delete a past one) summarizing the points raised for
   the section(s) reviewed. If a past point has been addressed, append
   a new entry noting that rather than removing the old one — the file
   is a running log, not a checklist. See the format and rules at the
   top of `FEEDBACK.md`.
5. Track page/length limits via `grep PAGEMARK` after Giuseppe
   compiles, and flag overruns.
6. Read-only on proposal content (`proposal/main.tex`,
   `proposal/cv-*.tex`, `references.bib`). Build/merge support
   (compiling, assembling the submission PDF) is fine since it doesn't
   touch content.
