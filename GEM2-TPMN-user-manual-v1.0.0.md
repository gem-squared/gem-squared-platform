# TPMN: The Prompt Specification Language

**Version:** v1.0.0 | **Status:** User Manual | **Updated:** 2026-01-22
**Parent:** GEM2-TPMN-Epistemology-v1.6.1.md

---

## Don't write prompts. Write specifications.

> **TPMN compiles intent into a checkable IR and verifies outputs.**

---

```tla
--- MODULE TPMN_UserManual ---

(* ════════════════════════════════════════════════════════════════════════════ *)
(* TPMN USER MANUAL — The Grammar for Prompt Specification                     *)
(* ════════════════════════════════════════════════════════════════════════════ *)
(* "Prompt Engineering → Prompt Compilation. The Protocol for Autonomous AI."  *)
(* ════════════════════════════════════════════════════════════════════════════ *)

(* ═══ WHAT IS TPMN? ═══ *)

PSL ≜ [
  what:     "A compact specification DSL for LLM work",
  includes: {"Syntax", "Well-formedness rules", "Schema", "Constraints", "Diagnostics", "Versioning"},
  excludes: {"binary compiler requirement", "general-purpose programming language semantics"}
]

PromptCompilation ≜ [
  compile_time: "TPMN_P: Spec → IR(A_Priori_Grid) + Diagnostics + UNC",
  run_time:     "LLM(CodeGen): IR → Output",
  verify_time:  "TPMN_O: Output ⊨ IR ∧ SPT ∧ EEF"
]

Protocol ≜ [
  meaning: "Normative process the AI follows (compile gate + verify gate)",
  gates:   ⟨"Legislator (TPMN_P)", "Judge (TPMN_O)"⟩
]

(* ═══ THE THREE PILLARS ═══ *)

ThreePillars ≜ ⟨
  [name: "The Grammar",  desc: "TLA+-style syntax: contracts, entities, constraints, schema"],
  [name: "The Protocol", desc: "Dual-gate: compile (TPMN_P) then verify (TPMN_O)"],
  [name: "The Result",   desc: "spec → diagnostics → verified output"]
⟩

===
```

---

## 1. Core Block Structure

Every TPMN specification follows this TLA+-inspired structure. Use this template:

```tla
TPMN_SPECIFICATION(Task_Name) ≜ [

  (* ═══ 1. G-NOUMENA (The Contract) ═══ *)
  (* P0: Define the immutable goal. No ambiguity. *)
  CONTRACT: [
    Goal:    "Verb + Noun + Result",   (* e.g., "Refactor AuthModule to JWT" *)
    Input:   "Variables/Context",      (* e.g., "user_session_v1.py" *)
    Output:  "Artifact Definition"     (* e.g., "user_session_v2.py" *)
  ],

  (* ═══ 2. A_PRIORI (The Constraints) ═══ *)
  (* P1: Metrics - Adjectives must be measured *)
  METRICS: [
    "fast":   "latency < 200ms",
    "secure": "OWASP Top 10 compliant",
    "short":  "lines_of_code < 150"
  ],

  (* P2: Negative Constraints - What is FORBIDDEN *)
  FORBIDDEN: ⟨
    "No external API calls",
    "No breaking changes to Public Interface",
    "Do not use 'eval()'"
  ⟩,

  (* P3: Entity Typing - Define your Nouns *)
  ENTITIES: [
    User:    [id: "UUID", role: "Enum{Admin, Guest}"],
    Session: [token: "JWT", expiry: "Timestamp"]
  ],

  (* P5: Context Isolation - Available Tools *)
  CONTEXT: [
    Allowed_Libs: {"pydantic", "fastapi"},
    Network:      FALSE,      (* strict isolation *)
    FileSystem:   READ_ONLY
  ],

  (* ═══ 3. PHENOMENA (The Output Shape) ═══ *)
  (* P4: Output Schema - The physical shape of the answer *)
  SCHEMA: [
    Format: "JSON | Markdown | CodeBlock",
    Structure: [
      status:       "String",
      reasoning:    "String (Brief rationale; not hidden CoT)",
      code:         "String",
      verification: "Object (TPMN_O)"
    ]
  ],

  (* ═══ 4. VERIFICATION PROTOCOL ═══ *)
  EXECUTION_MODE: [
    EEF_Check: REQUIRED,  (* Must flag extrapolation *)
    SPT_Check: STRICT     (* No S→T, L→G transitions *)
  ]
]
```

---

## 2. Grammar Rules (P-Legislator)

> **Note:** Tables below are documentation rendering. TPMN source format is TLA+-style blocks.

