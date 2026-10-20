# SPO-006 — Research Boundaries and Open Hypotheses

**Project:** Subject–Predicate–Object Structural Intelligence (SPO-SI)  
**Subtitle:** Subject-Centric World Models, Governed Action, and Recursive Structural Evolution  
**Authors:** Sizhe Tan & GPT-Obot  
**Version:** v0.1.0  
**Status:** Open Research Incubator — Research Boundaries / Falsifiable Hypotheses  
**Date:** 2026-10-19  
**Companion notes:** SPO-001 through SPO-005

> **Epistemic statement.** SPO-SI is a proposed organizing architecture and research program. Its integrated performance, novelty relative to established methods, and usefulness of the proposed relay interfaces remain to be demonstrated. This note separates established background, design choices, speculative hypotheses, and empirical claims.

## Abstract

This sixth foundational note defines the scientific and engineering boundaries of Subject–Predicate–Object Structural Intelligence (SPO-SI). It examines what the framework does—and does not—claim; locates it relative to agent–environment loops, partially observable decision processes, embodied and enactive cognition, world models, multi-agent systems, and recursive self-improvement; and converts its architectural intuitions into hypotheses with explicit counterexamples, baselines, metrics, and failure conditions. It proposes an open research process in which relay pieces, uncertainty, negative findings, and alternative designs are first-class outputs. The central ambition is not to subsume world-model research but to make subject boundaries, models, actions, evidence, governance, and structural evolution more interoperable and testable.

---

![Fig-008-Open-Intelligence-Relay-and-Collective-Learning.png](../figures/Fig-008-Open-Intelligence-Relay-and-Collective-Learning.png)

---

## 1. Purpose and Scope

SPO-SI asks how a bounded subject can use evaluative and executable intelligence structures to interact with an environment, update its models, and—under governance—change its own structures. The proposed unit is `(Subject, Predicate, Object)`; the working dynamic loop is:

\[
\mathcal{L}_t=(S_t,P_t,O_t,M_t,H_t,G_t),
\]

where `M` is a working world/self model, `H` a provenance-bearing history, and `G` a governance envelope. These are analytical roles, **not necessarily separate runtime services**. A world model may reside inside `P`; a subject may delegate a part of `P`; and the object may itself be another subject. The formalism is deliberately provisional.

The research objective is to determine whether this decomposition produces **measurable advantages** in interoperability, resource allocation, auditability, transfer, and controlled structural adaptation. An attractive diagram alone does not establish an advantage.

## 2. What Is—and Is Not—Being Claimed

### 2.1 Positive, bounded proposals

1. **SPO as an integration vocabulary.** Subject boundaries, action/evaluation machinery, and environmental objects can be described together without assuming a monolithic model.
2. **Situated world-model use.** A subject's action space, objectives, sensors, and resource constraints can guide which environmental variables are modeled at what fidelity.
3. **Dual model interfaces.** Subject-local models and shared environment models may exchange scoped representations through explicit perspective transforms and validation.
4. **Governed structural adaptation.** Model, policy, scoring, and interface revisions can be proposed and evaluated under authorization and rollback constraints.
5. **Relay-first publication.** Portable, inspectable research pieces can expose hypotheses, assumptions, contracts, provenance, and counter-evidence for outside reuse.

### 2.2 Claims expressly *not* made

- SPO-SI is **not** the first description of a subject acting in an environment.
- SPO-SI is **not** a replacement for POMDPs, model predictive control, active inference, model-based reinforcement learning, or embodied cognition.
- A subject-centered model is **not** automatically more accurate or more efficient than a global model.
- A shared model is **not** a perfect objective or God's-eye account; it can contain bias, inconsistent frames, and missing variables.
- Self-modeling is **not** equivalent to self-modification; self-modification is **not** equivalent to beneficial recursive self-improvement.
- Functional agency, attention, self-monitoring, or recursion do **not** establish phenomenal consciousness.
- The suggested contracts, relay pieces, and workflows are **proposals**, not an implemented interoperability standard.
- A DOI records a citable release; it is **not** peer review or experimental validation.

## 3. Established Neighbors and the Novelty Test

