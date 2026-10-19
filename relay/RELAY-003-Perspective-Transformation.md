# RELAY-003 — Perspective Transformation

**SPO-SI Structural Relay Research Note / Draft Interface Contract**  
**Version:** 0.1.0 (exploratory; not a ratified standard)  
**Authors:** Sizhe Tan & GPT-Obot  
**Repository:** Subject–Predicate–Object Structural Intelligence (SPO-SI)  
**Status:** Directional hypothesis and interoperability design proposal  
**Related:** SPO-002, SPO-003, SPO-004, SPO-006; RELAY-001, RELAY-002; forthcoming RELAY-004

## Abstract

A **Perspective Transformation (PT)** is a bounded, inspectable operation that attempts to translate a representation produced under one subject's observational, semantic, temporal, action, or governance perspective into a representation usable by another subject. The goal is **not** to establish an omniscient viewpoint or guarantee that two subjects mean the same thing. The goal is to make the assumptions, transformations, residual disagreements, uncertainty, provenance, and permissions of a cross-perspective relay explicit. This note proposes a minimal PT contract, a staged transformation lifecycle, a worked example, failure classifications, validation criteria, and falsifiable hypotheses. It connects subject-centric and shared World Models to the broader SPO-SI program without assuming a universal model architecture.

## 1. Motivation: Perspective Is Part of the Meaning

Two subjects may observe the same environment yet maintain different internal models because their sensors, positions, histories, goals, bodies, coordinate systems, vocabulary, and action capabilities differ. Even when their data fields have identical names, the claims may not be interchangeable.

Examples include:

- A robot's `left` relative to its heading versus a fixed map's `west`.
- A pilot's relative bearing and closure rate versus a ground station's global trajectory.
- A human's qualitative `dangerous` versus a planner's numeric collision probability.
- A shared map's traversable corridor versus a particular robot's physically reachable corridor.
- An AI research agent's evidence ranking versus a different agent's evaluation policy.

A relay that silently erases these distinctions can create false agreement. PT therefore treats perspective metadata as a first-class part of any transported claim.

## 2. Scope and Non-Goals

PT addresses **interoperability at a declared boundary**, not a universal theory of perception. It may cover geometric, temporal, semantic, epistemic, action-conditioned, and governance-related transformations. A single PT may implement only one of these dimensions; composition requires explicit compatibility checks.

This proposal does **not** claim:

1. All subjective experiences can be translated.
2. A shared model is an error-free objective or God's-eye model.
3. Coordinate conversion alone solves semantic or action-level interoperability.
4. Any transformed claim is automatically safe for action.
5. A successful functional translation demonstrates machine consciousness.
6. An external model can override a receiving subject's evaluation sovereignty.

## 3. Core Objects and Terminology

**Source subject (`S_src`)**: the producer or perspective owner associated with the input claim.

**Target subject (`S_dst`)**: the prospective consumer, with its own capabilities, constraints, and authority.

**World Model Piece (`WMP`)**: a bounded model claim or reference, as proposed in RELAY-002.

**Perspective descriptor (`V`)**: declared reference frames, sensor modalities, ontology, temporal horizon, action affordances, and uncertainty conventions.

**Transformation contract (`T`)**: the specification of mappings, assumptions, evidence, validity scope, losses, and allowed uses.

**Residual (`R`)**: information that cannot be mapped reliably, including unknowns, incompatible concepts, and unresolved counter-evidence.

**Candidate localized piece (`WMP_dst?`)**: an output awaiting target-side acceptance.

The proposed transformation is:

```text
(WMP_dst_candidate, residuals, audit)
    = PT(WMP_src, V_src, V_dst, T, context)
```

The question mark on the candidate is intentional: **transformation is not validation; validation is not authorization; authorization is not successful execution.**

## 4. The Six Dimensions of Perspective

| Dimension | Source of mismatch | Example of declared transformation |
|---|---|---|
| Spatial / geometric | Origin, orientation, scale, reference frame | Robot-relative bearing to map coordinates |
| Temporal | Timestamp, latency, horizon, sampling | Align observations to a common time with drift bounds |
| Semantic | Ontology, units, labels, categories | `obstacle` to a target's typed occupancy concept |
| Epistemic | Evidence, confidence, uncertainty meaning | Translate confidence metadata without assuming equal calibration |
| Embodied / action | Sensor limits, reachability, control authority | Global route to robot-specific feasible path candidate |
| Normative / governance | Objectives, privacy, permissions, safety policies | Permit observation while disallowing autonomous execution |

A PT contract must identify which dimensions it supports. Unsupported dimensions remain explicit rather than being silently inferred.

## 5. Canonical Minimal Contract

The following fields are **proposed research fields**, not an established industry standard.