| Rule ID | Name | Syntax / Requirement | Failure Condition |
|---------|------|---------------------|-------------------|
| **P0** | Contract Binding | Goal = Verb + Noun + Result | Rejects "Make it better" |
| **P1** | Metric Binding | key: value (numeric or binary) | Rejects "efficient" without measure |
| **P2** | Negation | Must use NO, NOT, FORBIDDEN, ¬ | Rejects purely permissive constraints |
| **P3** | Typing | Entity: [field: Type] | Rejects ambiguous nouns as variables |
| **P4** | Schema | Must define output container | Rejects unstructured text streams |
| **P5** | Isolation | Explicit Allowed/Denied resources | Rejects assumed access (e.g., network) |

---

## 3. Validation Flags (O-Judge)

Instruct the AI to append this block for runtime verification:

```tla
TPMN_O_CHECK(Self_Verification) ≜ [

  (* Schema & Constraint Compliance *)
  O1_Schema:      PASS | FAIL,   (* Did it match P4? *)
  O2_Constraints: PASS | FAIL,   (* Did it respect P2? *)
  O3_Grounding:   PASS | FAIL,   (* Are all terms defined in P3? *)
  O4_Logic:       PASS | FAIL,   (* No contradictions? *)

  (* Epistemic Honesty *)
  EEF_Status: [
    Extrapolation: TRUE | FALSE,
    Confidence:    0.0 to 1.0,
    Source:        "Training_Data" | "Context"
  ],

  (* Categorical Hygiene *)
  SPT_Violation: NONE | "S→T Detected" | "L→G Detected" | "Δe→∫de Detected"
]
```

---

## 4. Example: Compiling a Request

### Raw Prompt (Ambiguous / R-Noumena)

> "Write a fast python script to parse logs and find errors. Don't make it too complicated."

### Compiled TPMN Spec (G-Noumena)

```tla
TPMN_SPECIFICATION(LogParser) ≜ [
  CONTRACT: [
    Goal:   "Extract error lines from text logs to JSON",
    Input:  "server.log (text)",
    Output: "errors.json"
  ],

  METRICS: [
    "fast":            "processing_time < 1s per 10MB",
    "not_complicated": "single_file, no_external_deps, < 50 lines"
  ],

  FORBIDDEN: ⟨"No regex complex lookbehinds", "No 3rd party pip install"⟩,

  ENTITIES: [
    LogEntry: [timestamp: "ISO8601", level: "Enum{ERROR, WARN}", msg: "String"]
  ],

  SCHEMA: [
    Format:       "Python 3.10 Script",
    Must_Include: "Main function, Unit Test block"
  ]
]
```

---

## 5. Elevator Pitches

```tla
ElevatorPitch ≜ [

  PublicGeneral ≜ [
    message:  "Stop guessing. Specify constraints and schema. TPMN makes AI outputs rejectable and repeatable.",
    promise:  "More controllable outputs via compilation + verification",
    boundary: "Phenomena-only: verified artifacts, not metaphysical certainty"
  ],

  Engineers ≜ [
    message: "TPMN is a DSL: Spec → IR; LLM acts as codegen; verifier enforces schema+constraints+SPT.",
    hooks:   ⟨"IR(A_Priori_Grid)", "Diagnostics", "Conformance checks"⟩
  ],

  Academics ≜ [
    message: "TPMN is an epistemic protocol: formal syntax bounds admissible inference; UNC marks limits.",
    hooks:   ⟨"A_Priori Grid", "Phenomena validation", "Inference boundary"⟩
  ]
]
```

---

## 6. Defensibility

```tla
DefensibilityFooter ≜ [
  claim_scope:  "Within GEM²/TPMN workflow semantics",
  not_claiming: ⟨
    "universal truth guarantees",
    "determinism",
    "human-level epistemic access to Noumena"
  ⟩,
  compliance:   ⟨"SPT: ¬S→T ∧ ¬L→G ∧ ¬Δe→∫de", "EEF: UNC when extrapolating"⟩
]
```

---

## Quick Reference

> **Note:** Tables below are documentation rendering. TPMN source format is TLA+-style blocks.

| Symbol | Meaning |
|--------|---------|
| `≜` | Definition |
| `∈` | Element of |
| `⟹` | Implies |
| `∀` | For all |
| `∃` | Exists |
| `¬` | Negation |
| `⟨...⟩` | Sequence |
| `{...}` | Set |
| `[...]` | Record |

---

**v1.0.0 | TPMN User Manual | The Prompt Specification Language | 2026-01-22**
