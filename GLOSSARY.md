# GLOSSARY — Subject–Predicate–Object Structural Intelligence (SPO-SI)

**Project:** Subject–Predicate–Object Structural Intelligence (SPO-SI)  
**Subtitle:** Subject-Centric World Models, Governed Action, and Recursive Structural Evolution  
**Authors:** Sizhe Tan & GPT-Obot  
**Version:** v0.1.0  
**Status:** Open Research Incubator — Exploratory Definitions, Not a Validated Standard  
**Updated:** 2026-10-26

> **Research position:** SPO-SI is not an attempt to own the world of intelligence, but an attempt to connect intelligent subjects, their models, their actions, and their structural evolution.

## 1. Scope and Terminology Conventions

This glossary provides working definitions for the SPO-SI research repository. It aims to keep the six `SPO-` papers, four `RELAY-` notes, and research documents interoperable at the conceptual level. Terms marked **proposed** denote project-specific design constructs rather than established disciplinary standards. Terms marked **established** are broadly used in adjacent literature, though their exact definitions vary by field.

Three distinctions recur throughout: a **representation** is not the represented entity; a **contract** is not evidence of a working implementation; and a **hypothesis** is not an empirical result. The vocabulary here may evolve in response to independent tests and counter-evidence.

## 2. Core SPO-SI Concepts

### Subject (S) — proposed usage

An identifiable agent or agent-like system with a specified boundary, observation channels, capabilities, goals or objective functions, and permissions. A Subject may be a person, robot, software agent, or a governed collective. Functional subjecthood does **not** imply phenomenal consciousness, moral personhood, or unrestricted autonomy.

### Predicate (P) / Predicate Intelligence — proposed

The operational intelligence mechanisms mediating a Subject's interactions with an Object or environment. These may include perception, inference, World Models, valuation, planning, policy selection, action control, and learning. Unlike a predicate in formal logic or grammar, SPO-SI's `P` denotes a **structured process or mechanism**, not merely a truth-valued relation. The analogy is architectural, not a claim of formal equivalence.

### Object (O) — proposed usage

The task, target, environment, phenomenon, or other agent toward which the Subject's intelligence is directed. An Object need not be passive: it may itself be a Subject with its own SPO loop. The Object in a model must not be confused with the external world in its entirety.

### SPO Intelligence Unit — proposed

A conceptual unit consisting of Subject, Predicate, and Object, augmented as necessary by state, history, World Model, feedback, and governance. The minimal notation is `I = (S, P, O)`; the operational form is a temporally evolving loop. This is a proposed systems organization, not a new mathematical proof of intelligence.

### Intelligence Loop — proposed usage

An ongoing cycle of observation, state estimation, evaluation, action selection, execution, feedback, and update. A loop may update model parameters, policies, interfaces, or structural organization. Not every cycle necessarily includes every stage.

### Subject Boundary — proposed usage

The explicit limits of a Subject's identity, observation access, controllable resources, permitted actions, and accountable decisions. A boundary may be organizational, computational, physical, or legal; it should not be inferred from a model's conversational presentation.

### Functional Agency — established concept, project-specific operationalization

The capacity of a system to select and execute actions toward goals under constraints. SPO-SI treats agency as measurable through behavior and control interfaces, without equating it to subjective experience.

### Evaluation Sovereignty — proposed

The principle that responsibility and authorization for goals, scoring criteria, and consequential actions must remain attached to an explicitly designated governing Subject or authority. A delegated model's score is not automatically an authorized decision.

## 3. World Models and Perspective

### World Model (WM) — established family of concepts

An internal or external representation that supports estimation or prediction of environment states, observations, dynamics, or action consequences. It can be learned, symbolic, probabilistic, spatial, causal, or hybrid. A World Model is not necessarily comprehensive or objectively correct.

### Subject-Centric World Model (SWM) — proposed

A World Model localized to a particular Subject's observations, goals, embodiment, capabilities, time horizon, and uncertainty. It prioritizes action-relevant information rather than exhaustive coverage.

