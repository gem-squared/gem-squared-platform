# GEM² Platform Specification

> **"Prompt Engineering → Prompt Compilation → AI: from Magic to Engineering"**

**Version:** 1.5.5 | **License:** [CC BY-NC-SA 4.0](LICENSE) | **Updated:** January 2026

A formal framework for autonomous AI software development with **provable boundaries and epistemic honesty**.

---

## What is GEM²?

**GEM²** (Governance, Evidence, and Matrix Management) transforms AI-assisted development from heuristic craft to formal engineering. AI actors execute within **mathematically defined, verifiable boundaries** — not through hope, but through proof.

```
Traditional:  Prompt → AI → Hope
GEM²:         Prompt → TPMN_P → AI → TPMN_O → Trust
```

**TPMN is the compiler** — prompts are validated before execution, outputs verified after.

---

## Core Principles

| Principle | Meaning |
|-----------|---------|
| **Evidence over Time** | Progress = f(Evidence), not f(Time) |
| **Compilation over Craft** | Prompts are compiled, not crafted |
| **Dual-Gate Validation** | TPMN_P (before) + TPMN_O (after) |
| **Epistemic Honesty** | AI must admit when extrapolating (EEF) |
| **Realistic Completion** | Ω_accept = {V, B, S} — perfection not required |

---

## Quick Reference

### Essential 5 Concepts

| Concept | One-liner | Why it matters |
|---------|-----------|----------------|
| **TPMN_P** | Validates prompt BEFORE AI runs | Catches ambiguity early |
| **TPMN_O** | Verifies output AFTER AI runs | Ensures contract satisfaction |
| **EEF** | Flags when AI extrapolates | Epistemic honesty |
| **SPT** | Forbids S→T, L→G, Δe→∫de | Prevents illicit leaps |
| **Ω_accept** | {V, B, S} = completion | Realistic, not perfection |

### End-to-End Example

```
1. HUMAN:  "Create a function that sorts a list in < 10ms"
             ↓
2. TPMN_P: ✅ P1 (metric: 10ms), ✅ P4 (schema: function)
             ↓ extracts A_Priori_Grid
3. LLM:    Generates sort function
             ↓
4. TPMN_O: ✅ O1 (is function), ✅ O2 (no forbidden ops)
           ⚠️ O5: EEF flagged — "< 10ms" untested
             ↓
5. OUTPUT: Function + EEF warning: "Performance claim requires benchmark"
```

---

## The Conceptual Stack

```
GEM²            → Company + Platform + Mathematical Universe
GEM² platform   → GEM² + NTC-VPC + TPMN + GACC + GEM-KG
NTC-VPC         → Specification (conservation laws)
TPMN            → Legislator, DUAL-GATE (TPMN_P/O)
GACC + GEM-KG   → Orchestrator + Knowledge Graph
T_AI            → AI Actors executing within boundaries
```

---

## Philosophy

### The GEM² Discretization Principle

> **Origin**: The name "GEM²" is inspired by the Fundamental Theorem of Calculus (FTC).

**Two-Layer Noumena:**

```
R-Noumena (Reality)  = unknowable, uncontrollable — DISMISSED (outside GEM² scope)
G-Noumena (CONTRACT) = knowable, formal, immutable — the "reality" OF GEM² universe
```

**The Core Insight:**

```
Real World  = continuous, messy, ambiguous    (R-Noumena — DISMISSED)
GEM²        = discrete, clean, provable       (G-Noumena + A_Priori)
AI          = handles discrete things clearly (within INTERPOLATION_DOMAIN)
```

**The Equation:**

> **ANALOGY_ONLY**: The integral symbol below is a visual analogy, not Δe→∫de inference.

```
AI-interpolation: Σ GEM²[T][c] ↦ G-Noumena (CONTRACT satisfaction)
                  ─────────────────────────────────────────────────
                  (as Σf(xᵢ)Δx ≈ ∫f(x)dx)  [ANALOGY_ONLY]

NOT: Σ GEM²[T][c] ↦ Reality  ← L→G violation!
```

**Responsibility Boundaries:**

| Layer | GEM² Solves | NOT GEM² Responsibility |
|-------|-------------|-------------------------|
| P₀ → CONTRACT | Formalize requirements | Whether P₀ reflects reality |
| CONTRACT → Code | Satisfy CONTRACT | Whether CONTRACT is correct |
| Code → Evidence | Prove Ω_accept | Whether Ω_accept = real success |

