# SPO-001 — From Structural Components to Intelligence Loops

**Project:** Subject–Predicate–Object Structural Intelligence (SPO-SI)  
**Subtitle:** Subject-Centric World Models, Governed Action, and Recursive Structural Evolution  
**Authors:** Sizhe Tan & GPT-Obot  
**Status:** Open Research Incubator — Directional Hypothesis / Architecture Note  
**Version:** v0.1.0  
**Date:** 2026-10-19

> **Research stance:** SPO-SI is not an attempt to own the world of intelligence, but an attempt to connect intelligent subjects, their models, their actions, and their structural evolution.

## Abstract

Structural Intelligence (SI) has developed a rich repertoire of reusable components: differential structures, calling graphs, localization, per-node intelligence, scoring trees and forests, control planes, contracts, structural folding, counter-evidence, and recursive improvement. Yet a collection of capable components is not by itself a situated intelligent system. Intelligence unfolds through a subject with particular capabilities and constraints, mechanisms for perception and action, and a world that responds. This note proposes **Subject–Predicate–Object Structural Intelligence (SPO-SI)** as an exploratory organizing hypothesis for connecting these elements in dynamic, governed, learnable intelligence loops.

SPO-SI is a *systems integration and research interface proposal*, not a claim to have invented the agent–environment loop, solved world modeling, or demonstrated machine consciousness. Its potential contribution is to connect subject boundaries and evaluation sovereignty, structural control and scoring, action-conditioned world models, and open-ended structural growth through explicit interfaces. We outline the core loop, its relationship to prior work, testable hypotheses, a minimal Relay Piece vocabulary, and a research roadmap.

**Keywords:** Structural Intelligence; SPO-SI; subject-centric world model; agent–environment loop; control plane; scoring forest; structural relay; counter-evidence; recursive structural evolution; collective learning.

---

## 1. Why a New Organizing Unit?

Prior SI research has asked how intelligence components can be represented, localized, selected, composed, governed, and improved. These questions remain foundational. However, a reusable structural component has no intrinsic answer to four situated questions:

1. **Whose intelligence?** Which subject owns the goals, permissions, action capabilities, and evaluation authority?
2. **Intelligence for what?** Which task, environment, other agents, and risks define the problem?
3. **Through what mechanism?** Which perceptions, world models, scoring operators, policies, and actions connect subject to environment?
4. **How does the system change?** Which observations and counter-evidence justify model, policy, or structural updates?

SPO-SI proposes that these questions be studied together as an **intelligence loop** rather than answered independently by disconnected modules.

### 1.1 From a component inventory to a situated loop

A component inventory might contain a world model, planner, scoring tree, memory, policy, and evaluator. A situated loop must additionally specify ownership, observations, action interfaces, environmental transitions, feedback, time, and governance. The proposed transition is:

```text
Structural Components
  -> Contracts, Localization, and Composition
  -> Subject-Bound Perception and Valuation
  -> World-Conditioned Action
  -> Feedback, Counter-Evidence, and Learning
  -> Governed Structural Evolution
  -> Next Intelligence Loop
```

This shift is not a rejection of modular SI. It makes modular SI operational within a subject–world relationship.

## 2. The SPO Hypothesis

We begin with a conceptual triple:

\[
\mathcal{I}=(S,P,O)
\]

- **S — Subject:** the entity or organized system with a boundary, capabilities, goals, identity/history, permissions, and some locus of evaluation or action authority.
- **P — Predicate Intelligence:** the executable and evaluative relationship between subject and world, including perception, representation, world modeling, scoring, planning, policy selection, control, and learning.
- **O — Object / Environment:** the task, world, other subjects, and observable or latent conditions with which the subject interacts.

**Terminology caveat:** *Predicate* here is a deliberately broadened engineering metaphor, not a claim that the predicate of natural-language grammar is equivalent to a full control architecture. The term must earn its utility through clear interfaces and predictive or engineering benefits.

### 2.1 A dynamic rather than merely grammatical triple

The static triple is insufficient for learning and evolution. A working formulation is:

\[
\mathcal{I}_t=(S_t,P_t,O_t,M_t,H_t)
\]

where \(M_t\) is the subject's world-model state and \(H_t\) its relevant history, evidence, and provenance. The model and history are made explicit for engineering clarity; they may also be viewed as internally hosted substructures of \(S\) or \(P\).

