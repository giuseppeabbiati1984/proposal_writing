# Agent Instructions — proposal_writing

Repo-tracked instructions for AI coding agents (Claude, etc.) working in
this repo. Local secrets (e.g. git tokens) are kept separately in
`.agent-secrets.md`, which is gitignored — never merge secrets into this
file.

---

## CEBE Interdisciplinary Fellowship Proposal (2026)

### Context

Giuseppe (Aarhus University, CAE — structural health monitoring, hybrid
testing, system identification, structural dynamics, ML in structural
engineering) is preparing a PhD or Postdoc proposal for the CEBE
Interdisciplinary Fellowship Programme. Call reference kept in this repo
at `calls/CEBE_Interdisciplinary_Fellowship_2026.pdf`. LaTeX template at
`proposal/` (`main.tex`, `cv-template.tex`, see `proposal/README.md`).

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

### Evaluation criteria to keep visible while drafting

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

### Ask Giuseppe before drafting substantive content — never invent

- PhD or Postdoc track
- The interdisciplinary partner: field, department, university, and
  co-supervisor name if known
- Which CEBE research field(s) this targets (his profile points most
  naturally at #4 Digitalisation and automation, #5 Climate resilient
  and adaptive infrastructure, or #7 Extending the life of the built
  environment — confirm, don't assume)
- Existing research idea/question, or start from scratch
- Industry/stakeholder contacts to name
- Whether a candidate is already identified
- CV content for PI/co-supervisors — pull from what's provided or
  ORCID/Scopus, never fabricate publications or numbers

### Process

1. Confirm the missing details above before writing content.
2. Draft section by section as markdown first in this repo for easy
   review/iteration, then move into `proposal/main.tex`.
3. Use web search for State of the Art and the CEBE research roadmap
   (cebe.dk) — this is a 2026 programme, not something to answer from
   memory.
4. Flag any claim in the draft that's unverified.
5. Once content is settled, merge `proposal/main.tex` output with the
   CVs into the single submission PDF per `proposal/README.md`.
6. Actively track the page/length limits (`grep PAGEMARK` after
   compiling) — don't let sections drift past the stated maxima.
