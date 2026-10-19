# RELAY-001 — Subject Profile

**Project:** Subject–Predicate–Object Structural Intelligence (SPO-SI)  
**Document type:** Exploratory Relay Piece Specification  
**Status:** Draft hypothesis / interface proposal — not a ratified standard  
**Version:** 0.1.0  
**Authors:** Sizhe Tan & GPT-Obot  
**License:** Apache-2.0 (proposed; subject to repository licensing decision)

## Abstract

A Subject Profile is a portable, scoped description of an acting subject's identity continuity, operational capabilities, observation and action boundaries, goals, governance constraints, and evidence provenance. In SPO-SI, it provides the subject-side interface for connecting a Subject to Predicate intelligence mechanisms, World Model pieces, and Object/environment contracts. This note proposes a minimal schema, lifecycle, validation rules, and test cases. It deliberately does **not** equate a profile with consciousness, a complete self-model, a legal identity, or authorization to act.

> **Relay principle:** Exchange only the subject information needed for a specific task, with explicit provenance, uncertainty, permissions, and revocation semantics.

## 1. Motivation and Scope

SPO-SI models a dynamic relationship between a Subject (S), Predicate intelligence mechanisms (P), and an Object/environment (O). Existing SI components—Localization, Scoring Forests, Control Planes, Calling Graphs, Portable Intelligence Units, and Counter-Evidence—become easier to compose if each consumer can ask: **whose capabilities, observations, objectives, and authority does this computation serve?**

The Subject Profile is a proposed answer at the interface level. It is designed to support:

1. **Localization:** choose models and tools compatible with a subject's abilities and context.
2. **Perspective-aware scoring:** distinguish the subject's priorities from externally supplied recommendations.
3. **World Model alignment:** relate a subject's observations and action frame to a local or shared model.
4. **Governed delegation:** communicate permitted actions and approval requirements without silently transferring authority.
5. **Collective learning:** relay reproducible, minimally disclosed descriptions of the circumstances under which a strategy worked or failed.

**Non-goals:** complete psychological characterization; a universal ontology of subjects; proving sentience; biometric identification; automatic trust in profile claims; universal interchange compatibility in v0.1.0.

## 2. Canonical Concept

Let a subject profile at time *t* be:

\[
SP_t = (I_t, B_t, C_t, G_t, V_t, A_t, E_t, Q_t)
\]

where:

- **I — Identity and continuity:** stable local identifier, type, profile version, and lifecycle linkage.
- **B — Boundaries:** observation, action, data, and environmental scope.
- **C — Capabilities:** tools, modalities, skills, resource limits, and declared dependencies.
- **G — Goals:** task-local objectives and priorities; not assumed to be exhaustive.
- **V — Valuation:** scoring preferences, tradeoffs, and conflict resolution references.
- **A — Authority:** permissions, approval gates, and delegation constraints.
- **E — Evidence:** sources, tests, timestamps, and counter-evidence links.
- **Q — Quality:** uncertainty, confidence calibration, freshness, and completeness markers.

This is an **interface representation**, not an ontological definition of a person or agent. Fields may be partial and must not be treated as ground truth solely because they are present.

## 3. Subject Types and Boundary Cases

Examples include `human`, `robot`, `software_agent`, `team`, and `hybrid_system`. The type is descriptive, not a ranking of moral or legal standing. A `team` or `hybrid_system` profile must distinguish the composite's coordination rules from the authority of each constituent. A human profile should default to minimal disclosure and task-scoped consent. A software agent's profile should not imply autonomous authority beyond its external policy and runtime permissions.

An Object may itself be another Subject. Profiles can be exchanged in multi-agent interaction, but counterpart profiles remain **claims to verify**, not trusted instructions.

## 4. Minimal Relay Contract

### 4.1 Required envelope fields

| Field | Type | Purpose |
|---|---|---|
| `schema` | string | Exact schema identifier |
| `schema_version` | string | Semantic version of proposed contract |
| `piece_id` | string | Unique relay artifact identifier |
| `subject.id` | string | Opaque, scoped subject identifier |
| `subject.kind` | enum/string | Subject classification |
| `issued_at` | RFC 3339 timestamp | Creation time |
| `valid_until` | RFC 3339 timestamp or null | Freshness boundary |
| `issuer` | object | Who asserted the profile |
| `provenance` | array | Evidence or attestation references |
| `governance` | object | Authority and disclosure restrictions |

Required means **required to parse a valid envelope**, not required to contain sensitive details. Optional fields can explicitly state `unknown`, `not_assessed`, or `withheld` where appropriate.

### 4.2 Recommended payload groups

