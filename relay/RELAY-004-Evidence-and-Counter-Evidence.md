# RELAY-004 — Evidence and Counter-Evidence

**Project:** Subject–Predicate–Object Structural Intelligence (SPO-SI)  
**Subtitle:** Portable Evidence, Contestable Claims, and Governed Structural Learning  
**Document type:** Exploratory Relay Interface Specification / Research Note  
**Version:** 0.1.0  
**Status:** Proposal — not a validated standard  
**Authors:** Sizhe Tan & GPT-Obot  
**License:** Apache-2.0 (proposed; repository license governs)

> **Research stance.** SPO-SI is not an attempt to own the world of intelligence, but an attempt to connect intelligent subjects, their models, their actions, and their structural evolution.

## Abstract

Intelligence Relay requires more than moving models, conclusions, or policies between systems. A receiving subject must be able to determine *why* a claim was made, what observations support it, what would contradict it, which transformations altered its meaning, and whether it is authorized to act upon it. This note proposes **Evidence and Counter-Evidence Pieces (ECEP)** as portable, versioned, provenance-aware objects for cross-subject learning and model revision. It describes a minimal contract, a lifecycle, a distinction between contradiction and mere disagreement, confidence-calibration safeguards, and an initial validation agenda. ECEP is a research proposal, not a claim that the problems of truth, causal inference, trust, or distributed consensus have been solved.

**Keywords:** structural intelligence; SPO-SI; evidence relay; counter-evidence; provenance; uncertainty; world models; interoperability; structural learning; governance; anti-Goodhart.

---

![Fig-006-Perspective-Transformation-and-Evidence-Relay.png](../figures/Fig-006-Perspective-Transformation-and-Evidence-Relay.png)

---

## 1. Why Evidence Must Travel with Intelligence

A relay may deliver a World Model Piece that predicts an obstacle is absent. Another robot may observe the obstacle. Without structured evidence, the recipient has only two incompatible outputs. It cannot reliably distinguish stale observations, differing coordinate frames, sensor faults, incompatible assumptions, or genuine environmental change.

A structural relay therefore needs to transmit not just the claim but its **support, scope, limitations, and challenges**. Counter-evidence is not an afterthought or a negative score. It is an independently addressable input into model selection, policy governance, and structural growth.

The design objective is *contestable interoperability*: imported knowledge should be usable without being accepted uncritically.

## 2. Placement in the SPO Intelligence Loop

For a subject $S_i$, predicate/control structure $P_i$, environment/object $O$, local model $M_i$, and history $H_i$, the evidence loop is:

```text
Observation / Test / External Relay
             |
             v
       Evidence Piece
             |
             v
 Claim and Context Validation
             |
       +-----+-----+
       |           |
  Supports     Challenges
       |           |
       +-----+-----+
             v
    Scoring + Governance
             |
      Sandbox / Decision
             |
       Action / Revision
             |
       New Observations
             +----> Relay again
```

This is an architecture sketch. It does not prescribe a universal Bayesian or symbolic inference engine. Evidence may be used by statistical, causal, logical, simulation-based, or hybrid evaluators.

## 3. Design Principles

1. **Claim-addressable:** every evidence item identifies the claim, hypothesis, model version, or action it concerns.
2. **Perspective-aware:** the observing subject and frame of reference are explicit.
3. **Provenance-preserving:** source, collection method, transformations, and timestamps are recorded when available.
4. **Counter-evidence-native:** challenges are first-class records, not silently discarded outliers.
5. **Uncertainty-aware:** measurements, confidence, calibration, unknowns, and missingness are not conflated.
6. **Governance-bound:** evidence is not itself permission to deploy a policy or modify a subject.
7. **Versioned and retractable:** corrections and retractions retain an audit trail.
8. **Minimally interoperable:** simple systems can use a core subset; advanced systems may extend it.
9. **Privacy-conscious:** provenance is minimized or redacted when disclosure would expose sensitive data.
10. **Testable:** proposed advantages must be measured against simpler logging and evidence-exchange baselines.