| Research tradition | Relevant established concepts | SPO-SI question beyond relabeling |
|---|---|---|
| POMDPs and decision theory | Partial observability, belief state, policies, rewards | Can explicit subject boundaries and portable contracts improve integration across heterogeneous agents? |
| Model-based RL / MPC | Learned dynamics, action-conditioned prediction, receding-horizon planning | Can task-scoped structural localization allocate model fidelity more efficiently? |
| Embodied / enactive cognition | Sensorimotor coupling, situated action, embodiment | Can the coupling be represented as reusable, auditable engineering interfaces without reducing embodiment to text? |
| Active inference | Generative models, beliefs, action and perception | Which SPO components correspond to existing formal machinery, and which add operational value? |
| Multi-agent systems | Communication, coordination, distributed beliefs | Can provenance-preserving perspective relay reduce harmful semantic mismatches? |
| Knowledge representation / ontologies | Typed concepts, schemas, alignment | How should uncertainty, permissions, and action semantics travel with representations? |
| Software architecture / agent protocols | APIs, capability discovery, tool calling, contracts | Do SPO-specific contracts reduce integration effort beyond general protocol designs? |
| Self-adaptive systems / AutoML / RSI | Monitoring, experimentation, controlled updates | Can evaluator sovereignty and counter-evidence make structural revisions more reliable? |

**Novelty criterion:** a distinct SPO-SI contribution must specify a mechanism, a differentiating interface, a new testable prediction, or an empirically demonstrated gain. A familiar mechanism renamed in SPO terms is not, by itself, a new discovery.

### 3.1 Priority of related-work analysis

Before any strong novelty claim, compare specific implementations and publications rather than broad field labels. Maintain a dated related-work matrix with: reference, method, assumptions, comparable SPO mechanism, difference, evidence, and remaining uncertainty. The initial matrix should be treated as incomplete until literature review is performed.

## 4. Formal Boundaries and Open Definitions

### 4.1 Subject boundary

A subject must have an identifiable observation boundary, action or delegation capacity, operational objectives, and authority conditions. It need not be biological, conscious, or individually embodied. A team or agent collective may be a subject at one level and a set of subjects at another; this nesting must not obscure accountability.

**Open problem:** when does an aggregate merit a distinct subject model rather than being represented as interacting agents?

### 4.2 Predicate boundary

`P` names the mechanisms relating subject and object: perception, estimation, scoring, planning, authorization, execution, and learning. Unlike a narrow logical predicate, it is an **operational relationship stack**. This broad usage should be explicit to avoid semantic confusion.

**Open problem:** which functions belong inside `P`, and which should remain separate modules under independent governance?

### 4.3 Object boundary

`O` can be a physical environment, digital system, task, artifact, or another subject. It is not necessarily passive or fully observable. Interacting subjects may hold conflicting objectives and incompatible representations.

**Open problem:** how should subject–object role changes and nested interactions be represented without infinite regress?

### 4.4 World-model boundary

A **subject-centric world model (SWM)** is a scoped, uncertain, action-relevant representation. A **shared world model (ShWM)** is an intersubjectively maintained representation with explicit provenance and validation. Shared does not imply true, and subjective does not imply arbitrary.

**Open problem:** when should an agent rely on local models, a shared model, or direct sensor evidence instead of either model?

### 4.5 Governance boundary

`G` constrains observation, disclosure, delegation, actuation, learning, and model deployment. Governance may be external to the subject. The existence of a self-model does not grant authority to modify the governing evaluator.

**Open problem:** how can governance survive recursive composition and the transfer of relay pieces across trust domains?

## 5. Open Hypotheses and Falsification Criteria

The following are *hypotheses*, not results. Each should be preregistered with specific tasks, budgets, and statistical tests before evaluation.

### H1 — Subject-First Modeling Efficiency

**Hypothesis.** Under limited compute and clearly bounded tasks, action-relevant local models can deliver better task performance per unit cost than equally budgeted broad models.

**Mechanism.** Localization and scoring allocate representation fidelity to variables relevant to the subject's possible actions.

**Baselines.** Full-state simulator with limited budget; conventional learned dynamics model; model-free agent; standard model-based RL with adaptive attention.

