# AI Use Log

Record substantive AI use without including sensitive data. This log helps researchers prepare disclosures according to institutional or publisher policy; it does not replace those policies.

| Date | Tool/model | Task | Safe inputs | Outputs | Actual verification | Human responsible |
|---|---|---|---|---|---|---|
| 2026-09-07 | Codex; exact model identity not recorded | Prepared the initial builder and skills | User instructions, prior template structure, public standards sources | Project rules, skills, and working templates | Agent checked structure/links/frontmatter before commit; no human academic review was performed | NOT YET DESIGNATED |
| 2026-10-11 | ChatGPT (GPT-5.6 Sol) with GitHub connector | Initialized Ferry research workspace and Stage 0–1 framing | User-provided Ferry project context; repository rules; user-supplied Renstra Korbrimob 2025–2029; availability of prior literature matrices | Issue #1; RESEARCH-mode project brief; `SRC-001`; framing memo; initial `brain.md` context/phenomenon statements; research status; GRO-01 in PR #2 | Agent checked source claims against inspected Renstra passages and kept theory/method/novelty undecided; repository mechanical validation not yet run in this session; researcher verification of GRO-01 pending | Researcher NOT YET RECORDED |
| 2026-10-11 | ChatGPT (GPT-5.6 Sol) with GitHub connector | Verified GRO-04 continuation and framed GRO-05 research questions/hypotheses | Verified repository theory/literature/novelty statements, Issue #44 outputs, quality-gate rules, and researcher continuation approval | Issue #47; `DEC-022`; `RQ-001`–`RQ-003`; `CTB-001`; `IMP-001`–`IMP-002`; Stage 4 RQ memo; pre-FG1 audit; GRO-05 report | Agent traced each question to `GAP-007`/`NOV-001`, preserved non-causal wording, retained mixed DJD→Adaptive Performance direction, and withheld formal FG1 READY while GRO-05 and database parity remained unresolved | Researcher verification of GRO-05 pending |
| 2026-10-11 | ChatGPT (GPT-5.6 Sol) with GitHub connector | Recorded GRO-05 verification, locked person-level unit, and performed formal FG1 framing review | Researcher continuation approval; GRO/brain/project brief; gate rules; search/screening parameters; 35 logged empirical/novelty runs; matrix/source notes; closest/counterevidence and prior gate review | Issue #50; `DEC-023`; `DEC-024`; verified GRO-05; formal G1/G2/G3→FG1 review; updated coherence/status/project brief | Agent inspected the claimed review type against G2 rather than treating Scopus/WoS as a universal requirement; G1/G2/G3 and FG1 were assessed READY within a bounded scope. The agent separately identified upstream FG0 as still NOT ASSESSED, so Stage 5 remains blocked until that context gate is assessed. Repository PR validation pending | Researcher verified GRO-05 through explicit continuation approval; gate decision is agent review only |

For later entries, add corrections, limits of use, and the location of human verification when it actually occurs. Do not claim that AI use has institutional approval until the applicable policy has been verified.

## Builder identity update — 7 September 2026

Codex assisted with renaming the repository and drafting README usage guidance from user instructions. The project brief and standards register were made reusable for new projects. The agent checked local links, naming consistency, the remote repository, and Git synchronization state. No human academic review or substantive research was performed.

## Workflow and canonical-instruction update — 7 September 2026

Codex prepared the required-Issue workflow, cross-session checkpoints, and PR integration rules. The user clarified that upstream template maintenance may be performed directly, while copied RESEARCH projects require Issue/PR workflow. A duplicate instruction entrypoint was removed so `AGENTS.md` remains canonical. These checks concerned documentation and skill format, not supervisor review or empirical research.

## Research-infrastructure update — 7 September 2026

Codex added epistemic Issue/PR schemas, repository-integrity checks, provenance rules, versioning/migrations, a synthetic golden example, diagnostic quality gates, and multi-agent adapters. GitHub Actions mechanical validation passed before merge. This was repository engineering, not academic validation of a real study.

## Global-English documentation update — 7 September 2026

Codex translated repository documentation, templates, skills, examples, and project scaffolding to English for global portability. The language policy remains project-configurable: research outputs may be Indonesian, English, bilingual, or multilingual. Translation of repository instructions does not change the epistemic status of any research claim.