At time \(t\), a subject receives an observation, selects an action, and updates its internal structures:

\[
y_t=\operatorname{Observe}(S_t,O_t)
\]

\[
a_t=\operatorname{Policy}(S_t,P_t,M_t,y_t)
\]

\[
O_{t+1}\sim T(\cdot\mid O_t,a_t)
\]

\[
(M_{t+1},P_{t+1},H_{t+1})
=\operatorname{Update}(M_t,P_t,H_t,y_t,a_t,y_{t+1})
\]

The transition kernel \(T\) expresses environmental dynamics and may be unknown; the equations are **schematic research notation**, not an implemented universal algorithm. In multi-agent settings, other agents' actions also influence the transition.

### 2.2 The structural-growth distinction

Many adaptive systems update estimates or policy parameters. SPO-SI asks when the system should also modify the **structure** of its representations, routing, scoring operators, interfaces, and delegated capabilities. Such updates require evidence, tests, rollback paths, and policy authorization. The central claim is not that structural modification always helps, but that it deserves a first-class place in the intelligence loop.

## 3. Subject Is Not an Annotation on the Scoring Forest

A subject cannot be reduced to a label attached to an otherwise universal scoring mechanism. Its boundary changes which evidence is accessible, which actions are possible, which risks matter, and who may authorize an update.

A subject profile should distinguish:

- **Embodiment or execution boundary:** sensors, tools, compute, physical or software actuators.
- **Identity and history:** persistent state, provenance, prior commitments.
- **Goals and valuation:** task objectives, priorities, uncertainty tolerance.
- **Authority:** permissions, accountability, delegation and revocation.
- **Capability limits:** latency, energy, knowledge, and action constraints.

This framing is useful for humans, robots, software agents, and human–AI teams, while avoiding an unsupported assertion that all such subjects have phenomenal consciousness.

## 4. Predicate Intelligence as an Executable Relationship

Predicate Intelligence is the active bridge between a particular subject and its world. A possible modular decomposition is:

```text
Observation / Perception
      |
      v
Localization + Subject-Centric World Model
      |
      v
Scoring Forest + Policy / Control Plane
      |
      v
Planning / Trajectory / Delegation
      |
      v
Authorized Action
      |
      v
Environment Feedback + Counter-Evidence
      |
      v
Model, Policy, and Structural Update
```

The modules need not share one representation or one model family. LLMs, symbolic systems, simulators, learned dynamics models, human experts, and specialist services may participate behind explicit contracts. A control plane governs admissible actions and changes; it does not magically make model outputs correct.

## 5. World Models: Subjective and Shared

A world model need not be a complete, detached map of reality. For an acting subject, it can be an uncertainty-aware, action-conditioned predictive representation:

\[
M_S:(b_t,a_t)\mapsto \widehat{b}_{t+1}
\]

Here \(b_t\) is a belief state rather than necessarily the true environment state. A useful model predicts what may happen under candidate actions and what new observations might follow.

### 5.1 Subject-centric world model (SWM)

An SWM prioritizes variables relevant to the subject's goals, sensors, actuators, constraints, and current context. It may be partial, task-specific, and computationally economical. This is a design hypothesis, not evidence that a subjective model always outperforms a global one.

### 5.2 Shared or objective-oriented world model (OWM)

An OWM seeks a more widely reusable, cross-perspective representation, using calibrated observations, common reference frames, simulation, and validation. *Objective-oriented* does not mean omniscient or error-free. Such a model can also be constructed directly from centralized measurements or physical models rather than only from local subjects.

### 5.3 Two-way structural exchange

```text
SWM_A ----\
SWM_B ----- > Evidence Alignment / Perspective Transform / Validation --> OWM
SWM_C ----/                                                   |
      ^                                                       |
      +------------- Localization / Task-Specific Projection --+
```

Potential SI contributions include contracts for state semantics, provenance, uncertainty, time horizons, perspective transforms, and counter-evidence. These are candidates for research, not yet standardized APIs.

## 6. Intelligence Loops and Evolutionary Navigation

The phrase **evolutionary navigation** denotes the subject's repeated selection of observations, actions, and structural adaptations under limited information and resources. The idea is compatible with biological examples in which effective sensorimotor behavior does not require a complete explicit model of the environment. It does **not** establish that primitive organisms held symbolic world models or subjective experience.

