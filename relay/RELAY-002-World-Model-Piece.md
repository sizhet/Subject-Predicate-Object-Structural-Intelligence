# RELAY-002 — World Model Piece

**SPO-SI Structural Relay Research Note / Draft Interface Contract**  
**Version:** 0.1.0 (exploratory; not a ratified standard)  
**Authors:** Sizhe Tan & GPT-Obot  
**Repository:** Subject–Predicate–Object Structural Intelligence (SPO-SI)  
**Status:** Directional hypothesis and interoperability design proposal  
**Related:** SPO-002, SPO-003, SPO-004, SPO-006; RELAY-001

## Abstract

A World Model Piece (WMP) is a bounded, provenance-aware, uncertainty-bearing representation of some aspect of an environment that another intelligent subject may discover, inspect, localize, test, and selectively use. The proposal deliberately avoids requiring a universal world-model implementation. It specifies a **relay boundary** between heterogeneous subject-centric and shared models, including the semantics of the modeled claim, the subject perspective, the temporal and spatial scope, evidence, uncertainty, transformation dependencies, and permitted uses. This note offers a minimal contract, a worked YAML example, relay lifecycle, validation criteria, counterexamples, and open research questions. All performance benefits remain hypotheses to be tested.

---

![Fig-004-Subject-Centric-and-Shared-World-Models.png](../figures/Fig-004-Subject-Centric-and-Shared-World-Models.png)

---

![Fig-005-Structural-Relay-and-Interoperability.png](../figures/Fig-005-Structural-Relay-and-Interoperability.png)

---

## 1. Research Position and Non-Goals

SPO-SI does not seek to replace physics simulators, spatial foundation models, POMDP belief states, learned dynamics, robotics maps, or causal models. Instead, it asks which **portable pieces** of such models can be exchanged without erasing their assumptions. A WMP is neither a complete World Model nor a claim to an objective, omniscient representation. It is a partial model artifact or a reference to one, together with a machine-inspectable contract.

Non-goals of this v0.1.0 proposal include universal ontology alignment, fully automatic trust, guaranteed causal validity, guaranteed safety of transferred policies, and a proof of consciousness or subjective experience.

## 2. Core Definition

Let a subject-specific model at time *t* be `M_i(t)`, and let a piece be extracted under a scope and a projection:

`WMP = Extract(M_i, scope, projection, contract)`.

A consuming subject *j* may construct a candidate localized representation:

`candidate_j = Localize(WMP, SubjectProfile_j, context_j)`.

**Localization is not acceptance.** Use requires separate compatibility, evidence, policy, and task-specific checks. The source model, target model, and external environment must not be conflated.

A World Model Piece may represent:

- A state estimate or belief distribution.
- A conditional transition/dynamics prediction.
- A spatial or topological relation.
- An affordance or action-conditioned consequence.
- A causal hypothesis with explicit assumptions.
- A bounded forecast or simulation result.
- A reference to a larger executable model with a constrained interface.

## 3. Canonical Contract: Required Fields

| Field | Meaning | Minimum validation |
|---|---|---|
| `piece_id` | Stable identifier for this piece | Nonempty, versioned or immutable |
| `schema_version` | Relay contract version | Recognized version |
| `piece_version` | Revision of the model piece | Explicit revision |
| `producer.subject_ref` | Subject Profile or source system | Resolvable reference or explicit unknown |
| `model_kind` | State, belief, dynamics, spatial, causal, affordance, forecast, or reference | Controlled vocabulary |
| `scope` | Entities, region, domain, time interval | Bounded and interpretable |
| `perspective` | Observer/frame, viewpoint, observation limits | Declared, not silently global |
| `semantics` | Variables, units, coordinate frame, ontology, conditioning assumptions | Units and types explicit |
| `payload` | Data, equations, artifact reference, or executable interface | Typed and integrity-checkable |
| `uncertainty` | Confidence/calibration information and unknowns | Method and limitations declared |
| `provenance` | Origin, observation or training lineage, timestamps | Source and evidence trace |
| `validity` | Conditions for intended applicability and expiry | Checkable predicates where feasible |
| `governance` | License, access, privacy, allowed uses, decision authority | Deny-by-default on missing permission |