**The Honest Claim:**

GEM² solves **G-Noumena** (CONTRACT satisfaction), not **R-Noumena** (Reality).
If requirements are wrong, that's a **P₀/Human problem**, not a GEM² problem.

---

## Formal Foundations

### Ontology: Types and Domain

| Type | Definition | Purpose |
|------|------------|---------|
| **Domain** | {⊥, -1, 0, 1} | Four-valued logic for all matrices |
| **Ev_STATE** | {V, B, S, F, P} | Existence states |
| **EEF_Record** | Extrapolation flag | Epistemic honesty marker |

### Structure: Tensor and Universes

**Design Structure Matrix (DSM):**

| Property | Value |
|----------|-------|
| Size range | 3×3 to 7×7 |
| Diagonal cells | Components (BUSINESS logic) |
| Off-diagonal cells | Interfaces (INTERFACE logic) |

**Three Universes (Matrices):**

| Universe | Matrix | Meaning |
|----------|--------|---------|
| **Blueprint** | U_b | What SHOULD exist — design intent |
| **Existence (GEM)** | U_e | What DOES exist — happy path |
| **Resistance (CHAOS)** | U_r | What SURVIVES failure — fallback path |

### Laws: Conservation Invariants

| Law | Name | Scope | Meaning |
|-----|------|-------|---------|
| **L_S** | Set Law | CELL | Once value leaves ⊥, it cannot return |
| **L_C** | Calculus Law | LIFECYCLE | Layer transitions require threshold θ crossing |
| **L_A** | Algebra Law | MATRIX | Weight ⊕ operations preserve matrix semantics |

```
L_S: (U[T][c] ≠ ⊥) ⇒ □(U[T][c] ≠ ⊥)    — Cell monotonicity
L_C: (L_C → θ → L_S)                    — Continuous → threshold → Discrete
L_A: Coherence(U) preserved under ⊕     — Matrix algebra closure
```

### SPT: Strictly Prohibited Transitions

| Symbol | Transition | Meaning |
|--------|------------|---------|
| **S→T** | State → Trait | Never treat mutable as immutable |
| **L→G** | Local → Global | Never extrapolate local to universal |
| **Δe→∫de** | Evidence < 3 | Never expand small evidence to large claims |

---

## Operations

### Existence Derivation (ξ)

```
ξ(T,c) ≜ derive(U_b[T][c], U_e[T][c], U_r[T][c]) → Ev_STATE

Ω_accept ≜ {V, B, S}  (* Acceptable completion states *)
Ω_Tensor(T) ≜ ∀c ∈ Cells(T): ξ(T,c) ∈ Ω_accept
Ω_GEM²(P)   ≜ ∀T ∈ ProjectTensors(P): Ω_Tensor(T)
```

| State | Symbol | Meaning | Acceptable? |
|-------|--------|---------|-------------|
| Verified | V | Passed both GEM and CHAOS tests | ✅ |
| Buggy | B | Known issue, explicitly flagged | ✅ |
| Skipped | S | Test skipped with approval | ✅ |
| Failed | F | Must be fixed | ❌ |
| Pending | P | Not yet evaluated | ❌ |

### T_AI: AI Actor System

| Actor | Phase | Input → Output |
|-------|-------|----------------|
| **G_AI** | Genesis | P₀ → G-Project document |
| **S_AI** | Structure | G-Project → Tensor_Init |
| **D_AI** | Design | Tensor_Init → Cell_TLA contracts |
| **I_AI** | Implement | Cell_TLA → Code |
| **E_AI** | Execute | Code → Evidence (U_e, U_r) |

**GACC** orchestrates all actors.

### Three Pipelines

| Pipeline | Actors | Purpose |
|----------|--------|---------|
| **DEVELOP** | G, S, D, I, E | Forward engineering: P₀ → Code → Evidence |
| **ANALYSIS** | G, S, D, E | Reverse engineering: Code → Spec extraction |
| **VERIFY** | D, I | Code ↔ Contract validation |

---

## TPMN: The Compiler for AI

> **TPMN applies RLAIF principles at inference-time (NOT training).**

**TPMN_Compiler_Features:**

```
TPMN_Compiler_Features ≜ {
  IR:            "A_Priori_Grid — intermediate representation from prompt",
  Verify:        "TPMN_O — output verification against grid",
  RepairLoop:    "Auto-retry on TPMN_O failure with error context",
  AuditTrace:    "Lineage of validation decisions",
  BoundedRetries: "Max retry count before escalation"
}

Guarantee: TPMN_O.PASS ⟹ Output satisfies A_Priori_Grid
```