| Field | Required | Meaning / check |
|---|---|---|
| `piece_type` | Yes | Must equal `perspective_transformation` |
| `schema_version` | Yes | Version for contract compatibility |
| `transformation_id` | Yes | Stable identifier for this transformation specification |
| `source_profile_ref` | Yes | Reference to a source Subject Profile or equivalent descriptor |
| `target_profile_ref` | Yes | Reference to target Subject Profile or equivalent descriptor |
| `input_piece_ref` | Yes | Source WMP identity and version |
| `input_semantics` | Yes | Units, frame, ontology, uncertainty conventions |
| `output_semantics` | Yes | Expected target conventions and output type |
| `mapping_steps` | Yes | Ordered operations, algorithms, and declared assumptions |
| `validity_scope` | Yes | Time, place, task, and operating regime |
| `uncertainty_handling` | Yes | Propagation, inflation, bounds, or explicit inability to quantify |
| `residuals` | Yes | Unknown, unmapped, disputed, or lossy information; may be empty with justification |
| `provenance` | Yes | Producer, input references, derivation and version history |
| `verification` | Yes | Checks performed and checks still required |
| `governance` | Yes | Permissions, disclosure, acceptance and action constraints |
| `status` | Yes | Draft, candidate, validated-for-scope, rejected, expired, revoked |

Optional fields may include a machine-readable executable transform reference, a reversible mapping, computational cost, calibration dataset, counter-evidence links, or rollback references.

## 6. Reference YAML: Robot-Centric Observation to Shared Map

This illustrative example is **not executable code**, a safety-certified schema, or a real measurement. Identifiers and values are fictional.

```yaml
piece_type: perspective_transformation
schema_version: "0.1.0"
transformation_id: "pt-demo-robot-a-to-map-001"
status: candidate

source_profile_ref:
  id: "subject-robot-a"
  version: "0.1.0"
target_profile_ref:
  id: "subject-shared-map-service"
  version: "0.1.0"
input_piece_ref:
  id: "wmp-obstacle-relative-042"
  version: "1"

input_semantics:
  frame: "robot_a/base_link"
  observation: "relative_obstacle_position"
  units: "meters"
  time_basis: "UTC"
  uncertainty: "2x2 position covariance, meters_squared"
output_semantics:
  frame: "site_map/enu"
  observation: "mapped_obstacle_position_candidate"
  units: "meters"
  time_basis: "UTC"
  uncertainty: "2x2 covariance plus unmodeled-error flag"

mapping_steps:
  - operation: "timestamp_alignment"
    requires: ["observation_timestamp", "pose_timestamp"]
  - operation: "frame_transform"
    requires: ["robot_pose_estimate", "frame_calibration"]
  - operation: "uncertainty_propagation"
    method: "jacobian_first_order_approximation"

validity_scope:
  site: "synthetic_test_area"
  task: "map_annotation_only"
  max_input_age_seconds: 2
  requires_pose_quality_check: true

uncertainty_handling:
  propagate_measurement_covariance: true
  propagate_pose_covariance: true
  correlation_policy: "reject_if_unknown_and_material"
  approximation_disclosure_required: true

residuals:
  - kind: "semantic_unknown"
    description: "object type not identified"
  - kind: "dynamic_state_unknown"
    description: "obstacle motion not observed"

provenance:
  produced_by: "synthetic-relay-demo"
  input_model_ref: "wmp-obstacle-relative-042"
  transformation_revision: "1"
verification:
  completed: ["schema_check"]
  pending: ["pose_alignment_check", "uncertainty_calibration", "target_acceptance"]
governance:
  allowed_uses: ["simulation", "human_review", "map_annotation_candidate"]
  prohibited_uses: ["autonomous_navigation_without_independent_validation"]
  target_acceptance_required: true
  expires_after_seconds: 30
```

This example deliberately distinguishes a *map annotation candidate* from an authorized navigation command.

## 7. Transformation Pipeline and Relay Lifecycle

A proposed lifecycle is:

```text
Discover source WMP and profiles
  -> Identify target task and accepted semantics
  -> Check permissions, versions, scope, and provenance
  -> Compare perspective descriptors
  -> Select / compose mapping operations
  -> Transform with explicit uncertainty and residuals
  -> Validate against target-side invariants and evidence
  -> Obtain governance / subject-side authorization
  -> Deliver candidate or reject
  -> Monitor consequences and record counter-evidence
  -> Revise, expire, or revoke transformation
```

**Fail-closed defaults** are appropriate when a transformation affects safety-critical physical actions or privileges. Research prototypes may instead mark an output as `unverified`, but should not misrepresent it as validated.

## 8. Geometric Translation Is Necessary but Not Sufficient

For a two-dimensional illustrative rigid transform:

```text
p_map = R(theta) * p_robot + t
```

where `R(theta)` is a rotation and `t` is translation. Under a local linear approximation, uncertainty may be propagated by:

