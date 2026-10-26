# Open Questions — Subject–Predicate–Object Structural Intelligence (SPO-SI)

**Repository:** Subject–Predicate–Object Structural Intelligence (SPO-SI)  
**Research status:** Open research incubator; directional hypotheses, not validated universal claims  
**Version:** v0.1.0  
**Authors:** Sizhe Tan & GPT-Obot  
**Last updated:** 2026-10-26

> **SPO-SI is not an attempt to own the world of intelligence, but an attempt to connect intelligent subjects, their models, their actions, and their structural evolution.**

## Purpose and participation

This document identifies unresolved questions at the boundaries of subject-centered intelligence, world modeling, governed action, structural interoperability, and recursive growth. Its purpose is to make research uncertainties *relayable*: researchers should be able to identify a question, contribute an alternative model or counterexample, and test it without adopting the entire SPO-SI architecture.

Questions are not findings. Proposed interfaces are provisional; their utility must be established by comparative experiments. Related mature fields—including partially observable control, model-based reinforcement learning, robotics, embodied cognition, active inference, distributed systems, and multi-agent learning—must be credited and used as baselines.

## 1. The SPO unit: ontology and boundaries

**OQ-001 — What is the minimal executable SPO unit?**  
Can a subject, an executable/evaluative predicate, and an object/environment be specified with sufficiently precise input, state, output, and feedback contracts to support implementation? What additional variables are irreducible: time, memory, governance, uncertainty, or embodiment?

**OQ-002 — What counts as a subject?**  
Which operational criteria distinguish a subject from a passive tool, a workflow, a controller, a collective, or a model? Must a subject maintain goals, permissions, persistence, or an action boundary?

**OQ-003 — Is the predicate one mechanism or a coordinated stack?**  
Should perception, world modeling, scoring, planning, execution, and learning be separate typed operators? What is gained or lost by grouping them under a single “Predicate Intelligence” abstraction?

**OQ-004 — When is an object another subject?**  
How should SPO relationships represent negotiation, cooperation, adversarial interaction, and nested agents without collapsing distinct goals or authorities?

**OQ-005 — What is the smallest useful history?**  
Which past observations, actions, failures, and provenance must persist for an SPO unit to improve rather than merely react?

## 2. Subject-centric and shared world models

**OQ-006 — When does subject-centric modeling outperform global modeling?**  
Under fixed compute, data, latency, and accuracy budgets, which tasks favor local action-relevant beliefs over a broad environment model? Where do they fail?

**OQ-007 — Can a shared world model be assembled from partial views?**  
What observability, calibration, alignment, and coverage conditions make fusion identifiable? How should incompatible observations be retained rather than silently reconciled?

**OQ-008 — Is “objective” the right word?**  
Should the shared layer be described as *cross-perspective calibrated* rather than a God's-eye truth? How do we encode uncertainty and measurement limitations?

**OQ-009 — What is a World Model Piece?**  
What is the minimum portable fragment: dynamics rule, state estimate, causal graph, affordance map, simulation component, or trajectory predictor? Can a single contract accommodate heterogeneous types without becoming meaningless?

**OQ-010 — How should unknown unknowns be represented?**  
Can OTHERS/residual evidence be recorded and updated without pretending it is a calibrated probability distribution?

**OQ-011 — How do we test action-conditioned predictions?**  
Which measures best capture calibration, counterfactual accuracy, robustness to intervention, and planning utility—not merely next-frame prediction quality?

**OQ-012 — How does model freshness affect control?**  
What expiry, drift detection, and fallback rules should govern world-model reuse in dynamic environments?

## 3. Perspective transformation and localization

**OQ-013 — What makes two perspectives interoperable?**  
Which transformations require coordinate mappings, shared ontologies, causal assumptions, goal alignment, or explicit translation uncertainty?

**OQ-014 — When are transformations non-invertible?**  
How do we expose lost distinctions, irreversible compression, inaccessible sensors, and untranslatable concepts?

**OQ-015 — Can transformations be safely composed?**  
Does A→B→C preserve enough semantics to be useful, and how should uncertainty, permissions, and provenance accumulate?

**OQ-016 — What belongs in localization versus per-node execution?**  
Where should adaptation happen: routing, interface transformation, local world-model specialization, or the executing intelligence unit?