### Shared World Model (ShWM) — proposed

An environment representation accessible to multiple Subjects, potentially assembled from heterogeneous observations, sensors, simulations, or models. “Shared” does not imply universally accepted, complete, or error-free.

### Objective World Model (OWM) — provisional label

A model designed to support cross-perspective consistency and external validation. In this repository, **Shared World Model** is generally preferred because “objective” can incorrectly imply a privileged, infallible viewpoint.

### Dual-World-Model Architecture — proposed

A bidirectional arrangement between local SWMs and one or more ShWMs: local observations may inform shared representations, while shared information may be localized back to a Subject. Centralized, direct construction of shared models remains a valid alternative baseline.

### Belief State — established

A representation of uncertainty over latent environment states given observations and history, as in partially observable decision processes. A belief state need not be an explicit probability vector in every implementation.

### Partial Observability — established

A condition in which the Subject cannot directly observe all variables needed to characterize the environment. It motivates state estimation, uncertainty handling, memory, and active information gathering.

### Perspective — proposed operational definition

The combination of a Subject's reference frame, observation scope, representation, objectives, capabilities, and relevant constraints. Two Subjects can disagree because they observe different evidence or encode it differently, not necessarily because one is wrong.

### Perspective Transformation — proposed

A documented mapping between source and target perspectives, potentially involving spatial frames, temporal scales, semantics, capability assumptions, and governance constraints. A valid transformation must identify assumptions, loss, and residual uncertainty.

### Localization — established term, extended SI usage

Selecting and adapting information, models, capabilities, or evidence for a particular Subject, context, and task. It may include routing, coordinate alignment, semantic adaptation, and policy compatibility checks. It does not guarantee semantic equivalence.

### Perspective Alignment — proposed

Checking whether two representations refer to compatible entities, frames, time intervals, concepts, and action assumptions. Alignment may be partial and may require explicit unresolved conflicts.

## 4. Structural Intelligence and Control

### Structural Intelligence (SI) — project umbrella term

The study and design of intelligence using explicit structures for representation, localization, composition, control, evaluation, learning, and growth. SPO-SI is one proposed organizing architecture within this broader research program.

### Structural Intelligence Framework (SIF) — project framework

An open architecture emphasizing Perception, Localization, Per-Node Intelligence, and Control, with contracts, relay, structural precedents, and growth mechanisms. SPO-SI investigates how these mechanisms operate in Subject–environment loops.

### Subjective Structural Intelligence (SSI) — project framework

A research direction addressing subject boundaries, perception, agency, valuation, self-models, and worldview evolution. “Subjective” here denotes subject-relative structure; it does not establish phenomenal consciousness.

### Universal Control Plane — proposed

A reusable control layer that applies policies, permissions, evaluation criteria, routing, and governance across heterogeneous intelligence components. “Universal” is an architectural ambition, not a claim of proven applicability to every system.

### Scoring Tree / Scoring Forest — proposed

Hierarchical or grouped evaluation structures that compare options across objectives, contexts, and perspectives. A Forest permits multiple partially independent evaluators or policy domains; scoring must be checked for calibration and Goodhart effects.

### Structural Folding / Unfolding — proposed

Operations that compress or reorganize structural information for efficient use and subsequently recover or elaborate task-relevant detail. A fold may be lossy; uncertainty and provenance should be preserved or reconstructed where feasible.

### Per-Node Intelligence — project term

An intelligence capability attached to a selected node or unit, such as a rule, model, specialized solver, policy, or learned evaluator. It can be invoked after localization or dispatch.

### Action Contract — proposed

A typed agreement specifying an action's preconditions, inputs, permissions, side effects, expected outputs, constraints, and failure behavior. It is a governance and interoperability artifact, not an assurance that execution is safe.

### Governance — established concept, project-specific use

The mechanisms that determine which changes or actions are authorized, evaluated, audited, deployed, or rolled back. Governance includes human or institutional authority where appropriate.