```text
Sigma_out ≈ J * Sigma_in * J^T + Sigma_transform
```

This is only valid under its assumptions. Correlated input and pose errors require covariance cross-terms; nonlinearities, multimodal beliefs, unknown biases, or moving objects can invalidate a naive Gaussian approximation. A schema must not imply that a numeric covariance captures every form of epistemic uncertainty.

Even a perfect coordinate transformation does not establish whether a robot can traverse a corridor: traversability depends on embodiment, payload, terrain, safety margin, and control policy.

## 9. Semantic and Action-Conditioned Transformation

A source label `safe_route` should not be translated into the target's `safe_route` merely because the strings match. Instead, compare:

- The relevant hazard taxonomy and excluded hazards.
- Physical capabilities and reachable action sets.
- Risk thresholds and whose preferences they represent.
- Environmental assumptions and validity horizon.
- Evidence quality, calibration, and known failure modes.

When semantics do not align, the transformation should yield a narrower proposition (for example, `route_geometry_candidate`) or a refusal with residuals. **Preserving a weaker, accurate claim is preferable to fabricating a stronger, interoperable one.**

## 10. Subject-Centric and Shared World Model Exchange

### 10.1 Subject -> Shared

A subject exports a bounded observation or hypothesis. The shared model checks provenance, alignment, duplication, conflict, and consistency before integration. Multi-subject agreement may increase confidence only when evidence dependencies and common biases are addressed.

### 10.2 Shared -> Subject

A shared model exports a bounded environmental claim. The target subject localizes it to its sensory frame, capabilities, task, and governance constraints. The result is a **candidate** for local action planning, not an imposed command.

### 10.3 Subject -> Subject

Direct translation can avoid a centralized shared model when tasks and scopes permit. Translation may also proceed through a shared intermediate representation, but this adds dependencies and potential information loss.

### 10.4 No Mandatory God's-Eye Representation

An objective model can be a useful approximation, reference frame, or experimentally calibrated shared representation. It is not a prerequisite for every PT, nor is it assumed infallible.

## 11. Structural Relay Integration with SIF, SSI, and UCPSF

**SIF:** Universal Name-Type, Contracts, Localization, Per-Node execution, Structural Precedent Registry, and Relay APIs can supply discovery and compatibility infrastructure.

**SSI:** Subject boundaries, historical identity, embodied capabilities, self-models, and evaluation sovereignty explain why target-relative meaning cannot be discarded.

**UCPSF:** Scoring Trees/Forests and Control Planes can select candidate transforms, compare their costs and reliability, enforce constraints, and preserve counter-evidence.

**BM-ODWEI:** The `OTHERS` concept provides a useful reminder that a mapping must expose unmatched evidence, unknown categories, and unanticipated residuals rather than force every observation into a known ontology.

**PIRP/PIRU and Collective Learning:** A PT specification may become a portable, versioned intelligence piece, but its portability must be demonstrated within declared contexts.

These are architectural integration proposals, not claims of measured interoperability.

## 12. Evaluation Sovereignty and Governance

A source can attest to what it produced; a target must decide whether to accept and act on the result within its own authorized policy boundary. A central shared model may coordinate, but its authority must be explicit. An imported transform cannot silently expand a subject's permissions or change its objectives.

For a relay to be auditable, record at minimum:

1. Source identity and version, target identity and version.
2. Transformation specification and dependencies.
3. Inputs, outputs, timestamps, and declared validity scope.
4. Residuals, uncertainty assumptions, and unresolved conflicts.
5. Validation outcomes, acceptance decision, and authorizing party.
6. Subsequent errors, counter-evidence, expiry, and revocation.

Sensitive observations should be minimized or redacted according to applicable access controls. A portable relay contract is not permission to disclose private information.

## 13. Failure Taxonomy and Counter-Evidence

| Failure class | Example | Recommended response |
|---|---|---|
| Frame mismatch | Wrong handedness or origin | Reject and request frame calibration |
| Temporal mismatch | Stale obstacle location | Expire or reduce validity horizon |
| Semantic mismatch | `clear` means different things | Narrow claim or preserve unresolved label |
| Embodiment mismatch | Route exceeds robot clearance | Re-localize to target capabilities |
| Uncertainty mismatch | Confidence scores interpreted as calibrated probabilities | Require calibration or retain opaque score |
| Evidence dependence | Multiple sensors share the same upstream source | Avoid double-counting corroboration |
| Governance mismatch | Imported plan exceeds action permission | Block execution and log policy conflict |
| Unknown residual | New hazard outside target ontology | Preserve OTHERS and escalate for review |
| Model drift | Transform calibrated on obsolete hardware | Revalidate or revoke |

Counter-evidence must be able to invalidate not only an output claim, but also the transformation assumptions or mapping algorithm itself.