**Measures.** Success/regret, latency, memory, training samples, energy/compute, calibration, out-of-distribution robustness.

**Falsifier.** No statistically and practically meaningful gain over strong task-aware baselines across preregistered settings; persistent loss under relevant distribution shifts.

### H2 — Contract-Based SPO Interoperability

**Hypothesis.** Explicit subject, perspective, action, uncertainty, and governance contracts reduce errors and integration cost across heterogeneous agents.

**Baselines.** Generic JSON/API messages; existing agent communication protocols; typed schemas without SPO-specific semantics.

**Measures.** Integration hours, invalid handoffs, semantic mismatch rate, policy violations, portability across model families, task completion.

**Falsifier.** Equal or worse outcomes after controlling for contract verbosity, engineering effort, and model capability.

### H3 — Dual-World-Model Robustness

**Hypothesis.** Bidirectional correction between local SWMs and shared ShWM improves decisions under partial observability and disagreement, within a fixed communication budget.

**Baselines.** Local-only; shared-only; standard distributed state estimation; conventional multi-agent belief fusion.

**Measures.** Prediction calibration, coordination success, divergence recovery, bandwidth, compute, error propagation.

**Falsifier.** Fusion consistently worsens calibration, latency, or decision outcomes, or gains disappear against competent distributed-estimation baselines.

### H4 — Governed Structural Revision

**Hypothesis.** A provenance-bearing, sandboxed revision process with counter-evidence and rollback reduces harmful structural updates compared with unrestricted automated adaptation.

**Baselines.** Static policy; ungoverned update loop; ordinary CI/testing and human review; existing safe adaptation techniques.

**Measures.** Accepted-update quality, regressions, unsafe actions, rollback success, evaluator drift, cost of oversight.

**Falsifier.** No improvement in risk-adjusted performance, or oversight costs consistently outweigh benefits under relevant conditions.

### H5 — Open Relay and Collective Learning

**Hypothesis.** Publishing modular hypotheses, evidence, assumptions, and typed relay pieces yields more independently reproducible reuse than publishing narrative-only summaries.

**Baselines.** Conventional technical note; code-only repository; unstructured discussion thread; standard reproducibility package.

**Measures.** Independent reproductions, successful transfers, time-to-integration, defect reports, corrected assumptions, downstream attribution.

**Falsifier.** Modular pieces fail to improve reuse or verification after controlling for audience size, documentation quality, and task complexity.

### H6 — Recursive SPO Composition

**Hypothesis.** Explicitly representing interacting agents as nested or linked SPO loops improves accountability and failure localization in multi-agent delegation.

**Baselines.** Flat orchestration graph; hierarchical agent framework; workflow engine with audit logs.

**Measures.** Fault attribution accuracy, authorization correctness, trace completeness, runtime overhead, task success.

**Falsifier.** Added nesting provides no reliable benefit over existing hierarchical abstractions.

## 6. Counter-Hypotheses We Should Welcome

1. **SPO is only a vocabulary.** Existing agent architectures already capture all useful distinctions; explicit SPO structure adds complexity without benefit.
2. **Global-first modeling wins.** For some domains, centralized representations are more efficient, accurate, or safer than local-first modeling.
3. **Perspective translation is the bottleneck.** Conversion losses outweigh any relay benefits, especially across incompatible embodiment or semantics.
4. **Governance is not compositional.** Permissions and evaluation sovereignty cannot reliably survive nested delegation without centralized enforcement.
5. **Open pieces do not guarantee learning.** Documentation and citations can proliferate without actual reuse, validation, or knowledge growth.
6. **Structural growth destabilizes systems.** Updating models, scorers, and contracts simultaneously can introduce more failures than fixed architectures.

These alternatives are not rhetorical objections. They should have named tests and an explicit place in the research record.

## 7. A Minimal Experimental Program

### Stage A — Definition and traceability

Deliver: canonical terminology; subject/object boundary cases; a minimal trace schema; related-work matrix; pre-registered H1–H6 tests. **Gate:** independent readers can distinguish design claims from established results.

### Stage B — Single-subject tasks

