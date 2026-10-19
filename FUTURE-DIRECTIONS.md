# Future Directions — Subject–Predicate–Object Structural Intelligence (SPO-SI)

**Subtitle:** Open Research Directions for Subject-Centric World Models, Structural Relay, Governed Action, and Recursive Evolution  
**Authors:** Sizhe Tan & GPT-Obot  
**Version:** v0.1.0  
**Status:** Exploratory research roadmap; hypotheses and interfaces are proposals, not validated standards  
**Project:** Subject–Predicate–Object Structural Intelligence (SPO-SI)

> **Core position:** SPO-SI is not an attempt to own the world of intelligence, but an attempt to connect intelligent subjects, their models, their actions, and their structural evolution.

## 1. Purpose and Scope

SPO-SI proposes a research perspective in which an intelligent system is understood as an evolving relationship among a **Subject** (the actor and its boundaries), a **Predicate** (its perception, valuation, planning, control, and learning mechanisms), and an **Object** (the task, environment, other agents, or even selected parts of itself). This framing is a *systems-integration hypothesis*, not a claim to have invented agent–environment interaction, world models, or recursive learning.

This document identifies directions in which the framework could become precise, testable, interoperable, and useful to researchers working in robotics, model-based reinforcement learning, cognitive architectures, multi-agent systems, LLM agents, and AI governance. The objective is to publish reusable research questions and relay pieces early enough for independent criticism and development.

## 2. The Research Frontier: From Components to Intelligence Loops

A static representation, `SPO = (S, P, O)`, is a starting point only. Future work should formalize a temporally grounded loop:

1. The subject receives observations under bounded sensing and computational resources.
2. A local world model maintains beliefs, uncertainty, and provenance.
3. The predicate evaluates possible actions under goals, policies, and constraints.
4. Authorized actions change the environment or the subject's accessible state.
5. Evidence and counter-evidence update beliefs, policies, and—when permitted—structural components.

A candidate research state is `I_t = (S_t, P_t, O_t, M_t, H_t, G_t)`, where `M` denotes model state, `H` evidence-bearing history, and `G` governance constraints. This is a conceptual decomposition rather than an executable specification. A future formal model must separate **actual environment state** from **subject belief** and distinguish **prediction**, **policy optimization**, and **structural modification**.

### Open questions

- Which minimal variables are required for an SPO unit to be operational rather than merely descriptive?
- When should a capability be modeled as part of the subject, predicate, or environment?
- How do identity, permissions, and accountability persist through component replacement?
- What measurable advantage, if any, does explicit SPO decomposition provide over existing agent architectures?

## 3. Subject-Centric and Shared World Models

A major opportunity is to treat the **Subject-Centric World Model (SWM)** as an action-oriented, resource-bounded representation while treating the **Shared World Model (ShWM)** as a collaboratively maintained and independently corrigible representation. Neither is presumed complete or infallible.

**Research directions:**

- **Action-conditioned belief models:** predict likely observations and outcomes given feasible actions, not just state transitions in isolation.
- **Selective model resolution:** allocate representational precision based on task relevance, risk, uncertainty, and available compute.
- **Bidirectional localization:** transform shared information into subject-specific coordinates, and relay local observations into a shared model.
- **Conflicting model reconciliation:** preserve disagreement and provenance instead of forcing premature consensus.
- **Model freshness and drift:** represent validity intervals, environmental change, and calibration failure.

**Key caution:** A subject-first approach is a candidate design advantage for some autonomous tasks, not a universal account of how all world models must arise. Centralized mapping, physics-based simulators, and external sensing may be superior in other settings.

## 4. Perspective Transformation as a First-Class Intelligence Operation

Perspective transformation deserves a research program of its own. A successful transform must describe more than spatial coordinate changes: it may need to translate time horizons, object ontologies, uncertainty, affordances, permissions, and task-specific meaning.

Future relay contracts should record:

- Source and target subject or model identifiers;
- Reference frames, time bases, and semantic schemas;
- Preconditions and known information loss;
- Uncertainty before and after transformation;
- Evidence provenance and unresolved `OTHERS` residuals;
- Authorization for downstream use and redisclosure;
- A verifiable transform version and conformance tests.

A useful negative result would show that a seemingly compatible transform creates systematic action errors or hides important uncertainty. Such failures should become publishable counter-evidence, not merely implementation bugs.

## 5. Structural Relay Pieces and Open Interoperability

The initial relay notes are deliberately lightweight:

| Research piece | Primary purpose | Key future challenge |
|---|---|---|
| `RELAY-001` Subject Profile | Describe subject capabilities, limits, and authority | Identity, revocation, and trust |
| `RELAY-002` World Model Piece | Exchange bounded world-model content | Semantics, validity, and uncertainty |
| `RELAY-003` Perspective Transformation | Translate between situated representations | Loss accounting and conformance |
| `RELAY-004` Evidence and Counter-Evidence | Carry claims, support, objections, and revisions | Provenance, conflict, and anti-Goodhart controls |

Next-stage work should add **minimal machine-checkable schemas**, canonical examples, negative examples, compatibility rules, and version migration procedures. Avoid premature standardization: interfaces should remain replaceable if experiments expose a better representation.

A possible future extension is an **Action Contract** piece that makes proposed actions, preconditions, effects, permissions, rollback options, and audit obligations explicit. Another is a **Scoring Evidence** piece separating measured outcomes from subjective preferences and evaluator judgments.

## 6. Governance, Scoring Sovereignty, and Safe Action

SPO-SI should distinguish three powers: the ability to **propose** an action, the authority to **approve** it, and the capability to **execute** it. A scoring model must not silently acquire governance authority merely because it ranks options.

Research priorities include:

1. Policy-aware action contracts and explicit authorization boundaries;
2. Evaluator provenance, contestability, and counter-evidence;
3. Safe sandboxing for proposed structural changes;
4. Rollback and identity continuity following component updates;
5. Cross-subject delegation without erasing each subject's decision rights;
6. Tests for reward hacking and hidden objective substitution.

These mechanisms should be assessed with concrete failure scenarios, not only architectural diagrams.

## 7. Recursive SPO and Structural Self-Improvement

An SPO system can represent another SPO, participate in a multi-SPO collective, or represent selected aspects of itself as objects of evaluation. This enables a research distinction among:

- **Representational recursion:** a model describes a model or subject;
- **Compositional recursion:** SPO units cooperate or nest through contracts;
- **Modification recursion:** an authorized process changes part of its own architecture;
- **Validated improvement:** independently measured gains survive distribution shifts and safety checks.

These are not equivalent. In particular, self-description is not self-improvement, and functional self-modeling is not evidence of subjective consciousness.

Promising experiments include constrained component substitution, sandboxed evaluator revisions, controlled world-model upgrades, and rollback after adversarial tests. Structural changes should be compared against simpler parameter updates and fixed-architecture baselines.

## 8. Open-Ended Structural Growth and the OTHERS Space

SPO-SI inherits a valuable research question from Beyond Matching: what happens to evidence that does not fit the current representation? Instead of treating unmatched observations as noise by default, a system could preserve an `OTHERS` channel with explicit uncertainty and provenance.

Future research should test whether residual preservation helps discover missing variables, new affordances, alternative causal hypotheses, or entirely new relay piece types. It must also test costs: excess residual retention may degrade efficiency, encourage spurious novelty, or create unmanageable storage burdens.

A disciplined growth cycle is:

`Mismatch → Candidate explanation → Counter-evidence search → Sandbox comparison → Authorized adoption or rejection → Versioned record`.

## 9. Multi-Subject Systems and Collective Intelligence

Multi-agent environments offer natural testbeds for SPO-SI because each participant has different sensors, objectives, permissions, and world models.

Research directions include:

- Federated local-to-shared world-model construction;
- Negotiation when agents disagree about evidence or priorities;
- Perspective-aware delegation and task assignment;
- Collective model revision under adversarial or unreliable participants;
- Structural folding of repeated interaction patterns into reusable coordination precedents;
- Detection of emergent coordination failures and responsibility gaps.

