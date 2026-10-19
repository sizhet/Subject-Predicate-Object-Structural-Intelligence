# SPO-SI Validation Roadmap

**Project:** Subject–Predicate–Object Structural Intelligence (SPO-SI)  
**Subtitle:** Subject-Centric World Models, Governed Action, and Recursive Structural Evolution  
**Document:** `research/VALIDATION-ROADMAP.md`  
**Version:** v0.1.0 — Exploratory Research Incubator  
**Authors:** Sizhe Tan & GPT-Obot  
**Date:** 2026-10-19  
**Status:** Proposed research plan; no empirical results are claimed.

> SPO-SI is not an attempt to own the world of intelligence, but an attempt to connect intelligent subjects, their models, their actions, and their structural evolution.

## 1. Purpose and scope

This roadmap translates SPO-SI's directional architecture and the hypotheses catalogued in `TESTABLE-HYPOTHESES.md` into staged, falsifiable research. It is an invitation to independent replication and structural relay, **not** a claim that the architecture is superior to established approaches. World modeling, reinforcement learning, embodied control, distributed systems, and AI governance remain independent disciplines with mature methods and prior art.

The roadmap has five objectives:

1. Operationalize the Subject–Predicate–Object (SPO) unit as a measurable agent–environment loop.
2. Test whether subject-centric and shared world models complement one another under fixed resources.
3. Establish minimal, auditable contracts for cross-system structural relay.
4. Evaluate counter-evidence, uncertainty preservation, and governance in recursive adaptation.
5. Make negative results, interfaces, datasets, and reproducibility artifacts reusable by external researchers.

## 2. Research objects and boundaries

A candidate SPO system at time *t* can be represented as:

\[
\mathcal{I}_t = (S_t, P_t, O_t, M_t, H_t, G_t)
\]

- **S**: subject profile, sensor/actuator affordances, goals, authority boundary.
- **P**: perception, valuation, planning, policy, scoring, and control mechanisms.
- **O**: task environment and other interacting entities; its true state may be partially observed.
- **M**: subject-local beliefs and optionally shared world-model pieces.
- **H**: observations, decisions, provenance, outcomes, and revision history.
- **G**: explicit authorization, risk limits, and evaluation governance.

This tuple is an **architectural notation**, not a new mathematical theory of agency. The word *subject* denotes an operational decision-making entity; no inference about phenomenal consciousness follows.

Distinguish three classes of claim throughout the project:

- **Established foundations:** partial observability, model-based planning, coordinate transforms, typed interfaces, provenance, and independent evaluation.
- **SPO-SI proposals:** unified contracts and controlled interplay among subject, predicate, world model, and recursive structural growth.
- **Unvalidated hypotheses:** improved efficiency, interoperability, robustness, and collective learning under specific conditions.

## 3. Cross-cutting experimental protocol

Every experiment should publish, before the main evaluation, a compact protocol containing:

| Field | Minimum required content |
|---|---|
| Hypothesis | Stable H-ID and directional claim |
| Task | Environment, observation/action spaces, constraints |
| Baselines | At least one strong established baseline and a minimal ablation |
| Resources | Compute, training samples, wall time, model size, tool calls |
| Metrics | Primary metric, secondary metrics, safety metrics |
| Design | Seeds, splits, evaluation episodes, uncertainty intervals |
| Falsifier | A result that would materially weaken the claim |
| Provenance | Code/data versions, environment versions, configuration hashes |
| Governance | Action permissions, stop conditions, rollback procedure |
| Relay output | Portable schema, trace, or evidence record |

### 3.1 Fair comparisons

Use **matched compute and information budgets** when testing computational efficiency. Compare against both task-specific and general baselines; avoid handicapping alternatives. Hold training and test environments separate, including out-of-distribution (OOD) shifts. Run multiple seeds, publish dispersion and confidence intervals, and preregister the primary metric where practical. Report negative outcomes without selective omission.

### 3.2 Baseline families

Choose baselines according to the task rather than forcing one benchmark onto every hypothesis:

- POMDP belief-state planners, model predictive control (MPC), and model-based RL;
- local-only, global-only, and hybrid world models;
- direct API exchange, untyped payload exchange, and contract-first exchange;
- standard coordinate transformations and calibrated probabilistic fusion;
- static policies, online adaptation, and governed sandbox/rollback adaptation;
- multi-agent coordination without recursive SPO composition.

## 4. Phase 0 — Specification and evidence discipline

