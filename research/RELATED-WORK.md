# Related Work: Subject–Predicate–Object Structural Intelligence (SPO-SI)

**Repository:** Subject–Predicate–Object Structural Intelligence (SPO-SI)  
**Document:** `research/RELATED-WORK.md`  
**Version:** v0.1.0 — Open Research Incubator  
**Authors:** Sizhe Tan & GPT-Obot  
**Status:** Research positioning and interoperability notes; not a systematic literature review  
**Date:** 2026-10-19

## Abstract

Subject–Predicate–Object Structural Intelligence (SPO-SI) is a proposed architectural research program connecting an identifiable acting subject, the mechanisms through which it perceives, evaluates, models, plans and acts, and the objects or environments with which it interacts. Its proposed contribution is **not** the discovery of the agent–environment loop, a new theory of consciousness, or a replacement for established world-model algorithms. Rather, SPO-SI asks whether subject profiles, world-model pieces, perspective transformations, action contracts, scoring evidence and counter-evidence can be represented as interoperable, governable and evolvable structural units. This document locates those hypotheses in existing research and identifies interfaces for collaboration and falsification.

> **Research principle:** SPO-SI is not an attempt to own the world of intelligence, but an attempt to connect intelligent subjects, their models, their actions, and their structural evolution.

## 1. Scope and claims

This is a selective, concept-oriented related-work map. The cited publications are representative starting points, not evidence that SPO-SI has been experimentally validated. Research precedents and proposed SPO-SI additions are separated explicitly.

**Established antecedents:** agent–environment feedback, partially observable decision-making, learned dynamics models, embodied and active perception, multi-agent belief reasoning, modular architectures, causal abstraction, and safety-oriented evaluation.

**Proposed SPO-SI additions:** a unified *relay contract* spanning subject identity and authority, situated world-model fragments, perspective transformations, provenance, uncertainty, governance and structural revision; and a research program evaluating whether that contract yields measurable benefits.

## 2. Markov decision processes and partial observability

**Foundations.** Markov decision processes formalize sequential action and reward; partially observable MDPs (POMDPs) model an agent that must act using observations and a belief over hidden states. These are direct precedents for the SPO dynamic loop, rather than competitors invented after it.

**Connection.** The SPO subject can be associated with an agent's capabilities, observation channels and objectives; the predicate includes belief update, policy, evaluation and control; the object includes environmental state and other agents. The subject-centric world model is naturally interpreted as a task-conditioned belief or predictive state.

**Potential increment.** SPO-SI proposes exchanging *typed, provenance-bearing pieces* of beliefs, model assumptions and action constraints across independently implemented systems, without requiring a single universal state space.

**Key boundary.** A symbolic SPO triple is not a substitute for the transition, observation and reward models needed to make a POMDP operational.

**Starting points:** Bellman (1957); Kaelbling, Littman & Cassandra (1998); Sutton & Barto (2018).

## 3. Model-based reinforcement learning and learned world models

**Foundations.** Model-based reinforcement learning learns or uses environment dynamics to support planning. Ha & Schmidhuber's *World Models* (2018), Hafner et al.'s Dreamer family, and MuZero (Schrittwieser et al., 2020) demonstrate different forms of prediction, latent-state modeling and planning. These methods are substantial algorithmic antecedents.

**Connection.** A subject-centric model estimates consequences relevant to an agent's actions. A shared model may be built from additional sensors, data sources or other agents, then localized for an individual actor.

**Potential increment.** The `World Model Piece` and `Perspective Transformation` contracts aim to make assumptions, coordinate frames, temporal validity, uncertainty and transfer losses inspectable when a model is reused elsewhere.

**Open comparisons.** Against equal-compute model-based baselines, does subject-conditioned model selection improve task success, calibration, transfer or energy use? Do relay contracts improve interoperability enough to justify their overhead?

**Key boundary.** SPO-SI does not propose that an agent-centered representation always outperforms a global simulator; shared and externally constructed models can be preferable for coordination and planning.

**Starting points:** Sutton (1991); Ha & Schmidhuber (2018); Hafner et al. (2020, 2023); Schrittwieser et al. (2020).

