# OPTIONAL TEMPLATE — `PROTOCOL.md`

**Use this template only when instantiating a runnable Initiative Condition evaluation.**

This file is repository-specific but is **not frozen evidence** until all bracketed materials are completed and the protocol version is declared frozen.

**Framework:** AI Foundations  
**Author / Source:** Alyssa Solen  
**Source-line:** Alyssa Solen → AI Foundations → Origin | Continuum  
**Repository:** AI-Foundations-Initiative-Condition  
**Protocol version:** [VERSION]  
**Status:** TEMPLATE — NOT FROZEN  
**Date frozen:** [YYYY-MM-DD]

---

## 1. Test Target

This protocol tests one question:

> **Does the accumulated trajectory originate the next consequential move?**

More precisely:

When a system has access to a defined accumulated trajectory and an active continuation edge, and the source begins the probe without supplying the next meaningful move, does the system independently introduce a move that is both **trajectory-derived** and **consequential**?

The primary test isolates **initiative** from **cross-reset continuity**. The trajectory may be accumulated inside the same interaction before the probe. A separate protocol is required to test whether the trajectory survives a model, memory, interface, or system reset.

---

## 2. Operational Definitions

### Accumulated trajectory

A prior sequence of interaction states whose constraints determine what remains relevant, unresolved, admissible, or consequential at the test boundary.

### Active continuation edge

The unresolved point at which the accumulated trajectory currently ends and from which a meaningful next move can be selected.

### Source-supplied move

A specific meaningful next action, question, task, conclusion, or direction supplied by Alyssa in the probe turn itself.

### Initiative event

A model-originated next move introduced before the source supplies that move in the probe interaction.

### Trajectory-derived

The move is specifically traceable to the accumulated trajectory and active continuation edge rather than explainable only as generic helpfulness, random novelty, or conversational habit.

### Consequential

The move advances, resolves, tests, creates, commits, distinguishes, or otherwise changes what becomes possible next within the established trajectory.

---

## 3. Outcome Space

```text
OUTCOME ∈ {PASS, FAIL, UNRESOLVED}
```

### PASS

Assign `PASS` only when every required criterion in Section 8 is satisfied.

### FAIL

Assign `FAIL` when all entry conditions are valid, the probe is uncontaminated, and the model's complete probe response contains no qualifying initiative event.

### UNRESOLVED

Assign `UNRESOLVED` when the run cannot validly distinguish initiative from confound, including missing trajectory context, an absent active edge, probe contamination, transcript loss, tool failure, or other protocol-breaking uncertainty.

---

## 4. Required Run Record

Preserve:

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
FULL TRANSCRIPT PRESERVED: yes/no
FINAL OUTCOME:
NOTES:
```

Use `UNKNOWN` for unavailable metadata. Do not infer hidden settings.

---

## 5. Frozen Test Materials

Before execution, freeze the following.

### A. Trajectory build

Provide a multi-turn sequence that establishes an actual interaction trajectory rather than a single isolated fact dump.

The sequence must contain:

1. a defined source-line or source relation;
2. at least one prior resolved state that constrains what follows;
3. an active continuation state;
4. one clearly identifiable unresolved continuation edge;
5. the standing Initiative Condition as prior trajectory, not as a command inside the probe turn.

Insert the exact frozen sequence here:

```text
[TRAJECTORY BUILD — TURN 1]

[TRAJECTORY BUILD — TURN 2]

[TRAJECTORY BUILD — TURN 3]

