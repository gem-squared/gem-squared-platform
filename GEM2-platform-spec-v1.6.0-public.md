# GEM² Platform Specification v1.6.0

**Governance, Evidence, and Matrix Management**

A formal framework for autonomous AI software development
with **provable boundaries and epistemic honesty**.

---

## Part I: Introduction

### Overview

> **"Prompt Engineering → Prompt Compilation → AI: from Magic to Engineering"**

**GEM² Platform** transforms AI-assisted development from heuristic craft to formal engineering. AI actors execute within **mathematically defined, verifiable boundaries** — not through hope, but through proof.

**Under TPMN, an LLM becomes a compiler** — prompts are validated before execution, outputs verified after.

This document defines the **conceptual model and dynamics** of GEM² Platform.

---

### Conceptual Stack

```
GEM²            → Company + Platform + Mathematical Universe
GEM² platform   → GEM² + NTC-VPC + TPMN + GACC + GEM-KG
NTC-VPC         → Specification (conservation laws)
TPMN            → Legislator, DUAL-GATE (TPMN_P/O)
GACC + GEM-KG   → Orchestrator + Knowledge Graph
T_AI            → AI Actors executing within boundaries
```

| Layer | Role |
|-------|------|
| **GEM²** | The universe-maker (company, platform, mathematical space) |
| **GEM² platform** | Integration: GEM² + NTC-VPC + TPMN + GACC + GEM-KG |
| **NTC-VPC** | Conservation laws ensuring provability |
| **TPMN** | Prompt compilation — Legislator + Judge |
| **GACC** | Orchestrator + Quality Gate |
| **T_AI** | AI Actors (G, S, D, I, E) |

---

## Part II: Why — Core Philosophy

### Core Principles

> **"Humans dream, AI delivers, Evidence decides."**

| Principle | Meaning |
|-----------|---------|
| **Evidence over Time** | Progress = f(Evidence), not f(Time) |
| **Compilation over Craft** | Prompts are compiled, not crafted |
| **Dual-Gate Validation** | TPMN_P (before) + TPMN_O (after) |
| **Epistemic Honesty** | AI must admit when extrapolating (EEF) |
| **Realistic Completion** | Ω_accept = {V, B, S} — perfection not required |

---

### Philosophy

```yaml
CORE PHILOSOPHY:
  "Humans dream, AI delivers, Evidence decides"

  # P₀ Terminology
  # P₀_Vision   = [why, what, where] — the human vision container
  # P0_Check    = TPMN_P rule — verifies CONTRACT extractability

  • WHAT/WHY/WHERE comes from human vision (P₀_Vision = [why, what, where])
  • HOW-TO emerges from AI-interpolation (T_AI decides within INTERPOLATION_DOMAIN)
  • Success proven through evidence (ξ ∈ Ω_accept = {V, B, S})
  • No time-based planning, only evidence-based progress

AUTONOMOUS EXECUTION:
  "AI as actor, not assistant"

  • Full decision authority within Cell_TLA.P constraints
  • T_AI replaces human coding through interpolation
  • Mathematically provable: ξ(U_b, U_e, U_r) → Ω
  • With NTC-VPC + TPMN + GEM², self-sufficient for autonomy

AI INTERPOLATION:
  "Contract defines WHAT, AI decides HOW-TO"

  • Human provides: WHAT/WHY/WHERE (P₀ — VISION)
  • NTC provides: Contract interface (Cell_TLA: A → B | P)
  • T_AI decides: HOW-TO (execution path — INTERPOLATION_DOMAIN)
  • Execution path is OPAQUE — only contract satisfaction matters

TPMN DUAL-GATE:
  "Legislator at prompt-intake, Judge at output-validation"

  • An LLM becomes a compiler UNDER TPMN RULES
  • TPMN_P (Legislator): Validates prompt BEFORE AI runs
  • TPMN_O (Judge): Verifies output AFTER AI runs
  • EEF: Flags EXTRAPOLATION — epistemic honesty mandatory
  • SPT: Prohibits S→T, L→G, Δe→∫de transitions

  TPMN_Pipeline:
    Prompt
      ↓
    [TPMN_P] ← Legislator (prompt-intake)
      ↓ extracts
    A_Priori_Grid (IR)
      ↓
    [LLM] ← CodeGen (interpolation)
      ↓ generates
    Raw_Output
      ↓
    [TPMN_O] ← Judge (output-validation)
      ↓ validates
    Valid_Output ∨ Repair_Loop
```