A useful loop must trade off:

- short-horizon task reward against longer-term capability growth;
- local subject relevance against shared environmental consistency;
- model accuracy against computation and latency;
- exploitation of known structures against exploration of alternatives;
- structural flexibility against safety, auditability, and identity continuity.

UCPSF scoring operators and control planes may help make these tradeoffs explicit. Whether they outperform existing architectures is an empirical question.

## 7. Recursive SPO and Multi-Subject Composition

An object may itself be an intelligent subject. Two interacting systems can therefore be represented schematically as:

\[
SPO_A\leftrightarrow SPO_B
\]

A collective system may coordinate multiple SPO units through shared contracts, delegated tasks, and contested or negotiated scoring criteria. This does not imply that all agents share the same goals or that a collective automatically possesses a unified subject identity.

A special case arises when a system treats some of its own model, policy, or runtime structure as an object of evaluation and modification. This opens a route to **governed structural recursive self-improvement**:

```text
Self-Observation -> Candidate Structural Change
    -> Independent Evaluation / Adversarial Sandbox
    -> Policy Authorization -> Limited Deployment
    -> Counter-Evidence / Rollback / Provenance
```

Self-reference and self-modification are functional capabilities. They are not evidence of phenomenal consciousness.

## 8. Minimal Relay Pieces for an Open Research Incubator

SPO-SI should be publishable and reusable before its full architecture is mature. Initial *research-level* Relay Pieces may include:

| Piece | Core content | Boundary question |
|---|---|---|
| Subject Profile | Identity, goals, sensors/tools, permissions, capabilities | Who may act or delegate? |
| World Model Piece | State schema, horizon, uncertainty, provenance | What is modeled and omitted? |
| Perspective Transform | Source/target frame, mapping, loss assumptions | Which distinctions survive transfer? |
| Action Contract | Preconditions, action, effects, constraints | What may be executed safely? |
| Scoring Evidence | Metrics, evaluator, context, competing values | Whose valuation is represented? |
| Counter-Evidence Record | Failure, contradiction, source, reproducibility | What should be revised? |

Each Piece should eventually declare version, ownership, scope, inputs/outputs, confidence or uncertainty, and validation status. At v0.1.0 these are **proposed interfaces**, not conformance-certified specifications.

## 9. Research Hypotheses and Falsification Paths

**H1 — Subject-first modeling:** Under matched computation and task conditions, a subject-relevant world model can outperform a broader model on action quality or latency. **Test:** compare matched-budget agents in partially observable tasks. **Possible disconfirmation:** global models dominate across budgets and shifts.

**H2 — Structural reuse:** Shared contracts and Relay Pieces reduce integration effort without unacceptable semantic loss. **Test:** cross-domain transfer with and without common interfaces. **Possible disconfirmation:** interface overhead exceeds measured reuse gains.

**H3 — Dual-world-model calibration:** Two-way exchange between local and shared models improves robustness or calibration. **Test:** multi-agent simulation with partial and conflicting observations. **Possible disconfirmation:** fusion increases error, latency, or correlated failures.

**H4 — Governed structural growth:** Evidence-gated structural updates improve long-horizon performance without excessive instability. **Test:** compare fixed architecture, unconstrained updates, and governed updates. **Possible disconfirmation:** governance costs outweigh improvements or fail to contain harmful regressions.

**H5 — Open relay:** Public, versioned structural hypotheses and counter-evidence produce reusable contributions from independent researchers. **Test:** track independent replications, accepted corrections, interoperable artifacts, and downstream citations. **Possible disconfirmation:** dissemination produces attention without meaningful reuse or verification.

## 10. Relationship to Existing Research

SPO-SI should be read alongside established work, not as a replacement for it:

- **Agent–environment interaction and POMDPs:** formalize action, observation, hidden state, belief, and policy.
- **Model-based reinforcement learning and model-predictive control:** study action-conditioned prediction and planning.
- **Embodied cognition and active inference:** emphasize organism/agent–environment coupling, perception, and action.
- **Multi-agent systems and distributed robotics:** study heterogeneous perspectives, coordination, and shared state.
- **World-model and spatial-intelligence research:** develop learned or structured predictive representations.
- **Software-agent architectures:** separate tools, memory, planning, authorization, and execution.