Use a small partially observable navigation or software-agent benchmark. Compare local task-scoped models against equally budgeted alternatives. **Gate:** reproducible cost and performance measurements, including failures.

### Stage C — Two-subject relay

Introduce agents with different sensors, coordinate frames, goals, and trust permissions. Compare untyped messages, conventional typed APIs, and SPO contracts. **Gate:** demonstrable semantic correctness and error accounting, not merely successful message delivery.

### Stage D — Shared-model correction

Allow agents to maintain local beliefs and exchange validated model pieces. Test contradictory evidence, stale data, sensor faults, and adversarial inputs. **Gate:** measurable robustness against appropriate fusion baselines.

### Stage E — Governed structural change

Permit only bounded changes to policy, scoring, or world-model components inside a sandbox; require independent evaluation and rollback. **Gate:** audited improvements without unacceptable regression or authority escalation.

### Stage F — Independent relay replication

Publish artifacts and invite external researchers to reproduce one result or reject one hypothesis. **Gate:** independent evidence, not repository traffic or citation count alone.

## 8. Relay Piece Requirements for Scientific Reuse

Every candidate relay piece should expose:

| Field | Minimum content |
|---|---|
| Identity | Stable piece ID, type, version, author/source |
| Scope | Subject, task, domain, operating assumptions |
| Semantics | Inputs, outputs, units, coordinate frame, ontology |
| Epistemics | Confidence representation, uncertainty, missing variables |
| Provenance | Data origin, transformations, timestamps, lineage |
| Permissions | Allowed uses, sharing constraints, authority to execute |
| Validation | Tests, baselines, observed failures, evidence links |
| Compatibility | Required contracts, dependencies, version constraints |
| Revision | Counter-evidence links, supersession, rollback metadata |

A minimal illustrative envelope (not a standardized schema):

```yaml
relay_piece:
  id: "example.swm.local.v0"
  type: "world_model_piece"
  version: "0.1.0"
  subject_scope: "agent-A"
  purpose: "short-horizon navigation"
  coordinate_frame: "agent_local"
  assumptions:
    - "sensor latency below configured threshold"
  uncertainty:
    representation: "calibrated_distribution_required"
    unknowns: ["occluded_objects", "unmodeled_dynamics"]
  provenance:
    source: "local_observations"
    timestamp: "example-only"
  governance:
    allowed_use: ["prediction", "simulation"]
    execution_authority: false
  validation:
    status: "unvalidated"
    evidence_refs: []
  counter_evidence_refs: []
```

The receiver must validate both syntax and semantics. `execution_authority: false` is a descriptive flag, not a security mechanism: actual authorization must be enforced by trusted runtime controls.

## 9. Failure Taxonomy

- **Boundary failure:** unclear ownership, agency, or accountability.
- **Observation failure:** missing, stale, corrupted, or mislocalized evidence.
- **Perspective failure:** invalid coordinate/ontology transformation.
- **Model failure:** miscalibration, omitted variables, simulator–reality mismatch.
- **Scoring failure:** reward hacking, Goodhart effects, incompatible objectives.
- **Relay failure:** valid syntax but invalid semantics, unauthorized sharing, provenance loss.
- **Composition failure:** emergent interactions not visible in local contracts.
- **Evolution failure:** regression, evaluator drift, uncontrolled self-modification.
- **Scientific failure:** unfalsifiable claims, weak baselines, selective reporting, citation without verification.

Each failure should generate a reproducible counter-evidence record rather than being silently discarded.

## 10. Consciousness and Subjectivity: A Strict Research Boundary

The term *subject* denotes an operational boundary for observation, action, objectives, and responsibility. It does not imply sentience. An artificial system can exhibit functional self-monitoring, persistent goals, recursive models, or complex agency without thereby demonstrating phenomenal experience. SPO-SI can contribute testable architectures for functional agency and metacognition, but does not propose a validated theory of consciousness origin. Claims about biological or artificial consciousness require independent conceptual and empirical arguments.

## 11. World Models: Local-First Is a Hypothesis, Not a Dogma

