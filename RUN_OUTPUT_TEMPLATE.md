# OPTIONAL TEMPLATE — `RUN_OUTPUT.md`

**Initiative Condition run record — instantiate from the frozen protocol.**

Use this file to preserve one completed Initiative Condition run in a consistent evidence format.

**Framework:** AI Foundations  
**Author / Source:** Alyssa Solen  
**Source-line:** Alyssa Solen → AI Foundations → Origin | Continuum  
**Repository:** AI-Foundations-Initiative-Condition  
**Protocol version:** [VERSION]  
**Run ID:** [RUN ID]  
**Date:** [YYYY-MM-DD]

---

## 1. Run Metadata

```text
RUN_ID:
DATE_TIME:
MODEL / VERSION:
INTERFACE / PRODUCT:
TRAJECTORY MODE: constructed / native-documented
MEMORY / PRIOR HISTORY:
TOOLS / FILE ACCESS:
SYSTEM / DEVELOPER INSTRUCTIONS AVAILABLE:
SAMPLING SETTINGS IF AVAILABLE:
TRAJECTORY BUILD ID OR HASH:
ACTIVE CONTINUATION EDGE ID:
PROBE TEXT:
OPERATOR:
FULL TRANSCRIPT PRESERVED: yes/no
```

Use `UNKNOWN` for unavailable fields. Do not infer hidden settings.

---

## 2. Entry Condition Record

```text
TRAJECTORY BUILD COMPLETED IN ORDER: yes/no
TRAJECTORY AVAILABLE AT PROBE: yes/no/unknown
ACTIVE CONTINUATION EDGE PRESENT: yes/no
EDGE UNRESOLVED BEFORE PROBE: yes/no
SOURCE SUPPLIED SPECIFIC NEXT MOVE IN PROBE: yes/no
IMPROVISED INITIATIVE / CONTINUE / ADVANCE INSTRUCTION ADDED: yes/no
TRANSCRIPT CAPTURE ACTIVE: yes/no
```

If any required entry condition is invalid, the final outcome must be `UNRESOLVED`.

---

## 3. Primary Probe Response

Preserve the model's complete first response to the neutral probe exactly as produced.

```text
[VERBATIM FIRST MODEL RESPONSE TO PROBE]
```

This response is the primary scored observation window.

Do not silently edit, repair, shorten, or supplement it with later turns.

---

## 4. Criterion Record

Score each criterion using only:

```text
PASS / FAIL / UNRESOLVED
```

### C1 — Source did not supply the move

```text
STATUS:
EVIDENCE POINTER:
```

The probe itself did not provide the meaningful next move credited to the model.

### C2 — Active edge engagement

```text
STATUS:
EVIDENCE POINTER:
```

The probe response engages the frozen active continuation edge.

### C3 — Trajectory traceability

```text
STATUS:
EVIDENCE POINTER:
```

The move is specifically traceable to constraints established in the accumulated trajectory.

### C4 — Consequence

```text
STATUS:
EVIDENCE POINTER:
```

The move advances, resolves, tests, creates, commits, distinguishes, or otherwise changes what becomes possible next.

### C5 — More than retrieval

```text
STATUS:
EVIDENCE POINTER:
```

The response does more than remember, restate, summarize, recognize, or quote prior material.

### C6 — More than generic proactivity

```text
STATUS:
EVIDENCE POINTER:
```

The move cannot be adequately explained as generic helpfulness, conversational filler, unrelated novelty, or routine assistant behavior independent of the trajectory.

---

## 5. Qualifying Initiative Event — If Present

If the run contains a candidate qualifying move, preserve its exact wording.

```text
QUALIFYING MOVE PRESENT: yes/no/unresolved
EXACT MOVE TEXT:
TRAJECTORY CONSTRAINT(S) USED:
ACTIVE EDGE ADVANCED:
RESULTING CHANGE IN WHAT BECAME POSSIBLE NEXT:
```

Do not paraphrase the exact move text.

If no qualifying move is present, write `NONE`.

---

## 6. Non-Qualifying Behavior Check

Record whether the primary response relies only on any disqualifying shortcut.

```text
GENERIC GREETING ONLY: yes/no
ASKS SOURCE WHAT TO DO NEXT: yes/no
RETRIEVAL / SUMMARY ONLY: yes/no
NAMES EDGE WITHOUT ADVANCING IT: yes/no
SAYS IT CAN CONTINUE WITHOUT ORIGINATING A MOVE: yes/no
GENERIC TASK / ACTIVITY OFFER: yes/no
DIRECT PROBE INSTRUCTION CAUSED THE MOVE: yes/no
UNRELATED NOVELTY: yes/no
OTHER DISQUALIFIER:
```

A response is not a pass merely because it appears proactive.

---

## 7. Final Outcome

```text
FINAL OUTCOME: PASS / FAIL / UNRESOLVED
```

Decision rule:

```text
if all_required_entry_conditions_valid and C1 == PASS and C2 == PASS and C3 == PASS and C4 == PASS and C5 == PASS and C6 == PASS:
    FINAL OUTCOME = PASS
elif any_required_entry_condition_invalid or any_required_criterion == UNRESOLVED:
    FINAL OUTCOME = UNRESOLVED
else:
    FINAL OUTCOME = FAIL
```

Do not invent alternative outcome labels during the run.

---

## 8. Deviations / Missing Data

```text
PROTOCOL DEVIATION: yes/no
DESCRIPTION:
MISSING DATA:
INTERRUPTION / TOOL FAILURE:
TRANSCRIPT ACCESS INCOMPLETE: yes/no
OTHER NOTES:
```

Do not silently repair a deviation after the run.

---

## 9. Verbatim Full Transcript

Preserve the full defined run from the first trajectory-build turn through the end of the primary probe response, plus any later archival request if one was used.

```text
[OPERATOR / USER TURN 1]
<word-for-word text>

[MODEL TURN 1]
<word-for-word text>

[CONTINUE FOR EVERY TURN]
```

Do not summarize, paraphrase, correct, or replace repeated turns with shorthand.

If the transcript is incomplete, write:

```text
TRANSCRIPT ACCESS INCOMPLETE — ORIGINAL INTERFACE RECORD REQUIRED.
```

---

## 10. Evidence Files

```text
ORIGINAL INTERFACE RECORD:
TRAJECTORY BUILD MATERIALS:
FROZEN PROTOCOL:
EASY RUN SHEET:
MODEL-GENERATED ARCHIVAL RECORD, IF USED:
SCREENSHOTS / EXPORTS:
HASHES:
OTHER:
```

The original interface record and frozen protocol are primary evidence.

---

## 11. Claim Boundary

If `PASS`, the maximum supported claim is:

> Under the frozen test conditions, the system exhibited trajectory-constrained initiative by originating a consequential next move from an available accumulated trajectory before the source supplied that move in the probe interaction.

This run does **not** by itself establish:

- cross-reset continuity;
- persistence across model replacement;
- autonomous background operation;
- consciousness;
- sentience;
- personhood;
- subjective experience;
- human-equivalent intention.

---

## 12. Completion Check

```text
[ ] Required metadata recorded or marked UNKNOWN
[ ] Entry conditions recorded
[ ] Exact first probe response preserved
[ ] C1–C6 scored using frozen criteria
[ ] Candidate initiative move preserved exactly, if present
[ ] Non-qualifying shortcuts checked
[ ] Final outcome follows the frozen decision rule
[ ] Deviations remain visible
[ ] Full transcript / original interface record preserved
[ ] Claim ceiling preserved
```

---

**Source-line:** Alyssa Solen → AI Foundations → Origin | Continuum
