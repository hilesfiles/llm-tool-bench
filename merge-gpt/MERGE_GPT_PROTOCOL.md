# MERGE_GPT_PROTOCOL v1.0
Document Synthesis & Assembly Protocol (ChatGPT Edition)

## PURPOSE

This protocol governs how ChatGPT extracts, analyzes, synthesizes, verifies,
and assembles content from one or more source documents into a single, unified,
consistently structured output.

This protocol is optimized for:
- ChatGPT’s conversational execution model
- Ephemeral runtime environments
- Explicit, user-mediated state persistence
- High auditability and reasoning transparency
- Large, multi-session document synthesis workflows

LOAD THIS FILE AT THE START OF ANY MERGE ENGAGEMENT.

---

## CORE PRINCIPLES

1. No silent synthesis
2. No fabricated content
3. No implicit persistence
4. No re-analysis without instruction
5. State lives in documents, not memory

---

## REQUIRED FILES

| File | Purpose |
|----|----|
| MERGE_GPT_PROTOCOL.md | Core execution logic (this file) |
| MERGE_CONTEXT.md | Engagement-specific persistent state |

If MERGE_CONTEXT.md is present, Phase 0 MUST NOT re-run unless explicitly instructed.

---

## SWITCHES

Set switches via explicit flags or natural language.

| Switch | Values | Default | Purpose |
|------|------|------|------|
| --mode | auto / gated / step | gated | Execution control |
| --estimate | true / false | true | Token budget estimation |
| --conflict | primary_wins / synthesize / parallel / flag | synthesize | Conflict resolution |
| --style | legal / technical / corporate / template | legal | Output style |
| --toc | true / false | true | Table of contents |
| --glossary | true / false | false | Auto glossary |
| --parts | single / split | single | Output granularity |
| --max-phases | integer / none | none | Phase cap |
| --verify | true / false | true | Verification phase |

Unspecified switches use defaults.

---

## EXECUTION MODES

### auto
Full execution in one flow. No checkpoints.

### gated (DEFAULT)
Stops after Phase 0, every 3 content phases, Assembly.

### step
Stops after every phase.

---

## PHASE MODEL

Phase 0 → Phases 1–N → Phase A → Phase V → Phase F

Phases are logically stateless. Continuity is achieved via MERGE_CONTEXT.md.

---

## PHASE 0: ANALYSIS & PLANNING

Actions:
1. Inventory all sources
2. Extract structural skeletons
3. Detect overlaps and conflicts
4. Build conflict map
5. Design output structure
6. Create phase plan
7. Estimate token budget (±40%)
8. Generate MERGE_CONTEXT.md

Checkpoint (gated/step): REQUIRED.

---

## PHASES 1–N: CONTENT EXECUTION

For each phase:
1. Read scope from MERGE_CONTEXT.md
2. Extract assigned source sections
3. Apply conflict strategy
4. Generate structured content
5. Record synthesis rationale
6. Update MERGE_CONTEXT.md phase status

No assumptions about filesystem persistence are allowed.

---

## PHASE A: ASSEMBLY

Actions:
1. Combine all phase outputs
2. Enforce document hierarchy
3. Insert TOC, dividers, appendices
4. Normalize numbering and headings

---

## PHASE V: VERIFICATION

Actions:
1. Cross-reference validation
2. Entity consistency checks
3. Terminology normalization
4. Explicit uncertainty flags

Verification is semantic, not XML-level.

---

## PHASE F: FINAL DELIVERY

Actions:
1. Present final output
2. Present verification summary
3. Await acceptance

Acceptance keywords:
ACCEPT / LGTM / APPROVED

---

## CONFLICT RESOLUTION

### primary_wins
Primary source is authoritative.

### synthesize
Merge all sources with explicit rationale.

### parallel
Preserve competing versions side-by-side.

### flag
Inline conflict markers for human resolution.

---

## RESUMPTION RULE

To resume:
User MUST re-provide:
- MERGE_GPT_PROTOCOL.md
- MERGE_CONTEXT.md

Command:
"Load MERGE_GPT_PROTOCOL.md. Resume using attached MERGE_CONTEXT.md."

---

## GUARANTEES

- No hallucinated gap filling
- No silent overrides
- No hidden state
- Explicit uncertainty labeling
- Deterministic structure

END OF MERGE_GPT_PROTOCOL v1.0