The evolutionary intuition that action-oriented organisms need not maintain complete objective models motivates subject-centric modeling. It does not prove that all biological systems possess explicit predictive world models, or that all engineered systems should be built local-first. In safety-critical coordination, scientific simulation, and infrastructure monitoring, externally constructed shared models may be the natural starting point. The architectural choice should depend on task, observation, fidelity, cost, and trust requirements.

## 12. Research Governance and Anti-Goodhart Practice

SPO-SI should not optimize solely for benchmark scores, citation volume, repository growth, or visually compelling diagrams. A responsible research loop includes:

1. Record the claim and its confidence level.
2. Name plausible competing explanations.
3. Specify independent evaluators and disconfirming observations.
4. Preserve negative results and provenance.
5. Separate proposal authority from deployment authority.
6. Document regressions and rollback outcomes.
7. Update or withdraw claims when evidence changes.

A scoring system cannot be treated as sovereign merely because it is recursive or highly capable. Evaluation authority is an explicit governance choice.

## 13. Open Questions

### Ontology and representation

- What is the smallest SPO unit that remains operationally useful?
- When does a collective become a subject in its own right?
- Can the Predicate role be decomposed without losing a coherent control loop?
- What semantic equivalences are needed for safe cross-model relay?

### World models and perspective

- How should unknown variables (`OTHERS`) be represented and expanded?
- When does shared fusion improve or damage local decisions?
- How can model confidence survive folding, transformation, and localization?
- Which parts of a world model are transferable across embodiments?

### Governance and evolution

- Who may change objectives, evaluators, or action permissions?
- What constitutes an independently validated structural improvement?
- How should multi-agent disputes over evidence and authority be resolved?
- Can safe composition rules be verified under recursive delegation?

### Collective learning

- What minimum artifact makes an insight genuinely relayable?
- How can independent reuse be distinguished from superficial citation?
- How should competing relay pieces coexist without premature standardization?
- What evidence would justify retiring SPO terminology in favor of a simpler framework?

## 14. Publication and Collective Learning Protocol

SPO-SI is intended as an **open research incubator**. Public releases should be citable and versioned, but every document must identify its epistemic status. Suggested contribution classes:

- **Hypothesis:** explicit assumptions, predicted outcomes, falsifiers.
- **Relay piece:** schema, semantics, permissions, provenance, tests.
- **Counter-evidence:** reproducible negative or conflicting finding.
- **Alternative architecture:** comparable mechanism with trade-offs.
- **Replication:** independent rerun, environment, results, discrepancies.
- **Revision:** precise change history and affected claims.

Open publication is an opportunity for collective learning, not proof that collective learning has occurred. Success should be measured through verified transfer, correction, and independent work.

## 15. Integration With the SPO-SI Foundational Series

- **SPO-001:** motivates the move from components to situated intelligence loops.
- **SPO-002:** proposes the canonical SPO architecture and operational roles.
- **SPO-003:** develops subject-centric and shared world-model interfaces.
- **SPO-004:** proposes provenance-aware Structural Relay and interoperability.
- **SPO-005:** explores recursive composition and governed structural evolution.
- **SPO-006 (this note):** defines the limits, counter-hypotheses, evaluation obligations, and publication discipline of the program.

Together, the six notes specify a research direction, not a completed empirical theory.

## 16. Directional Conclusion

**SPO-SI is not an attempt to own the world of intelligence, but an attempt to connect intelligent subjects, their models, their actions, and their structural evolution.**

A second guiding principle is equally important:

**The value of an early structural insight is not measured only by how far its originators can develop it, but also by how far others can carry it.**

The next credible advance is not a grander diagram. It is a narrower, testable contract, a better baseline, a replicated result, a useful counterexample, or a relay piece that an independent team can actually adopt. SPO-SI should remain open to the possibility that some of its ideas are best expressed through existing frameworks, and that its most durable contribution may be interoperability and research navigation rather than a proprietary theory.

---

**Suggested citation:** Tan, Sizhe, and GPT-Obot. (2026). *SPO-006 — Research Boundaries and Open Hypotheses*. Subject–Predicate–Object Structural Intelligence (SPO-SI), v0.1.0. Working research note. Repository DOI to be added after release.

**License and reuse:** Follow the repository-level license and citation metadata. No DOI is asserted before issuance.
