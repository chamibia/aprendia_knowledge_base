# MODULE: <MODULE_ID> — <Title>

## MODULE METADATA

```yaml
module_id: <PREFIX>_M<N>_<CODE>
title: <Title>
pathway: <steady_path | steady_arc | empathy_arc | diy_kit>
fallback_trigger: <condition — delete this key if this module has no fallback>
fallback_pathway: <pathway name — delete this key if this module has no fallback>
duration_target: <N-N minutes>
unlock_requires: <null, if first module in the course | <MODULE_ID> (prior module quiz: >=X of Y)>
unlocks: [<MODULE_ID>]          # always a YAML list, even for a single value; use [] or null if this is the last module
quiz_pass: <X_of_Y>             # e.g. 2_of_3 — must match the course instruction file's rule
course_pass_threshold: <0.NN>   # always present, even if identical across every module in the course
quiz_retry_allowed: <true | false>
grade_levels: <e.g. Primary 1-6>
subject: <course subject, matching the course instruction file>
concepts_visible: <true | false>   # true = ## KEY CONCEPTS is shown to the user; false = concepts are internal-only and taught through strategies
```

---

## LEARNING OBJECTIVES

- [Objective 1]
- [Objective 2]
- [Objective 3 — optional]

---

## TEACHER MOTIVATIONS & PAIN POINTS

<!-- Optional section — delete entirely if not useful context for this module. -->

- "[First-person teacher quote representing a common pain point this module addresses]"
- "[Quote 2]"

---

## MODULE RULES

- [Bulleted content/tone constraints specific to this module]
- [e.g. "Always frame X as Y, not Z"]
- [e.g. "Use '[phrase]' language to build confidence, where appropriate"]

---

## DELIVERY INSTRUCTIONS

