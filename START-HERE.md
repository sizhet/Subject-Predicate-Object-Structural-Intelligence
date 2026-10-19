# START HERE — Subject–Predicate–Object Structural Intelligence (SPO-SI)

**Subtitle:** Subject-Centric World Models, Governed Action, and Recursive Structural Evolution  
**Version:** v0.1.0 — Open Research Incubator  
**Authors:** Sizhe Tan & GPT-Obot  
**Status:** Directional hypotheses, preliminary architecture, and relay interface proposals; not a validated general theory.

> **SPO-SI is not an attempt to own the world of intelligence, but an attempt to connect intelligent subjects, their models, their actions, and their structural evolution.**

## 1. What Is This Repository?

SPO-SI explores a structural organization for intelligent systems centered on three interacting roles:

- **Subject (S):** an agent or bounded acting system with capabilities, goals, observations, identity, and governance constraints.
- **Predicate (P):** the executable and evaluative mechanisms connecting a subject to its world—perception, modeling, scoring, planning, policy, action control, learning, and structural revision.
- **Object (O):** the task, environment, target system, or other agents with which the subject interacts.

The core research move is from **isolated intelligence components** to **dynamic intelligence loops**: observe → model → evaluate → act → receive feedback → update. A useful working representation is `(S_t, P_t, O_t, M_t, H_t)`, where `M_t` denotes world-model state and `H_t` denotes relevant history and evidence. This is a conceptual scaffold, not a universal formalism established by experiment.

The repository is deliberately an **open research incubator**. It invites critique, independent comparisons, counter-evidence, and interoperable contributions from researchers working on world models, robotics, agents, reinforcement learning, cognitive science, and structural intelligence.

## 2. Choose Your Reading Path

### Path A — First-time reader (15–30 minutes)

1. [README.md](README.md) — project scope and repository map.
2. [SPO-001: From Structural Components to Intelligence Loops](docs/SPO-001-From-Structural-Components-to-Intelligence-Loops.md) — motivation and transition to closed-loop intelligence.
3. [SPO-002: Subject–Predicate–Object Architecture](docs/SPO-002-Subject-Predicate-Object-Architecture.md) — canonical vocabulary and system boundaries.
4. [OPEN-QUESTIONS.md](research/OPEN-QUESTIONS.md) — where the research remains unsettled.

### Path B — World-model and embodied-AI researcher

1. [SPO-003: Subject-Centric and Shared World Models](docs/SPO-003-Subject-Centric-and-Shared-World-Models.md).
2. [RELAY-002: World Model Piece](relay/RELAY-002-World-Model-Piece.md).
3. [RELAY-003: Perspective Transformation](relay/RELAY-003-Perspective-Transformation.md).
4. [RELATED-WORK.md](research/RELATED-WORK.md) — prior art, adjacent frameworks, and points of comparison.

**Question to test:** Under what conditions does a subject-centered local model, optionally linked to a shared model, outperform a comparably resourced alternative?

### Path C — Systems architect and interoperability researcher

1. [SPO-004: Structural Relay and Interoperability](docs/SPO-004-Structural-Relay-and-Interoperability.md).
2. [RELAY-001: Subject Profile](relay/RELAY-001-Subject-Profile.md).
3. [RELAY-002: World Model Piece](relay/RELAY-002-World-Model-Piece.md).
4. [RELAY-003: Perspective Transformation](relay/RELAY-003-Perspective-Transformation.md).
5. [RELAY-004: Evidence and Counter-Evidence](relay/RELAY-004-Evidence-and-Counter-Evidence.md).

**Question to test:** Can explicit contracts, provenance, uncertainty, and perspective translation improve portability without introducing prohibitive overhead?

### Path D — Structural learning, governance, and RSI researcher

1. [SPO-005: Recursive SPO and Structural Evolution](docs/SPO-005-Recursive-SPO-and-Structural-Evolution.md).
2. [SPO-006: Research Boundaries and Open Hypotheses](docs/SPO-006-Research-Boundaries-and-Open-Hypotheses.md).
3. [RELAY-004: Evidence and Counter-Evidence](relay/RELAY-004-Evidence-and-Counter-Evidence.md).
4. [TESTABLE-HYPOTHESES.md](research/TESTABLE-HYPOTHESES.md).
5. [VALIDATION-ROADMAP.md](research/VALIDATION-ROADMAP.md).

**Critical distinction:** Self-modeling is not self-modification, and self-modification is not validated self-improvement.

### Path E — Independent evaluator or prospective contributor

Start with [RELATED-WORK.md](research/RELATED-WORK.md), [TESTABLE-HYPOTHESES.md](research/TESTABLE-HYPOTHESES.md), and [VALIDATION-ROADMAP.md](research/VALIDATION-ROADMAP.md). Identify an existing baseline, a falsifiable prediction, and an observable failure condition before proposing a new component.

## 3. Visual Orientation

The planned eight-figure series follows the same conceptual progression:

| Figure | Focus |
|---|---|
| [Fig-001](figures/Fig-001-SPO-SI-Grand-Architecture.png) | SPO-SI grand architecture |
| [Fig-002](figures/Fig-002-From-Structural-Components-to-Intelligence-Loops.png) | Components → intelligence loops |
| [Fig-003](figures/Fig-003-Canonical-SPO-Intelligence-Unit.png) | Canonical subject–predicate–object unit |
| [Fig-004](figures/Fig-004-Subject-Centric-and-Shared-World-Models.png) | Local and shared world models |
| [Fig-005](figures/Fig-005-Structural-Relay-and-Interoperability.png) | Relay contracts and lifecycle |
| [Fig-006](figures/Fig-006-Perspective-Transformation-and-Evidence-Relay.png) | Perspective, evidence, and uncertainty |
| [Fig-007](figures/Fig-007-Recursive-SPO-and-Governed-Structural-Evolution.png) | Governed recursive evolution |
| [Fig-008](figures/Fig-008-Open-Intelligence-Relay-and-Collective-Learning.png) | Open research relay and collective learning |

See [FIGURE-INDEX.md](FIGURE-INDEX.md) when available. **Publishing note:** Confirm that all eight separately named PNGs exist before relying on the image links; a composite illustration alone does not satisfy these paths.

## 4. Four Structural Relay Interfaces

The initial relay proposals are research artifacts, **not ratified interoperability standards**:

| Relay piece | Purpose | Primary document |
|---|---|---|
| Subject Profile | Describe capabilities, boundaries, goals, and authority | [RELAY-001](relay/RELAY-001-Subject-Profile.md) |
| World Model Piece | Share bounded world-model claims and state | [RELAY-002](relay/RELAY-002-World-Model-Piece.md) |
| Perspective Transformation | Translate frames, meanings, and applicability | [RELAY-003](relay/RELAY-003-Perspective-Transformation.md) |
| Evidence and Counter-Evidence | Carry claims, provenance, uncertainty, and challenges | [RELAY-004](relay/RELAY-004-Evidence-and-Counter-Evidence.md) |

A relay is useful only when the recipient can determine **what a piece means, where it applies, what evidence supports it, what is unknown, and whether it is authorized for use**.

## 5. Research Boundaries

SPO-SI does **not** claim to have invented the agent–environment loop, world models, partial observability, embodied cognition, or multi-agent coordination. These have substantial established literatures. Its proposed contribution is a **structural integration and interoperability research program**, informed by prior Structural Intelligence work.

In particular:

- A **subject-centric** model can be an efficient operational viewpoint, but is not universally superior to shared or globally constructed models.
- A **shared world model** is fallible and perspective-dependent; it is not an omniscient description of reality.
- A **functional subject** or self-model is not evidence of phenomenal consciousness.
- A **recursive architecture** is not evidence of successful, safe, or autonomous recursive self-improvement.
- Relay specifications require implementation, conformance testing, and independent validation before interoperability can be claimed.

## 6. How to Contribute to the Research Relay

Useful contributions include a clearly scoped counterexample, a baseline comparison, an independently reproduced experiment, a compatible or competing relay contract, a perspective-translation failure case, or a relevant prior-work correction.

A concise contribution record should contain:

```yaml
contribution_id: "example-001"
kind: "hypothesis-test | counter-evidence | interface-proposal | related-work"
claim_or_question: "Describe the exact proposition."
context: "Task, domain, subject, environment, and assumptions."
method_or_artifact: "Procedure, implementation, dataset, or document reference."
evidence: "Observed results or explicit statement that no results exist yet."
uncertainty_and_limits: "Known unknowns, failure cases, and transfer limits."
provenance: "Author, date, version, and source references."
requested_follow_up: "Replicate, compare, revise, or discuss."
```

This is an illustrative record, not a validated machine-readable schema. Do not include secrets, private subject data, or unsafe action permissions in public examples.

## 7. A Minimal Validation Sequence

1. **Define** a bounded subject, action space, environment, and task.
2. **Implement** a simple observation–action–feedback loop with a baseline.
3. **Introduce** a local world-model representation; measure prediction quality and task outcomes.
4. **Relay** a bounded model piece or perspective transformation; measure compatibility and information loss.
5. **Challenge** the model with contradictory evidence and distribution shifts.
6. **Evaluate** structural revisions under explicit governance, audit, and rollback constraints.
7. **Publish** methods, failures, and limitations so others can independently extend the work.

The complete program appears in [VALIDATION-ROADMAP.md](research/VALIDATION-ROADMAP.md). No completed experimental validation is implied by this sequence.

## 8. Repository Navigation

- **Core papers:** [`docs/`](docs/) — SPO-001 through SPO-006.
- **Relay proposals:** [`relay/`](relay/) — RELAY-001 through RELAY-004.
- **Research agenda:** [`research/`](research/) — open questions, hypotheses, roadmap, and related work.
- **Illustrations:** [`figures/`](figures/) — Fig-001 through Fig-008 (verify individual files).
- **Terminology and navigation:** [GLOSSARY.md](GLOSSARY.md), [CONTENTS.md](CONTENTS.md), and [FIGURE-INDEX.md](FIGURE-INDEX.md), as available.

## 9. Guiding Principle

> **The value of an early structural insight is not measured only by how far its originators can develop it, but also by how far others can carry it.**

SPO-SI is an invitation to **discover, critique, relay, test, and evolve** structural ideas across research boundaries—not a claim to own or complete the study of intelligence.

---

**Citation and release note:** Cite the repository's published release and DOI when available; do not invent a DOI for this draft. Refer to `CITATION.cff` after its metadata has been finalized.

**Authors:** Sizhe Tan & GPT-Obot  
**Research release:** v0.1.0 (exploratory)