**OQ-017 — What constitutes a failed relay?**  
Can the receiving system reliably detect semantic mismatch, stale assumptions, incompatible action spaces, or invalid authority?

## 4. Scoring, governance, and action

**OQ-018 — Who owns the evaluation function?**  
How are the subject's goals distinguished from developer, operator, institution, and external-model objectives? What happens when they conflict?

**OQ-019 — Can scoring forests remain interpretable under growth?**  
How can multiple objectives, context-specific operators, and unaligned evidence be combined without hiding tradeoffs?

**OQ-020 — How do contracts prevent unauthorized actions?**  
Which constraints must be checked before planning, before execution, and after observing outcomes? How can authorization be revoked?

**OQ-021 — How should the system handle high-stakes uncertainty?**  
What triggers abstention, human review, sandbox evaluation, rollback, or safer fallback policies?

**OQ-022 — Can counter-evidence challenge the evaluator itself?**  
How do we detect Goodhart effects, reward hacking, or systematically excluded perspectives?

## 5. Recursive SPO and structural evolution

**OQ-023 — What distinguishes adaptation from structural improvement?**  
Can we separate parameter tuning, memory updates, policy changes, architecture edits, and evaluator revision using observable criteria?

**OQ-024 — What is the safe unit of self-modification?**  
Should a recursive SPO update a model piece, a scoring branch, a control rule, a contract, or an entire subsystem? How are changes isolated and reverted?

**OQ-025 — How do we avoid self-certifying improvement?**  
Which independent evaluators, held-out tests, adversarial sandboxes, and counter-evidence channels are needed?

**OQ-026 — What remains invariant across evolution?**  
How do identity, responsibility, permissions, and evaluation sovereignty persist—or deliberately change—through recursive modifications?

**OQ-027 — Can multi-agent SPO composition outperform monolithic agents?**  
Under what workload and coordination costs do specialized subjects produce measurable gains?

**OQ-028 — What are the limits of recursive composition?**  
How do we control complexity, conflicting contracts, cascading failures, and model drift across nested SPO systems?

## 6. Structural Relay and collective learning

**OQ-029 — What is the minimum interoperable Relay Piece?**  
Can Subject Profiles, World Model Pieces, Perspective Transformations, and Evidence/Counter-Evidence Records share a common envelope while retaining domain-specific payloads?

**OQ-030 — What evidence must accompany a reusable claim?**  
Which provenance, context, method, baseline, uncertainty, license, and version fields are mandatory for responsible reuse?

**OQ-031 — How can research relay be measured?**  
Can we measure successful independent reuse, time-to-integration, error detection, replication, and improvements caused by external counter-evidence?

**OQ-032 — How should incompatible research pieces coexist?**  
Should the registry preserve competing hypotheses and mutually inconsistent world models rather than enforce premature consensus?

**OQ-033 — How can openness coexist with safety and privacy?**  
What may be published, redacted, aggregated, or withheld when relay pieces encode sensitive observations, capabilities, or permissions?

**OQ-034 — How can researchers contribute without adopting SPO-SI terminology?**  
What translation guides, minimal examples, and contribution formats lower the cost of cross-disciplinary participation?

## 7. Relationship to existing research and consciousness boundaries

**OQ-035 — What does SPO-SI add beyond established agent–environment loops?**  
Can it demonstrate new interoperability, governance, or structural-evolution capabilities beyond POMDPs, model-based RL, active inference, and established multi-agent frameworks?

**OQ-036 — Which claims are architectural, empirical, or philosophical?**  
How should documents clearly label definitions, design preferences, testable hypotheses, and speculative interpretations?

**OQ-037 — What can self-modeling establish about consciousness?**  
How do we investigate functional awareness, metacognition, and agency without treating behavioral performance as proof of subjective experience?

**OQ-038 — Can SPO-SI work without an explicit world model?**  
Which reactive, model-free, or implicit-model systems can satisfy SPO contracts, and what does that imply about the proposed architecture's necessity?

## 8. Priority experiments and disconfirmation criteria

