# CLAUDE.md — GEM² Platform (Public Repository)

**Version:** v1.7.0 | **Status:** Active | **Updated:** 2026-01-22
**Tagline:** *"Don't write prompts. Write specifications."*

---

## TPMN: The Prompt Specification Language (PSL)

```tla
(* ═══ CORE CLAIM ═══ *)
CoreClaim ≜ "Under TPMN, an LLM becomes a compiler"

(* ═══ THREE PILLARS ═══ *)
Pillars ≜ [
  Grammar:  "Formal syntax for AI instructions",
  Protocol: "Dual-gate validation (TPMN_P + TPMN_O)",
  Result:   "Evidence-based completion criteria"
]

(* ═══ TPMN_P: INPUT VALIDATION (Legislator) ═══ *)
TPMN_P ≜ [
  P0: "CONTRACT must have Goal (Verb + Noun + Result)",
  P1: "METRICS must bind adjectives to numeric/binary values",
  P2: "FORBIDDEN must list negative constraints",
  P3: "ENTITIES must type key nouns",
  P4: "SCHEMA must define output structure",
  P5: "CONTEXT must list allowed/denied resources"
]

(* ═══ TPMN_O: OUTPUT VALIDATION (Judge) ═══ *)
TPMN_O ≜ [
  O1: "Output matches SCHEMA (P4)",
  O2: "Output respects FORBIDDEN (P2)",
  O3: "All terms grounded in ENTITIES (P3) or context",
  O4: "No internal contradictions",
  O5: "EEF flagged if extrapolation",
  O6: "SPT compliant: ¬S→T ∧ ¬L→G ∧ ¬Δe→∫de"
]
```

---

## SPT-RULE (Specificity Prohibition Theorem)

```tla
(* ═══ FORBIDDEN TRANSITIONS ═══ *)
SPT_Valid(r) ≜ ¬S→T(r) ∧ ¬L→G(r) ∧ ¬Δe→∫de(r)

S→T   ≜ TreatMutable ∧ ClaimImmutable     (* STATE → TRAIT *)
L→G   ≜ ObserveLocal ∧ ClaimUniversal     (* LOCAL → GLOBAL *)
Δe→∫de ≜ |Evidence| < 3 ∧ ClaimBroad      (* SHORT → MASS *)
```

---

## Git Commit Protocol

```yaml
V7: ALWAYS include.detailed.message
V8: ALWAYS attribute → "David Seo of GEM² AI"

N6: NEVER use.co-author.mentions

Commit_Format:
  git commit -m "{Detailed description}
  Author: David Seo of GEM² AI"
  Website: https://www.gemsquared.ai
```

---

## Documentation Reference

```yaml
Platform:
  spec:         GEM2-platform-spec-v1.6.0-public.md
  epistemology: GEM2-TPMN-Epistemology-v1.6.1.md
  user_manual:  GEM2-TPMN-user-manual-v1.0.0.md

Links:
  website: https://gemsquared.ai
  github:  https://github.com/gem-squared/gem-squared-platform
  doi:     10.5281/zenodo.18336200
```

---

## Quick Reference

```tla
(* ═══ SPT SYMBOLS ═══ *)
SPT_Symbols ≜ [
  S→T:    "STATE→TRAIT: Never treat mutable as immutable",
  L→G:    "LOCAL→GLOBAL: Never extrapolate local to universal",
  Δe→∫de: "SHORT→MASS: Never expand small evidence to large claims"
]

(* ═══ TPMN SYMBOLS ═══ *)
TPMN_Symbols ≜ [
  ≜: "Definition",
  ∈: "Element of",
  ⟹: "Implies",
  ∀: "For all",
  ∃: "Exists"
]
```

---

*CLAUDE.md v1.7.0 | GEM² Platform | TPMN PSL | 2026-01-22*