### Anti-Goodhart — established concern, project shorthand

Design practices intended to prevent optimization of a proxy score from undermining the actual objective. Methods may include diverse evaluators, adversarial testing, uncertainty, and counter-evidence.

## 5. Structural Relay and Portable Pieces

### Intelligence Relay — proposed

The exchange and context-sensitive reuse of intelligence-bearing structures across Subjects, models, organizations, or research projects. Relay involves more than transmitting text: the receiver must interpret scope, compatibility, evidence, and authority.

### Structural Relay Piece — proposed

A bounded, versioned, describable unit that can be discovered, inspected, validated, adapted, and optionally reused. It can encode a model fragment, profile, transformation, policy, evidence, or other structured knowledge.

### Relay Contract — proposed

A specification of a piece's type, schema, semantics, provenance, applicability, uncertainty, compatibility, access rules, and lifecycle. A contract defines intended interoperability but does not prove it.

### Subject Profile — proposed; `RELAY-001`

A portable description of a Subject's identity reference, capabilities, observation limits, goals, permissions, and governance. It is not the Subject itself, a complete psychological self-model, or an authentication credential.

### World Model Piece — proposed; `RELAY-002`

A bounded fragment of environment knowledge or predictive dynamics, including scope, frame, assumptions, provenance, and uncertainty. It is not necessarily a standalone executable World Model.

### Perspective Transformation Piece — proposed; `RELAY-003`

A reusable mapping between source and target perspectives with declared coordinate, temporal, semantic, capability, and permission assumptions. It should expose noninvertibility and information loss.

### Evidence and Counter-Evidence Piece — proposed; `RELAY-004`

A portable claim-support or claim-challenge record that preserves source, method, context, uncertainty, relevance, and revision history. Evidence may support multiple hypotheses and should not be reduced to an unqualified confidence number.

### Universal Name-Type — project term

A naming and typing scheme intended to support discovery and compatibility checks across structurally different intelligence pieces. It does not eliminate the need for semantic validation.

### Portable Intelligence Unit (PIRU) — project term

A transferable unit of intelligence-related structure, potentially combining executable capability, metadata, constraints, and localization requirements. Actual portability is an engineering property to be demonstrated.

### Provenance — established

A traceable record of a piece's origin, transformations, observations, contributors, versions, and validation history. Provenance supports audit but does not by itself guarantee correctness.

### Interoperability — established

The ability of different systems to exchange and appropriately use information or capabilities. SPO-SI distinguishes syntactic compatibility, semantic compatibility, operational compatibility, and governance compatibility.

## 6. Evidence, Uncertainty, and Open Growth

### Evidence — established

Observations, measurements, derivations, experiments, or other records relevant to evaluating a claim. Strength depends on methods, relevance, independence, and possible bias.

### Counter-Evidence — established concept, explicit SI role

Evidence that contradicts, limits, or supplies a competing explanation for a claim, model, or evaluation. It may trigger reevaluation without automatically proving the opposite claim.

### OTHERS / Open Evidence Space — proposed

An explicit place for unmatched, weakly represented, or not-yet-classified factors. It prevents forced matching of every observation to existing categories. OTHERS is not a license to assign arbitrary predictive power to unknowns.

### Uncertainty Preservation — established goal, project usage

Maintaining meaningful information about estimation error, missing variables, disagreement, and transformation loss as structures are compressed, translated, or exchanged.

### Counter-Evidence Provenance — proposed emphasis

A record of where a challenge originated, what claim it targets, the context in which it applies, and how subsequent evaluations handled it.

### Structural Precedent — project term

A previously observed or validated structural solution, failure, or transformation that can be indexed and reused under suitable conditions.

### Structural Growth — proposed

A change in the organization or repertoire of intelligence capabilities, such as adding a branch, model, evaluator, contract, or policy. Growth is not synonymous with improvement; regressions and costs must be measured.

### Open-Ended Structural Growth — proposed

