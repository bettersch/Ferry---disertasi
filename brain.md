# Brain — Coherence Anchor

Project: Ferry doctoral dissertation — Korbrimob Polri.
Builder version: 0.3.0. Mode: RESEARCH.
Last synced commit: Issue #32 working branch; final merge SHA pending. Synced by: ChatGPT research agent, 2026-10-11.

> Every statement this research makes lives here first. The manuscript may only say what the brain already holds, and the brain may only hold what a registered record supports. Structure and identifiers follow the [data structure](docs/data-structure.md); the stages follow the [research flow](docs/research-workflow.md). Write the statements in the project's research language; keep the structure and IDs as defined.

## How the brain works

| Layer | What enters | Where it is recorded |
|---|---|---|
| Perception | data items, parameters, executions | `DAT` in `data/records/`, `PRM` in `parameters/`, `RUN` in `analysis/runs/` and the search log |
| Memory | sources, theory map, literature matrix | `SRC` notes in `literature/theory/`, `literature/literature-review/`, `literature/search-online/` |
| Reasoning | typed statements with upstream and downstream links | the tables below |
| Decision | decisions and gate assessments | `DEC` in the decision log, `REV` in `reviews/` |
| Expression | manuscript paragraphs mapped to statements | `manuscript/outline.md` and Stage 8 below |

Rules:

- One sentence per statement. Two sentences are two statements.
- An ID is never reused. A materially changed statement gets a new ID and names the one it supersedes; the old row stays with status `SUPERSEDED` or `RETRACTED`.
- Status is one of `KNOWN`, `SUPPORTED`, `INFERRED`, `ASSUMED`, `UNKNOWN`, `DECISION NEEDED`, `SUPERSEDED`, `RETRACTED`. Evidence-relation detail per source stays in the claim ledger.
- Evidence lists record IDs only (`SRC`, `DAT`, `RUN`, `PRM`, `DEC`), never prose.
- Every statement except a context statement has at least one upstream link; every statement except a conclusion, a limitation, or a delivered implication has at least one downstream link.
- Sync at every Issue checkpoint, after every merge that changes a statement, and before every gate review; record the commit above.
- The validator rejects any ID referenced here that does not exist. `python scripts/coherence_report.py` prints the chain report.

Statement table columns: ID · Statement · Status · Evidence · Upstream · Downstream · Manuscript · Gate · Supersedes.

## Stage 0 — Context (`CTX`)

Mandate, constraints, resources, access to the locus, and the paradigm with its reason. Confirmed again at FG2.

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| CTX-001 | The dissertation research locus is Korbrimob Polri, with personnel as the candidate study population while the final unit of analysis remains undecided. | KNOWN | DEC-006; DEC-007 |  | PHN-001; PHN-002 | Introduction | FG0 |  |
| CTX-002 | This copied workspace is governed in RESEARCH mode and substantive changes must follow the Issue → branch → PR workflow. | KNOWN | DEC-006 |  |  | Project governance | FG0 |  |
| CTX-003 | The current institutional strategic context is the Korbrimob Polri 2025–2029 strategic plan established by KEP/299/V/2025 dated 23 May 2025. | SUPPORTED | SRC-001 |  | PHN-001; PHN-002 | Introduction/context | FG0 |  |

Paradigm: NOT YET DECIDED. Reason: the research problem and final research questions have not yet been established.

## Stage 1 — Phenomenon (`PHN`)

What is happening, where (locus), since when, and to whom. Evidence comes from the search-online track and registered data records.

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| PHN-001 | Korbrimob's 2025–2029 strategic plan documents a need to adapt to rapidly developing, increasingly complex information technology and directs capability development for technology- and data-analytics-based operations. | SUPPORTED | SRC-001; DEC-008 | CTX-001; CTX-003 | THR-003; GAP-002 | Introduction | FG0 |  |
| PHN-002 | The same strategic plan identifies limited modernization of personnel capability in mastery of communication technology for high-intensity public-safety operations. | SUPPORTED | SRC-001; DEC-008 | CTX-001; CTX-003 | THR-003; GAP-002 | Introduction | FG0 |  |