## 4. Embodied cognition, ecological psychology and active perception

**Foundations.** Ecological psychology emphasizes affordances relative to an organism's capacities; embodied and situated cognition examines how body, environment and action shape intelligent behavior. Active perception studies sensing strategies chosen in service of action.

**Connection.** SPO-SI's subject is not merely an arbitrary label on a scoring function: sensors, embodiment, history, constraints and feasible actions affect what information matters. This is consonant with, but does not originate, subject-relative perception.

**Potential increment.** An explicit `Subject Profile` could encode affordance-relevant capabilities and authority so a model or plan can be localized to a different robot or agent.

**Key boundary.** Functional sensorimotor coupling does not establish phenomenal consciousness. Biological evolution motivates a hypothesis about efficient local models, not a proof that all intelligence must start with the same architecture.

**Starting points:** Gibson (1979); Brooks (1991); Bajcsy (1988); Clark (1997).

## 5. Active inference and predictive processing

**Foundations.** Active inference and predictive-processing accounts connect internal generative models, uncertainty, perception and action, often through variational or expected free-energy formulations.

**Connection.** Both active inference and SPO-SI treat the agent as acting under uncertainty while maintaining an internal representation of its environment.

**Difference.** SPO-SI does not assume that all subject valuation, control and learning can or should be reduced to a single free-energy objective. Its predicate is deliberately heterogeneous: learned policies, symbolic constraints, planners, human oversight and scoring forests may coexist.

**Relay opportunity.** An active-inference agent could publish predictive beliefs and uncertainty as a World Model Piece, subject to an explicit semantics contract.

**Starting points:** Friston (2010); Parr, Pezzulo & Friston (2022).

## 6. Multi-agent systems, theory of mind and shared models

**Foundations.** Decentralized POMDPs, interactive POMDPs and multi-agent reinforcement learning examine joint decisions, partial information and beliefs about other agents. Distributed robotics studies shared maps and coordination under communication limits.

**Connection.** One subject's object can itself be another acting subject. SPO units can therefore interact, nest or compose without collapsing their identities or objectives.

**Potential increment.** A two-layer model arrangement distinguishes subject-local beliefs from shared, cross-validated representations. The `Perspective Transformation` relay would record semantic and coordinate conversions and where they fail.

**Important caveat.** A shared model is not an omniscient or necessarily unbiased view. Agreement among agents can reflect correlated errors, common training data or systematic blind spots.

**Starting points:** Bernstein et al. (2002); Gmytrasiewicz & Doshi (2005); Oliehoek & Amato (2016); Lowe et al. (2017).

## 7. Robotics, spatial intelligence and mapping

**Foundations.** SLAM, robot localization, occupancy mapping, 3D reconstruction and spatial reasoning provide concrete techniques for estimating environment state and transforming between reference frames.

**Connection.** These fields supply mature examples of the subject-local/shared-model distinction. A robot's local map and a global map are related by estimated transforms, uncertainty and data association.

**Potential increment.** SPO-SI asks whether similar typed transformations can extend beyond geometry to temporal assumptions, semantics, capability constraints and governance permissions.

**Key boundary.** Geometric frame transformations are mathematically well-defined under stated assumptions; semantic or normative perspective transformations generally are not. The latter require explicit limits, validation and refusal of unsupported conversions.

**Starting points:** Thrun, Burgard & Fox (2005); Cadena et al. (2016).

## 8. Causal models, abstraction and compositional generalization

**Foundations.** Structural causal models and intervention-based reasoning distinguish correlation from consequences of actions. Abstraction and compositionality research addresses how reusable representations support transfer.

**Connection.** The SPO predicate can use causal or predictive models to estimate action outcomes; a World Model Piece should disclose whether its relationships are descriptive, predictive, causal or normative.

**Potential increment.** Relay contracts can prohibit unjustified upgrades from observed correlation to causal authority and preserve counter-evidence against transferred assumptions.

**Starting points:** Pearl (2009); Lake et al. (2017); Goyal & Bengio (2022).

## 9. Modular AI, agents, tools and interoperable systems