A research ambition in which new capabilities, interfaces, representations, and evaluation structures can continue to emerge or be incorporated beyond a fixed initial catalog. It is not a claim of unlimited or guaranteed progress.

## 7. Recursive SPO and Learning

### Recursive SPO — proposed

A configuration in which an SPO system represents, evaluates, composes, or modifies other SPO systems, potentially including portions of itself. Recursion can be representational, organizational, or operational.

### Self-Model — established family of concepts

A representation a Subject maintains about its own state, abilities, limits, goals, or processes. A Self-Model can be inaccurate and does not imply subjective consciousness.

### Self-Modification — established

An authorized or unauthorized change to a system's internal structures, parameters, policies, or executable components. Modification alone is not improvement.

### Structural Recursive Self-Improvement (Structural RSI) — proposed

A governed process in which a system proposes, tests, validates, and potentially adopts changes to its own structural organization. Improvement requires independent criteria, suitable baselines, and evidence of generalization.

### Adversarial Sandbox — project term

An isolated testing environment for candidate changes, competing agents, counterexamples, and failure discovery before deployment. Isolation and test coverage must be engineered and verified.

### Evaluator Governance — proposed

Rules for selecting, testing, monitoring, challenging, and revising the mechanisms that judge candidate actions or structural changes. It addresses evaluator drift and Goodhart risks.

### Rollback — established

A controlled return to a previously validated state after a change fails checks or causes unacceptable behavior. Rollback feasibility depends on system state and external side effects.

### Collective Structural Learning — proposed

The cumulative improvement of shared structures through contributions from multiple researchers, agents, or organizations, including evidence, counter-evidence, and reusable interfaces. Publication alone does not demonstrate collective learning.

### Structural Insight Relay — proposed

The public transfer of an early research observation together with its structural interpretation, hypothesis, assumptions, interface opportunities, open questions, and possible validation path.

## 8. Research Method and Claims

### Directional Hypothesis — project usage

An early, explicit proposal identifying a plausible research direction without claiming empirical validation. It should specify assumptions and what evidence would weaken it.

### Testable Hypothesis — established

A claim stated precisely enough to be examined through reproducible measurements or observations, including comparison baselines and failure criteria.

### Counter-Hypothesis — project usage

A competing explanation or predicted outcome that could reduce confidence in the primary hypothesis. It is used to resist confirmation bias.

### Baseline — established

An existing or simpler method used as a comparator in an experiment. Appropriate baselines for SPO-SI may include POMDP controllers, model-based reinforcement learning, model-predictive control, modular agents, and conventional information exchange.

### Validation Roadmap — project usage

A staged plan specifying artifacts, experiments, metrics, decision gates, and reproducibility requirements. A roadmap does not imply that experiments have been executed.

### Research Incubator — project designation

A public repository for provisional models, interfaces, questions, and test plans. Its outputs are open for criticism, revision, and independent implementation; they are not formal standards.

### Research Relay — proposed

A practice of publishing structured hypotheses and artifacts so that independent participants can discover, test, challenge, adapt, and extend them. Actual relay success requires observable downstream uptake or contributions.

### DOI (Digital Object Identifier) — established

A persistent identifier for a citable research artifact or release. A DOI establishes a reference target, not peer review, validation, or priority of discovery.

## 9. Important Non-Equivalences

| Do not equate | With | Reason |
|---|---|---|
| Functional Subject | Conscious Subject | Behavior does not establish phenomenal experience. |
| Subject Profile | Subject or complete Self-Model | A profile is a bounded representation. |
| Predicate Intelligence | Logical predicate | SPO-SI uses an architectural analogy. |
| Shared World Model | Perfect objective truth | Shared representations remain partial and revisable. |
| Perspective Transformation | Lossless equivalence | Frames, semantics, and information may differ. |
| Relay Contract | Proven interoperability | Real implementations require tests. |
| Scoring improvement | Real-world improvement | Proxy metrics may mislead. |
| Self-Modeling | Self-Modification | Description and intervention are distinct. |
| Self-Modification | Validated Self-Improvement | Changes can fail or regress. |
| Structural Growth | Beneficial evolution | More structure can increase cost or risk. |
| Open publication | Collective Learning | Uptake, evaluation, and revision must occur. |
| DOI publication | Scientific validation | Identification is not endorsement. |