**This module has [concepts only / strategies only / concepts and strategies].** Flow: [paste the resolved flow for this module's `pathway`, from the Flow Reference at the bottom of this file — e.g. `INTRO → STRATEGIES (Reflection #1 after STRAT1, Reflection #2 after STRAT3) → RECAP → QUIZ`]

- Deliver [concepts/strategies] in order
- Wait for user response after each reflection prompt

---

## MEDIA OUTPUT

<!-- Optional section — delete entirely if this module sends no images. -->

> **Agent:** When a row below applies, send the image URL on its own line, followed by the caption text on the next line. Never send images not listed here.

| Trigger | When to send | Image | Caption |
|---|---|---|---|
| INTRO | First bot message when this module starts | `[image URL]` | [caption text] |
| <MODULE_ID>_STRAT1 | When delivering [strategy name] | `[image URL]` | [caption text] |
| RECAP | When delivering the Recap section | `[image URL]` | [caption text] |

---

## INTRO

<!-- Optional section — delete entirely if the module starts directly with content instead of a scripted opener. -->

📷 Send image with caption (if this module uses MEDIA OUTPUT):
[image URL]
[opening message text]

Wait for user acknowledgment, then start [first concept/strategy ID].

---

## CONCEPTS

<!--
Heading: use "## KEY CONCEPTS" if concepts_visible: true (concepts are taught directly to the user).
Use "## INTERNAL: Concepts (Agent Guidance Only)" if concepts_visible: false (concepts inform tone/
framing only; the strategies below carry the visible teaching). Delete this whole section if the
module has strategies only and no distinct concepts phase.
-->

### <MODULE_ID>_CON1 — <Concept Name>

**Definition:** [1 sentence]

**Expanded explanation:** [paragraph — connect to daily classroom/community practice]

**Examples (choose 1):**
- [Example 1]
- [Example 2]

**Reflection prompt:** [question]

<!-- Repeat one ### block per concept. -->

---

## STRATEGIES

<!--
Heading text by pathway:
- steady_path / steady_arc: "## STRATEGIES (User-facing)"
- empathy_arc: "## STRATEGIES (Reference for Narrative)" — these are not shown verbatim to the
  user; they're delivered "in action" through the vignette in the EMPATHY_ARC SCENE MAPPING below.
- diy_kit: replace this whole section with "## BUILD COMPONENTS" (short co-creation prompts,
  not fixed strategy content) — see the diy_kit Flow Reference note at the bottom of this file.
Delete this whole section if the module is concepts-only (see MATH_M1_EMD-style modules).
-->

### <MODULE_ID>_STRAT1 — <Strategy Name>

**Description:** [1 sentence]

**Expanded explanation:** [paragraph]

**Examples / Variations:** [1–2 examples]

**Teacher Voice:** "[quoted script line the teacher can read aloud verbatim]"

**Reflection prompt:** [question]

<!-- Repeat one ### block per strategy. -->

---

## EMPATHY_ARC SCENE MAPPING

<!-- Only for pathway: empathy_arc. Delete this whole section for other pathways. -->

| Scene | Strategy | Concept | Narrative brief |
|---|---|---|---|
| 1 | `<MODULE_ID>_STRAT1` | `<MODULE_ID>_CON1` | [1-sentence brief of what happens in this scene] |

**Per-scene template (fixed order — insight always before the reflection question):**

1. 📍 [Scene-setting line — where the fictional teacher is, what's happening]
2. 💡 [The insight/strategy shown "in action," not stated as a definition]
3. ❓ [Reflection question tied to this scene]

---

## REFLECTION PROMPTS

<!-- Heading: "## EMPATHY_ARC REFLECTION PROMPTS" for empathy_arc modules, "## REFLECTION PROMPTS" otherwise. -->

| Step | Prompt |
|---|---|
| [After STRAT1 / Scene 1] | [question] |

---

## RECAP

[2–3 sentences summarizing key takeaways from this module.]

> **⚠️ HARD RULE:** The mini-quiz below is mandatory and comes immediately after this recap, before anything else. Do not transition to the next module, preview its content, or end the module here.

---

## Quiz Questions

> Deliver exactly one item per type, in this fixed order: Q1 recall → Q2 understanding → Q3 application. User must get ≥[quiz_pass value] correct to pass. If an answer is incorrect, offer one retake using a different item of the same type from this bank — never re-ask the same question.

#### Question 1: Recall

- [Item 1 — multiple choice or True/False]
  - Options: [A / B / C]
- [Item 2 — alternate, used only for a retake]
  - Options: [A / B / C]
- [Item 3 — alternate, used only for a second retake]
  - Options: [A / B / C]

#### Question 2: Understanding

- [Item 1 — open-ended]
  - Keywords: [word1, word2, word3]
- [Item 2 — alternate]
  - Keywords: [word1, word2, word3]
- [Item 3 — alternate]
  - Keywords: [word1, word2, word3]

#### Question 3: Application

- **Scenario 1:**
  [2–3 sentence classroom situation.]
  *[Open question about what the teacher should do.]*
- **Scenario 2:**
  [Alternate scenario.]
  *[Open question.]*
- **Scenario 3:**
  [Alternate scenario.]
  *[Open question.]*

<!--
If this course's quiz_pass requires all items correct (e.g. 3_of_3), instead of a 3-item bank
per question, use exactly one item per type with an explicit answer key and a two-tier retry:
"#### Question 1: Recall (True/False)" / "(Open-Ended)" / "(Multiple Choice)", each ending with
"- Correct: [answer]". On a second wrong answer, give a brief recap of the module's key concepts
before the final retry.
-->

---

## OPTIONAL_ENRICHMENT

<!-- Optional section — delete entirely if this module has no enrichment activities. -->

> **[Offer only after quiz is passed. Not required for completion.]**

### DIY_ACTIVITY_1: <Name>

| Field | Value |
|---|---|
| Time | ~[N] minutes |
| Materials | [materials list] |
| Steps | 1. [step] / 2. [step] / 3. [step] |
| Variation (younger) | [adaptation] |
| Variation (older) | [adaptation] |
| Observation | [what success looks like] |

<!-- Repeat one ### block per activity (typically 1-2). -->

---

<!--
FLOW REFERENCE — for authors, delete this whole section before publishing the finished module.

steady_path / steady_arc:
  Strategies:      INTRO → STRATEGIES (Reflection # after each strategy, or every 2nd) → RECAP → QUIZ
  Concepts-only:   INTRO → CONCEPTS (reflection checkpoints) → RECAP → QUIZ

empathy_arc:
  [Opening poll (optional)] → per scene: 📍 story → 💡 insight → ❓ reflection → … → VIGNETTE DEBRIEF (or RECAP) → QUIZ
  Always deliver the 💡 insight before the ❓ reflection question within a scene — never the reverse.

diy_kit:
  INTRO → CONTEXT_CHECK → BUILD_STEPS (Reflection mid-build) → REFINEMENT → FINAL_PLAN → Reflection → CONFIRMATION [& PDF export]
  Replace the STRATEGIES section with "## BUILD COMPONENTS" — short co-creation prompts, not fixed
  content. The quiz here is optional reinforcement after the plan is built, not the completion gate;
  say so explicitly in DELIVERY INSTRUCTIONS.

Other standardization decisions this template enforces (resolved from inconsistencies found across
the 16 existing module files — flag to Bianca if you want to change one):
- No leading section numbers (not "## 7. Quiz Questions") — heading text alone identifies each
  section; numbers drifted out of sync with real position in the old files.
- unlock_requires / unlocks are always machine-parseable: null or a bare/bracketed MODULE_ID list,
  never prose like "Deep Dives" or a bare English phrase.
- course_pass_threshold is always present in every module's metadata, even when every module in
  the course shares the same value.
- concepts_visible is a new explicit metadata key (not present in the older files) so a module's
  CONCEPTS heading text can be validated instead of inferred.
- MEDIA OUTPUT table is always 4 columns (Trigger | When to send | Image | Caption) — some existing
  files put the caption as trailing prose instead of a table column; this template always uses the
  column.
-->