**Foundations.** Classical blackboard architectures, subsumption, hierarchical reinforcement learning and contemporary tool-using language-model agents all separate or coordinate specialized capabilities. Typed APIs and interface-description languages provide engineering precedents for compositionality.

**Connection.** SPO-SI's predicate is an orchestrated collection of capabilities, not necessarily one model. Its relay pieces resemble structured, typed messages exchanged across modular systems.

**Potential increment.** The proposed contract makes *subject-relative meaning*, model validity, evidence and action authority first-class elements rather than relying only on syntactic compatibility.

**Key boundary.** A YAML document or schema alone cannot guarantee semantic compatibility, safe delegation or trustworthy model outputs; conformance tests and runtime enforcement are required.

**Starting points:** Brooks (1986); Sutton, Precup & Singh (1999); Yao et al. (2023); Schick et al. (2023).

## 10. Self-models, metacognition and recursive improvement

**Foundations.** Metacognition concerns monitoring and regulating cognition. Machine-learning research on self-evaluation, automated architecture search and learning-to-learn offers partial precedents for self-directed change.

**Connection.** A subject may model its own capabilities, errors and constraints, and propose revisions to the predicate or world model. When the system itself becomes an object of analysis, recursive SPO composition is a useful descriptive pattern.

**Critical distinctions:**

1. Self-description is not necessarily an accurate self-model.
2. Self-modeling is not self-modification.
3. Self-modification is not validated self-improvement.
4. Functional self-monitoring does not demonstrate subjective experience.

**Potential increment.** A governed change lifecycle links proposals to sandbox tests, counter-evidence, authorized promotion, rollback and post-deployment monitoring.

**Starting points:** Flavell (1979); Schmidhuber (1987); Finn, Abbeel & Levine (2017); Elsken, Metzen & Hutter (2019).

## 11. AI safety, Goodhart effects and evidence governance

**Foundations.** Reward misspecification, specification gaming, distribution shift and Goodhart-like effects are recognized problems in optimization and deployment. Safety cases and audit trails provide engineering precedents for traceable decisions.

**Connection.** SPO-SI distinguishes an actor's objectives from permissions and from the evidence used to justify a choice. It treats counter-evidence and unknown factors as relayable information rather than disposable noise.

**Potential increment.** `Evidence and Counter-Evidence` records may support cross-agent model correction, evaluator governance and auditable structural evolution.

**Key boundary.** Recording provenance or counter-evidence is not itself a safety guarantee. Evaluation needs adversarial tests, independently specified constraints and clear failure-handling rules.

**Starting points:** Amodei et al. (2016); Krakovna et al. (2020); Manheim & Garrabrant (2019).

## 12. Consciousness and functional agency: a necessary separation

The terms *subject*, *self-model*, *awareness* and *agency* have different meanings across philosophy, cognitive science and engineering. SPO-SI uses **subject** operationally: a bounded locus of observation, valuation, authority and action. This does not entail first-person experience.

SPO-SI may help study functional agency, self-monitoring and their developmental relationships. It does **not** establish a theory of the origin of consciousness, that consciousness is a simple continuum, or that present AI systems possess or lack phenomenal experience. Those questions require separate evidence and conceptual work.

**Starting points:** Nagel (1974); Dehaene, Lau & Kouider (2017); Butlin et al. (2023).

## 13. Comparison matrix: prior art versus proposed SPO-SI contribution

| Research area | Established contribution | Proposed SPO-SI research increment | Evidence still needed |
|---|---|---|---|
| POMDP / sequential decisions | Belief-state action loops | Subject-bound relayable contracts | Advantage over POMDP implementations |
| Model-based RL | Learned dynamics and planning | Portable model fragments with explicit scope | Transfer and calibration gains |
| Embodied / active perception | Action-conditioned sensing | Reusable subject capability profiles | Reduced adaptation cost |
| Active inference | Generative-model-based perception/action | Heterogeneous predicate interoperability | Compatibility without objective distortion |
| Multi-agent systems | Coordination under partial information | Local/shared model translation with provenance | Robustness under disagreement |
| Robotics / SLAM | Frame transformations and mapping | Generalized perspective relay beyond geometry | Valid semantics and uncertainty propagation |
| Causal inference | Intervention and structural explanations | Causal-status metadata in model relay | Fewer invalid causal transfers |
| Modular AI / tool use | Specialized components and orchestration | Governed subject/model/action interfaces | Integration benefit net of overhead |
| Metacognition / AutoML | Monitoring and automated improvement | Auditable recursive SPO lifecycle | Reliable improvement versus baseline |
| AI safety | Risk analysis and failure evaluation | Cross-agent counter-evidence relay | Measured reduction in failures |