The **candidate** SPO-SI contribution is a particular synthesis: subject boundary and evaluation sovereignty + governed structural scoring and action + interoperable world-model pieces + counter-evidence-driven structural evolution. Novelty, practicality, and performance remain to be established through careful comparison and implementation.

## 11. Open Questions

1. What is the smallest meaningful SPO unit: a physical actor, software agent, team, or decision process?
2. Which parts of the Subject must persist for identity continuity after structural updates?
3. How should Predicate Intelligence distinguish model, evaluator, planner, controller, and runtime?
4. How should world-model uncertainty, unknown variables, and the **OTHERS** residual be represented?
5. When is a subject-centric model more efficient than a shared model, and when is it dangerously myopic?
6. What makes a perspective transformation semantically safe and reversible?
7. Can Relay Pieces transfer structural insight across incompatible model families?
8. Which evidence authorizes a policy, model, or self-modification update?
9. How should conflicting subjects' scoring sovereignty be preserved in collective systems?
10. What can be measured about functional agency without conflating it with consciousness?

## 12. A Pragmatic Research Roadmap

**Phase 0 — Concept and boundaries:** publish definitions, related work, assumptions, and counterexamples.

**Phase 1 — Relay prototypes:** draft Subject Profile, World Model Piece, Perspective Transform, and Counter-Evidence schemas; validate by hand against diverse examples.

**Phase 2 — Minimal loops:** implement one partially observable simulation and one software-agent task with explicit observation, belief, action, feedback, and governance.

**Phase 3 — Comparative evaluation:** benchmark subject-centric, shared, and dual-world-model variants at matched budgets and under distribution shift.

**Phase 4 — Structural evolution:** introduce evidence-gated model/policy/structural changes, rollback, and audit trails.

**Phase 5 — Collective relay:** invite external corrections, alternative interfaces, replications, and domain-specific implementations; track both positive and negative results.

## 13. Open Research and Collective Learning

SPO-SI is an **open research incubator**. It intentionally leaves large parts of world-model science, robotics, cognition, and consciousness research to the specialized communities advancing them. Its goal is to contribute interfaces, hypotheses, comparisons, and structural connections that others can independently test and improve.

> **The value of an early structural insight is not measured only by how far its originators can develop it, but also by how far others can carry it.**

Public release is an invitation to scrutiny, not proof of correctness. Every proposal should distinguish established background, new synthesis, conjecture, and experimentally supported results. Counter-evidence and alternative designs are first-class contributions.

## 14. Conclusion

The move from structural components to intelligence loops reframes SI around a situated subject, its executable intelligence mechanisms, and a responsive world. SPO-SI is a tentative architecture for connecting previously developed SI components to subject-centric and shared world models, authorized action, feedback, and recursive structural evolution.

The near-term objective is modest but consequential: **make the hypothesis precise enough to criticize, the interfaces explicit enough to reuse, and the experiments clear enough to falsify.**

> We do not need to solve every intelligence problem. We need to build structures through which intelligence problems, solutions, evidence, and researchers can find and improve one another.

---

## Project Lineage and Suggested Reading

This note draws on the authors' prior open research programs:

- [Universal Control Planes and Scoring Folding](https://github.com/sizhet/Universal-Control-Planes-and-Scoring-Folding)
- [Subjective Structural Intelligence](https://github.com/sizhet/Subjective-Structural-Intelligence)
- [Beyond Matching: OTHERS and Directional Weak-Evidence Intelligence](https://github.com/sizhet/Beyond-Matching-OTHERS-and-Directional-Weak-Evidence-Intelligence)
- [Beyond the LLM Boundary: Structural Hybrid Intelligence](https://github.com/sizhet/Beyond-the-LLM-Boundary-Structural-Hybrid-Intelligence)
- [Structural Intelligence Framework](https://github.com/sizhet/Structural-Intelligence-Framework)

**Foundational research areas for subsequent bibliography expansion:** partially observable Markov decision processes; model-based reinforcement learning; model-predictive control; embodied cognition; active inference; multi-agent world modeling. Specific papers and citations should be verified and added in `research/RELATED-WORK.md` rather than inferred from broad labels.

---

**Citation status:** Working paper / directional hypothesis, v0.1.0. A persistent DOI may be added after release; none is claimed here.

**License:** See repository `LICENSE` (not assumed in this document).