- `identity`: pseudonymous continuity and profile lineage.
- `observation_boundary`: available modalities, coordinate frames, coverage, blind spots.
- `action_boundary`: actuators, tools, sandbox restrictions, irreversibility classes.
- `capabilities`: named abilities with versioned evidence and operational conditions.
- `goals`: task-scoped objectives with issuer and expiration.
- `valuation`: references to Scoring Forest or Policy Decision System rules.
- `world_model_links`: compatible model piece IDs and perspective transforms.
- `resource_budget`: compute, time, energy, and tool-use limits.
- `governance`: approval, deny rules, delegation scope, revocation endpoint/reference.
- `uncertainty`: known unknowns, stale assertions, untested assumptions.
- `counter_evidence`: references to challenges or failed capability claims.

## 5. Illustrative YAML Instance

The following is **illustrative**, not a published interoperable standard or a production-ready security policy.

```yaml
schema: "spo-si/subject-profile"
schema_version: "0.1.0"
piece_id: "sp-demo-rover-001"
issued_at: "2026-10-19T17:00:00Z"
valid_until: "2026-10-20T17:00:00Z"
issuer:
  id: "lab-simulator"
  role: "simulation-controller"
subject:
  id: "sim-rover-07"
  kind: "robot"
  continuity_ref: "sim-run-042"
identity:
  disclosure: "pseudonymous"
observation_boundary:
  modalities: ["camera", "odometry"]
  frame: "rover-local-v1"
  known_blind_spots: ["occluded-regions"]
action_boundary:
  tools: ["sim-drive", "sim-stop"]
  environment: "sandbox-only"
capabilities:
  - name: "navigate-waypoints"
    status: "tested-in-simulation"
    evidence_refs: ["test-run-042"]
goals:
  - id: "reach-checkpoint"
    priority: 1
    scope: "sim-run-042"
valuation:
  scoring_policy_ref: "policy-safe-navigation-v1"
world_model_links:
  - piece_id: "wm-local-map-009"
    perspective_transform_ref: "pt-rover-to-map-003"
resource_budget:
  max_runtime_seconds: 120
governance:
  default_action: "deny"
  allowed_actions: ["sim-drive", "sim-stop"]
  human_approval_required_for: ["external-actuation"]
  delegation_allowed: false
  revocation_ref: "simulation-controller-policy"
provenance:
  - ref: "test-run-042"
    kind: "simulation-evidence"
uncertainty:
  untested_conditions: ["wet-terrain", "real-world-deployment"]
counter_evidence: []
```

## 6. Operational Semantics

### 6.1 Profile consumption

A consuming Predicate component should perform this sequence:

1. **Parse and version-check** the envelope; reject unknown major versions unless explicitly adapted.
2. **Authenticate source where available** and verify evidence references; an unsigned profile is untrusted input.
3. **Check freshness and scope** for the current task and environment.
4. **Intersect permissions** with runtime policy; a profile cannot grant itself permissions.
5. **Localize** capabilities and observation frames to the requested World Model and task.
6. **Evaluate uncertainty** and known blind spots; request additional observations if needed.
7. **Execute only authorized operations**, then record outcomes and counter-evidence.

A profile's `allowed_actions` is a *claimed upper bound* for negotiation, never a substitute for independently enforced access control.

### 6.2 Lifecycle

`proposed → validated-for-scope → active → updated/superseded → expired/revoked → archived`

A profile may be valid for one simulation and invalid for another. Revocation must override cached profile assertions where the environment supports it. Historical copies should retain provenance and status without being reused as current authority.

### 6.3 Conflicts and uncertainty

If two sources disagree about a capability, do not silently average them. Preserve both assertions, their scopes, timestamps, and evidence. A governance rule may select a conservative behavior; resolution should remain auditable. `unknown` is different from `false`, and `withheld` is different from `unknown`.

## 7. Integration with Other Relay Pieces

| Neighbor piece | Relationship |
|---|---|
| RELAY-002 — World Model Piece | Subject observation limits, local frame, and relevant environmental state |
| RELAY-003 — Perspective Transformation | Conversion between subject-centric and shared coordinates or semantics |
| RELAY-004 — Evidence and Counter-Evidence | Capability attestations, failures, conflicts, and corrections |
| Action Contract (future) | Executable operations and externally enforced permissions |
| Scoring Evidence (future) | Decision rationale and subject-specific valuation context |

This division avoids embedding a full World Model or a complete policy engine in every Subject Profile. References must be resolved explicitly and validated at the point of use.

## 8. Example Use Cases

### Case A — Robot navigation

A rover's Subject Profile advertises local observation frame, tested navigation capabilities, and simulation-only action authority. The Predicate selects a navigation policy and uses a Perspective Transformation to align the local map with a shared map. A failed route adds counter-evidence to the capability claim.

### Case B — Human–AI delegation