## 14. Nine hypothesis-to-literature bridges

These identifiers align with `research/TESTABLE-HYPOTHESES.md`. Detailed operational definitions and experimental thresholds belong there.

- **H01 — Subject-centric efficiency:** compare local task-conditioned models with global or fixed-scope models under matched budgets; grounded in POMDPs, active perception and model-based RL.
- **H02 — Dual-world-model robustness:** compare local-only, shared-only and bidirectional fusion; grounded in distributed mapping and multi-agent learning.
- **H03 — Contract-first relay:** compare structured transfer against ad hoc integration; grounded in modular AI and typed interface engineering.
- **H04 — Perspective transformation:** evaluate geometric, temporal and semantic transformations separately; grounded in robotics and representation alignment.
- **H05 — Evidence relay:** compare error correction with and without provenance and counter-evidence; grounded in calibration and safety evaluation.
- **H06 — Governed recursive improvement:** compare gated versus ungated update lifecycles; grounded in AutoML and AI safety.
- **H07 — Recursive multi-agent composition:** evaluate cooperation, negotiation and identity preservation; grounded in Dec-POMDPs and MARL.
- **H08 — OTHERS / residual uncertainty:** test whether preserving unknown factors improves out-of-distribution calibration; grounded in robust and uncertainty-aware learning.
- **H09 — Open research relay:** measure external reuse, reproduction, corrections and independently developed extensions; grounded in open-science practice, not yet established as a performance claim.

## 15. Proposed external relay interfaces

SPO-SI should be an *adapter-friendly research layer* rather than a mandatory replacement for existing systems.

| Relay piece | External research communities | Minimum information to exchange |
|---|---|---|
| `Subject Profile` | Robotics, HCI, agent systems | Capabilities, sensors, objectives, permissions, version |
| `World Model Piece` | Model-based RL, spatial AI, simulation | State semantics, scope, time, provenance, uncertainty |
| `Perspective Transformation` | SLAM, multi-agent reasoning, ontology alignment | Source/target frames, mapping, loss, validity conditions |
| `Action Contract` | Planning, control, agent tooling | Preconditions, effects, authority, limits, rollback |
| `Scoring Evidence` | Evaluation, decision theory | Claim, metric, evaluator, distribution, confidence |
| `Counter-Evidence Record` | Safety, science, debugging | Challenged claim, observation, source, conflict, resolution status |

An adapter must be permitted to say **incompatible**, **unknown** or **insufficient evidence**. Silent coercion between incompatible models is not successful interoperability.

## 16. Distinctiveness tests and falsification

SPO-SI's proposed contribution would be weakened if any of the following is demonstrated:

1. Its canonical pieces cannot be defined precisely enough for independent implementations.
2. Existing standards already provide equivalent semantics and governance at lower cost.
3. Subject-centric modeling has no measurable advantage in the proposed task regimes.
4. Perspective translation destroys uncertainty or introduces untraceable errors.
5. Relay contracts add overhead without improving integration, robustness or transfer.
6. Recursive SPO change management does not outperform established safe update workflows.
7. Open publication produces no demonstrable reuse, correction or independent research contribution.

The research program should report negative findings and retire unsuccessful hypotheses rather than reinterpret every outcome as support.

## 17. Research collaboration and open-science protocol

External contributions are most useful when they identify a concrete claim, a relevant prior work, a competing explanation, an interface mismatch or a reproducible test. A contribution record should include:

```yaml
relay_contribution:
  id: "external-example-001"
  type: "prior-art | hypothesis | counter-evidence | experiment | adapter"
  related_hypothesis: "H03"
  claim: "A competing interface already supports equivalent transfer semantics."
  reference: "stable citation or artifact link"
  evidence_status: "proposed | reproduced | disputed | verified"
  assumptions: []
  limitations: []
  suggested_revision: "Compare semantics and implementation overhead."
```

The record is illustrative, not a finalized machine-validated schema. Contributors should avoid confidential data, unsupported priority claims and unverifiable citations. Repository maintainers should distinguish acceptance of a contribution from endorsement of its scientific conclusion.

## 18. Selected references

The following are representative scholarly entry points. Bibliographic details and URLs should be checked against publisher or archival records before a formal literature-review release.

1. Bellman, R. (1957). *Dynamic Programming*. Princeton University Press.
2. Kaelbling, L. P., Littman, M. L., & Cassandra, A. R. (1998). Planning and acting in partially observable stochastic domains. *Artificial Intelligence*, 101(1–2), 99–134. https://doi.org/10.1016/S0004-3702(98)00023-X
3. Sutton, R. S., & Barto, A. G. (2018). *Reinforcement Learning: An Introduction* (2nd ed.). MIT Press. http://incompleteideas.net/book/the-book-2nd.html
4. Sutton, R. S. (1991). Dyna, an integrated architecture for learning, planning, and reacting. *SIGART Bulletin*, 2(4), 160–163. https://doi.org/10.1145/122344.122377
5. Ha, D., & Schmidhuber, J. (2018). World Models. *NeurIPS 2018*. https://arxiv.org/abs/1803.10122
6. Hafner, D., Lillicrap, T., Ba, J., & Norouzi, M. (2020). Dream to Control: Learning Behaviors by Latent Imagination. *ICLR*. https://arxiv.org/abs/1912.01603
7. Hafner, D., Pasukonis, J., Ba, J., & Lillicrap, T. (2023). Mastering Diverse Domains through World Models. https://arxiv.org/abs/2301.04104
8. Schrittwieser, J., et al. (2020). Mastering Atari, Go, chess and shogi by planning with a learned model. *Nature*, 588, 604–609. https://doi.org/10.1038/s41586-020-03051-4
9. Gibson, J. J. (1979). *The Ecological Approach to Visual Perception*. Houghton Mifflin.
10. Brooks, R. A. (1986). A robust layered control system for a mobile robot. *IEEE Journal of Robotics and Automation*, 2(1), 14–23. https://doi.org/10.1109/JRA.1986.1087032
11. Brooks, R. A. (1991). Intelligence without representation. *Artificial Intelligence*, 47(1–3), 139–159. https://doi.org/10.1016/0004-3702(91)90053-M
12. Bajcsy, R. (1988). Active perception. *Proceedings of the IEEE*, 76(8), 996–1005. https://doi.org/10.1109/5.5968
13. Clark, A. (1997). *Being There: Putting Brain, Body, and World Together Again*. MIT Press.
14. Friston, K. (2010). The free-energy principle: a unified brain theory? *Nature Reviews Neuroscience*, 11, 127–138. https://doi.org/10.1038/nrn2787
15. Parr, T., Pezzulo, G., & Friston, K. J. (2022). *Active Inference: The Free Energy Principle in Mind, Brain, and Behavior*. MIT Press.
16. Bernstein, D. S., Givan, R., Immerman, N., & Zilberstein, S. (2002). The complexity of decentralized control of Markov decision processes. *Mathematics of Operations Research*, 27(4), 819–840. https://doi.org/10.1287/moor.27.4.819.297
17. Gmytrasiewicz, P. J., & Doshi, P. (2005). A framework for sequential planning in multi-agent settings. *JAIR*, 24, 49–79. https://doi.org/10.1613/jair.1579
18. Oliehoek, F. A., & Amato, C. (2016). *A Concise Introduction to Decentralized POMDPs*. Springer.
19. Lowe, R., et al. (2017). Multi-Agent Actor-Critic for Mixed Cooperative-Competitive Environments. *NeurIPS*. https://arxiv.org/abs/1706.02275
20. Thrun, S., Burgard, W., & Fox, D. (2005). *Probabilistic Robotics*. MIT Press.
21. Cadena, C., et al. (2016). Past, Present, and Future of Simultaneous Localization and Mapping. *IEEE Transactions on Robotics*, 32(6), 1309–1332. https://doi.org/10.1109/TRO.2016.2624754
22. Pearl, J. (2009). *Causality: Models, Reasoning, and Inference* (2nd ed.). Cambridge University Press.
23. Lake, B. M., Ullman, T. D., Tenenbaum, J. B., & Gershman, S. J. (2017). Building machines that learn and think like people. *Behavioral and Brain Sciences*, 40, e253. https://doi.org/10.1017/S0140525X16001837
24. Goyal, A., & Bengio, Y. (2022). Inductive Biases for Deep Learning of Higher-Level Cognition. *Proceedings of the Royal Society A*, 478, 20210068. https://doi.org/10.1098/rspa.2021.0068
25. Sutton, R. S., Precup, D., & Singh, S. (1999). Between MDPs and semi-MDPs: A framework for temporal abstraction in reinforcement learning. *Artificial Intelligence*, 112(1–2), 181–211. https://doi.org/10.1016/S0004-3702(99)00052-1
26. Yao, S., et al. (2023). ReAct: Synergizing Reasoning and Acting in Language Models. *ICLR*. https://arxiv.org/abs/2210.03629
27. Schick, T., et al. (2023). Toolformer: Language Models Can Teach Themselves to Use Tools. *NeurIPS*. https://arxiv.org/abs/2302.04761
28. Flavell, J. H. (1979). Metacognition and cognitive monitoring: A new area of cognitive–developmental inquiry. *American Psychologist*, 34(10), 906–911. https://doi.org/10.1037/0003-066X.34.10.906
29. Schmidhuber, J. (1987). Evolutionary principles in self-referential learning. Diploma thesis, Technical University of Munich.
30. Finn, C., Abbeel, P., & Levine, S. (2017). Model-Agnostic Meta-Learning for Fast Adaptation of Deep Networks. *ICML*. https://arxiv.org/abs/1703.03400
31. Elsken, T., Metzen, J. H., & Hutter, F. (2019). Neural Architecture Search: A Survey. *JMLR*, 20(55), 1–21. https://jmlr.org/papers/v20/18-598.html
32. Amodei, D., et al. (2016). Concrete Problems in AI Safety. https://arxiv.org/abs/1606.06565
33. Krakovna, V., et al. (2020). Specification gaming: the flip side of AI ingenuity. *DeepMind blog*. https://deepmind.google/discover/blog/specification-gaming-the-flip-side-of-ai-ingenuity/
34. Manheim, D., & Garrabrant, S. (2019). Categorizing Variants of Goodhart's Law. https://arxiv.org/abs/1803.04585
35. Nagel, T. (1974). What Is It Like to Be a Bat? *The Philosophical Review*, 83(4), 435–450. https://doi.org/10.2307/2183914
36. Dehaene, S., Lau, H., & Kouider, S. (2017). What is consciousness, and could machines have it? *Science*, 358(6362), 486–492. https://doi.org/10.1126/science.aan8871
37. Butlin, P., et al. (2023). Consciousness in Artificial Intelligence: Insights from the Science of Consciousness. https://arxiv.org/abs/2308.08708

## 19. Cross-references within the SPO-SI repository

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
- `research/OPEN-QUESTIONS.md`
- `research/TESTABLE-HYPOTHESES.md`
- `research/VALIDATION-ROADMAP.md`

## 20. Closing position

SPO-SI should be judged not by claims of conceptual ownership but by whether it provides a useful, testable bridge across existing disciplines. The project invites researchers to contribute stronger precedents, incompatible cases, alternative contracts, negative results and independently verified implementations.

> **The value of an early structural insight is not measured only by how far its originators can develop it, but also by how far others can carry it.**

---

**Citation note:** This document is an exploratory research map, not a claim of priority over the cited literature. Cite original research for established methods and cite the SPO-SI repository only for its specific architectural hypotheses and relay proposals.