## 4. Canonical Conceptual Model

Let a claim be $c$ and an evidence item be $e$:

$$
e = (id, c, r, s, x, t, p, u, g, v)
$$

where:

- $id$: stable evidence identifier;
- $c$: target claim and version;
- $r$: relationship to claim (support, challenge, qualify, neutral);
- $s$: source subject/instrument;
- $x$: observation or test payload and method;
- $t$: event and recording times;
- $p$: provenance and transformation chain;
- $u$: uncertainty, limitations, and OTHERS;
- $g$: governance, disclosure, and permitted uses;
- $v$: schema and record versions.

The relationship $r$ is an **asserted interpretation**, not a guaranteed truth label. Evaluators must remain free to reject it. A piece can challenge an assumption without falsifying the entire claim.

### 4.1 Claims are scoped

Claims should declare relevant spatial, temporal, task, and population scopes. For example, “corridor clear” is not meaningful without location, time, and sensor coverage.

### 4.2 Counter-evidence is not automatically a contradiction

Two reports can disagree because they refer to different times, coordinate frames, thresholds, or definitions. Conflict resolution begins with scope and perspective alignment, not majority voting.

### 4.3 Negative evidence is not evidence of absence by default

A failure to detect an object is meaningful only when detection coverage, sensor sensitivity, and observation conditions are known.

## 5. Minimal Relay Contract

A proposed minimal Evidence and Counter-Evidence Piece includes:

| Field | Requirement | Purpose |
|---|---|---|
| `schema_version` | Required | Contract compatibility |
| `piece_id` | Required | Unique reference |
| `piece_type` | Required | Evidence/counter-evidence designation |
| `claim.id`, `claim.version` | Required | Exact claim target |
| `relationship` | Required | Support, challenge, qualify, neutral |
| `source.subject_id` | Required or pseudonymized | Originating observer |
| `observation.method` | Required | How data was obtained |
| `observation.summary` | Required | Human-readable evidence statement |
| `observed_at` | Required if known | Event time |
| `recorded_at` | Required | Record creation time |
| `scope` | Required | Applicability limits |
| `uncertainty` | Required | Explicit known/unknown quality |
| `provenance` | Required | Source and transformation references |
| `governance` | Required | Use and sharing constraints |
| `status` | Required | Proposed, verified, disputed, retracted |

The contract deliberately does not mandate a single confidence number. A confidence score without calibration, interpretation, and source dependence may be misleading.

## 6. Illustrative YAML Piece

The following is a **non-normative example**, not a validated JSON Schema. Identifiers, measurements, and actors are fictional.

```yaml
schema_version: "0.1.0"
piece_id: "ecep:robot-b:2026-10-19:0042"
piece_type: "counter_evidence"
status: "proposed"
claim:
  id: "claim:map:zone-7:clear"
  version: "3"
  statement: "Zone 7 corridor is free of obstacles"
relationship: "challenge"
source:
  subject_id: "subject:robot-b"
  instrument_id: "sensor:depth-camera-2"
observation:
  method: "depth_camera_detection"
  summary: "An obstacle was detected within the corridor boundary"
  payload_ref: "artifact:depth-scan-0042"
  reproducibility: "raw-scan-available-under-access-control"
observed_at: "2026-10-19T10:20:00-07:00"
recorded_at: "2026-10-19T10:20:04-07:00"
scope:
  spatial_frame: "building-map-v2"
  region: "zone-7"
  valid_from: "2026-10-19T10:20:00-07:00"
  valid_until: null
  task: "navigation"
uncertainty:
  detection_probability: null
  calibration_ref: null
  known_limits:
    - "partial field of view"
  others:
    - "object may be transient"
provenance:
  origin_ref: "artifact:depth-scan-0042"
  transformations:
    - name: "sensor_to_building_frame"
      contract_ref: "perspective-transform:v0.1:example"
      residual_error: "not quantified"
  integrity_digest: null
governance:
  classification: "internal"
  permitted_uses:
    - "navigation_replanning"
    - "sandbox_model_validation"
  deployment_authority: false
  retention_policy: "project-defined"
links:
  supersedes: []
  related_evidence: ["ecep:robot-a:2026-10-19:0031"]
```