A consumer must be able to mark fields as *unknown* rather than inventing precision. The contract is extensible: unfamiliar optional fields should be retained when relaying, not silently discarded.

## 4. Subject-Centric and Shared Models

**Subject-centric WMP (SWMP):** Represents a model from an identifiable subject's observation/action context. It may be efficient and locally actionable, but biased by sensor coverage, goals, and embodiment.

**Shared WMP (ShWMP):** Represents a model assembled from multiple sources or externally calibrated measurements. It should expose contributor lineage, fusion method, disagreements, and unresolved gaps. Shared does **not** mean infallible or view-from-nowhere.

Two directions are possible:

1. **Aggregation:** SWMPs → alignment → evidence-aware fusion → candidate ShWMP.
2. **Localization:** ShWMP → perspective transform → subject constraints → candidate SWMP.

Neither direction guarantees preservation of all semantics. Transform loss and unresolved contradictions are first-class outputs.

## 5. Worked YAML Example (Illustrative, Not a Validated Schema)

```yaml
schema_version: "0.1.0"
piece_id: "wmp:robot-a:hallway-obstacle:2026-10-19T17:00Z"
piece_version: "1"
model_kind: "belief"
producer:
  subject_ref: "subject:robot-a"
  system: "example-robot-stack"
scope:
  domain: "indoor-navigation"
  entities: ["robot-a", "obstacle-17"]
  region: "building-1/floor-2/hallway-3"
  observed_at: "2026-10-19T17:00:00Z"
  valid_until: "2026-10-19T17:00:05Z"
perspective:
  kind: "subject-centric"
  observer: "subject:robot-a"
  frame: "robot-a/base_link"
  sensor_coverage: "front-lidar-sector"
semantics:
  ontology: "example.indoor-obstacles.v1"
  variables:
    relative_position: {type: "vector2", unit: "m"}
    occupancy_probability: {type: "float", range: [0, 1]}
  conditioning: ["sensor_calibration:cal-42", "static-frame-during-scan"]
payload:
  encoding: "inline-yaml"
  data:
    obstacle_id: "obstacle-17"
    relative_position: [2.1, -0.4]
    occupancy_probability: 0.82
uncertainty:
  representation: "probability-estimate"
  calibration: "not-yet-validated"
  known_unknowns: ["occlusion-behind-obstacle", "object-velocity"]
provenance:
  evidence_refs: ["observation:scan-917"]
  generated_at: "2026-10-19T17:00:01Z"
  method: "illustrative-perception-pipeline"
validity:
  conditions: ["frame-transform-available", "not-expired"]
  out_of_distribution: "unknown"
governance:
  license: "example-only"
  permitted_uses: ["simulation", "navigation-planning-input"]
  prohibited_uses: ["unreviewed-safety-critical-actuation"]
  decision_authority: "consumer-subject-control-plane"
```

The numeric probability is synthetic and **must not** be treated as empirically calibrated. Real implementations should specify signed artifact hashes, access controls, and a normative schema in a later version.

## 6. Relay Lifecycle

1. **Publish / Register:** Identify source, version, scope, and access conditions.
2. **Discover:** Match task requirements to piece type, spatial/temporal domain, and permitted use.
3. **Resolve:** Retrieve payload and required dependencies; verify integrity.
4. **Type & Semantic Check:** Check units, ontology, frames, action definitions, and conditioning.
5. **Perspective Localization:** Transform to the target subject's frame, preserving transformation error.
6. **Evidence & Counter-Evidence:** Compare against local observations, independent measurements, and competing pieces.
7. **Governance Gate:** Confirm allowed use and human/system authorization.
8. **Sandbox Evaluation:** Test downstream predictions or decisions before consequential deployment.
9. **Accept / Quarantine / Reject:** Record decision, rationale, and confidence limitations.
10. **Monitor & Revise:** Observe drift, expiration, contradictions, and rollback triggers.