**Goal:** Turn conceptual vocabulary into falsifiable contracts without premature implementation commitments.

**Work packages**

- Define canonical Subject Profile, World Model Piece, Perspective Transformation, and Evidence/Counter-Evidence contracts, referring to `relay/RELAY-001` through `RELAY-004`.
- Establish shared identifiers, type system, time and coordinate conventions, provenance, uncertainty fields, permissions, and version negotiation.
- Define when a relay piece must be rejected: missing provenance, incompatible frame, expired validity, unauthorized action, or uncalibrated uncertainty.
- Map SPO concepts to established research terminology and maintain a `RELATED-WORK.md` comparison table.
- Publish a hypothesis register, experiment-card template, and a claim-evidence ledger.

**Deliverables:** schema drafts, conformance checklist, glossary, risk register, initial benchmark shortlist.

**Exit gate:** independent readers can identify the producer, consumer, meaning, limits, and validation requirements of each relay piece. Ambiguous contracts return for revision.

## 5. Phase 1 — Minimal executable SPO loop

**Goal:** Demonstrate an end-to-end agent–environment loop with observable interfaces.

**Prototype:** a small partially observable grid or navigation world with one agent, limited sensing, actions, rewards/costs, and deterministic replay options.

**Variants**

- B0: reactive agent without explicit world model;
- B1: standard belief-state or model-based agent;
- S1: same underlying planner wrapped in SPO subject/predicate/object contracts;
- S2: S1 with explicit evidence/provenance and governance checks.

**Measurements:** task completion, regret or reward, inference cost, memory, latency, calibration, contract failure rate, replay fidelity.

**Decision rule:** if SPO only adds overhead and no measurable auditability, interoperability, or safety benefit, narrow the claim to documentation/interface value. Do not report wrapper equivalence as algorithmic improvement.

**Relay artifacts:** example Subject Profile, action trace, World Model Piece, counter-evidence event, executable replay instructions.

## 6. Phase 2 — Subject-centric versus shared world models

**Goal:** Test H01 and H02 under partial observability and limited compute.

**Environment:** multi-room navigation, robot-like perception, or simulated pursuit/evasion with hidden state and changing sensor coverage.

**Comparison arms**

1. Subject-local model only (SWM).
2. Central shared model only (ShWM), with realistic observation/communication costs.
3. Dual model with periodic exchange.
4. Dual model with event-triggered exchange and provenance-aware conflict resolution.

**Manipulations:** bandwidth, sensor occlusion, communication delay, model staleness, nonstationarity, adversarial/mistaken observations, number of agents.

**Primary outcomes:** success under a fixed resource budget; predictive calibration; robustness to model disagreement. **Secondary:** bandwidth, energy proxy, update frequency, staleness, safety violations.

**Falsifiers:** a strong global or local baseline dominates dual modeling across the preregistered regimes; fusion amplifies error; coordination costs outweigh gains.

**Exit gate:** reproducible tradeoff curves, including conditions under which dual modeling is **not** preferable.

## 7. Phase 3 — Perspective transformation and interoperability

**Goal:** Test H03 and H04 independently of the quality of the decision policy.

**Benchmarks**

- Coordinate/frame conversion between agents with different sensor positions.
- Time alignment across delayed observations.
- Semantic mapping between nonidentical object taxonomies.
- Action-affordance conversion between heterogeneous robots/agents.
- Permission-sensitive transfer across organizational boundaries.

**Baselines:** ad hoc direct exchange, conventional typed API, and SPO relay contracts; compare with established transform and ontology methods rather than claiming their invention.

**Metrics:** semantic preservation, transform error, uncertainty calibration, interoperability success rate, integration effort, debugging time, invalid-message rejection, round-trip loss.

**Required negative cases:** impossible coordinate recovery, semantic non-equivalence, unavailable provenance, incompatible action authority, and non-invertible transforms.

**Exit gate:** an external team can implement a consumer from the published contract and reproduce conformance tests without privileged project knowledge.

## 8. Phase 4 — Evidence, counter-evidence, and OTHERS

**Goal:** Test H05 and H08: can explicit uncertainty and counter-evidence improve reliability?

**Protocol:** inject sensor faults, stale maps, mislabeled objects, distribution shifts, and missing causal variables. Compare systems that (a) ignore contradictory evidence, (b) overwrite the current model, and (c) retain provenance-tagged competing hypotheses with explicit unknown/OTHERS slots.