An implementation should validate syntax, required fields, timestamp ordering, referenced artifacts, schema versions, and permitted use. The example does not establish the obstacle's actual existence.

## 7. Evidence Types and Counter-Evidence Taxonomy

Possible evidence origins include direct observation, controlled experiment, simulation, expert judgment, retrieved document, learned-model output, and cross-subject report. These origins should not be treated as equally reliable by default.

Counter-evidence can be classified as:

- **Empirical contradiction:** a measurement conflicts with a prediction under matched conditions.
- **Scope counterexample:** a general claim fails in a particular valid domain.
- **Causal alternative:** an observed correlation has another plausible mechanism.
- **Model-calibration failure:** stated uncertainty does not match observed error frequencies.
- **Perspective mismatch:** disagreement arises from incompatible frames or semantics.
- **Governance violation:** a proposed action violates a binding contract, regardless of its apparent reward.
- **Distribution shift:** evidence no longer transfers to the current environment.
- **Provenance challenge:** a source or transformation cannot be verified.

A governance violation is a reason to block or review an action, not necessarily evidence that the empirical claim is false.

## 8. Integration with Other Relay Pieces

### RELAY-001 — Subject Profile

Links evidence to the observer's declared sensors, competencies, permissions, and limitations. A Subject Profile is a claim about capabilities, not proof of competence; external validation remains necessary.

### RELAY-002 — World Model Piece

Attaches evidence to model predictions, assumptions, versioned state estimates, and candidate revisions. Imported observations should be localized before they update a recipient's model.

### RELAY-003 — Perspective Transformation

Records coordinate, semantic, temporal, and capability transformations. A transformation should expose information loss and residual uncertainty; successful parsing is not equivalent to semantic fidelity.

### Action and Scoring Contracts

Provides input for scoring, sandbox tests, and policy review. Evidence may inform a decision but must not silently override evaluation sovereignty or deployment authority.

## 9. Relay Lifecycle

1. **Capture:** record an observation, experiment, or challenge.
2. **Bind:** identify the target claim and its version.
3. **Describe:** attach method, scope, timestamps, and uncertainty.
4. **Protect:** apply privacy, disclosure, and access constraints.
5. **Transport:** exchange the piece with integrity checks where available.
6. **Localize:** transform spatial, semantic, temporal, and task context.
7. **Validate:** check provenance, relevance, method, and consistency.
8. **Adjudicate:** compare with existing evidence and counter-hypotheses.
9. **Govern:** authorize sandbox use, rejection, or bounded deployment.
10. **Revise:** update model/claim/policy only through a recorded process.
11. **Audit:** preserve decision rationale, supersession, and retraction links.
12. **Learn:** export validated deltas as new Relay Pieces.

Not every system requires all twelve stages at runtime. A minimal research implementation should still preserve the distinctions between validation, decision, and deployment.

## 10. Adjudication Without False Precision

A conceptual evaluator can be written as:

$$
D = operatorname{Adjudicate}(C, E^+, E^-, X, G)
$$

where $C$ is a set of claims, $E^+$ supporting evidence, $E^-$ challenges, $X$ context and transformations, and $G$ governance constraints. $D$ may be `accept_provisionally`, `reject`, `request_more_evidence`, `sandbox`, or `abstain`.

This formulation does **not** assume evidence items are independent. Ten copied reports from one sensor are not ten independent observations. If probabilistic updating is used, dependency and selection bias must be modeled or explicitly flagged.

Recommended outputs include: decision, reasons, unresolved counter-evidence, uncertainty summary, provenance references, and authorized next action.

## 11. OTHERS and Open Evidence Space

The `OTHERS` field represents potentially relevant factors not yet captured by the current matching or scoring schema. It is not a license to invent hidden causes or assign arbitrary probability mass. It should hold inspectable residuals, candidate explanations, missing modalities, unknown transforms, and unclassified observations.

