# GEM² TPMN Epistemology Specification

**Version:** v1.6.3 | **Status:** Companion | **Updated:** 2026-01-23
**Parent:** GEM2-spec-v1.5.8.md
**Tagline:** *"Don't write prompts. Write specifications."*

---

```tla
--- MODULE GEM2_TPMN_Epistemology ---

(* ════════════════════════════════════════════════════════════════════════════ *)
(* GEM² TPMN EPISTEMOLOGY — WHY does this work? — Philosophical foundation     *)
(* ════════════════════════════════════════════════════════════════════════════ *)
(* "Prompt Engineering → Prompt Compilation. The Protocol for Autonomous AI."  *)
(* ════════════════════════════════════════════════════════════════════════════ *)

(* ═══ PUBLIC INTRODUCTION: TPMN — The Prompt Specification Language ═══ *)

PSL_Introduction ≜ [

  (* --- HERO --- *)
  Hero ≜ [
    title:    "TPMN",
    subtitle: "The Prompt Specification Language",
    tagline:  "Don't write prompts. Write specifications."
  ],

  (* --- ONE-LINER --- *)
  OneLiner ≜ "Stop guessing. Specify constraints and schema. TPMN compiles intent into a checkable IR and verifies outputs.",

  (* --- DEFINITION BLOCK --- *)
  PSL ≜ [
    what:     "A compact specification DSL for LLM work",
    includes: {"Syntax", "Well-formedness rules", "Schema", "Constraints", "Diagnostics", "Versioning"},
    excludes: {"binary compiler requirement", "general-purpose programming language semantics"}
  ],

  PromptCompilation ≜ [
    compile_time: "TPMN_P: Spec → IR(A_Priori_Grid) + Diagnostics + UNC",
    run_time:     "LLM(CodeGen): IR → Output",
    verify_time:  "TPMN_O: Output ⊨ IR ∧ SPT ∧ EEF"
  ],

  Protocol ≜ [
    meaning: "Normative process the AI follows (compile gate + verify gate)",
    gates:   ⟨"Legislator (TPMN_P)", "Judge (TPMN_O)"⟩
  ],

  (* --- ELEVATOR PITCHES --- *)
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
  ],

  (* --- VISUAL HIERARCHY --- *)
  VisualHierarchy ≜ [
    headline: "TPMN: The Prompt Specification Language",
    sub:      ⟨"Syntax", "Logic", "Compilation"⟩,

    three_pillars: ⟨
      [name: "The Grammar",  desc: "A TLA+-style syntax to define contracts, entities, constraints, schema"],
      [name: "The Protocol", desc: "Dual-gate: compile (TPMN_P) then verify (TPMN_O)"],
      [name: "The Result",   desc: "AI behavior shaped like engineering: spec → diagnostics → verified output"]
    ⟩
  ],

  (* --- DEFENSIBILITY FOOTER --- *)
  DefensibilityFooter ≜ [
    claim_scope:  "Within GEM²/TPMN workflow semantics",
    not_claiming: ⟨
      "universal truth guarantees",
      "determinism",
      "human-level epistemic access to Noumena"
    ⟩,
    compliance:   ⟨"SPT: ¬S→T ∧ ¬L→G ∧ ¬Δe→∫de", "EEF: UNC when extrapolating"⟩
  ]
]

(* ═══ CONCEPTUAL FRAMING ═══ *)
ConceptualFraming ≜ [
  Legislator: [
    role:   "TPMN_P as 'Legislator' — AI defines constraints before execution",
    analog: "Kantian lawgiver — autonomy through self-imposed rational law"
  ],

  RLAIF_Perspective: [
    traditional: "RLAIF = Training-time AI feedback → model weight updates",
    tpmn:        "TPMN = Inference-time AI feedback → output validation/repair",
    distinction: "TPMN applies RLAIF principles at INFERENCE (NOT training)",
    structure:   "AI as Legislator (TPMN_P) + AI as Judge (TPMN_O) = AI-to-AI governance",
    tagline:     "Legislator at prompt-intake, Judge at output-validation",
    core_claim:  "An LLM becomes a compiler UNDER TPMN RULES"
  ],

  Evolution: [
    phase_1: "NOW — Inference-time AI feedback (ephemeral)",
    phase_2: "GEM-KG — Persistent AI feedback (stored judgments)",
    phase_3: "RLAIF — Feedback → training signal → model improvement",
    vision:  "GEM² + GEM-KG = Full-stack AI governance: inference → persistence → training"
  ]
]

(* ═══ DOCUMENT SCOPE ═══ *)
Scope ≜ [
  purpose:        "PHILOSOPHICAL — explains WHY TPMN works (Kantian mapping)",
  not_purpose:    "OPERATIONAL — does NOT define mechanically decidable predicates",
  predicates:     "ILLUSTRATIVE — convey concepts, not implementation specs",
  formal_defs:    "GEM2-spec-v1.5.8.md §TPMN_PRIMITIVES",
  extension_rule: "Any added pipeline concept MUST remain epistemic (WHY) and bind to spec via NotationBindings",
  non_goal:       "Do NOT define mechanically decidable predicates here; only schemas + mappings"
]

(* Predicates like Has_Explicit_Metric, Sat, etc. appear here as CONCEPTUAL *)
(* ILLUSTRATIONS. For mechanically decidable definitions with grammar, types, *)
(* and validation rules, consult the spec. Separation: Epistemology=WHY, Spec=WHAT *)

(* ═══ NOTATION BINDINGS ═══ *)
(* Maps illustrative syntax in this doc to formal spec primitives *)
NotationBindings ≜ [
  "Has_Explicit_Metric(adj)"            → "Has_Explicit_Metric(adj, Prompt) in spec",
  "Output.structure == Schema"          → "SchemaEq(Output.structure, Schema)",
  "Output ⊨ constraint"                 → "Sat(Output, constraint)",
  "new_term ∈ Output"                   → "term ∈ NewTerm(Output)",
  "Output.content is EXTRAPOLATION"     → "ClassifyInference(content, evidence) = EXTRAPOLATION",
  "EEF_Flag == True"                    → "EEF_Flag.extrapolation = TRUE",

  (* ═══ PIPELINE BINDINGS (v1.6.3) ═══ *)
  "KCR(p)"                              → "TPMN_P.Compile(p) + Diagnostics",
  "FNC(Pc)"                             → "P3_Entity_Typing + P3a..P3d commitments",
  "WSP(Pc)"                             → "LogicalForm_Epistemic (proposition schema + falsifiers)",
  "LogicalForm_Epistemic"               → "P6_LogicalForm (spec-side when defined)",
  "DecisionFn"                          → "GACC policy decision over {PASS, ASK_HUMAN, RETRY_AI, TERMINATE}",
  "RETRY_AI"                            → "Re-run LLM with same Pc, no human input"
]

TPMN_EPISTEMOLOGY ≜ [

  (* ═══ 1. THE PROBLEM: AI AS MAGIC ═══ *)

  TheProblem ≜ [
    current_state: "AI interaction is heuristic craft — 'Prompt Engineering'",
    symptoms: <<
      "Trial and error until output 'looks good'",
      "No formal rejection mechanism for ambiguous prompts",
      "Success depends on practitioner intuition",
      "No structural guarantee — only outcome judgment"
    >>,
    diagnosis: "AI use resembles MAGIC: incantations (prompts) → hope for results"
  ],

  (* ═══ 2. KANTIAN FOUNDATION ═══ *)

  KantianInsight ≜ [
    question:  "How is valid AI output possible?",
    analog:    "Kant: How is knowledge possible?",
    answer:    "By imposing necessary conditions (A Priori) on raw data"
  ],

  (* 2.1 The Three Kantian Concepts *)
  KantianMapping ≜ [

    Noumena ≜ [
      kant:   "Thing-in-itself — beyond direct access",
      tpmn:   "User's mental intent/vision — under-determined by prompt alone",
      note:   "The prompt is REPRESENTATION of Noumena, not Noumena itself",
      unc:    "Degree of access is epistemically uncertain, not proven absolute"
    ],

    Phenomena ≜ [
      kant:   "What we experience through sensibility",
      tpmn:   "Raw AI token stream — observable output",
      note:   "Without structure, this is noise, not knowledge"
    ],

    A_Priori ≜ [
      kant:   "Categories imposed BEFORE experience (causality, unity...)",
      tpmn:   "TPMN rules imposed BEFORE accepting output (P0-P5, O1-O6)",
      note:   "The grid that transforms noise into structured knowledge"
    ]
  ],

  (* 2.2 Synthetic A Priori *)
  SyntheticAPriori ≜ [
    definition: "Judgments that add structure (synthetic) independent of content (a priori)",

    analytic_example:  "A = A (true by definition, adds nothing)",
    synthetic_example: "O5: Every inference marked with EEF flag if extrapolation",

    why_tpmn_is_synthetic: <<
      "O5 adds INFERENCE_TYPE to raw statements",
      "P4 adds SCHEMA to flat text",
      "P3 adds ENTITY_TYPE to terms",
      "These structures are NOT in the raw data — TPMN creates them"
    >>,

    why_tpmn_is_a_priori: <<
      "Rules defined BEFORE any specific AI inference",
      "P4 (Output schema) imposed independent of content",
      "P5 (Context isolation) exists before content is generated"
    >>
  ],

  (* 2.3 Extended GEM² Kantian Framework *)
  (* GEM² creates its own metaphysical layer — "GEM² is a universe, not a tool" *)
  GEM2_KantianFramework ≜ [

    (* Two-Layer Noumena: Real vs GEM² *)
    R_Noumena ≜ [
      definition: "Real Noumena — the unknowable vision behind the prompt",
      maps_to:    "P₀.intent",
      status:     "DISMISSED — we do NOT care, we can NOT control",
      note:       "Like Kant's thing-in-itself, forever beyond complete access"
    ],

    G_Noumena ≜ [
      definition: "GEM² Noumena — the 'thing-in-itself' OF GEM² universe",
      maps_to:    "CONTRACT (Cell_TLA)",
      status:     "KNOWABLE — formal, immutable, the law of GEM² world",
      note:       "Within GEM², CONTRACT is the fundamental reality"
    ],

    (* Two-Layer A_Priori: Pure vs Synthetic *)
    Pure_A_Priori ≜ [
      definition: "Knowledge truly independent of experience",
      maps_to:    "TPMN rules (P0-P5, O1-O6)",
      note:       "Innate categories — exist before any execution"
    ],

    Synthetic_A_Priori ≜ [
      definition: "Accumulated knowledge that acts as pre-existing for new execution",
      maps_to:    "GEM-KG",
      evolution:  "∅ → accumulated judgments → operational A_Priori",
      note:       "Built from experience, but applied BEFORE new execution"
    ],

    (* A_Priori_Grid — The IR connecting Prompt to Verification *)
    A_Priori_Grid ≜ [
      definition: "Intermediate Representation (IR) extracted from prompt",
      maps_to:    "The Categories (P0-P5 results) + extracted constraints",
      structure:  "[g_noumena, metrics, constraints, entities, schema, p_results]",
      kantian:    "The synthesized form of intuition — what shapes AI generation",
      source:     "TPMN_P.Compile(Prompt)",
      consumed:   "LLM_Generate (shapes output), TPMN_O (verifies against)",
      note:       "Bridge between NL and formal verification — the 'compiled' prompt"
    ],

    (* Phenomena and Judgement *)
    Phenomena ≜ [
      definition: "Observable output — the artifact",
      maps_to:    "Generated_Code, Test_Results, Evidence",
      note:       "What AI produces, subject to TPMN_O verification"
    ],

    Synthetic_Judgement ≜ [
      definition: "Judgement that adds new content not in the premise",
      maps_to:    "AI Interpolation",
      process:    "CONTRACT (WHAT) + A_Priori (constraints) → HOW-TO (new content)",
      note:       "AI adds implementation path — truly synthetic"
    ],

    (* Structure and Classification *)
    Topology ≜ [
      definition: "Spatial arrangement of components",
      maps_to:    "DSM structure (spec §3)",
      note:       "The shape of the problem space"
    ],

    Existence_Classifier ≜ [
      definition: "Mechanism of classifying existence state",
      maps_to:    "ξ(T,c) function (spec §5.7)",
      derives:    "{V, B, S, F, P} from (U_b, U_e, U_r)",
      note:       "The judge of what exists and in what state"
    ]
  ],

  (* 2.4 The Discretization Principle *)
  (* Origin: GEM² name inspired by Fundamental Theorem of Calculus *)
  DiscretizationPrinciple ≜ [
    origin:  "GEM² inspired by FTC — bridging continuous and discrete",

    insight: [
      Real_World: "continuous, messy, ambiguous (R_Noumena — DISMISSED)",
      GEM2:       "discrete, clean, provable (G_Noumena + A_Priori)",
      AI:         "handles discrete things clearly (INTERPOLATION_DOMAIN)"
    ],

    (* CRITICAL: Epistemically honest equation — avoids L→G violation *)
    equation: [
      formula:    "Σ GEM²[T][c] ↦ G-Noumena (CONTRACT satisfaction)",
      NOT:        "Σ GEM²[T][c] ↦ Reality  ← L→G violation!",
      analogy:    "as Σf(xᵢ)Δx ≈ ∫f(x)dx",
      meaning:    "GEM² cells approximate CONTRACT satisfaction, not Reality",
      disclaimer: "Whether CONTRACT reflects Reality is OUTSIDE GEM² scope"
    ],

    (* Responsibility Boundaries — prevents L→G claims *)
    responsibility: [
      GEM2_solves: [
        "P₀ → CONTRACT:    Formalize requirements",
        "CONTRACT → Code:  Satisfy CONTRACT",
        "Code → Evidence:  Prove Ω_accept"
      ],
      NOT_GEM2: [
        "Whether P₀ reflects reality",
        "Whether CONTRACT is correct",
        "Whether Ω_accept = real-world success"
      ],
      boundary: "G-Noumena (requirements) ≠ R-Noumena (reality)"
    ],

    key_difference: [
      calculus:   "Σ → ∫ as Δx → 0 (approaches continuous limit)",
      gem2:       "Stays discrete — completion is Ω_accept = {V, B, S}, not perfection"
    ],

    purpose: "All GEM² structures transform requirements into discrete, computable, provable form"
  ],

  (* ═══ 3. THE SOLUTION: PROMPT COMPILATION ═══ *)

  ParadigmShift ≜ [
    from: "Prompt Engineering — heuristic craft",
    to:   "Prompt Compilation — formal process",

    definition: [
      Prompt_Engineering: "Craft of writing prompts that TEND to produce good outputs",
      Prompt_Compilation: "Formal process of transforming prompts into constrained execution contexts with pre-runtime validation and post-runtime verification"
    ]
  ],

  (* 3.1 Why "Compilation" is the correct term *)
  (* Note: These are ANALOGIES to compiler concepts, not TPMN rules *)
  CompilationJustification ≜ [

    FormalGrammar: [
      compiler: "Source language has defined syntax/semantics",
      tpmn:     "P1-P5 rules define valid prompt structure"
    ],

    StaticAnalysis: [
      compiler: "Errors detected BEFORE execution",
      tpmn:     "TPMN(P) rejects ambiguous prompts BEFORE AI executes the target task (generation)"
    ],

    TypeSystem: [
      compiler: "Variables must be declared/typed",
      tpmn:     "P3: Entities must be typed (User vs User_ID)"
    ],

    Transformation: [
      compiler: "Source → IR → Target",
      tpmn:     "Prompt → A Priori Grid → Constrained AI Context"
    ],

    Rejection: [
      compiler: "Syntax error → compilation fails",
      tpmn:     "Ambiguity → TPMN(P) fails → AI never called"
    ]
  ],

  (* ═══ 4. DUAL-GATE ARCHITECTURE ═══ *)

  DualGate ≜ [
    (* Updated flow with R/G-Noumena split *)
    flow: "R-Noumena (DISMISSED) → Prompt → TPMN_P → G-Noumena + A_Priori → AI → TPMN_O → Valid_Output",

    flow_detail: <<
      "R-Noumena: User's true intent — unknowable, DISMISSED",
      "Prompt: Representation of intent — what we receive",
      "TPMN_P: Validate → extract G-Noumena (CONTRACT) + A_Priori Grid",
      "G-Noumena: The immutable law OF GEM² universe",
      "A_Priori: Pure (TPMN rules P0-P5) + Synthetic (GEM-KG)",
      "AI: Generate within INTERPOLATION_DOMAIN",
      "TPMN_O: Verify against O1-O6 (including SPT)",
      "Valid_Output: Phenomena that satisfies G-Noumena"
    >>,

    separation: [
      tagline: "Legislator at prompt-intake, Judge at output-validation",
      TPMN_P:  "The Legislator — extracts G-Noumena + validates A_Priori (P0-P5)",
      TPMN_O:  "The Judge — verifies output against law (O1-O6, including SPT)"
    ]
  ],

  (* 4.1 TPMN(P) — Prompt Validator / The Legislator *)
  TPMN_P ≜ [
    role:   "Static analysis of prompt — compile-time checking",
    input:  "Raw User Prompt",
    output: "G-Noumena (validated CONTRACT) + A Priori Grid OR rejection",

    kantian_analog: "Transcendental Aesthetic — forms of intuition",

    checks: [

      (* P0: G-Noumena Clarity — ensures CONTRACT is extractable *)
      (* NOTE: P0_Check vs P₀_Vision disambiguation:                    *)
      (*   P₀_Vision = [why, what, where] — human vision container      *)
      (*   P0_Check  = This TPMN_P rule — validates extractability      *)
      (*   Relation: P0_Check verifies P₀_Vision yields clear G-Noumena *)
      P0_G_Noumena_Clarity ≜ [
        rule:    "Prompt must define clear CONTRACT (G-Noumena)",
        check:   "∃ Cell_TLA structure: A → B | P extractable from prompt",
        example: "Reject vague intent ('make it better'). Accept formal contract.",
        purpose: "Ensure G-Noumena is knowable before execution",
        note:    "R-Noumena (user's true intent) is DISMISSED — only G-Noumena matters"
      ],

      P1_Metric_Binding ≜ [
        rule:    "∀ adjective ∈ Prompt: Has_Explicit_Metric(adjective)",
        example: "Reject 'fast code'. Accept 'code running < 10ms'",
        purpose: "Eliminate ambiguous quality terms"
      ],

      P2_Negative_Constraint ≜ [
        rule:    "∃ constraint ∈ Prompt: defines_forbidden_case",
        example: "DO NOT use eval(). DO NOT return null.",
        purpose: "Spec is not rigid unless it defines what is forbidden"
      ],

      P3_Entity_Typing ≜ [
        rule:    "Key nouns must be typed/structured",
        example: "User ≜ [id: UUID, name: String] vs ambiguous 'User'",
        purpose: "Prevent AI from conflating object with reference",

        (* P3 Subrules — NounConstraint Refinement v1.6.2 *)
        subrules: [
          P3a_IdentityConstraint ≜ [
            rule:    "∀ entity_ref: Has_Stable_Identifier(entity_ref)",
            check:   "Same label must refer to same entity throughout",
            example: "'User' in line 5 = 'User' in line 20 (no identity drift)"
          ],
          P3b_ConceptConstraint ≜ [
            rule:    "∀ entity_ref: Has_TypeOrClass(entity_ref)",
            check:   "Declared type remains invariant across scope",
            spt:     "Guards ¬L→G (prevents type drift from local to global)",
            example: "User: Person — cannot later treat User as Organization"
          ],
          P3c_PointerConstraint ≜ [
            rule:    "∀ pointer_ref: Has_Anchor(pointer_ref)",
            check:   "References (pronouns, 'it', 'this') must resolve to defined entity",
            example: "'it' must anchor to specific entity, not float ambiguously"
          ],
          P3d_SchemaConstraint ≜ [
            rule:    "∀ dependent_noun: Has_Schema_Definition(dependent_noun)",
            check:   "Incomplete nouns (의존명사) must have schema declared BEFORE use",
            example: "'the result' requires: result ≜ [status: Bool, value: Int]",
            note:    "Compile-time obligation — forces completion pre-execution"
          ]
        ]
      ],

      P4_Output_Schema ≜ [
        rule:    "Shape of desired response explicitly defined",
        example: "Output: JSON with fields {status, data, error}",
        purpose: "A Priori grid must be shaped before content poured in"
      ],

      P5_Context_Isolation ≜ [
        rule:    "External dependencies (files, libs) explicitly listed",
        example: "Available: Python 3.11, pandas, numpy. NO network access.",
        purpose: "Prevent AI from assuming tools it doesn't have"
      ]
    ],

    failure_action: "Return to User: 'Ambiguity detected. Define [Term].'"
  ],

  (* 4.2 TPMN(O) — Output Validator / The Judge *)
  TPMN_O ≜ [
    role:   "Runtime verification of AI output",
    input:  "AI Output + A Priori Grid from TPMN(P)",
    output: "PASS (deliver to user) OR FAIL (retry loop)",

    kantian_analog: "Transcendental Analytic — application of categories",

    checks: [

      O1_Schema_Match ≜ [
        rule:    "Output.structure == P4_Output_Schema",
        example: "Expected JSON with 3 fields, got plain text → FAIL",
        purpose: "Structural compliance"
      ],

      O2_Constraint_Satisfaction ≜ [
        rule:    "∀ constraint ∈ P2: Output ⊨ constraint",
        example: "P2 said 'no eval()'. Output contains eval() → FAIL",
        purpose: "Semantic compliance with forbidden cases"
      ],

      O3_Symbol_Grounding ≜ [
        rule:    "∀ new_term ∈ Output: (new_term ∈ Prompt) ∨ (new_term ∈ Library)",
        example: "AI invents variable 'x' not in prompt or stdlib → FAIL",
        purpose: "Hallucination detection"
      ],

      (* O3x: NounConstraint Verification — corresponds to P3a-P3d *)
      O3a_Identity_Consistency ≜ [
        rule:    "¬∃e: SameLabel(e) ∧ DifferentEntity(e)",
        example: "'User' refers to different things in output → FAIL",
        purpose: "Identity drift prohibition",
        maps_to: "P3a_IdentityConstraint"
      ],

      O3b_Concept_Stability ≜ [
        rule:    "DeclaredType(e) remains invariant across output scope",
        example: "User declared as Person, later treated as Org → FAIL",
        purpose: "Type drift prevention",
        spt:     "Guards ¬L→G",
        maps_to: "P3b_ConceptConstraint"
      ],

      O3c_Pointer_Resolution ≜ [
        rule:    "∀ pointer: Resolved(pointer) ∨ Explicitly_UNC(pointer)",
        example: "'it' used without clear referent → FAIL (unless marked UNC)",
        purpose: "Reference anchoring verification",
        maps_to: "P3c_PointerConstraint"
      ],

      O4_Internal_Consistency ≜ [
        rule:    "∄ contradiction: (Statement_A ∧ Statement_B) → False",
        example: "Output says 'x > 5' and 'x < 3' → FAIL",
        purpose: "Logic consistency"
      ],

      O5_EEF_Verification ≜ [
        rule:    "If Output.content is EXTRAPOLATION: EEF_Flag == True",
        example: "AI guessed without marking uncertainty → FAIL",
        purpose: "Epistemic honesty — AI must admit when guessing"
      ],

      (* O6: SPT Compliance — prevents illicit categorical leaps *)
      O6_SPT_Compliance ≜ [
        rule:    "¬S→T(Output) ∧ ¬L→G(Output) ∧ ¬Δe→∫de(Output)",
        checks:  <<
          "S→T: No treating mutable STATE as immutable TRAIT",
          "L→G: No extending local observation to universal claim",
          "Δe→∫de: No expanding small evidence (< 3) to large conclusion"
        >>,
        example: "Claims 'always works' from 2 tests → FAIL (Δe→∫de violation)",
        purpose: "Prevent illicit categorical leaps (Transcendental Dialectic)"
      ]
    ],

    failure_action: "Auto-feed error to AI: 'Violation of [Ox]. Retry.'"
  ],

  (* ═══ 5. THE COMPILER PIPELINE ═══ *)

  (* Core Claim: An LLM becomes a compiler UNDER TPMN RULES *)
  (* TPMN_P = frontend (prompt-intake), LLM = codegen, TPMN_O = verifier (output-validation) *)

  CompilerPipeline ≜ [

    traditional: <<
      "Source Code",
      "→ Lexer (tokenize)",
      "→ Parser (AST)",
      "→ Semantic Analyzer (type check)",
      "→ IR (intermediate representation)",
      "→ Code Generator",
      "→ Executable"
    >>,

    tpmn: <<
      "User Prompt (Source)",
      "→ P3: Entity Extraction (Lexer)",
      "→ P4: Schema Validation (Parser)",
      "→ P1,P2: Constraint Binding (Semantic Analyzer)",
      "→ A Priori Grid (IR)",
      "→ LLM Inference (Code Generator)",
      "→ TPMN(O): Output Verification",
      "→ Valid Output (Executable)"
    >>
  ],

  (* ═══ 5.1 PIPELINE_for_TPMN_check (Epistemic Extension) ═══ *)
  (* DualGate stays canonical; PIPELINE refines compile/verify into 3 epistemic lenses *)

  PIPELINE_for_TPMN_check ≜ [

    Principle ≜ [
      claim:         "DualGate stays canonical; PIPELINE refines the compile/verify narrative into 3 epistemic lenses",
      compatibility: "TPMN_P and TPMN_O unchanged; PIPELINE is an explanatory decomposition"
    ],

    (* ═══ TERM DEFINITIONS (Self-Contained) ═══ *)
    Terms ≜ [
      Prompt_p ≜ [what: "Raw user prompt (NL input)", role: "Source"],
      Pc_Executable ≜ [
        what: "Executable prompt-contract record for LLM",
        form: "[Prompt + extracted CONTRACT + A_Priori_Grid + Diagnostics + LoopPolicy]",
        note: "Executable-for-LLM-under-TPMN rules, not machine-run program"
      ],
      ConfidenceScore ≜ [
        what:  "Scalar diagnostic from TPMN_P about prompt well-formedness",
        range: "implementation-defined (abstract in epistemology)"
      ],
      Oc ≜ [
        what: "ObjectConstraint — typed entity commitments",
        schema: [Entities, Anchors, Obligations, Invariants: ⟨"identity stable", "concept stable"⟩]
      ],
      Pp ≜ [
        what: "Proposition (Picture) that mirrors Oc's structure",
        schema: [Names, Relations, Constraints, Falsifiers, EvidenceReq]
      ],
      LoopPolicy ≜ [
        what: "Bounded retry/ask loop control",
        controlled_by: "BridgeOperator_GACC",
        fields: [max_rounds, cost_budget, uncertainty_budget]
      ]
    ],

    (* ═══ EPISTEMIC GATES ═══ *)
    KCR ≜ [
      name:    "Kantian Critique of Reason (epistemic gate)",
      input:   "Prompt_p",
      output:  "[Pc_Executable, Diagnostics]",
      logic:   "p → Pc | P5_Context_Isolation",
      purpose: "Verify at inference-boundary; classify interpolation vs extrapolation; require UNC when needed"
    ],

    FNC ≜ [
      name:     "Four-Noun Constraining (object boundary gate)",
      input:    "Pc_Executable",
      output:   "Oc",
      logic:    "Extract nouns/objects → enforce P3 typing + P3a..P3d stability",
      binds_to: "P3a, P3b, P3c, P3d"
    ],

    WSP ≜ [
      name:    "Wittgensteinian Picturing (logical-form gate)",
      input:   "Pc_Executable",
      output:  "Pp",
      purpose: "Represent 'WHAT should be HOW' as proposition with shared logical form; enable feasibility/falsifiability checks"
    ],

    LogicalForm_Epistemic ≜ [
      what: "Rule family requiring propositions to be expressible as logical forms with explicit falsifiers",
      note: "Epistemology describes WHY; operational decidability belongs to spec (binds to P6 when spec defines it)"
    ],

    DecisionFn ≜ [
      what:    "Deterministic selection of pipeline mode and next action",
      output:  "{PASS, ASK_HUMAN, RETRY_AI, TERMINATE}",
      inputs:  ⟨"ConfidenceScore", "EEF", "SPT_Risk", "CostBudget", "MaxRounds"⟩,
      RETRY_AI: "Re-run LLM with same Pc, no human input"
    ],

    (* ═══ PIPELINE MODES ═══ *)
    PipelineModes ≜ [
      BASIC ≜ [
        flow:           "p → KCR(p)",
        output:         "Pc",
        pass_condition: "DecisionFn(...) = PASS"
      ],
      OPTIONAL ≜ [
        left:  [flow: "p → KCR(p) → FNC(Pc)", output: "Pc + Oc"],
        right: [flow: "p → KCR(p) → WSP(Pc)", output: "Pc + Pp"],
        constraint: "If KCR fails → DecisionFn(...) = ASK_HUMAN ∨ TERMINATE"
      ],
      FULL ≜ [
        flow:       "p → KCR(p) → FNC(Pc) → WSP(Pc)",
        output:     "Pc + Oc + Pp",
        constraint: "DecisionFn enforces LoopPolicy bounds (GACC)"
      ]
    ],

    (* ═══ WITTGENSTEIN INTEGRATION ═══ *)
    WittgensteinIntegration ≜ [
      idea: "A proposition pictures a possible state-of-affairs via shared logical form",
      tpmn_mapping: [
        picture_form: "Pp.Names + Pp.Relations mirror Oc.Entities + Oc.Anchors",
        meaning:      "Meaning = conditions of satisfaction + falsifiers (phenomena testable)",
        guardrail:    "No L→G: proposition speaks only within declared model/contract scope"
      ]
    ],

    (* ═══ FEASIBILITY AND FALSIFIABILITY ═══ *)
    Feasibility_Falsifiability ≜ [
      feasibility ≜ [
        rule:     "If Pp requires undefined tools/contradictory constraints → mark UNC and ASK_HUMAN",
        binds_to: "P5 context isolation + O4 internal consistency"
      ],
      falsifiability ≜ [
        rule: "Every critical claim in Pc should admit at least one falsifier in Pp.Falsifiers",
        note: "If none exists → claim is non-testable within phenomena; mark UNC"
      ]
    ],

    (* ═══ LOOP SEMANTICS ═══ *)
    LoopSemantics ≜ [
      repeat: "ASK_HUMAN produces clarified prompt p'; rerun BASIC/OPTIONAL/FULL",
      stop:   "TERMINATE when LoopPolicy budget exhausted or contradictions persist"
    ]

  ],

  (* ═══ 6. GACC AS TRANSCENDENTAL UNITY ═══ *)

  GACC_Epistemology ≜ [
    kant:   "Transcendental Unity of Apperception — the 'I think' that accompanies all representations",
    gem2:   "GACC — the coordinator that validates all T_AI outputs",
    bridge: "Both provide the unifying condition for validity"
  ],

  (* ═══ 7. EEF AS CRITIQUE OF PURE REASON ═══ *)

  EEF_Epistemology ≜ [
    kant:     "Reason falls into antinomies when exceeding experience",
    tpmn:     "AI falls into hallucination when exceeding evidence",
    solution: "EEF flags EXTRAPOLATION — the boundary of valid inference",

    (* EEF vs TPMN_check: ORTHOGONAL mechanisms, not containment *)
    mechanism: [
      EEF:        "Message-instant — embedded in GEM2_MSG.metadata (self-assessment)",
      TPMN_check: "Task-discrete — compute_work in workflow (formal validation)",
      relation:   "EEF ∥ TPMN_check (orthogonal, different granularity)"
    ],

    mapping: [
      GND: "Grounded — stay within experiential bounds",
      EXT: "Externalized — make reasoning visible (Aufklärung)",
      UNC: "Uncertainty — acknowledge limits of knowledge",
      SPT: "SPT — avoid illicit categorical leaps"
    ]
  ],

  (* ═══ 8. SPT AS TRANSCENDENTAL DIALECTIC ═══ *)

  SPT_Epistemology ≜ [
    kant: "Transcendental Dialectic warns against illicit inferences",
    tpmn: "SPT warns against S→T, L→G, Δe→∫de",

    mapping: [
      "S→T":    "Don't treat contingent STATE as necessary TRAIT",
      "L→G":    "Don't extend local observation to universal claim",
      "Δe→∫de": "Don't expand small evidence to large conclusion"
    ],

    shared_principle: "Define what reasoning MUST NOT do"
  ],

  (* ═══ 9. THE THREE CRITIQUES OF GEM² ═══ *)

  ThreeCritiques ≜ [
    Critique_of_Pure_Reason: [
      kant: "What can we know?",
      gem2: "TPMN_check — What can AI validly produce?"
    ],

    Critique_of_Practical_Reason: [
      kant: "What should we do?",
      gem2: "SPT / EEF — What should AI do? (ethics of inference)"
    ],

    Critique_of_Judgment: [
      kant: "How do we judge completion/beauty?",
      gem2: "Ω_accept — When is the work 'complete'? (teleology)"
    ]
  ],

  (* ═══ 10. FROM MAGIC TO ENGINEERING ═══ *)

  Transformation ≜ [

    before: [
      process:  "Prompt → AI → Hope",
      nature:   "MAGIC — incantation with uncertain results",
      success:  "Depends on practitioner intuition",
      failure:  "Unexplainable — 'AI hallucinated'"
    ],

    after: [
      process:  "Prompt → TPMN(P) → AI → TPMN(O) → Trust",
      nature:   "ENGINEERING — formal process with guarantees",
      success:  "Depends on constraint satisfaction",
      failure:  "Explainable — 'Violated O2: constraint X'"
    ],

    key_insight: "The A Priori Grid is the missing 'compiler' for AI interaction"
  ],

  (* ═══ 11. IMPLICATIONS ═══ *)

  Implications ≜ [
    I1: "Formal justification for why TPMN works",
    I2: "Principled extension: any new check must be A Priori",
    I3: "Clear failure semantics: violation = categorical error",
    I4: "Philosophical grounding for AI alignment via structure",
    I5: "Teachable framework: engineers can learn rules, not craft"
  ],

  (* ═══ 12. PRACTICAL GUIDANCE ═══ *)

  PracticalGuidance ≜ [

    WhenToUse ≜ [
      use: <<
        "High-stakes specs (compliance, safety)",
        "Multi-agent coordination",
        "Long/complex prompts",
        "Ambiguous domains",
        "Hallucination risk is costly"
      >>,
      skip: <<
        "Casual chat",
        "Low-cost errors acceptable",
        "Exploratory brainstorming"
      >>
    ],

    Pros ≜ <<
      "Higher repeatability (platform benefit under fixed Spec/IR)",
      "Auditability",
      "Fewer hallucinations",
      "Clearer contracts",
      "Better multi-step reliability"
    >>,

    Cons ≜ <<
      "Upfront overhead",
      "Requires primitives/library",
      "Can over-constrain creativity (mitigable)",
      "Needs evidence/metrics discipline",
      "Tooling complexity",
      "False-negative risk",
      "Maintenance burden",
      "Learning curve"
    >>,

    (* MetaPattern: sufficient mitigation for all cons *)
    MetaPattern ≜ [
      "Gradual adoption":  "Start small, add rigor as needed",
      "Sensible defaults": "Works out-of-box, customize later",
      "Escape hatches":    "Override/bypass with justification",
      "Automation":        "Tooling reduces manual burden"
    ],

    CoreTakeaways ≜ <<
      "Separate WHY (epistemology) from WHAT (primitives)",
      "Bind informal symbols to spec predicates",
      "Enforce SPT + EEF",
      "Treat failures as repair loops with bounded retries",
      "PIPELINE: Prefer BASIC; escalate to FULL only when AmbiguityThreshold triggers"
    >>

  ]

]

(* ═══ SUMMARY TABLE ═══ *)

EpistemologyMapping ≜ [
  (* Noumena Split *)
  R_Noumena:     "Thing-in-itself (Real) — DISMISSED, unknowable",
  G_Noumena:     "Thing-in-itself (GEM²) — CONTRACT, the law of GEM² universe",

  (* A_Priori Split *)
  Pure_A_Priori:      "TPMN rules (P0-P5, O1-O6) — truly innate",
  Synthetic_A_Priori: "GEM-KG — accumulated, acts as pre-existing",

  (* TPMN Mechanisms *)
  TPMN_check:    "Synthetic A Priori Judgments — TASK (compute_work)",
  TPMN_P:        "Transcendental Aesthetic (pre-conditions) — P0-P5",
  TPMN_O:        "Transcendental Analytic (category application) — O1-O6",

  (* Coordination and Ethics *)
  GACC:          "Transcendental Unity of Apperception",
  EEF:           "Critique of Pure Reason (limits) — MESSAGE-INSTANT (∥ TPMN_check)",
  SPT:           "Transcendental Dialectic (forbidden inferences) — O6",

  (* Combined Grid *)
  A_Priori_Grid: "The Categories (P0-P5 ∪ O1-O6)"
]

(* ═══ PIPELINE GLOSSARY (v1.6.3) ═══ *)
PIPELINE_Glossary ≜ [
  Pc_Executable:        "Executable prompt-contract for LLM [Prompt + CONTRACT + A_Priori_Grid + Diagnostics + LoopPolicy]",
  KCR:                  "Kantian Critique of Reason — epistemic gate (p → Pc)",
  FNC:                  "Four-Noun Constraining — object boundary gate (Pc → Oc)",
  WSP:                  "Wittgensteinian Picturing — logical-form gate (Pc → Pp)",
  Oc:                   "ObjectConstraint — typed entity commitments + anchors + obligations",
  Pp:                   "Proposition (Picture) — names, relations, constraints, falsifiers, evidence requirements",
  LogicalForm_Epistemic:"Rule family for expressible logical forms (binds to P6 in spec)",
  DecisionFn:           "Policy decision → {PASS, ASK_HUMAN, RETRY_AI, TERMINATE}",
  LoopPolicy:           "Bounded retry control [max_rounds, cost_budget, uncertainty_budget]",
  BridgeOperator_GACC:  "Governor enforcing loop/cost policies — unifying validity condition"
]

(* ═══ T_AI SOP ALIGNMENT ═══ *)
T_AI_SOP ≜ <<
  "1. Receive Input (Prompt)",
  "2. Compile (TPMN_P): P0 checks G-Noumena clarity, P1-P5 validate constraints",
  "3. Generate: AI produces draft within INTERPOLATION_DOMAIN",
  "4. Verify (TPMN_O): O1-O5 + O6 (SPT/EEF rules)",
  "5. Deliver: Output Verification Block with Object-Content"
>>

(* Note: EEF ∥ TPMN_check — orthogonal mechanisms at different granularity *)
(* EEF: self-assessment embedded in every GEM2_MSG (instant)              *)
(* TPMN_check: formal validation as workflow task (discrete)               *)

===
```

---

**v1.6.3 | GEM² TPMN Epistemology | Companion to GEM2-spec-v1.5.8 | 2026-01-23**