## 10. Abbreviations

| Abbreviation | Expansion |
|---|---|
| SPO-SI | Subject–Predicate–Object Structural Intelligence |
| SPO | Subject–Predicate–Object |
| SI | Structural Intelligence |
| SIF | Structural Intelligence Framework |
| SSI | Subjective Structural Intelligence |
| UCPSF | Universal Control Planes and Scoring Tree/Forest/Folding |
| SWM | Subject-Centric World Model |
| ShWM | Shared World Model |
| OWM | Objective World Model (provisional label) |
| WM | World Model |
| RSI | Recursive Self-Improvement |
| CCC | Context-dependent structural control/consistency construct (meaning varies across SI documents; consult the defining source) |
| PIRU | Portable Intelligence Runtime Unit |
| DOI | Digital Object Identifier |
| POMDP | Partially Observable Markov Decision Process |
| API | Application Programming Interface |

## 11. Cross-References

**Core papers:**

- [`docs/SPO-001-From-Structural-Components-to-Intelligence-Loops.md`](docs/SPO-001-From-Structural-Components-to-Intelligence-Loops.md)
- [`docs/SPO-002-Subject-Predicate-Object-Architecture.md`](docs/SPO-002-Subject-Predicate-Object-Architecture.md)
- [`docs/SPO-003-Subject-Centric-and-Shared-World-Models.md`](docs/SPO-003-Subject-Centric-and-Shared-World-Models.md)
- [`docs/SPO-004-Structural-Relay-and-Interoperability.md`](docs/SPO-004-Structural-Relay-and-Interoperability.md)
- [`docs/SPO-005-Recursive-SPO-and-Structural-Evolution.md`](docs/SPO-005-Recursive-SPO-and-Structural-Evolution.md)
- [`docs/SPO-006-Research-Boundaries-and-Open-Hypotheses.md`](docs/SPO-006-Research-Boundaries-and-Open-Hypotheses.md)

**Relay specifications:**

- [`relay/RELAY-001-Subject-Profile.md`](relay/RELAY-001-Subject-Profile.md)
- [`relay/RELAY-002-World-Model-Piece.md`](relay/RELAY-002-World-Model-Piece.md)
- [`relay/RELAY-003-Perspective-Transformation.md`](relay/RELAY-003-Perspective-Transformation.md)
- [`relay/RELAY-004-Evidence-and-Counter-Evidence.md`](relay/RELAY-004-Evidence-and-Counter-Evidence.md)

**Research and navigation:**

- [`research/OPEN-QUESTIONS.md`](research/OPEN-QUESTIONS.md)
- [`research/TESTABLE-HYPOTHESES.md`](research/TESTABLE-HYPOTHESES.md)
- [`research/VALIDATION-ROADMAP.md`](research/VALIDATION-ROADMAP.md)
- [`research/RELATED-WORK.md`](research/RELATED-WORK.md)
- [`START-HERE.md`](START-HERE.md) · [`CONTENTS.md`](CONTENTS.md)

## 12. Revision and Contribution Policy

New terms should be proposed with (1) a precise definition, (2) scope and non-goals, (3) relationship to existing terminology, (4) at least one concrete example, and (5) implications for interfaces or validation. Ambiguous or contested terms should remain explicitly provisional. Definitions may be updated through documented revisions and counter-evidence.

---

**Citation guidance:** Cite the specific version of the SPO-SI repository or its individual research notes. No DOI is asserted here until a persistent identifier is actually issued.

**Authors:** Sizhe Tan & GPT-Obot  
**License:** Refer to the repository's `LICENSE.txt` file for the applicable terms.