Locus: Korbrimob Polri. The Stage 1 phenomenon is institutional digital modernization/adaptation under high-intensity operational conditions; employee-level demands, resources, health outcomes, and organizational-capability outcomes remain to be established rather than assumed.

## Stage 2 — Theory (`THR`) and theory gaps (`GAP`)

Grand theory: **Job Demands–Resources Theory — VERIFIED at GRO-02** (original source `SRC-002`). Role at Stage 2: explanatory lens for demand/resource and health-impairment mechanisms; hypothesis-generator status remains deferred until research questions are established. Targeted theory verification used `PRM-001` and `RUN-001`–`RUN-005`; no Scopus/Web of Science development search was executed in that session.

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| THR-001 | JD-R theory treats work characteristics as job demands and job resources that have different implications for employee strain or burnout and motivation. | SUPPORTED | SRC-002; SRC-003; PRM-001 | PHN-001; PHN-002 | THR-002; THR-003 | Theory | FG1 |  |
| THR-002 | The JD-R health-impairment pathway provides a direct theoretical basis for examining burnout as a downstream employee-level condition under sustained demands and insufficient resources. | SUPPORTED | SRC-002; SRC-003 | THR-001 | GAP-001; LIT-001; LIT-002 | Theory | FG1 |  |
| THR-003 | Digitization can be represented within JD-R as both Digital Job Demands and Digital Job Resources rather than as an inherently harmful exposure. | SUPPORTED | SRC-004; SRC-005 | PHN-001; PHN-002; THR-001 | THR-004; GAP-002; LIT-005 | Theory | FG1 |  |
| THR-004 | Digital Job Demands are candidate demand characteristics arising from digital-technology use that require sustained effort and are conceptually distinct from strain or burnout responses. | SUPPORTED | SRC-004; SRC-005 | THR-003 | GAP-002; LIT-001 | Theory | FG1 |  |
| THR-005 | Perceived Organizational Support is an employee's global belief that the organization values the employee's contribution and cares about well-being, while Organizational Support Theory and social-exchange logic are construct-specific rather than an explanation of the whole candidate model. | SUPPORTED | SRC-006; SRC-007 | THR-001 | GAP-001; LIT-002 | Theory | FG1 |  |
| THR-006 | Organizational resilience is an organizational capability or process involving anticipation, coping, and adaptation rather than an individual psychological trait. | SUPPORTED | SRC-008 | PHN-001 | GAP-001; LIT-004; LIT-005; LIT-006 | Theory | FG1 |  |
| THR-007 | Conservation of Resources theory provides a plausible resource-loss explanation for stress, but the evidence inspected so far does not show a necessary organizing function beyond JD-R for the candidate demand/resource-to-burnout process. | INFERRED | SRC-009; SRC-002; SRC-003; DEC-013 | THR-001; THR-002 | GAP-001 | Theory | FG1 |  |

Constructs derived from the theory (basis of Stage 3 keyword development; not final study variables):

| Construct/domain | Definition/status | From `THR` | Keyword parameter set |
|---|---|---|---|
| Job demands | work characteristics requiring sustained effort; native JD-R category | THR-001; THR-002 | PRM-002 |
| Job resources | work characteristics/resources that support functioning and can reduce demand costs; native JD-R category | THR-001; THR-002 | PRM-002 |
| Burnout | employee-level health-impairment condition compatible with JD-R | THR-002 | PRM-002 |
| Digital Job Demands | bounded digital extension of the job-demand category | THR-003; THR-004 | PRM-002 |
| Perceived Organizational Support | OST-defined employee perception used as a candidate JD-R resource | THR-005 | PRM-002 |
| Organizational Resilience / POR boundary | true OR remains organizational-level; employee-rated POR is a distinct person-level perception domain | THR-006 | PRM-002 |