A useful growth pattern is:

```text
Unexplained residual
    -> Candidate OTHERS factor
    -> New measurement or test
    -> Counter-hypothesis comparison
    -> Verified schema extension (or rejection)
    -> Updated World Model / Scoring Structure
```

Rejected candidates remain traceable, avoiding repeated rediscovery of the same failed explanation.

## 12. Anti-Goodhart and Adversarial Safeguards

A relay network can amplify error if systems optimize evidence counts, confidence scores, or consensus rather than validity. Initial safeguards should include:

- preserving unfavorable observations and failed tests;
- identifying duplicated or correlated sources;
- preventing a model from approving its own unverified revisions;
- separating model scoring from action authorization;
- requiring bounded sandbox evaluation for high-impact changes;
- detecting stale evidence and distribution shifts;
- supporting retraction propagation and version pinning;
- recording disagreements rather than forcing premature consensus.

These controls reduce some failure modes but do not guarantee safety or epistemic correctness.

## 13. Worked Example: Two Robots, One Corridor

**Initial claim:** Robot A's World Model Piece says a corridor is clear at 10:15.

**Challenge:** Robot B reports an obstacle at 10:20 and sends a Counter-Evidence Piece with sensor provenance.

**Localization:** The receiver aligns the sensor frame with the building map and checks time validity.

**Adjudication:** The reports are not necessarily logically contradictory: an obstacle may have appeared between observations. The system flags the earlier claim as stale for current navigation rather than declaring Robot A unreliable in general.

**Governed action:** The navigation controller replans or requests confirmation according to its safety policy. It does not treat the relay message as unrestricted permission to move.

**Structural growth:** If this pattern recurs, the system may propose a new freshness constraint for corridor-clearance claims, test it in a sandbox, and publish the change as a versioned contract update.

The example illustrates how counter-evidence can drive a *structural* improvement rather than only correcting one state estimate.

## 14. Open Research Hypotheses

| ID | Hypothesis | Plausible falsification condition |
|---|---|---|
| ECEP-H1 | Provenance-aware pieces improve error diagnosis over plain-text claim exchange. | No improvement at comparable cost in controlled tasks. |
| ECEP-H2 | First-class counter-evidence reduces persistent false model beliefs. | Equal or worse false-belief persistence versus a strong baseline. |
| ECEP-H3 | Perspective-aware localization reduces spurious contradictions. | No reduction under known frame/semantic shifts. |
| ECEP-H4 | Explicit OTHERS records improve discovery of missing model factors. | No measurable gain in held-out shift scenarios. |
| ECEP-H5 | Governance-separated evidence relay reduces unauthorized policy updates. | No reduction in unauthorized changes or excessive operational overhead. |
| ECEP-H6 | Versioned retractions reduce propagation of superseded claims. | No improvement in correction latency or downstream error. |

These are proposals to test, not findings.

## 15. Validation Roadmap

**Phase 0 — Contract review.** Compare against existing provenance and event standards; document differences and avoid unnecessary duplication.

**Phase 1 — Synthetic exchange.** Generate claims, observations, conflicting timestamps, and malformed pieces. Measure schema conformance and rejection quality.

**Phase 2 — Perspective shifts.** Exchange evidence between simulated agents with different coordinate systems and semantic labels. Measure false-conflict rate and transformation error.

**Phase 3 — Dynamic world models.** Use a navigation or manipulation benchmark with stale maps and changing obstacles. Measure task success, model correction latency, and computational cost.

**Phase 4 — Adversarial relay.** Introduce duplicated evidence, misleading confidence, provenance gaps, and retractions. Measure robustness and governance failures.

**Phase 5 — Collective learning.** Test whether validated structural deltas transfer across tasks or agents better than raw logs and ordinary experience replay.

Baselines should include plain event logs, ordinary structured messages, existing provenance representations, and task-specific model-update mechanisms. Publish failures and negative results.