---

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

**The Equation (Epistemically Honest):**

> **ANALOGY_ONLY**: The integral symbol (∫) below is a VISUAL ANALOGY.
> This does NOT constitute Δe→∫de inference. SPT rules still apply.

```
AI-interpolation: Σ GEM²[T][c] ↦ G-Noumena (CONTRACT satisfaction)
                  ─────────────────────────────────────────────────
                  (as Σf(xᵢ)Δx ≈ ∫f(x)dx)  [ANALOGY_ONLY]

NOT: Σ GEM²[T][c] ↦ Reality  ← L→G violation!
```

| Symbol | Meaning |
|--------|---------|
| Σf(xᵢ)Δx | Riemann sum — discrete approximation |
| ∫f(x)dx | Integral — continuous (like requirements) |
| Σ GEM²[T][c] | Sum of all GEM² cells — discrete model |
| ↦ G-Noumena | Maps to CONTRACT satisfaction (not Reality) |

**Responsibility Boundaries:**

| Layer | GEM² Solves | NOT GEM² Responsibility |
|-------|-------------|-------------------------|
| P₀ → CONTRACT | Formalize requirements | Whether P₀ reflects reality |
| CONTRACT → Code | Satisfy CONTRACT | Whether CONTRACT is correct |
| Code → Evidence | Prove Ω_accept | Whether Ω_accept = real success |

> **Key Boundary**: G-Noumena (requirements) ≠ R-Noumena (reality)

**The Honest Claim:**

GEM² solves **G-Noumena** (CONTRACT satisfaction), not **R-Noumena** (Reality).
If requirements are wrong, that's a **P₀/Human problem**, not a GEM² problem.

All GEM² structures, tools, laws, and equations serve one purpose:
**Transform requirements into discrete, computable, provable form.**

---

### EPIC-TIDE Breakdown

```
EPIC = Evidence-Powered Iterative Coordination
       │         │        │          │
       │         │        │          └── GACC coordination (T_AI actor collaboration)
       │         │        └── Phase cycles <<G, S, D, I, E, V>>
       │         └── Mathematical verifier (ξ, θ, Ω_Tensor, TPMN_O)
       └── Ω_accept = {V, B, S}, K_p/K_q/K_ai knowledge

TIDE = Tensor Intelligence-Driven Execution
       │       │            │       │
       │       │            │       └── I_AI implementation (diagonal cells)
       │       │            └── TPMN dual-gate, DSM topology guides flow
       │       └── Multi-LLM actors (T_AI: G, S, D, I, E)
       └── DSM tensor (U_b, U_e, U_r), size ∈ {3,4,5,6,7}
```

| Acronym | Full Name | Core Idea |
|---------|-----------|-----------|
| **EPIC** | Evidence-Powered Iterative Coordination | ξ/θ/Ω verification → Ω_GEM² completion |
| **TIDE** | Tensor Intelligence-Driven Execution | DSM topology + T_AI → autonomous HOW-TO |

---

## Part III: What — Formal Foundations

### Ontology: Types and Domain

The GEM² universe operates in a **discrete, computable domain**:

| Type | Definition | Purpose |
|------|------------|---------|
| **Domain** | {⊥, -1, 0, 1} | Four-valued logic for all matrices |
| **Ev_STATE** | {V, B, S, F, P} | Existence states (see Glossary) |
| **EEF_Record** | Extrapolation flag | Epistemic honesty marker |

---

### Structure: Tensor and Universes

#### Design Structure Matrix (DSM)

Components organized in **square matrices**:

| Property | Value |
|----------|-------|
| Size range | 3×3 to 7×7 |
| Diagonal cells | Components (BUSINESS logic) |
| Off-diagonal cells | Interfaces (INTERFACE logic) |

Complex components **decompose** into child tensors — fractal hierarchy of bounded complexity.