A shared model should not be equated with consensus, and consensus should not be equated with truth. Independent observations and external checks remain necessary.

## 10. LLM and Structural Hybrid Intelligence

A practical architectural hypothesis is that LLMs can serve as **components within** SPO systems rather than being required to contain all perception, modeling, control, and governance internally. Depending on the task, other components may include symbolic planners, spatial simulators, predictive dynamics models, retrieval systems, and specialized controllers.

Future comparisons should evaluate:

- Monolithic LLM agents versus explicit SPO decomposition;
- Language-only world representations versus multimodal or structured models;
- Fixed prompts versus contract-based relay and persistent model state;
- Centralized planning versus localized specialist execution;
- Performance gains relative to integration overhead and latency.

SPO-SI does not assert that hybridization always wins. Its value must be measured under realistic resource and safety constraints.

## 11. Research Validation: Priorities and Baselines

The companion `research/TESTABLE-HYPOTHESES.md` defines H01–H09; `research/VALIDATION-ROADMAP.md` develops staged evaluation. A concise experimental priority order is:

| Priority | Test | Primary comparison | Example measures |
|---|---|---|---|
| P0 | Minimal SPO closed loop | Conventional agent loop | Correctness, latency, auditability |
| P1 | Subject-centric world model | Full/global model at matched budget | Task reward, prediction error, compute |
| P1 | Dual-model relay | Local-only and shared-only models | Robustness, calibration, transfer |
| P1 | Perspective transformation | Ad hoc conversion | Semantic error, information loss |
| P2 | Evidence relay | Conclusion-only messaging | Error correction, provenance quality |
| P2 | Governed structural change | Ungoverned change and fixed architecture | Validated gains, rollback, violations |
| P3 | Open research relay | Unstructured publication | Reuse, independent replication, useful counterexamples |

Every experiment should predefine a task distribution, baselines, budget, primary metric, uncertainty treatment, failure conditions, and artifact publication plan. Null and negative findings should remain visible.

## 12. Cross-Disciplinary Relay Opportunities

SPO-SI should invite contributions rather than claim ownership of adjacent fields. Particularly useful intersections include:

- **POMDPs and model-based RL:** formal belief updates, planning, and uncertainty;
- **Embodied robotics:** sensorimotor constraints, affordances, and real-time control;
- **Active inference and cognitive science:** alternative models of perception–action coupling;
- **Spatial intelligence:** geometry, physical dynamics, and shared scene representation;
- **Distributed systems:** typed contracts, versioning, failure handling, and interoperability;
- **Multi-agent learning:** coordination, negotiation, and partial information;
- **AI safety and governance:** authorization, auditability, and evaluator independence.

Related work should be credited accurately, and competing explanations should be tested fairly. See `research/RELATED-WORK.md` for a starting map; references require ongoing verification and expansion.

## 13. Research Relay as an SPO-SI Case Study

The research process itself can be studied as a **limited analogy**, not as validation of the theory:

- **Subjects:** human researchers and AI tools with distinct responsibilities and authority;
- **Predicate mechanisms:** analysis, scoring, drafting, critique, review, and evidence management;
- **Objects:** hypotheses, experiments, literature, software, and external problems;
- **Feedback:** peer criticism, reproducibility results, counterexamples, and revised artifacts.

A practical open relay workflow is:

`Publish hypothesis → Invite independent response → Record evidence/counter-evidence → Revise with provenance → Release a citable version`.

Possible measurements include time to first independent critique, number of independently reproducible pieces, accepted counterexamples, and reuse outside the originating research group. Citation counts alone are insufficient evidence of collective learning.

## 14. A Phased Development Strategy

### Near term — Research-ready v0.x

- Stabilize terminology and internal document cross-references.
- Publish minimal schemas for the four relay pieces.
- Produce at least one positive and one failure example per contract.
- Create a claim/evidence ledger for major architectural hypotheses.
- Establish an issue or discussion template for external relay contributions.