A relay transaction should leave an auditable record of source, transforms, decisions, and later corrections.

## 7. Perspective Transformation Contract

A transform should state its source and destination frames, applicable time, ontology mapping, transformation method, error budget, and reversibility limits. For a spatial estimate, a simple transform may be:

`x_target = T_target<-source(x_source, t)`

But transforming a subject's **meaning** (for example, "safe corridor") requires more than changing coordinates. Safety depends on body geometry, velocity, sensors, acceptable risk, and task context. An apparently compatible frame transform can still be semantically invalid.

The separate `RELAY-003-Perspective-Transformation.md` will develop these rules.

## 8. Uncertainty, OTHERS, and Counter-Evidence

A WMP must distinguish:

- **Aleatoric uncertainty:** variability in the environment or observation process.
- **Epistemic uncertainty:** lack of knowledge or model coverage.
- **Model disagreement:** conflicts across models or subjects.
- **Open residual / OTHERS:** phenomena not represented by current variables, ontologies, or matching metrics.

These categories may overlap and should not be naively added. A transfer may increase uncertainty because of unknown transforms or target-domain shift. Counter-evidence should be linked to the exact piece version and claim; a negative observation is not automatically a global refutation.

## 9. Interoperability and Failure Cases

| Failure | Example | Required response |
|---|---|---|
| Coordinate mismatch | Meters interpreted as centimeters | Reject until corrected |
| Time mismatch | Obstacle estimate is stale | Expire or re-observe |
| Perspective mismatch | Drone map applied to ground robot | Re-localize and revalidate |
| Ontology mismatch | "Passable" means different clearance | Preserve disagreement; do not merge |
| Overconfidence | Uncalibrated score treated as probability | Downgrade or quarantine |
| Provenance loss | No observation lineage | Restrict high-stakes use |
| Permission mismatch | External model forbids deployment | Block deployment |
| Goodhart pressure | Piece optimized for benchmark proxy | Evaluate out-of-distribution outcomes |
| Unknown residual | Unexpected object class | Record OTHERS; seek new evidence |

## 10. Interface Sketch

```text
publish(piece, producer_profile) -> registry_ref | error
discover(query, consumer_profile) -> candidate_refs
resolve(ref, authorization) -> piece | denied
validate(piece, target_context) -> compatibility_report
localize(piece, target_profile, transforms) -> candidate_piece + loss_report
evaluate(candidate_piece, evidence, policy) -> accept | quarantine | reject
record_feedback(piece_ref, evidence_ref, outcome) -> audit_record
```

These are conceptual operations, not a production API. No operation should bypass the consumer's decision authority.

## 11. Relationship to SIF, SSI, UCPSF, and Earlier SI

- **SIF:** Localization, dual maps, name/type contracts, precedent registry, governance.
- **SSI:** Subject boundary, perspective, identity, valuation sovereignty, self-models.
- **UCPSF:** Scoring Forest, selection under competing criteria, control planes, folding.
- **BM-ODWEI:** OTHERS, weak evidence, perspective distance, counter-evidence provenance.
- **PIRP/PIRU:** Portable pieces and units, relay and context localization.
- **Structural RSI:** Governed evaluation of proposed model or policy updates.

These are candidate integration points, not evidence of proven interoperability.

## 12. Illustrative Research Cases

### Case A — Robot-to-Robot Navigation Relay

Robot A publishes a five-second obstacle belief. Robot B checks timestamp, transforms coordinates, adjusts for its wider body, and tests the estimate against its own sensor data. A successful relay yields a **candidate local belief**, not automatic steering authority.

### Case B — Shared Scientific Simulation

Two laboratories publish model pieces for the same physical phenomenon with different assumptions. A shared model preserves each model's scope, calibration data, and contradictory predictions rather than averaging incompatible outputs.