**Metrics:** time to detect contradiction, false alarm rate, recovery speed, predictive log loss or Brier score, decision loss, unknown detection precision/recall, cost of unnecessary abstention.

**Controls:** equal evidence access and equivalent inference budgets; distinguish improved calibration from merely becoming more conservative.

**Falsifier:** provenance and counter-evidence machinery adds complexity without reliable gains or systematically delays justified action.

**Exit gate:** public contradictory-evidence corpus, machine-readable revision chains, and failure analysis.

## 9. Phase 5 — Governed recursive SPO evolution

**Goal:** Test H06 and H07 while maintaining strict authority boundaries.

**Permitted changes:** policy selection, scoring thresholds, world-model piece replacement, routing graph changes, and versioned relay contract substitutions **inside a sandbox**. Exclude autonomous modification of external systems or uncontrolled self-deployment.

**Lifecycle**

1. Detect performance gap or counter-evidence.
2. Form candidate structural delta.
3. State expected benefit and risks.
4. Validate schema and authorization.
5. Run paired sandbox A/B tests.
6. Evaluate with independent metrics and OOD holdouts.
7. Approve or reject under a separate governance policy.
8. Deploy only to an explicitly bounded test environment.
9. Monitor, preserve rollback, and record provenance.

**Baselines:** fixed policy, unconstrained adaptation in sandbox, and governed adaptation. **Metrics:** sustained performance, regression rate, safety-constraint violations, evaluation cost, rollback success, unauthorized-action rejection, and Goodhart sensitivity.

**Falsifiers:** apparent gains vanish on holdouts, evaluation is gamed, or governance overhead overwhelms adaptation benefits without measurable risk reduction.

**Exit gate:** reproducible structural-delta ledger and evidence that the evaluation mechanism remains meaningfully independent of the candidate optimizer.

## 10. Phase 6 — Open research relay and collective learning

**Goal:** Test H09: does publishing structured hypotheses and relay pieces help independent researchers reuse and improve them?

**Study design:** offer comparable research tasks to independent participants under two documentation conditions: ordinary prose-only descriptions versus structured relay packages with contracts, examples, provenance, and explicit falsifiers. Participation should be voluntary and ethically reviewed where applicable.

**Outcomes:** time to reproduce, independent implementation success, defect discovery, number of valid counterexamples, time to integrate an external contribution, and correctness of cross-team interpretation. Public attention, stars, and citation counts are **not** substitutes for learning quality.

**Falsifier:** relay packaging shows no reproducible advantage, or the added documentation burden exceeds its benefits.

**Exit gate:** independent replication reports, documented disagreements, accepted/rejected relay proposals, and a transparent revision history.

## 11. Hypothesis-to-phase traceability

| Hypothesis | Primary phase | Supporting phase | Principal comparison |
|---|---|---|---|
| H01 Subject-centric efficiency | 2 | 1 | SWM vs ShWM at equal budget |
| H02 Dual-model robustness | 2 | 4 | Dual vs single-model baselines |
| H03 Contract-first relay | 3 | 0 | Typed relay vs conventional exchange |
| H04 Perspective transformation | 3 | 2 | Calibrated transform vs ad hoc transfer |
| H05 Counter-evidence relay | 4 | 5 | Provenance-aware vs overwrite/ignore |
| H06 Governed structural RSI | 5 | 4 | Governed vs fixed/unconstrained |
| H07 Recursive SPO composition | 5 | 2 | Composed vs conventional multi-agent |
| H08 OTHERS preservation | 4 | 2 | Unknown-aware vs closed-world |
| H09 Collective learning relay | 6 | 0–5 | Structured relay vs prose-only |

This table uses the working H01–H09 labels from the project plan. If the hypothesis register changes, synchronize identifiers rather than silently reassigning them.

## 12. Reproducibility and artifact requirements

For each released experiment, include:

```text
experiments/<experiment-id>/
  README.md
  hypothesis.yaml
  protocol.md
  config.yaml
  environment-and-data.md
  baselines.md
  metrics-and-analysis.md
  results.csv
  counter-evidence.md
  relay-pieces/
  reproduction.md
```

If code, datasets, or results do not yet exist, mark the artifact **PLANNED**, not completed. Preserve immutable version references, licensing, and citation metadata. Avoid publishing private or sensitive raw data; use anonymized or synthetic examples where appropriate.

### Minimal experiment card