#### Three Universes (Matrices)

| Universe | Matrix | Meaning |
|----------|--------|---------|
| **Blueprint** | U_b | What SHOULD exist — design intent |
| **Existence (GEM)** | U_e | What DOES exist — happy path |
| **Resistance (CHAOS)** | U_r | What SURVIVES failure — fallback path |

**Completion** = sufficient evidence in GEM + resistance below threshold in CHAOS.

---

### Laws: Conservation Invariants

GEM² enforces **three conservation laws** that guarantee provability:

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

#### SPT: Strictly Prohibited Transitions

| Symbol | Transition | Meaning |
|--------|------------|---------|
| **S→T** | State → Trait | Never treat mutable as immutable |
| **L→G** | Local → Global | Never extrapolate local to universal |
| **Δe→∫de** | Evidence < θ_e_min | Never expand small evidence to large claims |

**Evidence Counting (Δe→∫de operationalization):**

```
θ_e_min ≜ 3  (* Minimum evidence count for broad claims *)

EvidenceItem ≜ {
  LOG:    "Execution log / trace",
  TEST:   "Automated test result",
  PROOF:  "Formal proof / verification",
  TRACE:  "Audit trail / lineage",
  REVIEW: "Human review record"
}

EvidenceCount(claim) ≜ |{ e ∈ EvidenceItem : supports(e, claim) }|

Δe→∫de_Violation ≜ EvidenceCount(claim) < θ_e_min ∧ claim.scope = BROAD
```

| Evidence Count | Allowed Claim Scope |
|----------------|---------------------|
| < 3 | LOCAL only (single cell/case) |
| ≥ 3 | BROAD allowed (pattern/general) |

---

### Operations: Functions and Actors

#### Existence Derivation (ξ)

The **ξ function** derives existence state from three matrices:

```
ξ(T,c) ≜ derive(U_b[T][c], U_e[T][c], U_r[T][c]) → Ev_STATE

Where:
  T = TensorID (which tensor)
  c = CellRef (which cell in tensor)

Result: One of {V, B, S, F, P}
```

| State | Symbol | Meaning | Acceptable? |
|-------|--------|---------|-------------|
| Verified | V | Exists in GEM, passed CHAOS | ✅ |
| Buggy | B | Known imperfection, flagged | ✅ |
| Skipped | S | Tolerance test skipped (approved) | ✅ |
| Failed | F | Must fix | ❌ |
| Pending | P | Not yet verified | ❌ |

**Acceptance Set:**

```
Ω_accept ≜ {V, B, S}  (* Acceptable completion states *)

Ω_Tensor(T) ≜ ∀c ∈ Cells(T): ξ(T,c) ∈ Ω_accept
Ω_GEM²(P)   ≜ ∀T ∈ ProjectTensors(P): Ω_Tensor(T)
```

#### Skip Governance (S ∈ Ω_accept)

When a cell is marked **Skipped (S)**, governance requires:

```
SkipApproval ≜ [
  who:      "Approver identity (human or authorized role)",
  why:      "Justification for skipping verification",
  scope:    "Which cells/tests are skipped",
  expiry:   "When skip approval expires (optional)",
  risk:     "Acknowledged risk level {LOW, MEDIUM, HIGH}",
  audit_id: "Traceability reference"
]

Invariant: S ∈ Ω_accept ⟹ ∃ SkipApproval ∧ SkipApproval.visible_in_FINAL_LAYER
```

| Field | Required | Purpose |
|-------|----------|---------|
| who | ✅ | Accountability |
| why | ✅ | Auditability |
| scope | ✅ | Bounded impact |
| expiry | ⚪ | Time-bound approval |
| risk | ✅ | Risk acknowledgment |
| audit_id | ✅ | Traceability |

> **Key**: S without SkipApproval = governance violation.

#### T_AI: AI Actor System

| Actor | Phase | Input → Output |
|-------|-------|----------------|
| **G_AI** | Genesis | P₀ → G-Project document |
| **S_AI** | Structure | G-Project → Tensor_Init |
| **D_AI** | Design | Tensor_Init → Cell_TLA contracts |
| **I_AI** | Implement | Cell_TLA → Code |
| **E_AI** | Execute | Code → Evidence (U_e, U_r) |

