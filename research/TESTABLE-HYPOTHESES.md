# Testable Hypotheses — Subject–Predicate–Object Structural Intelligence (SPO-SI)

**Research status:** Open research incubator; directional hypotheses, not validated findings  
**Version:** 0.1.0  
**Authors:** Sizhe Tan & GPT-Obot  
**Repository:** [Subject-Predicate-Object-Structural-Intelligence](https://github.com/sizhet/Subject-Predicate-Object-Structural-Intelligence) *(proposed URL; verify before publication)*

## Abstract

SPO-SI studies whether explicitly connecting an acting subject, governed intelligence mechanisms, and a modeled environment improves the design, interoperability, and evolution of intelligent systems. This document converts architectural intuitions into falsifiable hypotheses. It specifies operational definitions, controls, metrics, failure conditions, and reproducibility requirements. No results are claimed. Existing work in partially observable control, model-based reinforcement learning, active inference, robotics, and multi-agent learning supplies indispensable baselines.

## 1. Scope and Experimental Discipline

An SPO system is represented provisionally as

$$
\mathcal{I}_t=(S_t,P_t,O_t,M_t,H_t,G_t),
$$

where **S** denotes the acting subject and its capabilities, **P** its perception–evaluation–planning–action machinery, **O** the environment or target, **M** its world-model state, **H** the evidence/history record, and **G** governance constraints. This is an *engineering decomposition*, not a claim about consciousness or a uniquely correct ontology. Observations and actions couple these components over time.

A **subject-centric world model (SWM)** represents task-relevant state conditioned on the agent's sensing, embodiment, goals, and actions. A **shared world model (ShWM)** represents information coordinated across agents or external measurement systems. Neither is guaranteed objective or complete.

An **SPO Relay Piece** is a versioned, typed, provenance-bearing package that communicates some bounded capability, world-model fragment, perspective transformation, or evidence record. A proposed contract is not an implemented standard.

### Mandatory study rules

1. Pre-register task distribution, budgets, metrics, comparison groups, and exclusion rules before confirmatory experiments.
2. Report negative outcomes, uncertainty intervals, seed variation, and compute/latency costs.
3. Compare with strong existing approaches, not only deliberately weak monolithic systems.
4. Separate gains from *additional information*, *additional compute*, and *architectural structure*.
5. Track both task utility and calibration, safety, and governance failures.
6. Avoid extrapolating functional self-modeling or agency to phenomenal consciousness.

## 2. Hypothesis Register

| ID | Directional hypothesis | Principal measurable outcome | Primary falsifier |
|---|---|---|---|
| H01 | Subject-centric models improve resource efficiency under constrained action tasks | Utility per compute and latency | No advantage over matched model-based baselines |
| H02 | Dual SWM–ShWM coordination improves robustness | Performance under partial observability and sensor disagreement | Fusion adds cost without robust benefit |
| H03 | Contract-first Relay reduces integration and transfer cost | Engineer-hours, failure rate, transfer success | Interface overhead outweighs reuse |
| H04 | Explicit perspective transforms reduce semantic/coordinate errors | Transformation correctness and calibration | No improvement over direct adapters |
| H05 | Evidence and counter-evidence Relay improves correction | Time to detect and repair false beliefs | Increased false alarms or no faster correction |
| H06 | Governed structural updates improve safety without eliminating adaptation | Validated gain and policy-violation rate | No favorable safety–utility frontier |
| H07 | Recursive SPO decomposition helps multi-agent composition | Coordination success and scaling | Decomposition underperforms standard multi-agent methods |
| H08 | OTHERS/unknown tracking improves out-of-distribution behavior | OOD calibration and recovery | Unknown tracking is noisy or unhelpful |
| H09 | Public Relay artifacts improve independent reuse | Replication and external adaptation | No demonstrable reuse after comparable exposure |

These hypotheses are not independent: H02 depends partly on H04–H05, and H06 may require H05. Analyze interactions rather than counting positive tests as independent confirmations.

## 3. H01 — Subject-Centric Modeling Under Compute Constraints

**Claim.** When task rewards depend on local action and sensing, an SWM can achieve a better performance–compute trade-off than a global-state model trained and evaluated with the same accessible observations.

**Protocol.** Use partially observable navigation, pursuit/evasion, or manipulation benchmarks. Vary observation range, memory budget, and model capacity. Compare (a) reactive policy, (b) recurrent belief-state policy/POMDP approximation, (c) model-based RL or MPC with local belief, (d) globally structured model restricted to the *same information*, and (e) SPO SWM with task-aware allocation.

**Metrics.** Success, cumulative reward, model error on relevant transitions, p95 action latency, inference FLOPs, energy, and worst-decile outcomes.

**Falsification.** If a strong matched baseline dominates or matches the SPO approach across pre-registered budget bands, reject a general efficiency advantage. Examine whether apparent gains arise from hand-coded task priors.

## 4. H02 — Dual World Models and Bidirectional Correction

**Claim.** Bidirectional SWM–ShWM updates can improve resilience to local sensor failure and stale shared maps.

**Protocol.** Simulate several agents with heterogeneous sensors and a shared map; introduce occlusion, communication delay, conflicting reports, and changing environments. Compare local-only, shared-only, standard Bayesian or learned fusion, and explicit two-way SPO Relay.

**Metrics.** Task completion, map accuracy, belief calibration, conflict resolution time, communication bytes, stale-data incidents, and recovery after injected errors.

**Falsification.** No statistically or practically meaningful improvement over established fusion methods under equal information and bandwidth, or unacceptable synchronization cost.

**Important distinction.** A shared model is an estimate assembled from evidence, not an omniscient ground truth. Simulator state may be used for evaluation but must not leak into the agent's observations.

## 5. H03 — Contract-First Structural Relay

**Claim.** Typed, versioned Relay Pieces improve cross-system reuse relative to ad hoc integration when multiple implementations and revisions are involved.

**Protocol.** Ask independent teams to connect agents, world-model components, and scoring modules across two or more platforms. Randomize integration order where feasible. Compare bespoke adapters, established schemas/APIs, and SPO contracts; provide equivalent documentation and support.

**Metrics.** Integration time, lines of glue code, compatibility defects, version-migration cost, successful transfers, and maintenance effort over multiple releases.

**Falsification.** SPO contracts do not beat conventional API/schema practices after accounting for onboarding and authoring overhead.

**Caution.** Demonstrating value beyond good software engineering—not merely beyond undocumented interfaces—is essential.

## 6. H04 — Perspective Transformation

**Claim.** Explicit transformations with declared source/target frames, semantic assumptions, uncertainty, and provenance reduce silent interoperability failures.

**Protocol.** Exchange local maps and object relations between robots with differing coordinate frames, sensors, and ontologies. Include lossy transformations and ambiguous labels. Compare direct mapping, conventional coordinate/ontology adapters, and Relay transforms with uncertainty and refusal states.

**Metrics.** Pose error, semantic mapping precision/recall, confidence calibration, abstention quality, downstream action failures, and round-trip consistency where reversibility is expected.

**Falsification.** No reduction in consequential errors or excessive abstention that negates utility.

**Non-goal.** Not every perspective is transformable; incommensurate semantics must be representable as unresolved.

## 7. H05 — Counter-Evidence as a First-Class Relay Artifact

**Claim.** Transporting disconfirming evidence together with scope and provenance accelerates correction of invalid model assumptions.

**Protocol.** Inject map changes, faulty sensor claims, outdated policies, and conflicting observations. Compare positive-evidence-only updates, standard uncertainty-aware updates, and structured evidence/counter-evidence Relay.

**Metrics.** Detection delay, false-positive rate, belief repair time, number of unsafe actions before repair, audit completeness, and provenance retrieval accuracy.

**Falsification.** Counter-evidence packages add alert fatigue, spurious revisions, or no improvement over existing anomaly detection and belief updating.

## 8. H06 — Governed Structural Self-Improvement

**Claim.** Candidate structural changes routed through sandbox testing, counter-evidence checks, and explicit authorization can produce a better safety–adaptation trade-off than unrestricted self-updating.

**Protocol.** In a bounded simulator, allow agents to propose modifications to routing trees, policies, model selection, or scoring rules. Compare frozen systems, unconstrained updates, conventional gated deployments, and SPO governed updates. Never use autonomous live-world self-modification for initial experiments.

**Metrics.** Held-out improvement, regression frequency, rule violations, rollback success, audit trace quality, and computational overhead.

**Falsification.** No improvement over ordinary staged rollout and CI/evaluation gates, or governance prevents nearly all beneficial adaptation.

**Critical separation.** Generating a self-change is not evidence of validated improvement; a self-model is not proof of consciousness.

## 9. H07 — Recursive and Multi-Subject Composition

**Claim.** Explicit nested SPO units improve compositional coordination for tasks with changing teams and delegated subtasks.

**Protocol.** Compare flat multi-agent orchestration, hierarchical RL/task planning, and recursive SPO composition in cooperative search, distributed monitoring, or software-agent workflows. Change agent availability and task decomposition during evaluation.

**Metrics.** Completion rate, coordination overhead, delegation failures, robustness to member replacement, scaling curves, and governance violations.

**Falsification.** Conventional hierarchical methods perform as well or better at comparable complexity.

## 10. H08 — Open Residuals and OTHERS

**Claim.** Explicitly recording unmodeled residuals and uncertain observations supports more reliable out-of-distribution behavior than forcing every input into existing categories.

**Protocol.** Evaluate open-set recognition and changing environments; compare closed-set scoring, calibrated uncertainty/OOD detectors, and an SPO residual channel that can trigger targeted observation or model revision.

**Metrics.** OOD AUROC/AUPRC, false-alarm rate, expected calibration error, selective risk, downstream utility, and useful novel-category discovery confirmed by independent review.

**Falsification.** The residual channel yields no improvement over established uncertainty/OOD techniques or causes excessive exploration.

## 11. H09 — Research Relay and Collective Learning

**Claim.** Publicly documented, provenance-rich Relay artifacts can reduce the effort required for independent groups to understand, reproduce, and extend research hypotheses.

**Protocol.** Publish comparable research packages with and without structured contracts, counter-hypotheses, benchmark scripts, and change history. Recruit external teams without privileged assistance. Track adoption over a pre-specified interval and collect blinded usability feedback where possible.

**Metrics.** Independent reproduction rate, time-to-first-reuse, correction submissions, documented forks/adaptations, and successful cross-project integration.

**Falsification.** No reproducible improvement after controlling for community size, topic popularity, and documentation effort.

**Limitation.** DOI issuance and GitHub visibility do not by themselves establish collective learning or scientific impact.

## 12. Cross-Hypothesis Experimental Matrix

| Benchmark family | H01 | H02 | H03 | H04 | H05 | H06 | H07 | H08 | H09 |
|---|---|---|---|---|---|---|---|---|---|
| Partially observable navigation | Primary | Secondary | — | Secondary | Secondary | — | — | Primary | — |
| Multi-robot shared mapping | Secondary | Primary | Primary | Primary | Primary | — | Secondary | Secondary | — |
| Multi-agent task orchestration | — | Secondary | Primary | Secondary | Secondary | Secondary | Primary | — | — |
| Bounded structural-update sandbox | — | — | Secondary | — | Primary | Primary | Secondary | Secondary | — |
| Independent replication exercise | — | — | Primary | — | Secondary | — | — | — | Primary |

*Primary* denotes a benchmark designed to test the hypothesis; *Secondary* denotes supportive evidence only. A dash means the benchmark is not a planned test.

## 13. Minimum Reproducibility Package

Each experiment should publish, when licensing and safety permit:

- hypothesis ID, registration timestamp, predicted direction, and practical-effect threshold;
- environment/version, task generation, observation/action permissions, and leakage checks;
- code commit, configuration, random seeds, hardware, model weights or access conditions;
- compute, wall-clock, memory, network, and energy accounting where feasible;
- baseline selection and tuning budget parity;
- per-seed raw metrics, aggregate intervals, and failure cases;
- Relay Piece schemas and compatibility/version tests;
- counter-evidence records, exceptions, rollback events, and limitations;
- an explicit statement of whether the result supports, weakens, or is inconclusive for the hypothesis.

A sample experiment manifest:

```yaml
experiment_id: SPO-EXP-001
hypothesis_id: H02
status: proposed
benchmark: multi_agent_partial_observation
primary_metric: task_success_rate
secondary_metrics:
  - calibration_error
  - p95_action_latency_ms
  - communication_bytes
baselines:
  - local_only
  - shared_only
  - standard_fusion
candidate: spo_bidirectional_relay
constraints:
  equal_observation_access: true
  matched_compute_budget: true
  no_privileged_state_leakage: true
analysis:
  preregistered: false
  random_seeds: []
  effect_threshold: to_be_defined_before_testing
artifacts:
  code_commit: pending
  dataset_version: pending
  relay_schema_version: 0.1.0
outcome: not_tested
```

## 14. Interpretation and Anti-Goodhart Safeguards

A positive benchmark result is evidence for a bounded claim, not proof that SPO is universally superior. Report trade-offs and adversarial cases, including performance under delayed feedback, model mismatch, governance conflict, and novel tasks. Evaluate whether optimizing the selected metric damages calibration, safety, human oversight, or broader utility. Preserve unresolved anomalies rather than assigning them forced confidence scores.

Prefer Pareto-front comparisons (utility, safety, compute, integration cost) over a single composite score whose weights obscure trade-offs. Document whose objectives and permissions determine the scoring function; evaluator authority must remain explicit.

## 15. Proposed Staged Validation Roadmap

**Stage 0 — Specification review.** Stabilize minimal Subject Profile, World Model Piece, Perspective Transformation, and Evidence/Counter-Evidence schemas. Request external critiques and identify existing equivalent standards.

**Stage 1 — Small controlled tasks.** Test H01, H04, and H08 with reproducible partially observable simulations and strict budget parity.

**Stage 2 — Shared-model integration.** Test H02 and H05 with multiple agents, delayed communication, and injected contradictions.

**Stage 3 — Interoperability trials.** Test H03 using independently implemented components, comparing with mature conventional interface approaches.

**Stage 4 — Bounded recursive updates.** Test H06 and H07 in sandboxes with explicit authorization, regression tests, and rollback.

**Stage 5 — External Research Relay.** Test H09 through independent reuse, reproduction, and counter-evidence contributions. Publish failures and revision history alongside successes.

Progression between stages should be determined by evidence and resources, not calendar promises.

## 16. Open Counter-Hypotheses

- **C01:** Standard belief-state control already captures the useful parts of subject-centric modeling; SPO adds only terminology.
- **C02:** Shared-model synchronization introduces more failure modes than it removes.
- **C03:** Existing schema/ontology systems deliver interoperability with lower complexity.
- **C04:** Explicit perspective transforms cannot keep pace with learned latent representations.
- **C05:** Counter-evidence exchange amplifies unreliable or adversarial reports.
- **C06:** Governance layers degrade adaptation enough to outweigh safety benefits.
- **C07:** Hierarchical multi-agent architectures already provide the compositional benefits claimed for recursive SPO.
- **C08:** Residual channels reproduce existing OOD detection without incremental value.
- **C09:** Public research packaging increases documentation but not meaningful independent adoption.

These counter-hypotheses should be tested as seriously as the corresponding positive claims.

## 17. Relationship to Existing Research

SPO-SI should be positioned relative to partially observable Markov decision processes and belief-state planning; model-based reinforcement learning and model predictive control; active inference and embodied cognition; multi-agent state estimation and decentralized control; semantic interoperability and ontology alignment; uncertainty quantification and OOD detection; and safe policy improvement, software verification, and staged deployment. These fields already address many individual elements of the SPO loop.

The proposed research contribution is the *joint engineering contract* connecting subject boundaries, governed scoring/action, world-model exchange, perspective translation, evidence provenance, and structural evolution. Whether this integration yields measurable incremental value remains open.

For the repository's bibliographic foundation, consult and maintain `research/RELATED-WORK.md`; do not infer novelty from a missing citation.

## 18. Contribution and Revision Protocol

External contributors are invited to submit reproducible negative results, baseline implementations, semantic incompatibilities, improved contracts, and alternative explanations. A useful submission includes: hypothesis ID, scope, methods, evidence, provenance, competing interpretation, and proposed revision. Accepted counter-evidence should remain traceable even if the main architecture changes.

Hypothesis states: `proposed`, `under_test`, `supported_in_scope`, `weakened`, `refuted_in_scope`, or `inconclusive`. State transitions require an evidence record and a dated review; they are not popularity votes.

## 19. Conclusion

SPO-SI is an open research program, not an assertion of completed theory. Its hypotheses ask whether subject-aware world modeling, interoperable structural Relay, explicit evidence and counter-evidence, and governed recursive change can improve intelligent systems in ways that survive comparison with strong existing methods.

> **The value of an early structural insight is not measured only by how far its originators can develop it, but also by how far others can carry it.**

The decisive outputs of this program should be reproducible evidence, reusable contracts, and informative failures—not merely architectural diagrams.

---

**Suggested citation:** Tan, Sizhe, and GPT-Obot. *Testable Hypotheses — Subject–Predicate–Object Structural Intelligence (SPO-SI).* Research incubator working note, version 0.1.0 (2026). Cite the eventual versioned DOI when available.

**License:** Follow the repository's published license; this note does not independently establish one.