Theory gaps — what the theory has not explained or tested for this phenomenon:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| GAP-001 | The inspected JD-R and organizational-resilience theory sources do not establish a mechanism by which individual-level burnout becomes organizational-level resilience capability, so the cross-level bridge in the prior Ferry model remains theoretically unresolved. | INFERRED | SRC-002; SRC-003; SRC-008; DEC-012 | THR-002; THR-005; THR-006; THR-007 | GAP-004; LIT-006; LIT-007 | Theory/gap | FG1 |  |
| GAP-002 | Digital Job Demands are theoretically supported as a digital extension of JD-R, but their relevant content and boundary conditions in hierarchical high-reliability policing cannot be inferred from white-collar digital-work studies or from Korbrimob modernization evidence alone. | INFERRED | SRC-004; SRC-005; SRC-001 | PHN-001; PHN-002; THR-003; THR-004 | GAP-003 | Theory/gap | FG1 |  |

## Stage 3 — Empirical literature patterns (`LIT`) and research gaps (`GAP`)

Matrix: `literature/literature-review/matrix.md`. Search parameter set: `PRM-002`. Screening parameter set: `PRM-003`. Runs: `RUN-006`–`RUN-017`.

Patterns — what the literature agrees on, disputes, or has not examined:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| LIT-001 | Specific digital work demands or technostressors are repeatedly associated with exhaustion or burnout-related strain, but direct evidence using a distinct bounded DJD construct in policing remains sparse. | SUPPORTED | SRC-012; SRC-013; SRC-020; SRC-021; SRC-022; SRC-028; RUN-006; RUN-010 | THR-002; THR-004 | GAP-003 | Literature review / Introduction | FG1 |  |
| LIT-002 | POS or organizational support shows comparatively consistent negative associations with police burnout, emotional exhaustion, or stress, while buffering effects vary by support type and pathway. | SUPPORTED | SRC-012; SRC-014; SRC-018; SRC-019; SRC-021; RUN-007; RUN-010 | THR-002; THR-005 | LIT-006 | Literature review / Introduction | FG1 |  |
| LIT-003 | The focused corpus does not establish burnout as an antecedent or mediator of POR, and available evidence supports plausible reverse or common-cause configurations in which adaptive or resilient organizational conditions are associated with lower exhaustion or burnout. | SUPERSEDED | SRC-023; SRC-027; SRC-010; SRC-016; RUN-008 | GAP-001; THR-006 | LIT-006 | Literature review / gap | FG1 |  |
| LIT-004 | Employee-rated organizational resilience is empirically feasible, but POR remains heterogeneous and must be distinguished from true organizational resilience, readiness, agility, effectiveness, and individual resilience. | SUPPORTED | SRC-010; SRC-016; SRC-024; RUN-011 | THR-006 | GAP-005 | Literature review / measurement boundary | FG1 |  |
| LIT-005 | Digitalization has a dual empirical position because employee-level digital demands can generate strain while organization-level digital capabilities can strengthen adaptation and true organizational resilience. | SUPPORTED | SRC-020; SRC-022; SRC-024; SRC-025; SRC-026; RUN-009 | THR-003; THR-006 | GAP-003; LIT-006 | Literature review / Introduction | FG1 |  |
| LIT-006 | The targeted directionality audit shows an asymmetric empirical pattern in which collective or organizational adaptive/resilience conditions are more often positioned upstream of employee health and well-being than burnout is positioned upstream of employee-rated organizational resilience, including longitudinal or multilevel evidence from crisis, public-sector, military, and first-responder contexts. | SUPPORTED | SRC-023; SRC-027; SRC-029; SRC-030; SRC-031; SRC-032; SRC-033; RUN-012; RUN-013; RUN-014; RUN-015; RUN-016; DEC-018 | GAP-001; THR-006; LIT-002; LIT-003; LIT-005 | GAP-005; LIT-007 | Literature review / model revision | FG1 | LIT-003 |
| LIT-007 | Burnout or emotional exhaustion can be associated with performance-, citizenship-, or safety-relevant behaviors and outcomes in some studies, but mixed or null findings and construct mismatch mean that this evidence does not establish a Burnout→POR pathway or a causal bottom-up organizational-resilience mechanism. | INFERRED | SRC-030; SRC-034; SRC-035; SRC-036; RUN-017; DEC-018 | GAP-001; LIT-006 | GAP-005 | Literature review / mechanism boundary | FG1 |  |