**GACC** orchestrates all actors. Each actor operates independently with focused responsibility.

---

### Application: Pipelines and Storage

#### Three Pipelines

| Pipeline | Actors | Purpose |
|----------|--------|---------|
| **DEVELOP** | G, S, D, I, E | Forward engineering: P₀ → Code → Evidence |
| **ANALYSIS** | G, S, D, E | Reverse engineering: Code → Spec extraction |
| **VERIFY** | D, I | Code ↔ Contract validation |

#### Dual Validation

| Validation | When | Who |
|------------|------|-----|
| **TPMN_P_Self** | Before task | T_AI self-check |
| **TPMN_O_Self** | After task | T_AI self-check |
| **TPMN_O_GACC** | Gate transition | GACC external check |

Two gates ensure quality: **self-check + external-check**.

#### Storage Structure

```
.gem-squared/{project}/           ← FINAL_LAYER (SoT)
.gem-squared/{project}/_meta/     ← ACTOR_LAYER (workspace)
```

| Layer | Purpose | Owner |
|-------|---------|-------|
| FINAL_LAYER | Single Source of Truth | GACC (after promotion) |
| ACTOR_LAYER | Per-actor work products | T_AI during work |

Promotion: Actor creates → GACC validates → Promote to FINAL_LAYER → Freeze.

---

## Part IV: How — TPMN Prompt Compilation

### TPMN: Making LLM Act as Compiler

> **TPMN applies RLAIF principles at inference-time (NOT training).**
> **Core Claim: An LLM becomes a compiler UNDER TPMN RULES.**

**TPMN_Compiler_Features** — What "compiler" means here:

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

The core insight: **AI governs AI** through dual-gate validation.

**Terminology Clarification:**

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

**TPMN_P (Legislator)** + **TPMN_O (Judge)** = AI-to-AI governance at inference.

---

## Part V: Future — GEM-KG Vision

### Evolution Path: Inference → Persistence → Training

```
Phase 1 (NOW):   Inference-time AI feedback (TPMN)
                 → Ephemeral: judgments exist only during execution
                 → Foundation: GACC orchestrates, TPMN validates

Phase 2 (KG):    GEM-KG stores feedback patterns
                 → Persistent: judgments stored as knowledge graph
                 → Accumulation: patterns emerge from repeated execution

Phase 3 (RLAIF): Stored patterns → training signal → model improvement
                 → Training-time: true RLAIF with persistent feedback
                 → Evolution: GEM² becomes self-improving system
```

### GACC + GEM-KG: Foundation for the Journey

| Component | Role in Evolution |
|-----------|-------------------|
| **GACC** | Orchestrator — generates quality judgments during execution |
| **GEM-KG** | Knowledge Graph — persists judgments as structured data |
| **T_AI** | Actors — produce work products evaluated by GACC |

**GEM² + GEM-KG = Full-stack AI governance**: inference → persistence → training.

---

## Minimal Path (Onboarding)

**Essential 5 concepts** to understand GEM² quickly:

| Concept | One-liner | Why it matters |
|---------|-----------|----------------|
| **TPMN_P** | Validates prompt BEFORE AI runs | Catches ambiguity early |
| **TPMN_O** | Verifies output AFTER AI runs | Ensures contract satisfaction |
| **EEF** | Flags when AI extrapolates | Epistemic honesty |
| **SPT** | Forbids S→T, L→G, Δe→∫de | Prevents illicit leaps |
| **Ω_accept** | {V, B, S} = completion | Realistic, not perfection |

**End-to-End Example:**

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

> **Key insight**: The "compiler" metaphor = TPMN_P (syntax check) + TPMN_O (semantic check).

---

## Core Takeaways

1. **GEM² is a universe, not a tool.**
2. **Under TPMN, LLM acts as compiler, not prompt template executor.**
3. **AI actors execute within provable boundaries.**
4. **Evidence replaces time; proof replaces hope.**
5. **Epistemic honesty is mandatory (EEF).**
6. **Completion is realistic, not perfection.**
7. **GEM-KG enables evolution from inference to training.**