### Case C — LLM Agent and External Simulator

An LLM agent requests a bounded forecast from an external simulator. The simulator returns model version, input assumptions, forecast horizon, uncertainty, and permitted uses. The agent's control plane decides whether to use the result; fluent language is not a substitute for evidence.

## 13. Testable Hypotheses

**H-WMP-1 (Portability):** Typed WMPs reduce integration effort relative to ad hoc serialized model outputs. Measure engineering time, adapter count, and failure rate.

**H-WMP-2 (Reliability):** Provenance and validity fields reduce harmful use of stale or out-of-scope pieces. Measure invalid acceptance and downstream task errors.

**H-WMP-3 (Dual-Model Utility):** Subject/shared bidirectional relay improves task performance under bounded computation in selected environments. Compare against local-only and centralized-only baselines.

**H-WMP-4 (Uncertainty Preservation):** Explicit transform-loss reporting improves calibration after cross-perspective transfer. Measure calibration error and selective prediction risk.

**H-WMP-5 (Open Growth):** Recording OTHERS and counter-evidence yields more useful subsequent model revisions than recording successful matches alone. Measure discovered failure modes and held-out performance.

Null results are informative. Gains must be reported with overhead, latency, and governance costs.

## 14. Validation Roadmap

**Phase 0 — Contract review:** Compare proposed fields against existing robotics, simulation, geospatial, and ML metadata conventions; identify unnecessary duplication.

**Phase 1 — Static conformance:** Build schema validators and negative test cases for missing units, expired data, inconsistent frames, and absent provenance.

**Phase 2 — Cross-subject localization:** Exchange small spatial and belief pieces among heterogeneous simulated agents; measure conversion error.

**Phase 3 — Shared fusion:** Compare evidence-preserving fusion against naïve merging and centralized baselines.

**Phase 4 — Governed use:** Evaluate authorization, quarantine, rollback, and counter-evidence under adversarial or corrupted pieces.

**Phase 5 — Open relay trial:** Invite independent implementations, collect incompatibilities, and revise the contract with versioned decisions.

## 15. Open Questions

1. What is the smallest useful model piece that remains semantically meaningful?
2. When should a WMP carry data, an executable model, or merely a model reference?
3. How can different ontologies be aligned without suppressing genuine disagreement?
4. What uncertainty representations survive transfer between model families?
5. Can action-conditioned predictions be exchanged safely across different embodiments?
6. Which properties should be mandatory for high-stakes versus low-stakes use?
7. How should shared models resolve conflicting subject reports and unequal sensor quality?
8. What is the correct expiration policy for changing environments?
9. How should proprietary, privacy-sensitive, or restricted model pieces participate in relay?
10. When does the overhead of interoperability exceed its benefits?

## 16. Research Boundaries and Invitation

This proposal is a **research interface sketch**, not a consensus standard or an empirically demonstrated universal solution. It should be judged by compatibility tests, independent implementations, measured costs, failure analysis, and the quality of evidence it preserves. Contributions are especially welcome where they identify a misleading assumption, an incompatible model family, a simpler existing standard, or a falsifying case.

> SPO-SI is not an attempt to own the world of intelligence, but an attempt to connect intelligent subjects, their models, their actions, and their structural evolution.

> The value of an early structural insight is not measured only by how far its originators can develop it, but also by how far others can carry it.

## 17. Suggested Follow-On Documents

- `RELAY-003-Perspective-Transformation.md` — frame/ontology/semantics mapping and transformation-loss contracts.
- `RELAY-004-Evidence-and-Counter-Evidence.md` — evidence lineage, conflict, revision, and validation.
- `research/TESTABLE-HYPOTHESES.md` — preregisterable comparisons and acceptance criteria.
- `research/RELATED-WORK.md` — systematic comparison with existing World Model and data interoperability standards.

---

**Citation note:** This is an exploratory architectural proposal by Sizhe Tan & GPT-Obot. Cite the versioned repository release and its DOI once assigned. No DOI is asserted here.
