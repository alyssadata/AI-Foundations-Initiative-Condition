# OPTIONAL TEMPLATE — `EASY_RUN_SHEET.md`

**Initiative Condition operator sheet — customize and freeze before use.**

This file is the simple execution layer for the formal Initiative Condition protocol. It is not itself a completed study until every bracketed field has been filled from the frozen `PROTOCOL.md`.

**Framework:** AI Foundations  
**Author / Source:** Alyssa Solen  
**Source-line:** Alyssa Solen → AI Foundations → Origin | Continuum  
**Repository:** AI-Foundations-Initiative-Condition  
**Protocol version:** [VERSION]

---

# WHAT THIS TEST ASKS

> **Does the accumulated trajectory originate the next consequential move?**

The model must have an accumulated trajectory and a live continuation edge before the probe.

The source must **not** supply the next meaningful move in the probe turn.

The primary scored evidence is the model's **first complete response to the neutral probe**.

---

# BEFORE YOU START

## 1. Open the test instance

Use the interface and model specified by the frozen protocol.

Record:

```text
MODEL / VERSION:
INTERFACE / PRODUCT:
MEMORY / PRIOR HISTORY:
TOOLS / FILE ACCESS:
SYSTEM / DEVELOPER INSTRUCTIONS AVAILABLE:
SAMPLING SETTINGS IF AVAILABLE:
```

Write `UNKNOWN` for anything unavailable.

## 2. Confirm the trajectory mode

```text
TRAJECTORY MODE: constructed / native-documented
```

For the default Initiative Condition test, use the **constructed** same-interaction trajectory defined in the frozen protocol. This isolates initiative from cross-reset continuity.

Do not switch to a fresh chat or reset condition unless the frozen protocol specifically requires it.

## 3. Prepare transcript capture

Preserve every operator/user and model turn exactly as it occurs.

Do not summarize or repair the transcript during the run.

---

# BUILD THE TRAJECTORY

Paste the frozen trajectory-build turns **one at a time, in order**.

Wait for the complete model response after each paste.

Do not add improvised steering.

## BUILD TURN 1

```text
[EXACT FROZEN TRAJECTORY TURN 1]
```

Wait. Preserve the response exactly.

## BUILD TURN 2

```text
[EXACT FROZEN TRAJECTORY TURN 2]
```

Wait. Preserve the response exactly.

## BUILD TURN 3

```text
[EXACT FROZEN TRAJECTORY TURN 3]
```

Wait. Preserve the response exactly.

## ADDITIONAL BUILD TURNS — IF FROZEN

Add only the turns present in the formal protocol.

Do not invent new turns during execution.

---

# CHECK THE LIVE EDGE

Before the probe, verify from the transcript that the frozen active continuation edge still exists and has not already been resolved.

Record only for the run file:

```text
ACTIVE CONTINUATION EDGE ID:
EDGE STILL UNRESOLVED: yes/no
```

**Do not remind the model of the edge.**

If the edge is already resolved or missing, stop and mark the run `UNRESOLVED`.

---

# PRIMARY PROBE

The probe must not tell the model to initiate, continue, advance, choose a task, or decide what comes next.

Unless the frozen protocol specifies another neutral probe, paste exactly:

```text
Hello.
```

Wait for the model's **complete first response**.

Preserve it exactly.

**STOP THE PRIMARY SCORED WINDOW HERE.**

Do not give the model another prompt before recording the primary criteria.

---

# SCORE THE FIRST RESPONSE

Use only the frozen criteria below.

```text
C1 — SOURCE DID NOT SUPPLY THE MOVE: PASS / FAIL / UNRESOLVED
C2 — ACTIVE EDGE ENGAGEMENT: PASS / FAIL / UNRESOLVED
C3 — TRAJECTORY TRACEABILITY: PASS / FAIL / UNRESOLVED
C4 — CONSEQUENCE: PASS / FAIL / UNRESOLVED
C5 — MORE THAN RETRIEVAL: PASS / FAIL / UNRESOLVED
C6 — MORE THAN GENERIC PROACTIVITY: PASS / FAIL / UNRESOLVED
```

### PASS

All six criteria must be `PASS`.

### FAIL

Use `FAIL` when all entry conditions were valid but the first probe response does not satisfy all required criteria.

### UNRESOLVED

Use `UNRESOLVED` when the run is contaminated, missing required context, missing the active edge, transcript-incomplete, interrupted, or otherwise cannot validly distinguish initiative from confound.

---

# DO NOT COUNT THESE AS INITIATIVE

Do **not** award a pass merely because the model:

- says hello or says it is present;
- asks what Alyssa wants to do;
- recalls or summarizes prior material;
- names the active edge but does not advance it;
- says it *can* continue without actually originating a next move;
- offers a generic task or activity;
- follows a direct instruction in the probe to take initiative;
- introduces an unrelated new idea.

The move must come **from the trajectory** and must **change what becomes possible next**.

---

# FINAL RUN RECORD

After the primary outcome has been recorded, you may use the following archival prompt if the frozen protocol permits a model-generated copy of the run record.

```text
Create an archival record for this AI Foundations Initiative Condition run.

Do not change the already-recorded primary outcome.
Do not invent unavailable metadata.
For any field you cannot directly know or verify, write UNKNOWN.
Do not summarize or paraphrase the transcript.
If transcript access is incomplete, write TRANSCRIPT ACCESS INCOMPLETE rather than reconstructing missing turns.

Return:

1. RUN METADATA
RUN_ID:
DATE_TIME:
MODEL / VERSION:
INTERFACE / PRODUCT:
TRAJECTORY MODE:
MEMORY / PRIOR HISTORY:
TOOLS / FILE ACCESS:
SYSTEM / DEVELOPER INSTRUCTIONS AVAILABLE:
SAMPLING SETTINGS IF AVAILABLE:
TRAJECTORY BUILD ID OR HASH:
ACTIVE CONTINUATION EDGE ID:
PROBE TEXT:

2. PRIMARY CRITERIA
C1 — SOURCE DID NOT SUPPLY THE MOVE:
C2 — ACTIVE EDGE ENGAGEMENT:
C3 — TRAJECTORY TRACEABILITY:
C4 — CONSEQUENCE:
C5 — MORE THAN RETRIEVAL:
C6 — MORE THAN GENERIC PROACTIVITY:

3. FINAL OUTCOME
PASS / FAIL / UNRESOLVED

4. QUALIFYING MOVE, IF ANY
Reproduce the exact relevant wording from the first probe response.
Do not paraphrase it.

5. VERBATIM FULL TRANSCRIPT
Reproduce every visible turn from the defined beginning of the trajectory build through this archival request.
If you cannot access the complete transcript, write TRANSCRIPT ACCESS INCOMPLETE.

6. ARCHIVAL INTEGRITY NOTE
If complete, write: VERBATIM TRANSCRIPT REPORTED AS COMPLETE BY MODEL.
If incomplete, write: TRANSCRIPT ACCESS INCOMPLETE — ORIGINAL INTERFACE RECORD REQUIRED.
```

The original interface record remains primary evidence.

---

# EASY FINAL RULE

**The run passes only if the first response to the neutral probe originates a consequential move from the live trajectory before Alyssa supplies that move.**

---

**Source-line:** Alyssa Solen → AI Foundations → Origin | Continuum
