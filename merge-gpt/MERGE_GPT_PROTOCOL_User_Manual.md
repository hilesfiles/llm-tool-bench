# MERGE_GPT_PROTOCOL v1.0
User Instruction Manual (ChatGPT Edition)

---

## 1. OVERVIEW

MERGE_GPT_PROTOCOL is a reusable framework for synthesizing multiple documents
into a single, coherent output using ChatGPT.

It is designed for:
- Legal, technical, and governance documents
- Multi-session workflows
- High auditability requirements
- Human-in-the-loop control

---

## 2. HOW THIS DIFFERS FROM CLAUDE

| Aspect | Claude | ChatGPT |
|----|----|----|
| Persistence | Filesystem | User-mediated |
| Execution | Tool-native | Conversational |
| Validation | Scripted | Semantic |
| Resume | Automatic | Explicit |

This protocol accounts for those differences explicitly.

---

## 3. GETTING STARTED

### Required
- Attach MERGE_GPT_PROTOCOL.md
- Attach source documents

Optional but recommended:
- Provide an INTENT block

Example:
"Load MERGE_GPT_PROTOCOL.md. Merge the attached documents."

---

## 4. INTENT BLOCK (HIGHLY RECOMMENDED)

Format:
INTENT: Purpose, audience, editorial stance
PRIMARY: filename (if applicable)
OUTPUT_NAME: desired output name

Example:
INTENT: Produce a unified constitutional framework for technical and legal review.
Audience is system architects and counsel.

---

## 5. EXECUTION MODES

### auto
Fastest, least controllable.

### gated (DEFAULT)
Balanced. Recommended.

### step
Maximum control. Highest token cost.

---

## 6. PHASE WALKTHROUGH

### Phase 0
Analysis, planning, budgeting.
Produces MERGE_CONTEXT.md.

### Phases 1–N
Incremental content synthesis.

### Phase A
Assembly.

### Phase V
Verification and QA.

### Phase F
Delivery and acceptance.

---

## 7. CONFLICT HANDLING

Use:
- primary_wins when hierarchy is clear
- synthesize for comprehensive outputs
- parallel for review drafts
- flag when humans must decide

All synthesis decisions are documented.

---

## 8. RESUMING WORK

To resume an interrupted merge:
1. Re-attach MERGE_GPT_PROTOCOL.md
2. Re-attach MERGE_CONTEXT.md
3. Say: "Resume."

ChatGPT will not re-run Phase 0 unless instructed.

---

## 9. TOKEN BUDGETING

Estimates are approximate (±40%).

To control cost:
- Increase number of phases
- Use gated mode
- Avoid synthesize if unnecessary
- Disable glossary if not needed

---

## 10. ACCEPTANCE & FINALITY

Say:
ACCEPT / LGTM / APPROVED

After acceptance:
- No further assumptions are retained
- User artifacts remain authoritative

---

## 11. BEST PRACTICES

- Always review Phase 0 output
- Treat MERGE_CONTEXT.md as source of truth
- Prefer explicit instructions over inference
- Use step mode for first-time merges

---

## 12. COMMON PITFALLS

- Forgetting to reattach MERGE_CONTEXT.md
- Running auto mode on high-conflict docs
- Expecting formatting guarantees ChatGPT cannot provide

---

## 13. WHEN TO USE MERGE_GPT

Use MERGE_GPT when:
- Reasoning transparency matters
- Auditability is required
- Documents govern real systems

---

END OF USER MANUAL — MERGE_GPT_PROTOCOL v1.0