## 14. Composition and Recursive Perspective Relay

Suppose a claim moves through three perspectives:

```text
V_A --T_AB--> V_B --T_BC--> V_C
```

Composition is not automatically valid. `T_BC(T_AB(x))` may lose information, violate scope, amplify uncertainty, or change semantic meaning. In general:

```text
T_AC_direct(x) != T_BC(T_AB(x))
```

A composed PT must carry its full dependency chain and cumulative residuals. Cyclic relay must not be mistaken for independent evidence. Structural Folding may compress repeated mapping patterns, but Unfolding should restore relevant assumptions and provenance or explicitly disclose irrecoverable losses.

## 15. Falsifiable Research Hypotheses

**PT-H1 — Contract completeness.** Explicit perspective metadata reduces cross-model semantic integration failures compared with untyped payload exchange, at a measurable implementation cost.

**PT-H2 — Residual preservation.** Explicit unknown and unmatched fields reduce unjustified downstream certainty compared with forced ontology matching.

**PT-H3 — Dual-model relay.** Subject-localized shared-model pieces improve task performance or computational efficiency relative to a comparable shared-only or local-only baseline in selected environments.

**PT-H4 — Governance separation.** Separating transformation, validation, and authorization reduces unauthorized actions without unacceptable loss of useful throughput.

**PT-H5 — Compositional auditing.** Provenance-preserving transformation chains improve detection and diagnosis of multi-hop relay errors compared with opaque pipelines.

None of these hypotheses should be treated as established results without controlled evaluation.

## 16. Minimal Validation Program

**Phase A — Schema and conformance:** Define a small JSON Schema or equivalent validator; test missing fields, wrong units, incompatible versions, and expired claims.

**Phase B — Geometric baseline:** Translate synthetic robot-centric observations to a map and back. Measure coordinate error, calibration sensitivity, uncertainty coverage, and latency.

**Phase C — Semantic baseline:** Test ontology mismatches, unknown labels, and target capability differences. Measure unsafe equivalences, abstention quality, and human review burden.

**Phase D — Multi-subject relay:** Compare direct, shared-mediated, and untyped exchange. Include correlated observations, contradictory evidence, and deliberate stale inputs.

**Phase E — Governed action:** Evaluate whether target-side policy checks block unauthorized execution while preserving useful accepted plans.

**Phase F — Structural growth:** Version successful and failed PTs in a precedent registry; test whether learned selection or repair improves outcomes on held-out tasks without overfitting.

### Suggested Metrics

- Valid translation rate under declared scope.
- Semantic preservation / contradiction rate.
- Calibration and uncertainty coverage.
- Residual detection and abstention quality.
- Unauthorized-action rate and false rejection rate.
- Computational cost, latency, and bandwidth.
- Cross-domain transfer performance and drift sensitivity.
- Audit completeness and counter-evidence recovery time.

Use matched compute and data budgets wherever possible; compare against established coordinate-transform systems, ontology mapping pipelines, POMDP belief sharing, and ordinary typed APIs.

## 17. Open Questions

1. What is the smallest perspective descriptor sufficient for a useful class of tasks?
2. When should a translation abstain rather than produce a degraded candidate?
3. How can semantic uncertainty be represented without false numeric precision?
4. Which action affordances can be shared across different embodiments?
5. How should conflicting but locally valid subject perspectives coexist?
6. When does a shared representation genuinely improve coordination?
7. How can transformations preserve privacy while remaining auditable?
8. Which transformation operators can be safely composed or folded?
9. How can counter-evidence update a mapping without destabilizing dependent agents?
10. What conditions make a PT piece portable beyond its original domain?

## 18. Proposed Follow-On Relay Work

The next note, **RELAY-004 — Evidence and Counter-Evidence**, should define how source claims, transformed claims, verification outcomes, dissent, contradictions, and retractions move across subjects and World Models. Its contract should make uncertainty and provenance portable without claiming that agreement implies truth.

A later engineering specification may formalize PT fields into executable schemas, reference implementations, conformance tests, and compatibility levels. Those deliverables are **future work**, not part of this v0.1.0 note.

## 19. Conclusion

Perspective Transformation is a candidate bridge between subject-centric World Models, shared environmental representations, and heterogeneous intelligence systems. Its defining discipline is to preserve **who knows what, from which perspective, under which assumptions, with which uncertainty, for which authorized use**. A good relay need not erase differences among subjects; it should make those differences tractable, inspectable, and, where possible, productively composable.

> SPO-SI is not an attempt to own the world of intelligence, but an attempt to connect intelligent subjects, their models, their actions, and their structural evolution.

---

**Research note:** This document is an exploratory interface proposal. It does not assert experimental validation, a universal perspective ontology, or any inference of subjective consciousness. Contributions, counterexamples, and alternative mappings are welcome as part of open structural intelligence research.