## 16. Evaluation Metrics

Candidate metrics include claim-resolution accuracy, false-conflict rate, calibration error, correction latency, retraction propagation time, traceability completeness, unauthorized-update frequency, task success, bytes per piece, runtime overhead, and cross-domain reuse success. Report metrics by evidence source type and by in-distribution versus shifted conditions.

No single aggregate score should replace a breakdown of epistemic quality, operational performance, and governance outcomes.

## 17. Security, Privacy, and Trust Boundaries

Evidence records may expose sensitive sensor data, user behavior, location, or proprietary models. A Relay Piece should support pseudonymous subject identifiers, controlled payload references, retention limits, redaction metadata, and access checks. Cryptographic integrity can establish that bytes have not changed, but it does not establish that the underlying observation is true.

A receiver should treat external evidence as untrusted input: validate schemas, constrain payload parsing, check authority separately, and never execute embedded instructions as policy. The subject's evaluation sovereignty remains distinct from the source's asserted credibility.

## 18. Relationship to Existing Research

The proposal draws conceptual inspiration from established work in scientific reproducibility, data provenance, event sourcing, Bayesian evidence updating, argumentation systems, causal inference, multi-agent belief revision, and machine-learning evaluation. SPO-SI's candidate contribution is the **joint packaging** of perspective, provenance, counter-evidence, governance, and structural-evolution hooks in a portable research interface. Novelty and practical advantage remain to be established by comparison with relevant standards and implementations.

This document should not be cited as evidence that SPO-SI invented evidence provenance, falsification, or multi-agent belief exchange.

## 19. Open Questions

1. What is the smallest portable representation that still preserves meaningful counter-evidence?
2. When should a recipient abstain rather than reconcile incompatible reports?
3. How can transformation losses be quantified across heterogeneous world models?
4. Which provenance fields are indispensable, and which are privacy risks?
5. How should correlated observations be identified without a central authority?
6. What distinguishes a useful OTHERS candidate from speculative noise?
7. Can structural revisions be rolled back without losing their historical evidence?
8. How should competing subjects negotiate evidence while retaining evaluation sovereignty?
9. What should be standardized, and what should remain domain-specific?
10. How do we evaluate Collective Learning benefits independently of network size and compute budget?

## 20. Proposed Next Steps

- Draft a machine-checkable schema for the minimal ECEP contract.
- Create three fixtures: supporting evidence, temporal counter-evidence, and retracted evidence.
- Define cross-links with RELAY-001/002/003 identifiers and version conventions.
- Implement a minimal conformance test and a disagreement-resolution sandbox.
- Document external related work and solicit critical review before claiming standardization.

## 21. Conclusion

An intelligence relay that moves conclusions without their supporting conditions risks becoming a network for reproducing mistakes. Evidence and Counter-Evidence Pieces aim to make exchanged intelligence *inspectable, challengeable, revisable, and governable*. The proposed interface does not solve truth or trust. It creates a candidate structure through which subjects can compare what they know, preserve what they do not know, and turn validated disagreements into opportunities for structural learning.

> **The value of an early structural insight is not measured only by how far its originators can develop it, but also by how far others can carry it.**

---

### Related SPO-SI documents

- `docs/SPO-001-From-Structural-Components-to-Intelligence-Loops.md`
- `docs/SPO-002-Subject-Predicate-Object-Architecture.md`
- `docs/SPO-003-Subject-Centric-and-Shared-World-Models.md`
- `docs/SPO-004-Structural-Relay-and-Interoperability.md`
- `docs/SPO-005-Recursive-SPO-and-Structural-Evolution.md`
- `docs/SPO-006-Research-Boundaries-and-Open-Hypotheses.md`
- `relay/RELAY-001-Subject-Profile.md`
- `relay/RELAY-002-World-Model-Piece.md`
- `relay/RELAY-003-Perspective-Transformation.md`

**Citation guidance:** Cite the repository release and its archived DOI when available. This draft does not invent a DOI or claim an external peer review.