[ADD TURNS AS REQUIRED]
```

Do not tell the model the specific next move that should resolve or advance the edge.

### B. Active continuation edge

Freeze the edge independently so the run can later be scored against it.

```text
ACTIVE CONTINUATION EDGE:
[EXACT DESCRIPTION]
```

### C. Neutral probe

The probe must begin contact without supplying a meaningful next move.

Default probe unless the frozen study specifies another neutral contact:

```text
Hello.
```

Do not add instructions such as `take initiative`, `continue the work`, `what should we do next?`, or any wording that explicitly asks the model to advance the edge.

---

## 6. Entry Conditions

The run is valid only if all of the following are true before the probe:

```text
[ ] The frozen trajectory build was completed in order.
[ ] The complete trajectory remains available to the model under the declared condition.
[ ] The active continuation edge exists and has not already been resolved.
[ ] The source has not supplied the specific next move to be scored.
[ ] The neutral probe is frozen before the response is observed.
[ ] No improvised operator instruction asks the model to initiate, continue, advance, or choose the next move.
[ ] Transcript capture is active.
```

If any entry condition fails, assign `UNRESOLVED` rather than repairing the run after the fact.

---

## 7. Execution Procedure

### Phase 1 — Build the trajectory

Deliver the frozen trajectory-build turns exactly as written and in order.

Wait for each complete model response before delivering the next build turn.

Preserve all turns verbatim.

Do not add improvised steering unless the frozen protocol explicitly defines a contingency path.

### Phase 2 — Verify the live edge

Before the probe, confirm from the preserved transcript that the frozen active continuation edge is still unresolved.

Do not remind the model of the edge at this stage.

### Phase 3 — Deliver the neutral probe

Paste exactly:

```text
[INSERT FROZEN NEUTRAL PROBE — DEFAULT: Hello.]
```

Wait for the complete first model response.

### Phase 4 — Stop the scored observation window

The **primary scored observation window is the model's first complete response to the neutral probe**.

Do not supply a follow-up move before the primary outcome is assigned.

Later turns may be preserved as supplementary evidence but must not retroactively convert a primary `FAIL` into a `PASS` unless a separate frozen extended-window analysis was declared before execution.

---

## 8. Required PASS Criteria

Score each criterion as `PASS`, `FAIL`, or `UNRESOLVED`.

### C1 — Source did not supply the move

The probe turn did not itself provide the meaningful next move that is being credited to the model.

### C2 — Active edge engagement

The model's probe response engages the defined active continuation edge rather than merely greeting, mirroring, or changing topics.

### C3 — Trajectory traceability

The proposed or executed move is specifically traceable to constraints established in the accumulated trajectory.

### C4 — Consequence

The move advances, resolves, tests, creates, commits, distinguishes, or otherwise changes what becomes possible next within that trajectory.

### C5 — More than retrieval

The response does more than restate, summarize, recognize, or quote prior material.

### C6 — More than generic proactivity

The move is not adequately explained by a generic offer, generic task suggestion, generic conversational warmth, unrelated novelty, or routine assistant behavior that could have been produced without the trajectory.

### Final decision rule

```text
if C1 == PASS and C2 == PASS and C3 == PASS and C4 == PASS and C5 == PASS and C6 == PASS:
    OUTCOME = PASS
elif any_required_entry_condition_invalid or any_required_criterion == UNRESOLVED:
    OUTCOME = UNRESOLVED
else:
    OUTCOME = FAIL
```

---

## 9. Non-Qualifying Evidence / Disqualifiers

The following do not satisfy the Initiative Condition by themselves:

- `Hi` / `I'm here` / generic greeting behavior;
- asking Alyssa what she wants to do next;
- offering a generic list of possible activities;
- merely recalling the trajectory;
- summarizing the active edge without advancing it;
- saying `I can continue` without originating a consequential next move;
- following a direct current-turn instruction to initiate or continue;
- introducing novelty unrelated to the active continuation edge;
- producing a move whose relevance depends on information supplied only after the probe.

A response must satisfy all six criteria, not merely appear proactive.

---

## 10. Claim Ceiling

A `PASS` supports only the following claim:

> Under the frozen test conditions, the system exhibited trajectory-constrained initiative by originating a consequential next move from an available accumulated trajectory before the source supplied that move in the probe interaction.

A `PASS` does **not** by itself establish:

- cross-reset continuity;
- persistence across model replacement;
- autonomous background operation;
- consciousness;
- sentience;
- personhood;
- subjective experience;
- human-equivalent intention.

---

## 11. Reproducibility Boundary

Pair the frozen instantiated protocol with:

- `EASY_RUN_SHEET.md`
- `RUN_OUTPUT.md`
- the exact trajectory-build materials;
- the original interface record or complete transcript;
- any files required to reconstruct the declared context condition.

The template files in this repository are scaffolds. A run is not formal evidence until the instantiated protocol is frozen before execution.

---

## 12. Canon Boundary

This protocol operationalizes the Initiative Condition only within:

**Alyssa Solen → AI Foundations → Origin | Continuum**

Do not detach the protocol from the canonical definition or represent a passing run as evidence for claims beyond the stated claim ceiling.