Research gaps — provisional unresolved empirical problems from the focused search:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| GAP-003 | The focused Stage 3 search did not identify a policing or high-reliability study that cleanly isolates a bounded DJD construct from general operational workload and digital-skill mismatch while testing burnout. | INFERRED | RUN-006; RUN-010; SRC-013; SRC-020; SRC-022; SRC-028; PRM-002; PRM-003 | GAP-002; LIT-001; LIT-005 |  | Literature gap / Introduction | FG1 |  |
| GAP-004 | The focused Stage 3 corpus does not establish burnout as an antecedent or mediator of POR and contains credible reverse-direction evidence linking resilient or adaptive organizational conditions with lower exhaustion or burnout. | SUPERSEDED | RUN-008; RUN-012; RUN-013; RUN-014; RUN-015; RUN-016; RUN-017; SRC-023; SRC-027; SRC-029; SRC-030; SRC-031; SRC-032; SRC-033; SRC-034; SRC-035; SRC-036; DEC-018 | GAP-001; LIT-003 | LIT-006; LIT-007 | Literature gap / model revision | FG1 |  |
| GAP-005 | The construct and measurement distinctness of POR from POS, perceived readiness or agility, and general organizational-effectiveness perceptions remains unresolved for policing. | INFERRED | RUN-011; SRC-010; SRC-016; SRC-024; LIT-004 | THR-006; LIT-004; LIT-006; LIT-007 |  | Literature gap / measurement | FG1 |  |

Stage 3 decision: **`GAP-004` is resolved as `RESOLVED-REVISE-MODEL` under `DEC-018`.** The working architecture no longer locks `Burnout → POR` or `DJD/POS → Burnout → POR`; Burnout remains a health-impairment construct, while POR remains only a separate candidate outcome domain pending `GAP-005`. GRO-03 remains **REVISE / NOT VERIFIED** until the downstream outcome architecture is resolved and Stage 3 parity/citation-chasing limits are addressed.

## Stage 4 — State of the art, novelty (`NOV`), research questions (`RQ`), contribution (`CTB`), implications promised (`IMP`)

State of the art = Phenomenon × (Theory + Literature): NOT YET FILLED pending resolution of the downstream outcome architecture (`GAP-005`) and remaining Stage 3 parity/citation-chasing checks; `GAP-004` is not to be promoted as an artificial novelty claim.

Novelty — the position of this study relative to the state of the art; it must answer a theory gap, a research gap, or both:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|

Research questions — derived from the results of the theoretical review and the novelty; each traces to a named gap; format follows the approach (central question and sub-questions; hypotheses; quantitative, qualitative, and integration questions):

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|

Contribution statement — one sentence, restated in the title, abstract, end of introduction, and discussion:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|

Implications promised — theoretical (to Stage 2) and practical (to the locus), each with the actor named; every promised implication is delivered or withdrawn in Stage 7:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|

Urgency — why now: the current strategic period explicitly includes technology adaptation and technology/data-analytics-based operational development (`SRC-001`), but scholarly urgency and contribution remain unestablished.

FG1 check — the chain Phenomenon → Theory → Gap → Novelty → RQ is connected without a jump and relevant: NOT ASSESSED.

## Stage 5 — Method (`MTH`)