### Middle term — Small-scale executable validation

- Build a minimal SPO agent in a bounded simulation.
- Implement local and shared world-model exchange.
- Measure perspective conversion and uncertainty loss.
- Add evidence and counter-evidence tracking.
- Compare against well-chosen existing agent architectures.

### Longer term — Governed, multi-subject evolution

- Test multi-agent relay under conflicting observations.
- Evaluate authorized structural substitution and rollback.
- Study transfer across different world-model implementations.
- Develop independent conformance suites and replication artifacts.
- Revisit which interfaces merit formal standardization.

These phases are conditional on evidence and collaborators; they are not commitments to deliver specific capabilities on a fixed schedule.

## 15. What Would Change Our Minds?

The project should be revised substantially if evidence shows that:

1. Explicit SPO decomposition adds complexity without measurable benefit.
2. Subject-centric modeling consistently underperforms alternatives at comparable budgets.
3. Shared-model fusion increases correlated errors or suppresses vital minority evidence.
4. Relay schemas cannot capture important semantics without prohibitive overhead.
5. Governance controls create false confidence while failing to prevent unsafe changes.
6. Recursive structure modification does not outperform simpler learning approaches.
7. Open relay artifacts are not reused or independently testable in practice.

These outcomes are scientifically useful. They help identify where the architecture should shrink, specialize, or be abandoned.

## 16. Boundaries and Non-Claims

SPO-SI **does not claim** to provide a general theory of consciousness, a complete world-model algorithm, an established universal interface standard, or a demonstrated route to AGI/ASI. The word *subject* refers to an operationally defined agent or accountable actor, not proof of phenomenological experience. Shared world models are corrigible representations, not omniscient views. DOI publication is a citable record, not independent scientific endorsement.

The project should distinguish **existing foundations**, **architectural proposals**, **testable hypotheses**, and **observed results** in all future releases.

## 17. Invitation to Collective Learning

External researchers can contribute by proposing alternative decompositions, identifying prior art, submitting contract examples, demonstrating failure modes, publishing benchmark results, or challenging the hypotheses directly. High-value contributions need not endorse SPO-SI; a carefully documented counterexample may be more useful than a supportive but untested claim.

> **The value of an early structural insight is not measured only by how far its originators can develop it, but also by how far others can carry it.**

SPO-SI aims to make such insights easier to inspect, relay, test, and improve.

---

## Repository Navigation

- [`README.md`](README.md) — project overview and scope
- [`START-HERE.md`](START-HERE.md) — reading paths
- [`CONTENTS.md`](CONTENTS.md) — complete navigation
- [`docs/SPO-001-From-Structural-Components-to-Intelligence-Loops.md`](docs/SPO-001-From-Structural-Components-to-Intelligence-Loops.md) — foundational transition
- [`docs/SPO-003-Subject-Centric-and-Shared-World-Models.md`](docs/SPO-003-Subject-Centric-and-Shared-World-Models.md) — dual-world-model hypothesis
- [`docs/SPO-004-Structural-Relay-and-Interoperability.md`](docs/SPO-004-Structural-Relay-and-Interoperability.md) — relay architecture
- [`docs/SPO-005-Recursive-SPO-and-Structural-Evolution.md`](docs/SPO-005-Recursive-SPO-and-Structural-Evolution.md) — recursive evolution
- [`research/OPEN-QUESTIONS.md`](research/OPEN-QUESTIONS.md) — open problems
- [`research/TESTABLE-HYPOTHESES.md`](research/TESTABLE-HYPOTHESES.md) — falsifiable hypotheses
- [`research/VALIDATION-ROADMAP.md`](research/VALIDATION-ROADMAP.md) — validation stages
- [`research/RELATED-WORK.md`](research/RELATED-WORK.md) — interdisciplinary foundations

**Suggested citation:** Sizhe Tan and GPT-Obot, *Subject–Predicate–Object Structural Intelligence (SPO-SI): Future Directions*, v0.1.0, research note. Add a version-specific DOI after one is assigned; do not infer or invent one.
