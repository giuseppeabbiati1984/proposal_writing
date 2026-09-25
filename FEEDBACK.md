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
- Call requirements not addressed: why a PhD (vs postdoc) and why this
  candidate (Lorenzo not mentioned in 2.1); time split across research
  groups (L280, "18 months at ETHZ") unclear if AU/ETH count as 3–4 groups.

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
- Case study inconsistent: global-south bridges (L231) vs Aarhus in the
  summary; "University of Salvador" (L231) vs UFBA (L297, L326).
- Feasibility/risk for one PhD in 3 years not addressed (data sparsity at
  global-south sites, hallucination, recruitment, XR hardware).
- "A new paradigm" (L271) unsupported. Three-condition comparison (L259)
  and data-sufficiency study (L245) are commented out.

### Research Environment and Supervision (strategy, science)
- Roles per person clear, but synergy asserted per person, not as jointly
  emergent. Nobody with an evidenced LLM/KG track record; verify once
  CVs are filled.

### Stakeholders (strategy)
- Aarhus Municipality and COWI roles passive ("share input", "be exposed
  to", L329); richer commented text (L315–321) was cut. Danish Road
  Directorate (named in RF7 roadmap p.11) absent.

### Project relevance to CEBE research fields (strategy, RF7 check)
- No explicit WP7.1–7.4 mapping (fits WP7.1 and WP7.4).
- L348 claims RF7 AU baseline focuses on sensing hardware, but roadmap
  pp.13–14 lists AU-led "AI/Robot assisted operation of SHM" and "UAV
  inspection with computer vision": differentiation needed.
- RF3/RF4/RF5 interfaces not discussed; roadmap p.16 names semantic
  modelling, DT engineering and agentic AI as RF4/RF7 shared topics.

### Sustainability (strategy, formalities)
- Heading must be "Sustainability goals of the project and relation to
  the CEBE program vision" (template L199), currently "Sustainability"
  (L364).
- No trade-offs stated (trade-off paragraph commented out, L380); no
  explicit link to CEBE vision.

### Formalities
- Length (live text, comments excluded): Project Description ~2,200
  words (motivation 509, SotA 390, approach 917, environment 260,
  stakeholders 137) — borderline for 4 pages; relevance ~184 and
  sustainability ~154 words, likely within 1/2 page. Compile and
  `grep PAGEMARK main.log` to confirm.
- Typos: "brdige" (L237); "Assoc.d" (L237, L380) and "will Assoc."
  (L249, L253) — likely find-and-replace of "associate"; "will be
  organize" (L237); "will supervised" (L286); "expertise in on" (L288);
  "at at AU" (L280); "Geometic" should be "Geomatic" (L109–110).
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