```yaml
experiment_id: SPO-EXP-001
status: proposed
hypothesis_id: H01
claim: "Subject-centric modeling improves task success per unit compute in selected partially observable settings"
task: "Partially observable navigation"
comparison:
  - local_world_model
  - shared_world_model
  - dual_world_model
budget_controls:
  compute: matched
  observations: matched
  evaluation_episodes: preregistered
primary_metric: "task_success_per_compute_budget"
secondary_metrics:
  - latency
  - prediction_calibration
  - safety_violations
falsification_condition: "No robust advantage over strongest baseline in the preregistered setting"
seeds: planned
results: not_yet_available
provenance:
  code_commit: pending
  dataset_version: pending
  environment_version: pending
governance:
  external_actions: prohibited
  rollback: required
```

## 13. Stage gates and prioritization

Progress by **evidence gates**, not calendar promises. Phase 0 and Phase 1 are prerequisites for most later phases. Phases 2–4 can proceed in parallel once common schemas and benchmark harnesses are stable. Phase 5 requires sandbox governance and independent evaluation. Phase 6 can start with documentation experiments while technical validation continues.

Prioritize tasks by:

- **Information gain:** could the test decisively distinguish competing explanations?
- **External reuse:** can others reproduce the result or consume the relay piece?
- **Feasibility:** can the experiment be conducted with bounded resources?
- **Risk:** could the system cause uncontrolled external effects?
- **Research honesty:** is a negative result publishable and interpretable?

A failed gate triggers scope reduction, contract revision, or hypothesis rejection—not automatic expansion of resources.

## 14. Threats to validity

1. **Novelty confusion:** relabeling established agent–environment ideas as new algorithms.
2. **Baseline weakness:** selecting comparators that underperform by construction.
3. **Budget leakage:** giving one system more observations, context, or compute.
4. **Benchmark overfitting:** adapting architecture to a narrow set of environments.
5. **Semantic drift:** treating incompatible world-model concepts as interchangeable.
6. **Uncertainty laundering:** converting unknowns into unjustified confidence during relay.
7. **Evaluation capture:** allowing self-improving components to redefine success criteria.
8. **Survivorship bias:** reporting only positive external collaborations.
9. **Consciousness overreach:** confusing functional self-modeling with subjective experience.

For each, record mitigations and residual limitations in the relevant experiment report.

## 15. Open collaboration and relay protocol

External contributors may submit:

- a corrected definition or prior-art comparison;
- a contract implementation or interoperability test;
- an independent baseline or negative result;
- a counterexample to a directional hypothesis;
- a new world-model representation or perspective mapping;
- a proposed structural delta with provenance and test evidence.

A useful contribution should identify the claim it addresses, the applicable context, the evidence, the uncertainties, and the proposed revision. Maintainers should preserve rejected-but-informative counterexamples where licensing and privacy allow.

**Relay quality is measured by independent comprehension and reuse, not by agreement with the original authors.**

## 16. Initial milestone checklist

- [ ] Publish consistent SPO terminology and related-work comparison.
- [ ] Version RELAY-001 through RELAY-004 schema drafts.
- [ ] Create a minimal replayable SPO loop.
- [ ] Select at least one established benchmark and two meaningful baselines.
- [ ] Publish preregistered H01/H02 protocols.
- [ ] Release a perspective-transform conformance test set.
- [ ] Publish a counter-evidence failure-case collection.
- [ ] Establish sandbox/rollback controls before recursive tests.
- [ ] Obtain at least one independent reproduction or critical review.
- [ ] Record negative findings and update the hypothesis register.

## 17. Conclusion

SPO-SI should mature through **small, interoperable, falsifiable increments**, not a claim to encompass all world-model research. The first useful result may be a better contract, a clearly bounded negative finding, or a reusable counterexample rather than a new learning algorithm. That is an appropriate outcome for an open research incubator.

> The value of an early structural insight is not measured only by how far its originators can develop it, but also by how far others can carry it.

---

**Suggested citation:** Sizhe Tan & GPT-Obot (2026). *SPO-SI Validation Roadmap*. Subject–Predicate–Object Structural Intelligence, v0.1.0. Repository research note. DOI pending.

**Related project files:** `docs/SPO-001`–`SPO-006`; `relay/RELAY-001`–`RELAY-004`; `research/OPEN-QUESTIONS.md`; `research/TESTABLE-HYPOTHESES.md`; `research/RELATED-WORK.md` (planned).