## Research flow, anchors, and reporting parameters — 17 September 2026

Claude Opus 5 (Claude Code) restructured the builder into a research flow with flow gates, added `GRO.md` as the direction anchor and `brain.md` as the coherence anchor, introduced `DAT`/`PRM`/`RUN` records with three literature tracks, made reporting standards parameters selected by the design, and added writing-standards and specialist-methodology registers. The agent checked repository links, skill frontmatter, identifier resolution, and GRO section discipline with `scripts/validate_repository.py`, and exercised the new checks against deliberately broken sections to confirm they fail. Reporting-standard item lists are paraphrases that each project must verify against the official checklist. This was repository engineering; no academic validation, human review, or empirical research was performed.

## Title, abstract, display items, and language default — 17 September 2026

Claude Opus 5 (Claude Code) added title, abstract, and keyword rules following Scopus and Web of Science indexing conventions and the abstract checklists of the reporting standards, with presets for PRISMA 2020 for Abstracts and CONSORT for Abstracts; added figures-and-tables rules; strengthened Stage 8 with an evidence-order drafting sequence and recorded outlet limits; and set English as the default research-output language, with another language used only on an explicit recorded instruction. Checklist item wording is a paraphrase that each project must verify against the official source. Repository integrity checks passed. This was repository engineering; no academic validation or human review was performed.

## Revision cycle — 17 September 2026

Claude Opus 5 (Claude Code) added Stage 9 and the gate FG5 for revision: a verbatim intake of reviewer comments, decomposition into numbered revision points, a column for the concern behind each comment marked confirmed or inferred, routing to the layer each point hits so that design and framing objections reopen their flow gate instead of being edited, a justification for every change, and a point-by-point response letter built from the table. Reviewer comments are treated as material to be answered rather than instructions to be executed. Repository integrity checks passed. No real reviewer comments were processed and no academic judgment was made.

## Entry-document consistency pass — 17 September 2026

Claude Opus 5 (Claude Code) reconciled the entry documents with the final 0.3.0 state: corrected stale stage counts and flow-gate ranges across `AGENTS.md`, `README.md`, and the docs; removed a duplicate stage table from `README.md`; replaced leftover vocabulary from a superseded GRO model; and added an explicit description of the mechanism — what triggers what, what each gate blocks, and where the researcher's judgment enters — so that a human reader and an agent can follow the same account. The changelog entry for 0.3.0 was rewritten to match the shipped state and now records the known limits. Repository integrity checks passed. Documentation only; no research artifact was changed.

## Ferry research initialization — 11 October 2026

ChatGPT initialized the copied Ferry repository as a RESEARCH workspace under Issue #1 and draft PR #2. It used only project information already supplied by the researcher and inspected Stage 1 institutional evidence from the user-supplied Renstra. The current working title and prior four-construct model were preserved as candidates rather than treated as approved scientific decisions. No theory, research question, method, measurement instrument, causal effect, novelty, ethics approval, or participant access was established. GRO-01 was reported for researcher verification and must not be treated as verified until the researcher records that decision.

## Stage 4 RQ framing — 11 October 2026

ChatGPT interpreted the researcher’s explicit continuation approval after the GRO-04 verification request as verification of that section, then translated `GAP-007` and `NOV-001` into three bounded association-based research questions. Directional expectations were retained only for relations with current support; DJD→Adaptive Performance remained exploratory because challenge/hindrance evidence is mixed. No mediation, moderation, estimator, method, instrument, causal effect, or data-access assumption was introduced. The agent created a pre-FG1 audit but did not declare FG1 READY because GRO-05 still required researcher verification, the person-level unit lock was not yet explicit, and evidence-coverage status still required a formal gate decision.

## GRO-05 verification and formal FG1 review — 11 October 2026

ChatGPT interpreted the researcher’s explicit continuation approval after the GRO-05 verification request as verification of the reported research-question direction. It locked the current substantive unit to individual Korbrimob personnel, assessed G1, G2 and G3 against the repository’s formal quality-gate criteria, and recorded FG1 READY for the bounded framing. The G2 decision did not claim exhaustive coverage: missing authenticated Scopus/Web of Science parity remains a material limitation and reopen trigger. During the same review, the agent identified that FG0 Context had never been formally assessed; therefore it did not proceed to method selection despite FG1 being READY.