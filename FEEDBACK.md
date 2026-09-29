# Proposal Review Feedback Log

Append-only log of reviewer feedback on the CEBE Interdisciplinary
Fellowship proposal (see `AGENTS.md` for the reviewer role and
knowledge base this feedback is grounded in).

**Rules for this file:**
- Only ever append a new entry at the bottom. Never edit or delete a
  past entry, even once its points are addressed — the log is a
  history, not a checklist.
- To mark something addressed, add a new entry that references the
  earlier one (e.g. "Re: 2026-09-05 State of the Art — now cites
  Angst et al. for corrosion baseline, resolved.").
- One entry per review pass. Note the section(s) reviewed and the date.

**Entry format:**
```
## YYYY-MM-DD — Section reviewed
- Point 1
- Point 2
```

---

## 2026-09-02 — Log created

No proposal content has been drafted yet — `proposal/main.tex` and the
CV files still hold placeholder text (`[Full Name]`, `[Motivation...]`,
etc.), and no CVs exist yet for Jhonattan, Carolin, Ueli, or Lorenzo.
Nothing to review substantively yet. This log will be appended to as
Giuseppe writes and updates sections.

## 2026-09-25 — application/main.tex (all sections except Project Summary, on hold)

Scope: `application/main.tex` only; Project Summary excluded (on hold);
CVs not reviewed (still placeholders). Review by three subagents:
science (Opus), strategy (Sonnet), formalities (Haiku, spot-checked by
orchestrator). Line numbers refer to main.tex as of this date.

### Cross-cutting (highest priority)
- Novelty not yet stated: placeholders in live text at L147
  "[some immersive sentence needed]", L154 "[ something immersive]",
  L156 "DT and A [something that is novel about this]I", L158
  "[technical contribution]".
- LLM+KG grounding for bridge maintenance is no longer new on its own
  (li_human---loop_2026 is cited; 2025–26 papers found via web search do
  near-identical work, see science). Most defensible novelty: controlled
  human–AI evaluation (grounded vs ungrounded assistance, XR vs desktop;
  reliance, situational awareness, decision quality with practising
  engineers), and possibly durability-constrained hypothesis generation.
- Interdisciplinarity partly nominal: FEM/synthetic data (T1.1, L237)
  never used by WP2/WP3; SHM/OMA/model updating (PI expertise, L286)
  plays no role in reasoning; corrosion appears only as a KG label
  (L238); Angst's role (L288) peripheral.
- ~~Call requirements not addressed: why a PhD (vs postdoc) and why this
  candidate (Lorenzo not mentioned in 2.1); time split across research
  groups (L280, "18 months at ETHZ") unclear if AU/ETH count as 3–4 groups.~~

### Motivation, Significance and Scientific Challenges (science, strategy)
- Q1–Q3 (L179–181) lack operational measures and baselines; Q2 unassigned
  (L184); Q3 has no comparison condition.
- Is "immersive" central? L271 contribution says "AI and AR", not XR.
- Uncited claims: Morandi, bridges beyond nominal life / global south
  (L147, L350), "SHM has developed tremendously" (L147).

### State of the Art (science)
- All 12 cite keys resolve (both .bib files). Duplicate entries across
  bibs: raees_people_2026, berretta_human_2026; several Han & Shin
  duplicates in references_ga.bib.
- Missing coverage: durability/corrosion literature; bridge ontologies /
  IFC semantic enrichment; human factors (situational awareness, trust
  calibration, workload).
- L197 "ontologies at the centre of SHM research" cites a generic
  ML+ontology review. "LLMs to fold DTs" (L192, L348) unclear.
- Say what WP1/WP2 add beyond li_human---loop_2026.
- Candidate bib entries already available: raees_people_2026,
  berretta_human_2026, isailovicBridgeDamageDetection2020,
  han_closed-loop_2026, xu_brim_2019, zhuIFCgraphFacilitatingBuilding2023,
  laksono_knowledge-based_2026, spencer_advances_2025,
  luMultilevelBridgeCorrosion2025, fanTechniquesCorrosionMonitoring2022.
- Web search (outside applicant bibliography): KG-driven bridge
  maintenance with LLM + chain-of-thought (2025); Illinois IDEALS thesis
  on domain LLM + KG for bridge maintenance; hierarchical KG for slab
  bridge inspection (AEI 2026); LLM-in-XR review (CHI 2025);
  SituationAdapt (UIST 2024).

### Scientific Approach, Methodology, and Novelty (science)
- Strengths: evidence/knowledge/inference/hypothesis separation (L227);
  T2.1 avoids another defect detector (L242); moisture example (L243);
  T3.3 metrics (L251).
- No ground truth for "decision accuracy"; participants (number, profile)
  and baselines undefined; no benchmark/metric for WP2 agent.
- ~~Case study inconsistent: global-south bridges (L231) vs Aarhus in the
  summary; "University of Salvador" (L231) vs UFBA (L297, L326).~~
- Feasibility/risk for one PhD in 3 years not addressed (data sparsity at
  global-south sites, hallucination, recruitment, XR hardware).
- "A new paradigm" (L271) unsupported. Three-condition comparison (L259)
  and data-sufficiency study (L245) are commented out.

### Research Environment and Supervision (strategy, science)
- Roles per person clear, but synergy asserted per person, not as jointly
  emergent. Nobody with an evidenced LLM/KG track record; verify once
  CVs are filled.

### Stakeholders (strategy)
- ~~Aarhus Municipality and COWI roles passive ("share input", "be exposed
  to", L329); richer commented text (L315–321) was cut. Danish Road
  Directorate (named in RF7 roadmap p.11) absent.~~

### Project relevance to CEBE research fields (strategy, RF7 check)
- ~~No explicit WP7.1–7.4 mapping (fits WP7.1 and WP7.4).~~
- ~~L348 claims RF7 AU baseline focuses on sensing hardware, but roadmap
  pp.13–14 lists AU-led "AI/Robot assisted operation of SHM" and "UAV
  inspection with computer vision": differentiation needed.~~
- ~~RF3/RF4/RF5 interfaces not discussed; roadmap p.16 names semantic
  modelling, DT engineering and agentic AI as RF4/RF7 shared topics.~~


### Sustainability (strategy, formalities)
- ~~Heading must be "Sustainability goals of the project and relation to
  the CEBE program vision" (template L199), currently "Sustainability"
  (L364).~~
- ~~No trade-offs stated (trade-off paragraph commented out, L380); no
  explicit link to CEBE vision.~~

### Formalities
- Length (live text, comments excluded): Project Description ~2,200
  words (motivation 509, SotA 390, approach 917, environment 260,
  stakeholders 137) — borderline for 4 pages; relevance ~184 and
  sustainability ~154 words, likely within 1/2 page. Compile and
  `grep PAGEMARK main.log` to confirm.
- ~~Typos: "brdige" (L237); "Assoc.d" (L237, L380) and "will Assoc."
  (L249, L253) — likely find-and-replace of "associate"; "will be
  organize" (L237); "will supervised" (L286); "expertise in on" (L288);
  "at at AU" (L280); "Geometic" should be "Geomatic" (L109–110).~~
- Project Summary wrapped in \textcolor{blue}: remove before submission.
- `ragged2e` package added vs template (minor).
- No budget figures or start date in main.tex (check whether required
  in the PDF or elsewhere in the submission).

## 2026-09-25 — Correction to the 2026-09-25 main.tex review (State of the Art, T2.2)

Re: 2026-09-25 State of the Art, web-search findings. After checking
the abstracts, only two of the cited papers overlap closely with T2.2
(graph-grounded LLM reasoning):
- Wang, Xiong, Zhu & Cai, "Knowledge graph-driven bridge maintenance
  decision-making via integrating large language models and
  chain-of-thought reasoning" (BMKG-DCoT), Automation in Construction
  181, 2026 — LLM iteratively queries a KG of historical defects and
  repairs to recommend maintenance by case analogy.
- Q. Chen, "Domain-specific adaptation of large language models and
  integration with knowledge graph analytics for enhanced bridge
  maintenance decision making", PhD dissertation, University of
  Illinois, 2025 — LLM extraction from inspection reports, bridge KG,
  RAG-based decision support (NBI data).
- Correction: Zhu et al., "A hierarchical knowledge graph for slab
  bridges inspection and maintenance" (AEI 2026) uses fuzzy Bayesian
  reasoning and no LLM; it overlaps with the T1.2 knowledge graph, not
  with T2.2. The earlier entry overstated it.
- Adjacent (no KG): Mariniello, Pastore & Asprone, "LLM agents for
  explainable bridge portfolio maintenance scheduling under
  uncertainty", Expert Systems with Applications, 2026 — LLM decisions
  constrained by a physics-based degradation simulator.
- Possible differentiation for T2.2: single-asset DT, fusion of new
  multimodal observations with site-specific context, hypothesis
  generation with explicit evidence/knowledge/inference separation, and
  human evaluation in WP3 (neither close paper evaluates human use).

## 2026-09-27 — application/main.tex (all sections incl. Project Summary), CV's/CV-Giuseppe.tex, budget.tex

Scope: `application/main.tex` (full, Project Summary now included),
`application/CV's/CV-Giuseppe.tex`, `application/budget.tex`. Other CVs
and abstract.tex not reviewed. Review by three subagents: science (Opus),
strategy (Sonnet), formalities (Haiku, corrected by orchestrator where it
misread the repo). Compiled in the session (latexmk, no undefined
citations/references). Line numbers refer to the files as of this date
(uncommitted working copy).

### Page limits (measured on the compiled PDF, A4, 2.5 cm margins)
- Project Summary 0.65 p (limit 1/2) — over by ~0.15 p.
- Project Description (2.1–2.5) 5.46 p (limit 4 excl. references) — over
  by ~1.5 p. Breakdown: 2.1 = 1.30, 2.2 = 0.77, 2.3 = 2.48 (Fig. 1 ≈ 0.35),
  2.4 = 0.55, 2.5 = 0.31.
- Sec. 3 relevance 0.60 p (limit 1/2) — over by ~0.1 p.
- Sec. 4 sustainability 0.54 p (limit 1/2) — borderline.
- References ~1.75 p (21 entries); Appendix A (photos) 1 p — the call
  lists no appendix; it is not counted here but may be queried.
- CV-Giuseppe: 2 p (OK). budget: 1 p.

### Cross-cutting (highest priority)
- Length: ~1.5 pages must come out of 2.1–2.5 and ~0.15 p out of the
  Summary. Most compressible: 2.1 (1.3 p, motivation + vision + Q1–Q4 +
  candidate), the last two sentences of the Summary (transferability
  restated twice), Fig. 1 (0.35 p).
- Team/roles inconsistent (strategy, formalities): frontpage L112–113
  labels Angst and Georgakis "Co-PI" — a role the call does not define
  (PI + co-supervisors). Georgakis (new since 09-25; L113, L299) is not in
  the agreed team list, has no CV file, and his task at L299 ("supervise
  the formulation of maintenance plans, definition of SHM data") overlaps
  Angst's at L303 ("supervise the formulation of maintenance plans ...").
  Decide: relabel as co-supervisor + add a CV, or drop from the frontpage.
- Stakeholders (strategy): the 09-25 point marked resolved is NOT resolved
  in substance — Aarhus Municipality and COWI were commented out
  (L336–337), not made active. Live text now has only two Global-South
  universities and no Danish owner/industry partner. Against the call's
  "Involvement of building sector stakeholders" criterion and the RF7
  roadmap's named Danish stakeholders (Danish Road Directorate, Banedanmark,
  COWI, Ramboll, NIRAS), this is the weakest criterion as it stands.
- Novelty against the closest prior work is still not stated (science):
  wang_knowledge_2026 (BMKG-DCoT), mariniello_llm_2026,
  zhu_hierarchical_2026 are all in references_ga.bib and none is cited;
  Chen (Illinois 2025) not in bib. L231 claims the evidence/knowledge/
  inference/hypothesis separation is new but compares it to nothing.
- Q4 (immersion) is never tested: T3.3 (L259) compares conventional /
  ungrounded AI / grounded AI; XR is not a factor. Title and C3/C4 promise
  XR effects; Summary (L134) does not mention XR at all.
- PI's SHM/FEM expertise and Angst's durability still have no job in the
  method: FEM/synthetic data (T1.1, L247) unused downstream; corrosion is a
  KG label (L248) and an example (L253); "prognosis" (L303) maps to no
  task. Suggested direction: physics/durability models as the
  hypothesis-check and next-measurement layer (also yields seeded ground
  truth for T3.3) — would make the interdisciplinarity necessary rather
  than additive.
- No ground truth, benchmark, participant numbers/profile, or risk/
  mitigation paragraph (data access at two sites, UAS permits in Nairobi
  CBD, hallucination, recruitment, ethics approval for human studies).
- ETH stay funding: budget.tex L64 says the 18-month ETHZ stay depends on
  external mobility grants to be applied for in year 1. The call requires
  equal time at each group; a reviewer will read this as a feasibility
  risk unless stated as a contingency in the proposal.

### Project Summary (science, strategy)
- Over length; "support engineers what the combined evidence means"
  (L134) lacks a verb; "human–AI decision paradigm" moved here from L271
  and still unsupported; XR absent; transferability claimed but no design
  in 2.3 tests it. Still wrapped in \textcolor{black} — remove.

### 2.1 Motivation (science, strategy)
- Uncited: bridges exceeding nominal life, Morandi, Global-South
  deterioration, shortage of personnel (L148). berretta_human_2026 (in
  bib) contradicts "human–AI workflows ... underexplored for inspection"
  (L155) unless the gap is narrowed to asset-level reasoning.
- L177 says "three questions", L179–184 list four.
- Q1: granularity levels/metric undefined. Q2: "logical consistency" not
  operationalised; realistic baseline is document-RAG, not a bare LLM
  (BMKG-DCoT already beats that). Q3 as written repeats ChatTwin's N=24
  study (luo_chattwin_2026). Q4: "interaction modalities" undefined and
  not carried out in 2.3. L186 assigns Q2 to AU; diagram labels Q2 joint.
- PhD rationale (L189) says why Lorenzo is available, not why a PhD (vs
  postdoc) is the right vehicle — explicit call requirement.

### 2.2 State of the Art (science)
- Miscitation: L202 "conversational agents that combine LLMs and
  ontologies to operate a DT" → li_human---loop_2026 builds a KG with
  ontology-guided LLM extraction + GNN; no conversational agent, no DT
  operation. L197 celik_vision_2026 is a VLM-for-damage-documentation
  review, weak support for the "history-wide reasoning bottleneck".
- Uncited but in bib and relevant: wang_knowledge_2026,
  mariniello_llm_2026, zhu_hierarchical_2026, raees_people_2026 (reliance),
  berretta_human_2026, karaaslanArtificialIntelligenceAssisted2019 (AR+AI
  bridge inspection), laksono_knowledge-based_2026,
  isailovicBridgeDamageDetection2020, durability entries (fan 2022, lu
  2025). Own work: Oakes/Gomes/Abbiati 2024 (ontological DT engineering)
  is in the CV and directly relevant to L202.
- Durability and human-factors literature (SA/Endsley, trust
  calibration, workload) still absent although measured in T3.3.
- Bib hygiene: raees_people_2026 and berretta_human_2026 duplicated
  across the two .bib files; multiple duplicates in references_ga.bib.
- Web search (outside bibliography): Pan et al. 2026 "Graph-DT-GPT"
  (Autom. Constr., same group as ChatTwin: LLM grounded on graph DTs, no
  user study); Chacón et al. 2026 "Semantic digital twins for masonry
  bridges" (Eng. Struct. 357 — likely the reference in the TODO at L202);
  Fawad et al. 2025 immersive bridge DT with HoloLens (Computers in
  Industry 164, no AI, no user evaluation). No 2025–26 work found that
  combines bridge LLM+KG DT, XR and a controlled study with engineers —
  the combination holds, but each part has a close precedent.

### 2.3 Approach (science)
- Strengths: evidence/knowledge/inference/hypothesis separation (L231);
  moisture-below-joint example (L253); T2.1 not "another defect
  detector"; three-condition T3.3 with named measures (L259).
- L233 "AI will be able to guess which sources" — unscientific wording,
  unclear meaning. L233 "bidirectional communication" — nothing actuates
  the physical bridges; by fitzgerald_engineering_2024 this is a shadow +
  human feedback.
- L253 last sentence ("The quality of AI-supported assessment changes as
  ... will be also investigated") ungrammatical and has no design; it is
  the only method behind Sustainability O2 (L398).
- Two sites chosen for access, not as a designed contrast. Web: Ponte do
  Funil had structural recovery works 2023–24 (records likely exist);
  Nairobi Expressway opened 2022, run by a private concessionaire (little
  history; data access depends on the operator, not UoN).
- C1 "validated" against what? C3/C4 overlap; four contributions vs three
  papers.

### 2.4 Research Environment (science, strategy)
- PI claim at L294 is supported by the CV (Talasila 2026 DT platform,
  "Modelling for DTs", NARX/surrogates) but 2.3 gives it nothing to do.
- Nobody with an evidenced LLM/KG record; Jhonattan "leads integration
  with LLMs" (L296) — check his CV. L296 "BIM modeling." fragment.
- 18 months at ETHZ now explicit (time split resolved).

### 3 Relevance to CEBE (strategy, RF7 check)
- WP7.1/7.4 mapping now substantive and traceable to the RF7 chapter
  (mission quote, AU-led "AI/Robot assisted operation of SHM", WP7.4
  risk-informed decisions); RF4/RF5 interfaces cited — resolved.
- Differentiation from the AU-led target is thin because that target
  already contains "AI"; one clause separating sensing/inspection
  automation from downstream interpretation would fix it.
- Roadmap frames the WP7.1 gap quantitatively (capacity/reliability
  updating); the proposal's contribution is interpretive — avoid
  implying it delivers the quantitative gap. RF3 interface not mentioned
  (minor). Two bib keys for the roadmap (cebe_research_roadmap_2026,
  cebe_research_roadmap_main_2026) — confirm both are intended.

### 4 Sustainability (strategy)
- Heading, trade-offs and CEBE-vision link resolved. L409 "Therefore
  HAI-BRI SDG 11 ..." missing verb; "guaranty" → "guarantee".

### CV-Giuseppe.tex (formalities, science)
- Call minimum content: all present (PhD year, achievements, supervision
  counts, 5+5 publications, ORCID/Scopus). 2 pages.
- L58 \lengthnote is live: "[Target length: max 2 pages ...]" PRINTS at
  the top of the CV — set \templatenotesfalse or delete the line.
- L60 bracketed placeholder "[Associate Professor in Structural
  Mechanics]"; L81 "University of Aarhus" (elsewhere "Aarhus
  University"); L99 "7master's"; L59 missing space before
  "\textbf{Scopus h-index:}"; "9 doctoral thesis" → theses.
- DOIs given as bare "10.xxxx" inside \url{} — not clickable; use
  https://doi.org/... . Oakes 2024 still "to appear" though it has a DOI.
  Overfull hbox at L125–126 (long URL). Talasila 2026 DOI/ISSN checked
  via web: appears correct.
- Achievements statement (L92) is funding volume only; nothing on
  scientific contribution to DT/SHM or on impact — the call asks for
  "achievements and relevant impacts". Recent-relevant list: Maestro2
  and DIGIT-BENCH are weakly relevant to this project.

### budget.tex (formalities)
- Yearly totals wrong: 2027 sums to 952,000 (stated 951,000); 2028 to
  957,000 (stated 960,000); 2029 to 981,000 (stated 979,000). Grand total
  2,890,000 is correct. Consumables 19+45+36 = 100,000 exactly at cap;
  supplement 750,000 and education rate 240,000 match the call.
- Terminology: "PhD school fees" vs call's "PhD education rate".
- Header comment still "Budget (sketch)" / "pdflatex budget-sketch.tex";
  "Costs for cloud computing ARE associated" (caps); square brackets left
  around foundation names (L65); "4% yearly increase" is 4.17% then 4.0%.
- The call's application guideline lists no budget; budget.tex is not
  \input in main.tex. Clarify where it is submitted (EasyChair form?
  internal AU form?) or whether it should go into the PDF.
- ETH stay funded outside CEBE (see cross-cutting).

### Formalities, main.tex
- Structure and headings mirror the call exactly; formatting (mathptmx
  12 pt, single spacing, 2.5 cm) conforms. ragged2e/\justifying and
  \parskip=0.8em are switched on from 2.3 onward but not in 1–2.2, so
  paragraph spacing changes mid-document.
- "University of Nairobi (UN)" (L230, L335) — acronym clashes with United
  Nations; use UoN or none. "FUBSE" used once.
- Typos/grammar: L134 "support engineers what"; L189 "hold +5 years",
  "start in January 1st, 2027", "36m"; L197 "However, DT paradigm,
  emerged"; L180–183 "how ... shall"; L296 "BIM modeling." fragment; L409
  "guaranty", missing verb. \projectname carries a trailing space inside
  \textbf (L64).
- Frontpage "Submission date: 2026-09-30" fine; double space at L109 is
  harmless in LaTeX.
- Photo credits in Appendix (Seinfra/BA press; Pexels) — fine if the
  appendix stays.

### Status of 2026-09-25 points
- Resolved: placeholders in live text; "ontologies at the centre";
  "LLMs to fold DTs"; case-study inconsistency; time split; WP7.1–7.4
  mapping; RF4/RF5 interfaces; sustainability heading/trade-offs; three-
  condition comparison restored; listed typos.
- Partly: novelty vs prior work (evaluation back, but closest works
  uncited); Q1–Q3 measures (comparisons added, metrics/ground truth
  missing); Angst's role (expanded in 2.4, no task); "new paradigm"
  (moved to Summary); data-sufficiency study (one sentence, no design);
  why PhD/why candidate (candidate yes, PhD-vs-postdoc no).
- Still open: T1.1 FEM unused; SHM plays no role; ground truth/
  participants/benchmark; feasibility/risk; uncited motivation claims;
  durability and human-factors literature; candidate bib entries uncited;
  no evidenced LLM/KG track record; \textcolor wrapper; length.
- Re-opened: Stakeholders — marked resolved on 09-25, but Danish partners
  were removed rather than strengthened.

## 2026-09-29 — Formalities only: full application (main.tex, abstract.tex, budget.tex, all CVs, support letters)

Scope: formal aspects only, at Giuseppe's request (no science/strategy
pass). Files: `application/main.tex`, `application/abstract.tex`,
`application/budget.tex`, `application/CV's/` (CV-Giuseppe.tex,
CV-Lorenzo.tex, CV-Ueli.tex, CV_CarolinReichherzer.pdf,
CV_ChristosGeorgakis.pdf, CV_JhonattanMartinez.pdf, CV_UeliAngst.pdf),
the two support letters, templates and READMEs, against the call PDF.
Formalities subagent (Haiku) run and corrected by the orchestrator where
it misread the files (it marked the PDF CVs fully compliant, said
Jhonattan's CV is in Times, and said the support letters name the
bridges — none of which holds). Compiled in the session (latexmk, scratch
copy). Line numbers refer to the uncommitted working copy as of today.

### Page limits (measured on the compiled PDF, A4, 2.5 cm margins)
- Project Summary 0.42 p (limit 1/2) — OK. Re: 2026-09-27, resolved.
- Project Description (2.1–2.5) 3.95 p (limit 4 excl. references) — OK,
  but only ~35 pt (2–3 lines) of slack, Fig. 1 included. Re: 2026-09-27
  (5.46 p), resolved; do not add text without re-measuring.
- Sec. 3 relevance 0.46 p, Sec. 4 sustainability 0.47 p (limit 1/2 each)
  — OK, both tight; Sec. 4's heading wraps onto two lines. Re:
  2026-09-27, resolved.
- References 2.5 p (excluded). Appendix A removed — resolved.
- CV-Giuseppe.tex compiles to **3 pages** (limit 2) — OVER. Regression
  since 2026-09-27 (was 2 p). Two overfull hboxes (L111–113, L135–136).
- CV-Lorenzo.tex 2 p (OK, with the template note still printing, see
  below). CV_Carolin/Christos/Jhonattan/Ueli PDFs: 2 p each (OK).
- Note: `\pagenumbering{gobble}` in the CV files makes `PAGEMARK` print
  an empty page number, so the CV page check must use `pdfinfo`/the PDF.

### Cross-cutting (highest priority)
- CV set is inconsistent with the team on the frontpage (L109–114): six
  people (PI, four co-supervisors incl. Christos Georgakis, candidate)
  but CVs exist as 3 .tex (Giuseppe, Lorenzo, Ueli-placeholder) + 4 PDFs
  (Carolin, Christos, Jhonattan, Ueli). Ueli has both a placeholder .tex
  and a complete PDF; Jhonattan/Carolin/Christos have no .tex. Decide one
  source per person; `AGENTS.md` (Team, five CV files) and
  `application/README.md` (pdfunite line with `CV-Jhonattan.pdf`,
  `CV-Carolin.pdf`) are out of date — Georgakis is absent from both.
  Ask: update AGENTS.md/README to the six-person team and the PDF-CV
  reality? (Doc edits, not proposal content.)
- Placeholders still live: CV-Ueli.tex is 100% template (L65 `[Year]`,
  L69 `[link]`, L74–76, L81–82, L89–102) — drop it or fill it;
  CV-Giuseppe.tex L62 title still in square brackets
  `[Associate Professor in Structural Mechanics]`; budget.tex L64
  foundation names in square brackets (re: 2026-09-27, still open);
  abstract.tex is the placeholder sentence only.
- Template scaffolding that WILL print: CV-Lorenzo.tex L37 and
  CV-Ueli.tex L56 `\lengthnote{...}` with `\templatenotestrue` (L23/L45)
  → "[Target length: ...]" appears under the CV heading. Set
  `\templatenotesfalse` (README rule) before the final build. In main.tex
  every `\lengthnote` is commented, so nothing prints there.
- Build is not reproducible as documented: main.tex L42
  `\graphicspath{{figures/}}` is relative to `application/`, but L357
  `\bibliography{application/references_ga, application/references}` is
  relative to the repo root. From the root the figures fail; from
  `application/` (as README says) the bib fails. It only built with
  TEXINPUTS/BIBINPUTS set. Ask how you compile (VS Code root + settings?)
  and align paths or the README so the final build is one command.
- Stakeholder identities vs the signed letters: L298 "Prof. Dayana
  Bastos" — letter signed "Professor Dayana Bastos Costa, Federal
  University of Bahia (UFBA)"; L299 "Prof. Peter Njeru Njue" — letter
  signed "Arch. Peter Njeru Njue, Chairman and Lecturer" (not a
  professor). Also, neither letter names a bridge: Bahia offers
  "suitable bridge and/or critical-infrastructure case studies in
  Brazil", Nairobi "suitable critical infrastructure in Kenya, including
  potential bridge case studies", whereas Summary L138, 2.3 L196 and 2.5
  L298–299 state access to the Ponte do Funil and the Nairobi Expressway
  viaducts. Reviewers who read the letters will notice; either soften the
  wording or get letters that name the assets. Ask: are the letters going
  into the single PDF (the call lists no annex)?
- Christos Georgakis: added as co-supervisor (frontpage L111, 2.4 L273)
  — his CV states he is Lead of CEBE Research Field 7. Not a call
  violation, but a formal point a panel may raise (RF7 lead on an RF7
  application); worth being aware of. AGENTS.md "Team" still lists four
  supervisors. Re: 2026-09-27 "Co-PI" label — resolved (now
  "Co-supervisor").

### Frontpage / structure / formatting (main.tex)
- Required structure mirrored exactly: frontpage with title, roles,
  affiliations, ToC; headings 1, 2.1–2.5, 3, 4 verbatim from the call;
  order correct. Preamble: mathptmx 12 pt, `\singlespacing`, 2.5 cm — OK.
- Deviations from `main-template.tex` (not violations): references placed
  after Sec. 4 (L356–357) instead of after Sec. 2; `ieeetr` instead of
  `unsrtnat`; two bib files (`references_ga.bib` 365 kB personal
  library + `references.bib`) — AGENTS.md only knows `references.bib`.
- `\justifying` + `\parindent 0` + `\parskip 0.8em` switched on at L192,
  L260, L286, L311, L337 but not in Sec. 1–2.2 → indented paragraphs up
  to 2.2, block paragraphs from 2.3 on (re: 2026-09-27, still open). The
  negative `\vspace{-0.3cm}` after each task (L219–233) and `-0.2cm` in
  2.4/3/4 are what keep the sections under the limits; fine, but fragile.
- L110 double space "Assist. Prof.  Jhonattan"; L114 "Ph.D. Candidate"
  vs "PhD project" (L101) and "PhD" everywhere else; L120 "Submission
  date: 2026-09-30" is the deadline day — fine if that is the plan.
- Names/titles across frontpage, 2.4 and CVs: Jhonattan "Martinez"
  (L110) / "Jhonattan G. Martinez" (L271) / CV "Jhonattan G. Martinez" /
  AGENTS.md "Martinez Ribon" — pick one. Ueli "Prof." (L113, L277) — CV
  says Associate Professor since 06/2024 (CV-Ueli.tex L60 says
  "Professor"); acceptable as a courtesy title, but be consistent with
  his own CV. Carolin "Dr.", D-BAUG, ETH Zurich — matches her CV
  (Postdoctoral Fellow, ETH, since July 2026). Christos: frontpage says
  "Dept. of Civil and Architectural Engineering", his CV says "Aarhus
  University / Structural Dynamics and Geotechnical Engineering" — OK.
- Fig. 1 (L198–211) has no photo credits; the appendix that carried them
  (Seinfra/BA press; Mukula Igavinchi/Pexels) is commented out
  (L362–386). Add credits to the caption or confirm the licence allows
  omission.

### Fixed facts (main.tex, budget.tex)
- Duration 36 months (L177), start 1 Jan 2027 (L177; budget.tex L7, L62)
  — within max 3 yrs and before the 30 May 2027 start deadline. OK.
- Time split: 18 months at ETHZ (L263) of 36 — equal split. OK. Note the
  call says "each of the participating research groups": with three AU
  supervisors from two/three AU groups and two ETHZ groups, the split is
  by university, not by group — defensible, just be aware.
- Interdisciplinarity: ≥2 groups, PI at a CEBE partner (AU), PhD
  enrolled/employed at AU, cross-university — OK.
- Budget arithmetic (budget.tex L48–55): salary 576+600+624 = 1,800,000;
  education rate 3×80,000 = 240,000 (call figure); consumables
  19,000+45,000+36,000 = 100,000 (exactly at the cap); supplement
  3×250,000 = 750,000 (call figure); total 2,890,000 — all correct.
- Budget presentation: L49 label "PhD school fees" — the call's term is
  "PhD education rate" (used in budget-sketch.tex L18); L48 "4% yearly
  increase" is 4.17 % then 4.0 % (re: 2026-09-27, open); L62 "ARE"
  (open); header comments L2–6 still say "(sketch)" and "Build: pdflatex
  budget-sketch.tex" — stale; `budget-sketch.tex` still in the folder
  with different numbers (travel 85,000, in-kind compute) — delete or
  mark superseded to avoid submitting the wrong one. Budget is still not
  `\input` in main.tex and the call lists no budget section; the two
  "Internal Application Form 2026-09-24*.xlsx" files suggest it goes to
  the AU internal form — confirm, and confirm the xlsx numbers match
  budget.tex (not checked here).
- ETH stay funded outside CEBE (budget.tex L64) — re: 2026-09-27, still
  open as a feasibility statement.

### Internal consistency, acronyms, typos (main.tex, rendered text checked)
- L221 `\asset will` renders "case-study bridgeswill" (macro swallows
  the space) — use `\asset{} will` or `xspace`. Other `\asset` uses are
  followed by punctuation and render fine. `\projectname` (L65) still
  carries the trailing space inside `\textbf`.
- L175 "SA" used before it is defined at L185; BIM/FEM (L216) and SDG
  (L350) never expanded; XR defined twice (Summary L136, L163); "UN" for
  University of Nairobi (L196, L299) — the letter itself uses "UoN"
  (re: 2026-09-27, open).
- L321 "(WP5.1)\cite" and L325 "framework\cite" — no space before the
  citation bracket in the PDF.
- L170–171 Q1/Q2 start lower-case after the label.
- Typos/grammar visible in the PDF (list only): L136 "develop human–AI
  interaction framework" (article); L161 "the integrating of"; L163 "by
  a building a system"; L177 "+5 years", "start in January 1st, 2027",
  "36m" (open since 09-27); L185 "investigated in for for"; L187
  "engineers SA"; L228 "will be also investigated" (open); L233 "T3.2.
  will"; L273 "sill support"; L341 "CEBE vision"; L350 "guaranty",
  "Therefore HAI-BRI SDG 11" missing verb (both open since 09-27); L153
  "Genova" (Genoa in English).
- Re: 2026-09-27 — resolved: `\textcolor` wrapper on the Summary; "three
  questions / four listed" (now two); Appendix; Co-PI labels; Summary,
  2.1–2.5, Sec. 3 and Sec. 4 lengths.

### abstract.tex
- Placeholder only (L4 "The abstract must be between 200 and 1000
  characters."). The call's application guideline lists no abstract, so
  this is presumably the EasyChair form field — still to be written, and
  it is not part of the single PDF. Ask: where is it needed?

### CVs — required minimum content (call §5)
- CV-Giuseppe.tex (3 p — OVER): name/affiliation OK; title in brackets
  (L62); PhD year 2014 in Education (L72) — OK; achievements (L91) OK;
  supervision current/total (L98–99) OK but "7master's" (missing space),
  "9 doctoral thesis" (theses), and the call asks current + former, not
  total; ORCID + Scopus OK. Publications: "Five most important" lists
  SIX (L121–126); "Five recent" has an EMPTY `\item` (L132) that renders
  as a blank numbered entry, so 5 + 1 blank. Affiliation wording
  inconsistent: header "Dept. of Civil and Architectural Engineering
  (CAE), Aarhus University" (L63) vs "Department of Engineering, Section
  of Civil and Architectural Engineering, University of Aarhus" (L80–81).
  L134 Oakes et al. "to appear, 2024" — stale. DOIs as `\url{10.1016/...}`
  (L121–136) are not clickable links (no https://doi.org/ prefix).
  Heading L107 "Selected research project" (singular). Cutting one
  "most important" paper, the empty item and the bracket, plus tightening
  Selected projects, should bring it back to 2 pages.
- CV-Lorenzo.tex (2 p): candidate CV — the call only requires max 2
  pages for the candidate; content is complete (ORCID, education,
  publications 5+5). Full name "Lorenzo Iván Loyola Osorio" (L40) vs
  "Lorenzo Loyola" everywhere in main.tex — fine, but consistent use of
  one form is cleaner. L3–4 header comments stale ("cv-pi.tex",
  "application/cv/cv-candidate.tex"). `\lengthnote` prints (see above).
  L62 "R&D Senior Consultant, Rene Lagos Engineers (2026-now, part-time,
  remote)" — a concurrent job alongside a full-time PhD may draw a
  question; your call whether to keep it in.
- CV_JhonattanMartinez.pdf (2 p): name/title/affiliation/ORCID OK; PhD
  given as "2016–2020" (acceptable); achievements OK. Gaps: supervision
  gives master's only ("10 completed, 3 ongoing") — PhD and postdoc
  counts (current and former) missing, even if 0; publications are 7
  journal + 1 chapter, not structured as 5 most important + 5 recent
  relevant (8, not 10). Format: US Letter page size (all others A4) and
  Aptos/Arial fonts — will look different in the merged PDF.
- CV_CarolinReichherzer.pdf (2 p): name/title/affiliation OK; PhD 2021
  OK; ORCID present only as a hyperlink labelled "ORCID" (URL not
  printed — fine on screen, invisible on paper); achievements OK.
  Gaps: supervision gives "Master (active) 1, Bachelor (past) 1,
  mentored 1 PhD" — no explicit PhD/postdoc current/former numbers;
  publications 4 "most important" + 5 "most relevant" = 9, not 5 + 5.
  Fonts OpenSans/MavenPro/Ubuntu/Nunito (not Times).
- CV_ChristosGeorgakis.pdf (2 p): complete — name/title/affiliation, PhD
  2001, achievements + impact, supervision table current/former, 5 + 5
  publications with relevance notes, ORCID; Times New Roman, A4. Only
  fully compliant supervisor CV. (Written for this call: header "CEBE
  Interdisciplinary Fellowship Programme 2026".)
- CV_UeliAngst.pdf (2 p): name/title (Associate Professor)/affiliation
  OK; PhD 2011 OK; achievements OK; Scopus ID 22978555600 + Researcher ID
  OK (call accepts Scopus or ORCID); 5 + 5 publications OK. Gap:
  supervision given as "14 completed PhD theses (11 as main advisor),
  80+ BSc/MSc theses" — no current PhD/postdoc/master's numbers and no
  former-postdoc number. Helvetica. Contains date of birth, marital
  status and phone — not required; his choice.
- Missing .tex CVs (CV-Jhonattan.tex, CV-Carolin.tex, no CV-Christos):
  not gaps if the PDFs are the submitted versions — see cross-cutting.

### Submission package (call §5, §8)
- Single PDF order per call: frontpage + proposal, CV of PI, CVs of
  co-supervisors, CV of candidate. README's `pdfunite` line lists old
  file names and omits Christos — update before assembling. Mixed page
  sizes (Letter for Jhonattan) survive `pdfunite`; consider normalising
  to A4.
- Font: the call's Times New Roman applies to "the proposal"; the CVs
  are not explicitly bound, but three of the four PDF CVs are in other
  fonts — no violation, purely a uniformity question.
- Not in the call and not in the PDF: abstract (form field?), budget
  (internal form?), support letters (annex?). Confirm each destination
  so nothing is left out at upload.

### Top formal fixes before 30 Sept
1. CV-Giuseppe.tex back to 2 pages; remove the sixth "most important"
   entry, the empty `\item` (L132) and the brackets on L62.
2. Decide the CV source per person; drop or fill CV-Ueli.tex; set
   `\templatenotesfalse` in CV-Lorenzo.tex (and CV-Ueli.tex if kept).
3. Fix the figure/bib path mismatch so `latexmk` builds from one place.
4. Stakeholder names/titles to match the letters (L298–299); decide how
   to word bridge access given what the letters actually promise.
5. L221 `\asset` spacing, L273 "sill", the L321/L325 missing spaces, and
   the typo list above.
6. Ask Jhonattan, Carolin and Ueli for the missing numbers (PhD/postdoc
   current+former) and, for Jhonattan and Carolin, a 5 + 5 publication
   list; if they resend, keep to 2 pages.
7. Budget.tex header/labels; remove or mark budget-sketch.tex; confirm
   the internal xlsx matches.
8. Update README (pdfunite line) and AGENTS.md (team, CV list) — on
   request.

## 2026-09-29 — Re: 2026-09-29 formalities — submission package decided

Giuseppe's decision: the single PDF = main.tex PDF + CVs + budget.tex PDF +
the two support-letter PDFs. Test merge in the session (scratch copy):
28 pages, 2.5 MB. Consequences, all formal:
- Order: keep the call's order for the required parts (frontpage +
  proposal, CV PI, CVs co-supervisors, CV candidate), then budget and
  letters as annexes after the candidate CV.
- budget.pdf prints a page number "1" at its foot (article default; the
  CVs use \pagenumbering{gobble}) — a stray "1" mid-package. One-line fix
  in budget.tex (gobble) — budget.tex is not off-limits, but not changed
  here without a go-ahead.
- Mixed page sizes: CV_JhonattanMartinez.pdf and the Nairobi letter are
  US Letter (612x792), everything else A4. Cosmetic; leave the signed
  letter untouched, optionally re-export Jhonattan's CV as A4.
- pdfunite (README) produced a file with a broken xref (pdfinfo "Internal
  Error", qpdf warning "reported number of objects ... not one plus the
  highest object number"); the same merge with
  `qpdf --empty --pages <files> -- submission.pdf` is clean. Use qpdf (or
  pdftk) and run `qpdf --check` on the result before upload; README's
  merge command should be updated (on request).
- Since the budget page will be read by reviewers: budget.tex L62 "ARE",
  L64 square brackets around the foundation names, L49 "PhD school fees"
  vs the call's "PhD education rate", and the 4 %/4.17 % increase now
  matter as visible text.
- Since the letters will be read by reviewers: the mismatch between
  "access to the Ponte do Funil / Nairobi Expressway viaducts" (main.tex
  L138, L196, L298–299) and the letters' generic "suitable ... case
  studies" wording, and the Prof./Arch. title and "Bastos Costa" surname
  points, stand as flagged in the entry above.
- The proposal's ToC (auto-generated) lists only Sec. 1–4; the call does
  not require the annexes to appear in it.

## 2026-09-29 — Formalities re-check after edits (full application)

Scope as in the 2026-09-29 formalities entry. Files changed since then:
main.tex (Summary, 2.2, 2.4), abstract.tex, budget.tex, CV-Giuseppe.tex,
CV-Lorenzo.tex; CV-Ueli.tex removed. Recompiled and re-measured in the
session (scratch copy); test merge with qpdf: 27 pages, 2.5 MB, clean.

### Resolved (re: 2026-09-29)
- CV-Giuseppe.tex back to 2 pages; empty `\item` removed; DOIs now plain
  "DOI:" text. CV-Lorenzo.tex `\templatenotesfalse` set; no "[Target
  length]" note prints in any PDF. CV-Ueli.tex placeholder removed —
  CV_UeliAngst.pdf is the single source.
- main.tex: L273 "sill"; 2.2 "in for for", "lead" → "leads"; Summary
  "Evidence will be".
- abstract.tex written: 876 characters (limit 200–1000), plain text, no
  LaTeX macros — OK for the EasyChair field.
- Page limits unchanged and within: Summary 0.39 p, Description 3.95 p,
  relevance 0.46 p, sustainability 0.47 p.

### Still open (formal)
- CV-Giuseppe.tex L62 title still in square brackets; L98 "7master's";
  L100 "9 doctoral thesis"; "Five most important" still lists SIX
  (L121–126). Page 2 is now completely full, and two overfull lines
  protrude ~1 cm into the right margin (project list L111–113, 29 pt;
  publication L122–123, 40 pt) — visible in print.
- main.tex L221 "bridgeswill" (`\asset will`); L321/L325 missing space
  before `\cite`; SA used at L175 before its definition; Fig. 1 without
  photo credits; L298–299 stakeholder name/title vs the letters; the
  remaining typo list from the earlier entry (L136 article, L161, L163,
  L177, L187, L228, L233, L341, L350).
- budget.tex: L48 now "4.17 % yearly increase", but 600,000 → 624,000 is
  4.0 % (4.17 % would give 625,000) — label still does not match year 3;
  L62 "ARE"; L64 square brackets; L49 "PhD school fees"; page number "1"
  printed at the foot (stray in the merged package); `budget-sketch.tex`
  still in the folder.
- abstract.tex names only "the research group of Prof. Ueli Angst at ETH
  Zurich" as the collaboration, while the frontpage lists two ETHZ
  co-supervisors (Reichherzer, Angst) — consistent enough, but a panel
  reading both may ask where Carolin's group sits.
- Supervisor PDF CVs unchanged: Jhonattan (no PhD/postdoc counts, 8 not
  5+5 publications, US Letter), Carolin (no PhD/postdoc counts, 9
  publications), Ueli (no current counts). Nairobi letter US Letter.
- Build paths (figures vs bib) unchanged; README merge line unchanged.