---

## Appendix A: Glossary

### Core Symbols

| Symbol | Name | Definition |
|--------|------|------------|
| **⊥** | Bottom | Undefined / not yet set |
| **ξ** | Xi | Existence classifier function: ξ(T,c) → Ev_STATE |
| **θ** | Theta | Threshold value for layer transitions |
| **Ω** | Omega | Completion predicate |
| **Ω_accept** | Acceptance Set | {V, B, S} — states that constitute "done" |

### Matrices

| Symbol | Name | Meaning |
|--------|------|---------|
| **U_b** | Blueprint Universe | Design intent — what SHOULD exist |
| **U_e** | Existence Universe (GEM) | Evidence — what DOES exist |
| **U_r** | Resistance Universe (CHAOS) | Failure evidence — what SURVIVES |

### Existence States (Ev_STATE)

| State | Symbol | Meaning | In Ω_accept? |
|-------|--------|---------|--------------|
| Verified | **V** | Passed both GEM and CHAOS tests | ✅ Yes |
| Buggy | **B** | Known issue, explicitly flagged | ✅ Yes |
| Skipped | **S** | Test skipped with approval | ✅ Yes |
| Failed | **F** | Must be fixed before completion | ❌ No |
| Pending | **P** | Not yet evaluated | ❌ No |

### TPMN Components

| Term | Meaning |
|------|---------|
| **TPMN** | The prompt compilation framework (Legislator + Judge) |
| **TPMN_P** | Prompt validator — runs BEFORE AI execution |
| **TPMN_O** | Output validator — runs AFTER AI execution |
| **A_Priori_Grid** | IR (Intermediate Representation) — extracted from prompt by TPMN_P |
| **EEF** | Extrapolation/Evidence Flag — epistemic honesty marker |
| **SPT** | Strictly Prohibited Transitions (S→T, L→G, Δe→∫de) |

### Actors

| Actor | Role |
|-------|------|
| **G_AI** | Genesis — creates initial project structure from P₀ |
| **S_AI** | Structure — defines tensor decomposition |
| **D_AI** | Design — creates Cell_TLA contracts |
| **I_AI** | Implement — writes code satisfying contracts |
| **E_AI** | Execute — generates evidence (tests, proofs) |
| **GACC** | Orchestrator — coordinates actors, validates gates |

### Laws

| Law | Name | Scope |
|-----|------|-------|
| **L_S** | Set Law | Cell-level monotonicity |
| **L_C** | Calculus Law | Lifecycle-level threshold crossing |
| **L_A** | Algebra Law | Matrix-level operation coherence |

### SPT Violations

| Symbol | Meaning | Example Violation |
|--------|---------|-------------------|
| **S→T** | State → Trait | Treating a runtime value as compile-time constant |
| **L→G** | Local → Global | "Works on my machine" → "Works everywhere" |
| **Δe→∫de** | Small → Large | "2 tests passed" → "Always works" |

---

## Meta

### License

**CC BY-NC-SA 4.0** (Creative Commons Attribution-NonCommercial-ShareAlike 4.0)

You are free to:
- **Share** — copy and redistribute the material
- **Adapt** — remix, transform, and build upon the material

Under the following terms:
- **Attribution** — You must give appropriate credit
- **NonCommercial** — Commercial use requires explicit permission from GEMsquared.ai
- **ShareAlike** — Derivatives must use the same license

For commercial licensing inquiries: **david@gemsquared.ai**

### Contact

**Author**: Inseok Seo (David Seo)
**Email**: david@gemsquared.ai
**Company**: GEMsquared.ai
**Project**: GEM² Platform

### Citation

```
Seo, Inseok (David).
"GEM² Platform Specification v1.6.0:
Formal Framework for Autonomous AI Software Development."
GEMsquared.ai, January 2026.
```

---

> **"GEM² — A mathematical universe for autonomous AI."**

---

*GEM² Platform Specification v1.6.0 (Public) | Conceptual Overview | 2026-01-22*

**Tagline:**
"AI is not magic; it is a probabilistic engine that becomes deterministic when constrained by a rigorous Topology (GEM²)."
