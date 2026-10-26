# Figure Index — Subject–Predicate–Object Structural Intelligence (SPO-SI)

**Version:** v0.1.0  
**Authors:** Sizhe Tan & GPT-Obot  
**Status:** Open Research Incubator — Directional Hypotheses and Architecture Notes  
**Repository:** [Subject-Predicate-Object-Structural-Intelligence](https://github.com/sizhet/Subject-Predicate-Object-Structural-Intelligence)

## 1. Figure Catalog

| Figure | Title | Canonical file | Main topic |
|---|---|---|---|
| Fig-001 | SPO-SI Grand Architecture | [`figures/Fig-001-SPO-SI-Grand-Architecture.png`](figures/Fig-001-SPO-SI-Grand-Architecture.png) | System-wide architecture and intelligence loops |
| Fig-002 | From Structural Components to Intelligence Loops | [`figures/Fig-002-From-Structural-Components-to-Intelligence-Loops.png`](figures/Fig-002-From-Structural-Components-to-Intelligence-Loops.png) | Transition from modular SI to dynamic subject–world interaction |
| Fig-003 | Canonical SPO Intelligence Unit | [`figures/Fig-003-Canonical-SPO-Intelligence-Unit.png`](figures/Fig-003-Canonical-SPO-Intelligence-Unit.png) | Subject, Predicate, Object, state, history and governance |
| Fig-004 | Subject-Centric and Shared World Models | [`figures/Fig-004-Subject-Centric-and-Shared-World-Models.png`](figures/Fig-004-Subject-Centric-and-Shared-World-Models.png) | Local models, shared models, localization and validation |
| Fig-005 | Structural Relay and Interoperability | [`figures/Fig-005-Structural-Relay-and-Interoperability.png`](figures/Fig-005-Structural-Relay-and-Interoperability.png) | Portable pieces, contracts and relay lifecycle |
| Fig-006 | Perspective Transformation and Evidence Relay | [`figures/Fig-006-Perspective-Transformation-and-Evidence-Relay.png`](figures/Fig-006-Perspective-Transformation-and-Evidence-Relay.png) | Perspective translation, provenance, uncertainty and counter-evidence |
| Fig-007 | Recursive SPO and Governed Structural Evolution | [`figures/Fig-007-Recursive-SPO-and-Governed-Structural-Evolution.png`](figures/Fig-007-Recursive-SPO-and-Governed-Structural-Evolution.png) | Self-modeling, sandbox testing and governed structural RSI |
| Fig-008 | Open Intelligence Relay and Collective Learning | [`figures/Fig-008-Open-Intelligence-Relay-and-Collective-Learning.png`](figures/Fig-008-Open-Intelligence-Relay-and-Collective-Learning.png) | Open hypotheses, external critique and collective growth |

## 2. Figure Descriptions and Suggested Captions

### Fig-001 — SPO-SI Grand Architecture

**Caption:** A directional architecture for subject-centered structural intelligence: a subject interacts with an environment through governed perception, modeling, scoring, planning, and action, while feedback supports evidence-driven structural evolution and external intelligence relay.

**Key elements:** Subject; Predicate intelligence; Object/environment; subject-centric world model; shared model; control plane; feedback; relay; structural evolution.

### Fig-002 — From Structural Components to Intelligence Loops

**Caption:** The proposed transition from reusable structural intelligence components to an integrated, time-dependent intelligence loop with observation, action, feedback, learning, and possible structural growth.

**Key elements:** Structural components; composition; subject; environment; observation; action; feedback; adaptation.

### Fig-003 — Canonical SPO Intelligence Unit

**Caption:** A canonical Subject–Predicate–Object unit, extended with world-model state, history, contracts, and governance to distinguish a dynamic executable architecture from a static semantic triple.

**Key elements:** Subject boundary and capabilities; Predicate mechanisms; Object/environment; world model; historical state; policy constraints.

### Fig-004 — Subject-Centric and Shared World Models

**Caption:** Multiple subject-centric world models exchange selected representations with a shared world model through localization, fusion, validation, and reverse projection, without assuming an infallible objective viewpoint.

**Key elements:** Local models; shared model; bidirectional localization; fusion; model disagreement; uncertainty.

### Fig-005 — Structural Relay and Interoperability

**Caption:** Contract-first exchange of structural intelligence pieces across heterogeneous subjects and models, with discovery, localization, validation, authorization, execution, feedback, and revision.

**Key elements:** Subject Profile; World Model Piece; Perspective Transformation; Action Contract; Scoring Evidence; Counter-Evidence Record.

### Fig-006 — Perspective Transformation and Evidence Relay

**Caption:** Perspective transformation between distinct subject and model contexts, retaining source provenance, semantic constraints, uncertainty, OTHERS, and evidence/counter-evidence rather than silently equating incompatible representations.

**Key elements:** Source and target perspective; transform contract; uncertainty; provenance; contradiction; counter-evidence.

### Fig-007 — Recursive SPO and Governed Structural Evolution

**Caption:** An SPO system may model selected aspects of itself and propose structural modifications, but deployment requires explicit evaluation, sandbox testing, counter-evidence review, authorization, and rollback safeguards.

**Key elements:** Self-model; candidate change; scoring; adversarial sandbox; approval; controlled deployment; monitoring.

### Fig-008 — Open Intelligence Relay and Collective Learning

**Caption:** Open research artifacts connect hypotheses, models, experiments, evidence, counter-evidence, and independent researchers through a traceable relay process that can support collective structural learning.

**Key elements:** Public repository; research contributors; hypotheses; validation; criticism; revisions; reusable research pieces.

## 3. Article-to-Figure Placement Matrix

| Document | Primary figures | Optional supporting figures |
|---|---|---|
| `README.md` | Fig-001, Fig-008 | — |
| `docs/SPO-001-From-Structural-Components-to-Intelligence-Loops.md` | Fig-002 | Fig-001 |
| `docs/SPO-002-Subject-Predicate-Object-Architecture.md` | Fig-003 | Fig-001 |
| `docs/SPO-003-Subject-Centric-and-Shared-World-Models.md` | Fig-004 | Fig-006 |
| `docs/SPO-004-Structural-Relay-and-Interoperability.md` | Fig-005 | Fig-006 |
| `docs/SPO-005-Recursive-SPO-and-Structural-Evolution.md` | Fig-007 | Fig-003 |
| `docs/SPO-006-Research-Boundaries-and-Open-Hypotheses.md` | Fig-008 | Fig-001 |
| `relay/RELAY-001-Subject-Profile.md` | Fig-003 | Fig-005 |
| `relay/RELAY-002-World-Model-Piece.md` | Fig-004 | Fig-005 |
| `relay/RELAY-003-Perspective-Transformation.md` | Fig-006 | Fig-004 |
| `relay/RELAY-004-Evidence-and-Counter-Evidence.md` | Fig-006 | Fig-007 |
| `research/VALIDATION-ROADMAP.md` | Fig-008 | Fig-007 |

Other research files can link to relevant figures without embedding duplicates.

## 4. Markdown Embedding Convention

Use relative links from the file's own directory. Example in a root-level document:

```markdown
![Fig-001 — SPO-SI Grand Architecture](figures/Fig-001-SPO-SI-Grand-Architecture.png)

*Figure 1. SPO-SI Grand Architecture: directional subject–world intelligence-loop architecture.*
```

Example in `docs/` or `relay/`:

```markdown
![Fig-004 — Subject-Centric and Shared World Models](figures/Fig-004-Subject-Centric-and-Shared-World-Models.png)

*Figure 4. Subject-centric and shared world models connected by bidirectional localization and validation.*
```

Do not insert an image link before its target PNG is committed; otherwise GitHub will display a broken image.

## 5. Visual and Scientific Conventions

- **Format:** Prefer 16:9 PNG, legible at typical GitHub display widths; preserve editable source diagrams separately if available.
- **Color semantics:** Blue = Subject; teal = Predicate/control; orange = Object/environment; purple = Relay; neutral gray = governance/evidence. Do not rely on color alone to convey meaning.
- **Notation:** Solid arrows denote proposed operational flows; dashed arrows denote conditional, exploratory, or hypothesized relations. Define arrow semantics in each figure when needed.
- **Evidence status:** Figures illustrate *proposed architectures*, not empirically validated systems. Distinguish established methods from SPO-SI conjectures.
- **Consistency:** Use exactly the eight canonical filenames above; keep the internal figure numbers synchronized with captions and article references.
- **Accessibility:** Provide descriptive alt text and explanatory captions. Avoid tiny text and overcrowded diagrams.

## 6. Pre-Release Figure Checklist

- [ ] Eight **separate** PNGs exist in `figures/` under the exact canonical filenames.
- [ ] Each figure's number, title, labels, and arrows have been visually checked.
- [ ] All captions and cross-references match the actual artwork.
- [ ] Relative paths work from root-level, `docs/`, `relay/`, and `research/` files.
- [ ] The images are readable on GitHub desktop and mobile views.
- [ ] The figures are explicitly presented as architecture proposals or research hypotheses where appropriate.
- [ ] README and the paper references have no broken image links.
- [ ] The released figure assets and documentation belong to the same tagged version.

## 7. Open Research and Attribution

SPO-SI is an open, exploratory research program. Its figures are intended to facilitate criticism, structural relay, interoperability discussions, and independent testing—not to claim ownership of the broader world-model or embodied-intelligence research fields.

> **SPO-SI is not an attempt to own the world of intelligence, but an attempt to connect intelligent subjects, their models, their actions, and their structural evolution.**

**Authors:** Sizhe Tan & GPT-Obot  
**Version:** v0.1.0  
**Document:** `FIGURE-INDEX.md`