| Component | Role | Kantian Analog |
|-----------|------|----------------|
| **TPMN_P** | Legislator — validates prompt BEFORE AI runs | Transcendental Aesthetic |
| **TPMN_O** | Judge — verifies output AFTER AI runs | Transcendental Analytic |
| **EEF** | Epistemic honesty — flags extrapolation | Critique of Pure Reason |
| **SPT** | Prohibited transitions (S→T, L→G, Δe→∫de) | Transcendental Dialectic |

```
Flow: Prompt → TPMN_P → A_Priori_Grid → LLM → TPMN_O → Valid_Output
```

### RLAIF at Inference-Time

```
RLAIF_Training    ≜ Traditional RLAIF — feedback updates model weights
RLAIF_Inference   ≜ TPMN approach — feedback validates/repairs outputs

Key distinction: TPMN performs NO WEIGHT UPDATES.
TPMN = runtime gating/verification/repair, NOT training.
```

| Traditional | TPMN |
|-------------|------|
| Training-time | Inference-time |
| Model weights change | Output validated/repaired |
| Feedback is historical | Feedback is immediate |
| Requires training runs | Works with any LLM |

---

## Future: GEM-KG Vision

```
Phase 1 (NOW):   Inference-time AI feedback (TPMN)
                 → Ephemeral: judgments exist only during execution

Phase 2 (KG):    GEM-KG stores feedback patterns
                 → Persistent: judgments stored as knowledge graph

Phase 3 (RLAIF): Stored patterns → training signal → model improvement
                 → Evolution: GEM² becomes self-improving system
```

**GEM² + GEM-KG = Full-stack AI governance**: inference → persistence → training.

---

## Core Takeaways

1. **GEM² is a universe, not a tool.**
2. **TPMN is a compiler, not a prompt template.**
3. **AI actors execute within provable boundaries.**
4. **Evidence replaces time; proof replaces hope.**
5. **Epistemic honesty is mandatory (EEF).**
6. **Completion is realistic, not perfection.**
7. **GEM-KG enables evolution from inference to training.**

---

## Glossary

### Core Symbols

| Symbol | Name | Definition |
|--------|------|------------|
| **⊥** | Bottom | Undefined / not yet set |
| **ξ** | Xi | Existence classifier: ξ(T,c) → Ev_STATE |
| **θ** | Theta | Threshold for layer transitions |
| **Ω** | Omega | Completion predicate |
| **Ω_accept** | Acceptance Set | {V, B, S} — states that = "done" |

### Matrices

| Symbol | Name | Meaning |
|--------|------|---------|
| **U_b** | Blueprint | What SHOULD exist |
| **U_e** | Existence (GEM) | What DOES exist |
| **U_r** | Resistance (CHAOS) | What SURVIVES |

### SPT Violations

| Symbol | Meaning | Example |
|--------|---------|---------|
| **S→T** | State → Trait | Runtime value treated as constant |
| **L→G** | Local → Global | "Works here" → "Works everywhere" |
| **Δe→∫de** | Small → Large | "2 tests passed" → "Always works" |

---

## License

**CC BY-NC-SA 4.0** — [Full text](LICENSE)

- **Share & Adapt**: Free for non-commercial use with attribution
- **Commercial Use**: Requires explicit permission

For commercial licensing: [david@gemsquared.ai](mailto:david@gemsquared.ai)

---

## Contact

**Author**: Inseok Seo (David Seo)
**Email**: [david@gemsquared.ai](mailto:david@gemsquared.ai)
**Website**: [gemsquared.ai](https://gemsquared.ai)

---

## Citation

```bibtex
@misc{seo2026gem2,
  author = {Seo, Inseok (David)},
  title = {GEM² Platform Specification v1.5.5: Formal Framework for Autonomous AI Software Development with Provable Boundaries and epistemic honesty},
  year = {2026},
  publisher = {GEMsquared.ai},
  howpublished = {\url{https://gem-squared.github.io/gem-squared-platform}}
}
```

---

> **"AI is not magic; it is a probabilistic engine that becomes deterministic when constrained by a rigorous Topology (GEM²)."**

---

*GEM² Platform Specification v1.5.5 | © 2026 GEMsquared.ai | [CC BY-NC-SA 4.0](LICENSE)*
