# Brain — Coherence Anchor

Project: Ferry doctoral dissertation — Korbrimob Polri.
Builder version: 0.3.0. Mode: RESEARCH.
Last synced commit: 6e6fcf2b35bae45e2fab729abae32c3a75ae1833 (Issue #50 working-branch checkpoint before final FG1 coherence sync). Synced by: ChatGPT research agent, 2026-10-11.

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
| CTX-001 | The dissertation research locus is Korbrimob Polri, with personnel as the candidate study population while the final unit of analysis remains undecided. | SUPERSEDED | DEC-006; DEC-007 |  | CTX-004 | Introduction | FG0 |  |
| CTX-002 | This copied workspace is governed in RESEARCH mode and substantive changes must follow the Issue → branch → PR workflow. | KNOWN | DEC-006 |  |  | Project governance | FG0 |  |
| CTX-003 | The current institutional strategic context is the Korbrimob Polri 2025–2029 strategic plan established by KEP/299/V/2025 dated 23 May 2025. | SUPPORTED | SRC-001 |  | PHN-001; PHN-002 | Introduction/context | FG0 |  |
| CTX-004 | For the verified GRO-05 framing, the substantive unit of analysis is individual Korbrimob personnel, with bounded Digital Job Demands, Perceived Organizational Support, Burnout, and Adaptive Performance treated as person-level constructs or outcomes. | KNOWN | DEC-023 | CTX-001 | PHN-001; PHN-002; RQ-001; RQ-002; RQ-003 | Introduction / Method framing | FG1 | CTX-001 |

Paradigm: NOT YET DECIDED. Reason: the research questions and person-level unit are now verified, but paradigm/design selection belongs to Stage 5 and must follow the verified question set rather than be back-filled into the framing.

## Stage 1 — Phenomenon (`PHN`)

What is happening, where (locus), since when, and to whom. Evidence comes from the search-online track and registered data records.

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| PHN-001 | Korbrimob's 2025–2029 strategic plan documents a need to adapt to rapidly developing, increasingly complex information technology and directs capability development for technology- and data-analytics-based operations. | SUPPORTED | SRC-001; DEC-008 | CTX-004; CTX-003 | THR-003; GAP-002 | Introduction | FG0 |  |
| PHN-002 | The same strategic plan identifies limited modernization of personnel capability in mastery of communication technology for high-intensity public-safety operations. | SUPPORTED | SRC-001; DEC-008 | CTX-004; CTX-003 | THR-003; GAP-002 | Introduction | FG0 |  |

Locus: Korbrimob Polri. The Stage 1 phenomenon is institutional digital modernization/adaptation under high-intensity operational conditions; employee-level demands, resources, health outcomes, and organizational-capability outcomes remain to be established rather than assumed.

## Stage 2 — Theory (`THR`) and theory gaps (`GAP`)

Grand theory: **Job Demands–Resources Theory — VERIFIED at GRO-02** (original source `SRC-002`). Role at Stage 2: explanatory lens for demand/resource and health-impairment mechanisms; its hypothesis-generator role now supports the verified GRO-05 directional association expectations, subject to Stage 5 design and identification limits. Targeted theory verification used `PRM-001` and `RUN-001`–`RUN-005`; no Scopus/Web of Science development search was executed in that session.

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
| GAP-002 | Digital Job Demands are theoretically supported as a digital extension of JD-R, but their relevant content and boundary conditions in hierarchical high-reliability policing cannot be inferred from white-collar digital-work studies or from Korbrimob modernization evidence alone. | INFERRED | SRC-004; SRC-005; SRC-001 | PHN-001; PHN-002; THR-003; THR-004 | GAP-003; GAP-007 | Theory/gap | FG1 |  |

## Stage 3 — Empirical literature patterns (`LIT`) and research gaps (`GAP`)

Matrix: `literature/literature-review/matrix.md`. Search parameter sets: `PRM-002`; `PRM-004`; `PRM-005`; `PRM-006`. Screening parameter set: `PRM-003`. Runs: `RUN-006`–`RUN-040`.

Patterns — what the literature agrees on, disputes, or has not examined:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| LIT-001 | Specific digital work demands or technostressors are repeatedly associated with exhaustion or burnout-related strain, but direct evidence using a distinct bounded DJD construct in policing remains sparse. | SUPPORTED | SRC-012; SRC-013; SRC-020; SRC-021; SRC-022; SRC-028; RUN-006; RUN-010 | THR-002; THR-004 | GAP-003; GAP-007 | Literature review / Introduction | FG1 |  |
| LIT-002 | POS or organizational support shows comparatively consistent negative associations with police burnout, emotional exhaustion, or stress, while buffering effects vary by support type and pathway. | SUPPORTED | SRC-012; SRC-014; SRC-018; SRC-019; SRC-021; RUN-007; RUN-010 | THR-002; THR-005 | LIT-006; LIT-011; GAP-007 | Literature review / Introduction | FG1 |  |
| LIT-003 | The focused corpus does not establish burnout as an antecedent or mediator of POR, and available evidence supports plausible reverse or common-cause configurations in which adaptive or resilient organizational conditions are associated with lower exhaustion or burnout. | SUPERSEDED | SRC-023; SRC-027; SRC-010; SRC-016; RUN-008 | GAP-001; THR-006 | LIT-006 | Literature review / gap | FG1 |  |
| LIT-004 | Employee-rated organizational resilience is empirically feasible, but POR remains heterogeneous and must be distinguished from true organizational resilience, readiness, agility, effectiveness, and individual resilience. | SUPPORTED | SRC-010; SRC-016; SRC-024; RUN-011 | THR-006 | GAP-005; LIT-008 | Literature review / measurement boundary | FG1 |  |
| LIT-005 | Digitalization has a dual empirical position because employee-level digital demands can generate strain while organization-level digital capabilities can strengthen adaptation and true organizational resilience. | SUPPORTED | SRC-020; SRC-022; SRC-024; SRC-025; SRC-026; RUN-009 | THR-003; THR-006 | GAP-003; LIT-006; LIT-013; GAP-007 | Literature review / Introduction | FG1 |  |
| LIT-006 | The targeted directionality audit shows an asymmetric empirical pattern in which collective or organizational adaptive/resilience conditions are more often positioned upstream of employee health and well-being than burnout is positioned upstream of employee-rated organizational resilience, including longitudinal or multilevel evidence from crisis, public-sector, military, and first-responder contexts. | SUPPORTED | SRC-023; SRC-027; SRC-029; SRC-030; SRC-031; SRC-032; SRC-033; RUN-012; RUN-013; RUN-014; RUN-015; RUN-016; DEC-018 | GAP-001; THR-006; LIT-002; LIT-003; LIT-005 | GAP-005; LIT-007; LIT-009 | Literature review / model revision | FG1 | LIT-003 |
| LIT-007 | Burnout or emotional exhaustion can be associated with performance-, citizenship-, or safety-relevant behaviors and outcomes in some studies, but mixed or null findings and construct mismatch mean that this evidence does not establish a Burnout→POR pathway or a causal bottom-up organizational-resilience mechanism. | INFERRED | SRC-030; SRC-034; SRC-035; SRC-036; RUN-017; DEC-018 | GAP-001; LIT-006 | GAP-005; GAP-006; LIT-011 | Literature review / mechanism boundary | FG1 |  |
| LIT-008 | Recent scale-development evidence shows that organizational resilience can be measured with increasingly explicit ability/process structures through employee reports, so measurement immaturity alone is not a sufficient reason to reject POR. | SUPPORTED | SRC-037; SRC-038; RUN-018; RUN-023 | THR-006; LIT-004 | GAP-005 | Literature review / outcome audit | FG1 |  |
| LIT-009 | Readiness and organizational agility have mature public-sector and some direct police evidence, but readiness is typically tied to a specific change/emergency and agility is commonly positioned as an organizational resource/capability upstream of employee outcomes. | SUPPORTED | SRC-029; SRC-039; SRC-040; SRC-041; SRC-044; SRC-045; RUN-019; RUN-020; RUN-026; RUN-027 | LIT-004; LIT-006 | GAP-005 | Literature review / outcome audit | FG1 |  |
| LIT-010 | Adaptive Performance has a mature person-level literature, public-sector evidence and an Indonesian validated scale, giving it stronger level and field alignment for Ferry than employee-rated organizational capability outcomes, while direct policing-specific relation evidence remains limited. | INFERRED | SRC-001; SRC-042; SRC-043; SRC-046; RUN-021; RUN-024; RUN-025; RUN-028; DEC-019 | PHN-001; PHN-002; THR-001; LIT-007; LIT-009 | GAP-006; LIT-012; GAP-007 | Literature review / outcome audit | FG1 |  |
| LIT-011 | Longitudinal police JD-R evidence and broader police/meta-analytic performance evidence support strong demand/resource–burnout relations and a modest adverse burnout–performance association, but they do not identify Burnout as a mediator of Adaptive Performance in policing. | SUPPORTED | SRC-048; SRC-049; SRC-050; SRC-051; RUN-031; RUN-032; RUN-033; DEC-020 | LIT-002; LIT-007; LIT-010 | GAP-006; GAP-007 | Literature review / relation architecture | FG1 |  |
| LIT-012 | Organizational support/POS is positively associated with Adaptive Performance in broader organizational evidence, with job crafting, engagement and self-efficacy appearing as plausible mechanisms, while direct policing-specific POS–Adaptive Performance evidence remains limited. | SUPPORTED | SRC-052; SRC-053; RUN-030; RUN-034; DEC-020 | THR-005; LIT-010 | GAP-006; GAP-007 | Literature review / relation architecture | FG1 |  |
| LIT-013 | Digital or general job demands do not have a uniformly negative performance implication because challenge/hindrance appraisal can produce divergent adaptation and performance responses, so the sign of DJD–Adaptive Performance should remain open until demand content is bounded. | SUPPORTED | SRC-054; SRC-055; RUN-029; RUN-035; DEC-020 | THR-003; THR-004; LIT-005; LIT-010 | GAP-003; GAP-006; GAP-007 | Literature review / relation architecture | FG1 |  |
| LIT-014 | Direct police evidence already links organizational support and technology difficulty with officer stress/well-being, and longitudinal police-change evidence already links resources, challenge seeking and job crafting with adaptivity, so neither a generic digital-stress relation nor a resource→adaptivity relation is novel by itself. | SUPPORTED | SRC-057; SRC-062; SRC-063; RUN-036; RUN-037; RUN-040 | LIT-002; LIT-010; LIT-012 | GAP-007; NOV-001 | Literature review / novelty boundary | FG1 |  |
| LIT-015 | Broader digital-work evidence differentiates digital demand content and shows divergent challenge/hindrance implications for behavior and Adaptive Performance, while a recent PRESISI-linked public-sector study already combines technostress, burnout/engagement and generic performance; these counterexamples narrow Ferry's contribution to construct-bounded asymmetric outcomes rather than a variable-combination claim. | SUPPORTED | SRC-058; SRC-059; SRC-060; SRC-061; RUN-036; RUN-038; RUN-039; DEC-021 | THR-003; THR-004; LIT-013 | GAP-007; NOV-001 | Literature review / novelty boundary | FG1 |  |

Research gaps — provisional unresolved empirical problems from the focused search:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| GAP-003 | The focused Stage 3 search did not identify a policing or high-reliability study that cleanly isolates a bounded DJD construct from general operational workload and digital-skill mismatch while testing burnout. | SUPERSEDED | RUN-006; RUN-010; SRC-013; SRC-020; SRC-022; SRC-028; PRM-002; PRM-003 | GAP-002; LIT-001; LIT-005; LIT-013 | GAP-007 | Literature gap / Introduction | FG1 |  |
| GAP-004 | The focused Stage 3 corpus does not establish burnout as an antecedent or mediator of POR and contains credible reverse-direction evidence linking resilient or adaptive organizational conditions with lower exhaustion or burnout. | SUPERSEDED | RUN-008; RUN-012; RUN-013; RUN-014; RUN-015; RUN-016; RUN-017; SRC-023; SRC-027; SRC-029; SRC-030; SRC-031; SRC-032; SRC-033; SRC-034; SRC-035; SRC-036; DEC-018 | GAP-001; LIT-003 | LIT-006; LIT-007 | Literature gap / model revision | FG1 |  |
| GAP-005 | The construct and measurement distinctness of POR from POS, perceived readiness or agility, and general organizational-effectiveness perceptions remains unresolved for policing. | SUPERSEDED | RUN-011; RUN-018; RUN-019; RUN-020; RUN-021; RUN-022; RUN-023; RUN-024; RUN-025; RUN-026; RUN-027; RUN-028; SRC-010; SRC-016; SRC-024; SRC-037; SRC-038; SRC-039; SRC-040; SRC-041; SRC-042; SRC-043; SRC-044; SRC-045; SRC-046; SRC-047; DEC-019 | THR-006; LIT-004; LIT-006; LIT-007 | LIT-008; LIT-009; LIT-010; GAP-006 | Literature gap / outcome architecture | FG1 |  |
| GAP-006 | The specific direct, indirect, reverse and rival relations linking bounded Digital Job Demands, POS, Burnout and individual Adaptive Performance in policing or comparable high-reliability work were under-reconstructed before the Issue #41 relation audit. | SUPERSEDED | PRM-005; RUN-029; RUN-030; RUN-031; RUN-032; RUN-033; RUN-034; RUN-035; SRC-048; SRC-049; SRC-050; SRC-051; SRC-052; SRC-053; SRC-054; SRC-055; SRC-056; DEC-020 | LIT-001; LIT-002; LIT-007; LIT-010 | LIT-011; LIT-012; LIT-013 | Literature gap / relation audit | FG1 |  |
| GAP-007 | In the inspected corpus, high-intensity policing evidence does not yet establish which digital-demand contents are distinct from ordinary operational workload and digital-skill mismatch or whether those bounded demands show asymmetric relations with Burnout and Adaptive Performance alongside POS; the unresolved problem is therefore one of construct boundary and divergent outcomes rather than simple literature absence. | INFERRED | PRM-006; RUN-036; RUN-037; RUN-038; RUN-039; RUN-040; SRC-057; SRC-058; SRC-059; SRC-060; SRC-061; SRC-062; SRC-063; DEC-021 | GAP-002; LIT-011; LIT-012; LIT-013; LIT-014; LIT-015 | NOV-001 | Literature gap / novelty | FG1 | GAP-003 |

Stage 3 decision remains **`GAP-006 = RESOLVED-PARALLEL-ASYMMETRIC` under `DEC-020`**, now followed by the Stage 4 refinement of `GAP-003` into `GAP-007`. The working architecture retains DJD–Burnout and POS–Burnout as the strongest health-impairment relations, POS–Adaptive Performance and Burnout–Adaptive Performance as qualified associations, and leaves DJD–Adaptive Performance direction open because challenge/hindrance evidence is mixed. Burnout mediation is not restored.

## Stage 4 — State of the art, novelty (`NOV`), research questions (`RQ`), contribution (`CTB`), implications promised (`IMP`)

State of the art = Phenomenon × (Theory + Literature): direct police research already covers technology difficulty/support and stress/well-being, and longitudinal police-change research already covers resource/challenge processes and adaptivity; outside policing, digital JD-R studies already differentiate digital demand content and show double-edged health/performance implications. The defensible unresolved problem is therefore not a new-variable or new-location claim but the boundary and asymmetric consequences of a clearly bounded digital-demand domain under high-intensity policing modernization (`GAP-007`).

Novelty — the position of this study relative to the state of the art; it must answer a theory gap, a research gap, or both:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| NOV-001 | Ferry's defensible novelty is a provisional theory-boundary, construct-clarification and empirical-pattern test of whether a clearly bounded digital job-demand domain, distinguished from general operational workload and digital-skill mismatch, shows asymmetric relations with Burnout and Adaptive Performance alongside POS in high-intensity policing, rather than a claim of a new grand theory, unique context or exact variable combination. | INFERRED | DEC-021; PRM-006; RUN-036; RUN-037; RUN-038; RUN-039; RUN-040; SRC-057; SRC-058; SRC-059; SRC-060; SRC-061; SRC-062; SRC-063 | GAP-007; THR-003; THR-004; LIT-014; LIT-015 | RQ-001; RQ-002; RQ-003; CTB-001 | Introduction / novelty | FG1 |  |

Research questions — derived from the results of the theoretical review and the novelty; each traces to a named gap; the current wording is VERIFIED at GRO-05 and remains associative rather than causal:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| RQ-001 | Sejauh mana Tuntutan Kerja Digital yang relevan bagi personel Korbrimob Polri dapat dibedakan secara empiris dari beban kerja operasional umum dan ketidakcocokan keterampilan digital? | KNOWN | DEC-022; DEC-023 | GAP-007; NOV-001; GAP-002 | CTB-001; IMP-001 | Introduction / RQ | FG1 |  |
| RQ-002 | Bagaimana hubungan Tuntutan Kerja Digital yang telah dibatasi secara konseptual dan Perceived Organizational Support dengan Burnout pada personel Korbrimob Polri? | KNOWN | DEC-022; DEC-023 | GAP-007; NOV-001; THR-002; THR-005; LIT-001; LIT-002 | CTB-001; IMP-001; IMP-002 | Introduction / RQ | FG1 |  |
| RQ-003 | Bagaimana hubungan Tuntutan Kerja Digital yang telah dibatasi secara konseptual, Perceived Organizational Support, dan Burnout dengan Adaptive Performance pada personel Korbrimob Polri? | KNOWN | DEC-022; DEC-023 | GAP-007; NOV-001; LIT-010; LIT-011; LIT-012; LIT-013 | CTB-001; IMP-001; IMP-002 | Introduction / RQ | FG1 |  |

Working directional expectations under `DEC-022` are associative, not causal: DJD–Burnout (+), POS–Burnout (−), POS–Adaptive Performance (+), and Burnout–Adaptive Performance (−). DJD–Adaptive Performance remains exploratory/open; Burnout mediation and POS moderation are not restored.

Contribution statement — one sentence, restated in the title, abstract, end of introduction, and discussion only if later design/findings continue to support it:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| CTB-001 | Penelitian Ferry berkontribusi dengan menguji batas penerapan digital JD-R pada high-intensity policing melalui pembedaan tuntutan kerja digital dari beban operasional umum dan ketidakcocokan keterampilan digital serta pengujian pola hubungan asimetrisnya dengan Burnout dan Adaptive Performance bersama POS sebagai sumber daya organisasi yang dipersepsikan. | INFERRED | DEC-021; DEC-022; DEC-023 | NOV-001; RQ-001; RQ-002; RQ-003 | IMP-001; IMP-002 | Title / Abstract / Introduction / Discussion | FG1 |  |

Implications promised — theoretical (to Stage 2) and practical (to the locus), each with the actor named; every promised implication is delivered or withdrawn in Stage 7:

| ID | Statement | Status | Evidence | Upstream | Downstream | Manuscript | Gate | Supersedes |
|---|---|---|---|---|---|---|---|---|
| IMP-001 | Bagi literatur JD-R dan digital JD-R, penelitian ini menjanjikan klarifikasi tentang batas konstruk Tuntutan Kerja Digital dan perlunya membedakan konsekuensi health-impairment dari Adaptive Performance tanpa mengasumsikan semua digital demands bersifat merugikan. | INFERRED | DEC-021; DEC-022; DEC-023 | CTB-001; THR-003; THR-004; RQ-001; RQ-002; RQ-003 |  | Introduction / Discussion | FG1 |  |
| IMP-002 | Bagi pimpinan dan fungsi SDM Korbrimob Polri, penelitian ini menjanjikan dasar empiris untuk membedakan tuntutan digital spesifik yang terkait dengan strain dari kondisi dukungan yang terkait dengan fungsi adaptif, dengan rekomendasi akhir tetap dibatasi oleh desain dan hasil penelitian. | INFERRED | DEC-022; DEC-023 | CTX-003; PHN-001; PHN-002; CTB-001; RQ-002; RQ-003 |  | Introduction / Discussion | FG1 |  |

Urgency — why now: the current strategic period explicitly includes technology adaptation and technology/data-analytics-based operational development (`SRC-001`); the scholarly urgency is tied to resolving the digital-demand boundary and health-versus-adaptation tension rather than assuming digitalization is harmful.

FG1 check — **READY** under the formal Issue #50 gate review: G1, G2, and G3 are READY for the bounded framing. `DEC-024` limits G2 to a focused evidence reconstruction rather than systematic/comprehensive coverage. This closes the FG1 framing gate itself but does not override the upstream FG0 Context gate, which remains NOT ASSESSED; Stage 5 method selection therefore remains blocked until FG0 is assessed and closed.

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
| Gaps are motivated | every live `GAP` has upstream `THR` or `LIT` and downstream `NOV` or `RQ`; `GAP-004`–`GAP-006` are superseded and `GAP-003` is refined by `GAP-007` | PASS for current live novelty chain | GAP-007; NOV-001 |
| Questions are grounded | every `RQ` has upstream `GAP` and `NOV` | PASS for verified RQs | RQ-001; RQ-002; RQ-003 |
| Questions are answered | every `RQ` has at least one `FND` (FG3) and one `CCL` (FG4) | NOT ASSESSED | RQ-001; RQ-002; RQ-003 |
| Findings have evidence | every `FND` lists at least one `DAT` or `RUN` | NOT ASSESSED | |
| Discussion is a dialogue | every `DIS` has upstream `FND` and `THR` or `LIT` | NOT ASSESSED | |
| Promises are kept | every promised `IMP` has a delivering `IMP` or a recorded withdrawal | NOT ASSESSED | IMP-001; IMP-002 |
| Limitations bite | every `LIM` names the `CCL` or `IMP` it weakens | NOT ASSESSED | |
| Method traces | every `MTH` links a `DEC` or `PRM` | NOT ASSESSED | |
| Manuscript is mapped | every paragraph in the outline maps to at least one statement | NOT ASSESSED | |
| No dangling links | validator passes; coherence report shows no dangling or orphan IDs | NOT ASSESSED pending Issue #50 PR validation | CTX-004; RQ-001; RQ-002; RQ-003; CTB-001; IMP-001; IMP-002 |

A PASS here is a mechanical and structural result. It is not an academic quality gate; those are assessed in `reviews/`.