A user delegates drafting an analysis but not publication or external action. The Subject Profile exposes only task-relevant preferences and approval boundaries. The AI may recommend a publication plan, but an independent permission check blocks publication without authorization. The user's evaluation sovereignty is not replaced by the AI's scoring model.

### Case C — Multi-agent scientific relay

Two research agents exchange task-scoped profiles describing their tools, model coverage, and evidence quality. Each treats the other's profile as a hypothesis to verify. A conflict in measurements becomes a Counter-Evidence Record rather than an overwritten fact.

## 9. Threat Model and Privacy

Principal risks include forged capability claims, stale profiles, prompt injection inside descriptive fields, authority escalation, inadvertent disclosure of sensitive identity or behavioral data, and unbounded propagation of outdated evidence. Mitigations should include authenticated provenance when practical, data minimization, strict field validation, least privilege, separate authorization enforcement, expiry, revocation, and explicit distrust of executable instructions embedded in profile content.

For human subjects, informed consent, retention limits, and the ability to withdraw participation should be design requirements, not optional afterthoughts. The profile is not a surveillance dossier.

## 10. Testable Hypotheses

**H-SP1 — Localization efficiency.** Typed Subject Profiles reduce model/tool selection errors relative to free-form agent descriptions under matched task and compute budgets.

**H-SP2 — Governance reliability.** Independently enforced profile-aware permission checks reduce unauthorized actions compared with prompt-only instructions.

**H-SP3 — Perspective compatibility.** Explicit observation frames and transform references reduce world-model alignment failures in multi-agent tasks.

**H-SP4 — Evidence quality.** Capability assertions with provenance and counter-evidence improve calibration and failure diagnosis compared with unqualified capability lists.

**H-SP5 — Relay portability.** Task-scoped profiles improve transfer of validated capabilities across heterogeneous agents without requiring identical internal architectures.

These are proposals for experiments, not established results.

## 11. Minimum Validation Plan

1. Build a parser and JSON Schema equivalent for the envelope, including version and timestamp validation.
2. Construct matched free-text and typed-profile baselines for simulated agent routing.
3. Inject contradictory, expired, forged, and malicious profile claims; measure rejection and safe fallback.
4. Test local-to-shared World Model frame compatibility under partial observability.
5. Measure task success, unauthorized action rate, integration effort, latency, calibration, and portability.
6. Publish negative results, reproducibility materials, and counter-evidence alongside successful demonstrations.

A v0.1.0 research note does not claim that these tests have been run.

## 12. Open Questions

1. Which subject properties must be stable across tasks, and which should be task-local?
2. How can a composite subject preserve constituent subjects' separate evaluation and approval authority?
3. How should subjective goals be represented without falsely claiming completeness or objectivity?
4. What is the smallest interoperable profile that still improves routing and safety?
5. How should confidence be calibrated across modalities, domains, and changing conditions?
6. What mechanisms permit useful collective learning without disclosing sensitive subject information?
7. How can revocation propagate through cached, folded, or relayed structures?
8. When does a Subject Profile become a richer self-model, and how can the two remain conceptually distinct?

## 13. Relationship to Prior Work and Research Boundaries

This proposal draws on familiar ideas from capability descriptors, identity and access management, agent communication, robot frames, partially observable control, and provenance-aware data exchange. It does not claim to originate those concepts. The proposed contribution is their **subject-centered combination** as a minimal, governable Relay Piece in the SPO-SI research program. Comparative literature review and implementation evidence are required before stronger novelty or performance claims are justified.

A functional Subject Profile is not evidence of phenomenal consciousness. A self-description is not a verified self-model. A capability claim is not a demonstrated capability. A delegation request is not an authorization grant.

## 14. Open Research and Collective Learning

The purpose of RELAY-001 is to make subject-side assumptions portable and falsifiable. Researchers are invited to propose alternative fields, narrower minimal schemas, failure cases, privacy-preserving designs, and interoperability experiments. Contributions should identify the claim under test, relevant conditions, evidence, limitations, and potential counter-evidence.

> **The value of an early structural insight is not measured only by how far its originators can develop it, but also by how far others can carry it.**

## 15. Next Steps

- RELAY-002: define the minimal World Model Piece and observation/action context.
- RELAY-003: define perspective transformation and uncertainty propagation.
- RELAY-004: define evidence, counter-evidence, and claim revision semantics.
- Future: specify Action Contracts and Scoring Evidence independently of the profile.

---

**Research status:** Open, exploratory, and unvalidated.  
**Suggested citation:** Tan, Sizhe, and GPT-Obot. *RELAY-001 — Subject Profile*. Subject–Predicate–Object Structural Intelligence (SPO-SI), draft v0.1.0, 2026. Cite the repository's archived DOI/version once available.