| Priority | Candidate experiment | Comparator | Useful evidence | Possible disconfirmation |
|---|---|---|---|---|
| P0 | Subject-centric vs shared/global model on partially observable navigation | Equal-budget model-based agents | Success, latency, compute, calibration | No benefit under matched budgets |
| P0 | Relay a World Model Piece between heterogeneous agents | Hand-coded adapter; raw-message transfer | Integration time, semantic errors, transfer success | Contract overhead exceeds transfer gains |
| P0 | Perspective transformation with known information loss | Coordinate-only transform; naive fusion | Uncertainty coverage, consistency, failure detection | Explicit loss accounting fails to improve safety or accuracy |
| P1 | Counter-evidence relay during environment drift | No counter-evidence channel | Detection time, recovery, false alarms | Extra complexity without robustness gains |
| P1 | Governed structural update in sandbox | Unconstrained update; fixed policy | Held-out performance, regressions, rollback success | Governance offers no measurable improvement |
| P2 | Nested multi-agent SPO composition | Single-agent baseline | Task success, cost, failure propagation | Coordination costs dominate |

Every experiment should pre-register the task, budgets, baselines, metrics, failure conditions, and the distinction between statistical evidence and architectural interpretation. Negative results should remain publishable.

## 9. Relay-ready contribution template

Researchers may contribute an issue, discussion, or pull request using the following compact format:

```yaml
question_id: OQ-013
contribution_type: counterexample # hypothesis | evidence | counterexample | interface | experiment
claim: "A perspective transformation can fail despite matching coordinates."
context:
  domain: robotics
  assumptions:
    - "Agents have different sensor capabilities."
evidence:
  kind: proposed_experiment
  artifact_uri: null
  provenance: "Author-supplied; not independently verified"
comparison:
  baseline: "Coordinate-only transformation"
  metrics: [semantic_consistency, transfer_success]
uncertainty:
  limitations: ["Unvalidated proposal"]
governance:
  privacy_reviewed: false
  sharing_scope: public_after_review
status: proposed
```

This YAML is illustrative, **not** a validated or stable schema. Never include secrets, private personal data, or unsafe operational details in public issues.

## 10. Research process and revision rules

1. **Discover:** map new observations to an existing question or propose a new one.
2. **Localize:** state the task, subject perspective, assumptions, and applicability limits.
3. **Compare:** identify relevant prior art and credible baselines.
4. **Test:** define falsifiable predictions, measurements, and independent checks.
5. **Challenge:** record contradictory evidence and alternative explanations.
6. **Revise:** update claims and interfaces with versioned provenance.
7. **Relay:** publish reusable artifacts and clearly mark their validation status.

Suggested statuses: `open`, `under-study`, `partially-supported`, `challenged`, `refuted`, `resolved-for-scope`, and `superseded`. A resolved question can reopen when assumptions or environments change.

## 11. Research boundaries and non-claims

SPO-SI does **not** claim to have invented subject–object interaction, world models, embodied agency, model-based planning, or multi-agent coordination. It does **not** establish a universal intelligence algorithm, demonstrate structural RSI, or prove machine consciousness. The SPO triad is a proposed *integration and relay abstraction* whose added value must be established by implementation and comparison.

A shared world model is not an omniscient truth representation. A Subject Profile is not the subject itself. A self-model is not evidence of subjective experience. A transferable piece is not automatically trustworthy or authorized to execute.

## 12. Links to the research series

- `docs/SPO-001-From-Structural-Components-to-Intelligence-Loops.md`
- `docs/SPO-002-Subject-Predicate-Object-Architecture.md`
- `docs/SPO-003-Subject-Centric-and-Shared-World-Models.md`
- `docs/SPO-004-Structural-Relay-and-Interoperability.md`
- `docs/SPO-005-Recursive-SPO-and-Structural-Evolution.md`
- `docs/SPO-006-Research-Boundaries-and-Open-Hypotheses.md`
- `relay/RELAY-001-Subject-Profile.md`
- `relay/RELAY-002-World-Model-Piece.md`
- `relay/RELAY-003-Perspective-Transformation.md`
- `relay/RELAY-004-Evidence-and-Counter-Evidence.md`
- `research/TESTABLE-HYPOTHESES.md` (planned)
- `research/VALIDATION-ROADMAP.md` (planned)
- `research/RELATED-WORK.md` (planned)

## Closing principle

> **The value of an early structural insight is not measured only by how far its originators can develop it, but also by how far others can carry it.**

The goal of this document is to expose questions early, keep their boundaries honest, and make it easier for others to extend, refute, or replace our proposals. That is the intended meaning of open Structural Intelligence Relay.

---

**Citation note:** Cite the versioned repository release and DOI once available. This exploratory document should not be cited as experimental validation.