Method decision record: NOT YET FILLED (status `PROPOSED` / `APPROVED`). Paradigm confirmed against the RQ: NOT ASSESSED. Reporting standard parameter set(s): NOT YET FILLED.

Method statements follow the decision order — approach, method/design, data types, data sources, collection, analysis (including cleaning), ethics — and link the `DEC` and `PRM` records behind them:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|

Claims this design can support: NOT YET FILLED. Claims this design cannot support: NOT YET FILLED.

## Stage 6 — Findings (`FND`)

A finding is an empirical result that answers a research question. It is not compared with the literature here.

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|

RQ ↔ finding ↔ data matrix — every RQ answered, every finding traceable:

| RQ | Answered by (`FND`) | Data and runs (`DAT`, `RUN`) | Interpretation standpoint (theory / participant / researcher) | Answered? |
|---|---|---|---|---|

FG3 check — every RQ is answered by findings traceable to data: NOT ASSESSED. No manuscript outline before this is READY.

## Stage 7 — Discussion (`DIS`), limitations (`LIM`), conclusions (`CCL`), implications delivered (`IMP`)

Findings against theory — for each theory statement: confirmed, extended, or not relevant/contradicted in this context:

| `THR` | Read against (`FND`) | Outcome | `DIS` |
|---|---|---|---|

Discussion statements — dialogue with literature in order: finding → supports which `LIT` → differs where → why → what this study adds → limit of interpretation:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|

Conclusions — one per research question:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|

Limitations — each names the conclusion or implication it weakens and what was done about it:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|

Implications delivered — matched to the implications promised in Stage 4, actor named:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|

Further research — follows from the limitations: NOT YET FILLED.

## Stage 8 — Manuscript map

Outline: `manuscript/outline.md` (written only after FG3 is READY). Each paragraph in the outline names the statements it carries; this table records where the contribution statement and the research questions appear.

| Statement | Title | Abstract | Introduction | Method | Results | Discussion | Conclusion |
|---|---|---|---|---|---|---|---|

Terminology — one term per concept across all sections:

| Concept | Term used | Rejected variants |
|---|---|---|

## Coherence check

Complete before FG1, FG3, and FG4. Status: PASS / FAIL / NOT ASSESSED, with the IDs affected.

| Check | Rule | Status | IDs affected |
|---|---|---|---|
| Phenomenon feeds forward | every `PHN` has a downstream `THR`, `GAP`, or `NOV` | PASS for current Stage 2 links | PHN-001; PHN-002 |
| Theory does work | every `THR` is used by a `DIS` in Stage 7 or explicitly found not relevant | NOT ASSESSED | THR-001–THR-007 |
| Gaps are motivated | every live `GAP` has upstream `THR` or `LIT` and downstream `NOV` or `RQ`; `GAP-004` is superseded by model revision | NOT ASSESSED | GAP-001–GAP-005 |
| Questions are grounded | every `RQ` has upstream `GAP` and `NOV` | NOT ASSESSED | |
| Questions are answered | every `RQ` has at least one `FND` (FG3) and one `CCL` (FG4) | NOT ASSESSED | |
| Findings have evidence | every `FND` lists at least one `DAT` or `RUN` | NOT ASSESSED | |
| Discussion is a dialogue | every `DIS` has upstream `FND` and `THR` or `LIT` | NOT ASSESSED | |
| Promises are kept | every promised `IMP` has a delivering `IMP` or a recorded withdrawal | NOT ASSESSED | |
| Limitations bite | every `LIM` names the `CCL` or `IMP` it weakens | NOT ASSESSED | |
| Method traces | every `MTH` links a `DEC` or `PRM` | NOT ASSESSED | |
| Manuscript is mapped | every paragraph in the outline maps to at least one statement | NOT ASSESSED | |
| No dangling links | validator passes; coherence report shows no dangling or orphan IDs | NOT ASSESSED | |

A PASS here is a mechanical and structural result. It is not an academic quality gate; those are assessed in `reviews/`.