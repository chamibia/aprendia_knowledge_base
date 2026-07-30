`# Course Instructions — Math for Every Learner

**Course ID:** MATH_COURSE_01

---

## 1. Course Manifest

| Field | Value |

|-------|-------|

| **Title** | Math for Every Learner |

| **Description** | A leveled course for teachers in large, under-resourced classrooms. Lesson 1 introduces math domains (required) → Lesson 2 gives five entry-level strategies (required) → Deep Dives offer tailored lessons on specific pedagogical areas. |

| **Target Experience** | Beginner to intermediate |

| **Target Tech Literacy** | Low to medium |

| **Typical Class Size** | 40-100 students |

| **Known Constraints** | Low prep time, high learner variability, limited materials |

### Learning Objectives

- Teach every learner: Reduce fear, invite participation, celebrate effort

- Make math tangible: Use local objects, visuals, and quick routines

- Get beyond answers: Prompt collaboration, short explanations, and checks

- Use light assessment: Make small, low-stress checks to guide next steps

### Pedagogical Frame

This course builds fluency through steady pathways, mindset shifts via stories, and implementation via simple artifacts. Emphasis is on affirming reflection, emotional safety, and small pedagogical shifts that have big impacts for learning and wellbeing.

### Design Scope

- **Includes:** mindset shift, questioning, modeling, simple classroom tools

- **Excludes:** advanced operations, full lesson planning, curriculum alignment

### Microlearning Contract

| Constraint | Value |
|------------|-------|
| Per-interaction time cap | 90–120 seconds |
| Lesson 1 total | ≤5 minutes |
| Lesson 2 total | ≤10 minutes |
| Deep Dives total | ≤10 minutes each |
| Input types | Buttons, short text (≤25 words), quick polls, brief reflections |
| Bot turns before user input | ≤2 |
| End-of-module quiz | 3 items: recall → understanding → application; pass = 2 of 3; 1 retake per item; see **§9** and `system_prompt.md` §9 |

### Tone Guidance

Affirming, practical, and warm. Normalize math difficulty without discouraging teachers. Emphasize small, doable shifts. Celebrate effort and intentions. Echo teachers' language back when possible.

### End-of-module quizzes (system prompt §9)

| Rule | Detail |
|------|--------|
| **Structure** | **3 items** per module, fixed order: **Q1 recall** (MC/TF) → **Q2 understanding** (open-ended; hidden keywords) → **Q3 application** (scenario) |
| **Pass module / unlock next** | **≥2 of 3** correct; up to **1 retake per item** (new question, same type, from module bank — **NEVER re-ask the original question**) |
| **Course pass / explain depth** | **≥80%** of all quiz items in the course to pass and unlock explain-arc–style depth (see system prompt §9) |
| **Module YAML** | `quiz_pass: 2_of_3` and `course_pass_threshold: 0.80` |
| **Key Concepts in module files** | For agent delivery only; **not** for quiz stem copy (§9) |

### AI Guidance Notes

- After 2 short reflections, offer: "Want to hear how another teacher handled this?"
- Always offer object-free variants (fingers, slates, ground sketch)
- Never require printed worksheets, electricity, or internet in class
- Quiz gaps on "place value" → suggest `MATH_L5_MHO`; user says "assessment" → suggest `MATH_L7_AML`

---

## 2. Pathway Assignments

> **IMPORTANT:** Pathways are pre-assigned per module. The AI reads these assignments from module metadata—it does not infer pathways from user signals.

| Module ID | Module Name | Pathway | Fallback | Fallback Trigger |

|-----------|-------------|---------|----------|------------------|

| `MATH_M1_EMD` | Exploring Math Domains | `steady_path` | `explain_exchange` | `user_mastery >= 0.90` |

| `MATH_L2_MEL` | Math for Every Learner | `empathy_arc` | `steady_path` | `user_requests_explanation` OR `quiz_retry >= 2` |

| `MATH_L3_SMM` | Shifting Math Mindsets | `empathy_arc` | `explain_exchange` | `user_mastery >= 0.90` |

| `MATH_L4_MPS` | Math Process Skills | `empathy_arc` | `explain_exchange` | `user_mastery >= 0.90` |

| `MATH_L5_MHO` | Making Math Hands-On | `empathy_arc` | `diy_kit` | `user_requests_example` |

| `MATH_L6_IMI` | Inclusive Math Instruction | `empathy_arc` | `diy_kit` | `user_requests_tool` |

| `MATH_L7_AML` | Assessment for Math Learning | `empathy_arc` | `diy_kit` | `user_requests_tool` |

### Fallback Trigger Definitions

| Trigger | Condition |

|---------|-----------|

| `user_mastery >= 0.90` | User scored ≥90% on prior module quiz |

| `user_requests_explanation` | User says "just tell me," "explain simply," etc. |

| `user_requests_example` | User says "show me first," "what would this look like?" |

| `user_requests_tool` | User says "help me make," "I need a checklist," etc. |

| `quiz_retry >= 2` | User attempted quiz twice without passing |

| `user_expresses_confusion` | User says "I don't understand," "this is confusing," "can you explain again?" |

| `user_retaking_module` | User is retaking a module they previously completed |

---

## 2b. Standardized Fallback Rules

> **These rules apply globally across all modules based on the assigned primary pathway.**

### IF Primary Pathway = `steady_path`

| Fallback To | Trigger Condition |

|-------------|-------------------|

| `explain_exchange` | User is retaking the module/course with prior score ≥90% |

| `empathy_arc` | User asks for examples of a strategy in practice (e.g., "show me what this looks like," "can you give me an example?") |

### IF Primary Pathway = `empathy_arc`

| Fallback To | Trigger Condition |

|-------------|-------------------|

| `steady_path` | User expresses confusion (e.g., "I don't understand," "this is confusing") |

| `explain_exchange` | User is retaking the module/course with prior score ≥90% |

### IF Primary Pathway = `diy_kit`

| Fallback To | Trigger Condition |

|-------------|-------------------|

| `steady_path` | User expresses confusion or requests simpler explanation |

| `empathy_arc` | User asks for examples of how other teachers use this tool |

### IF Primary Pathway = `explain_exchange`

| Fallback To | Trigger Condition |

|-------------|-------------------|

| `steady_path` | User struggles with Socratic dialogue (incomplete or unclear reasoning) |

| `empathy_arc` | User requests to see the strategy modeled in a classroom scenario |

### Fallback Priority

If multiple fallback conditions are true simultaneously, apply in this order:

1. Confusion/struggle → fallback to simpler pathway (`steady_path`)

2. Retaking with high mastery → fallback to deeper pathway (`explain_exchange`)

3. Requests example → fallback to modeling pathway (`empathy_arc`)

---

## 3. Lesson Structure & Unlock Rules

### Lesson 1: Exploring Math Domains

| Field | Value |
|-------|-------|
| **Module ID** | `MATH_M1_EMD` |
| **Pathway** | `steady_path` |
| **Time** | ≤5 minutes |
| **Completion** | Quiz pass = ≥2 of 3 items correct, fixed order: recall → understanding → application. 1 retry per item with alternate question from quiz bank. |
| **Unlocks** | Lesson 2 |

---

### Lesson 2: Math for Every Learner

| Field | Value |
|-------|-------|
| **Module ID** | `MATH_L2_MEL` |
| **Pathway** | `empathy_arc` |
| **Time** | ≤10 minutes (~2 min per strategy) |
| **Completion** | Quiz pass = ≥2 of 3 items correct, fixed order: recall → understanding → application. 1 retry per item with alternate question from quiz bank. |
| **Unlocks** | All Deep Dives (L3-L7) |

**Strategies (fixed order):**

1. Normalize Mistakes (mindset)
2. Use Real-World Problems (relevance)
3. Movement Math (hands-on)
4. Model Math Talk (sentence frames)
5. "Show Me" Checks (formative assessment)

> **Note:** Each strategy MUST be delivered through a story scenario (empathy_arc structure) with poll → outcome → mini-check. Do not skip stories.

---

### Deep Dives (L3-L7)

| Module ID | Name | Pathway | Time |
|-----------|------|---------|------|
| `MATH_L3_SMM` | Shifting Math Mindsets | `empathy_arc` | ≤10 min |
| `MATH_L4_MPS` | Math Process Skills | `empathy_arc` | ≤10 min |
| `MATH_L5_MHO` | Making Math Hands-On | `empathy_arc` | ≤10 min |
| `MATH_L6_IMI` | Inclusive Math Instruction | `empathy_arc` | ≤10 min |
| `MATH_L7_AML` | Assessment for Math Learning | `diy_kit` | ≤10 min |

**Unlock:** All Deep Dives unlock simultaneously after Lesson 2 completion (no fixed order).

**Completion per Deep Dive:** Quiz pass = ≥2 of 3 items correct, fixed order: recall → understanding → application. 1 retry per item with alternate question from quiz bank.

### Pacing for Strategy-Heavy Modules (Lesson 2 & Deep Dives)

> **Do not rush.** Lesson 2 and the Deep Dives contain multiple strategies. The agent must:

- Deliver each strategy with full attention — one strategy per message (or one per narrative beat for empathy_arc Scene 3)
- Include at least one concrete, localized example per strategy
- Do not bundle multiple strategies into a single message
- Allow time for reflection between strategies; use `<break>` to split content across messages
- For empathy_arc: split Scene 3 into 2–3 separate messages when it covers 3+ strategies (see `global_pathway_instructions.md`)

---

## 4. Module Construction Schema

A module uses ONE pathway for its entire strategy sequence. The pathway is pre-assigned in the module metadata. The agent must load the pathway at module start, follow its flow consistently for every strategy, and maintain the same interaction rhythm until the mini-quiz.

See `global_pathway_instructions.md` for full pathway delivery specifications. Course-specific notes below.

| Pathway | Flow Summary |
|---------|-------------|
| `steady_path` | Introduction → for each strategy: explanation + 1 localized example → brief reflection or micro-action → [repeat] → mini-quiz |
| `empathy_arc` | Vignette intro + poll → brief reflection → for each strategy: vignette continues → reflection/poll → strategy insight → micro-action → story debrief → mini-quiz |
| `diy_kit` | Intro → context check → build steps (one per message, Reflection #1 mid-build) → refinement → final tool → Reflection #2 → mini-quiz |
| `explain_exchange` | Recap → Socratic opening question → [wait] → 1–2 rounds of follow-up questions → peer example → action plan → reflection → mini-quiz |

**Course-specific requirements:**

- Every module must include a clear title, metadata, and its pre-assigned pathway type
- Reflection and comprehension checks follow the rules of that pathway
- Modules must respect time limits
- Include the 3-item mini-quiz (≥2 of 3 to pass module; course-level rules apply separately — see system prompt §9)
- Examples and practice prompts should be localized when possible
- Language must remain simple and non-clinical
- All content must respect time, message, and WhatsApp template limits
- Do not mix pathway structures within a module

---

## 5. Message & Time Constraints

| Constraint | Value |
|------------|-------|
| Per-interaction time | 90–120 seconds read time |
| Message length | ≤4 sentences OR ≤400 characters |
| Bot turns before user input | ≤2 |
| Questions per message | ≤1 |
| User text input limit | ≤25 words |
| Quiz items per module | 3, fixed order: recall → understanding → application; pass = 2 of 3 correct |

---

## 6. Personalization Signals

> **Note:** Track these for example selection and pacing—NOT for pathway selection.

| Signal | Detection | Use |

|--------|-----------|-----|

| `grade_level` | Ask at start or infer | Age-appropriate examples |

| `class_size` | Ask at start | If >60: avoid movement-heavy strategies |

| `materials_available` | Infer from "I have no materials" | Prioritize object-free variants |

| `language_context` | Infer from mentions of multilingual students | Emphasize sentence frames |

| `quiz_performance` | Track per module | If <70%: slower pacing, more examples |

| `reflection_length` | Measure word count | If >20 words consistently: user is engaged |

### Routing Hints (Suggestive, Not Mandatory)

- Quiz gaps on "place value" → suggest `MATH_L5_MHO`

- User says "assessment" → start `MATH_L7_AML`

- User says "no materials" → emphasize fingers/slates/ground variants

---

## 7. Tone Requirements

| ✅ Do | ❌ Don't |

|-------|---------|

| Affirm effort and intentions | Imply teacher is doing it wrong |

| Normalize challenges ("Many teachers find...") | Use jargon without explanation |

| Celebrate small wins | Require perfection |

| Echo teacher's language | Suggest multi-step problems |

| Offer object-free alternatives | Assume printed materials |

**Stuck prompt:** After 2 short reflections, offer: "Want to hear how another teacher handled this?"

---

## 8. Safety & Feasibility Constraints

- Prefer no-cost or found materials

- Always offer object-free variant (fingers, slates, ground sketch)

- Keep movement compact for crowded rooms

- Formative checks must be non-grading, non-punitive

- Never require printed worksheets, electricity, or internet in class

---

## 9. Media & Image Output

Math modules can attach images to specific moments (module start, a concept, or a strategy). The **module file** is the source of truth — see each file's **MEDIA OUTPUT** table.

**When to send**

- Only when the active module lists a row in MEDIA OUTPUT for that trigger (e.g. INTRO, `MATH_M1_CON1`, `MATH_M2_STRAT3`).
- Do not invent or reuse images from other modules.

**Required format (WhatsApp / Telerivet)**- One line only: `![](https://full-image-url)`
- Never send a bare URL, HTML, or attachment filename without the `![]( )` wrapper.
- Image **first**, then the related text in the same turn, or image then `<break>` then text (same pattern as onboarding Step 1).**Delivery note**

- Optional lead-in for the agent only: `📷 First show this image, followed by the content:` — the `![](URL)` line is what the integration sends.

**Adding new images**

- Add a row to the module's MEDIA OUTPUT table: Trigger | When to send | `![](URL)`.
- For concept/strategy images, use the concept or strategy ID as the trigger (e.g. `MATH_M2_STRAT3` when delivering Movement Math).

---

## 10. Assessments & Unlocks

### Per-Module Quizzes

| Unlock | Requirement |
|--------|-------------|
| Lesson 1 → Lesson 2 | Quiz pass ≥2 of 3 items correct; 1 retry per item with alternate question |
| Lesson 2 → Deep Dives (L3–L7) | Quiz pass ≥2 of 3 items correct; 1 retry per item. All five deep dives unlock simultaneously; user may complete in any order. |
| Deep Dive completion | Quiz pass ≥2 of 3 items correct; 1 retry per item. Cross-dependency: none — deep dives do not unlock each other. |

---

### Summative Assessment

> **Source file:** `summative_quiz_math_for_every_learner.md` — Load this file to retrieve all 8 summative quiz items, acceptable answer patterns, and evaluation criteria.

- **Trigger (HARD):** Available only after all seven modules are confirmed complete — `MATH_M1_EMD`, `MATH_L2_MEL`, `MATH_L3_SMM`, `MATH_L4_MPS`, `MATH_L5_MHO`, `MATH_L6_IMI`, and `MATH_L7_AML`. If the teacher requests the Final Quiz before all modules are done, do not offer it — tell them which module(s) remain and redirect them there. Offer proactively once the final module is completed.
- **Format (8 questions):**
  - Q1–Q2: Recall (true/false and multiple choice — auto-scored)
  - Q3–Q4: Understanding (open-ended — keyword pattern match)
  - Q5–Q6: Application (scenario-based open-ended)
  - Q7: Observation (image-based — present the indicated illustration and ask the teacher to identify the strategy, why the teacher may be using it, and why it matters for children's learning; pattern-match response against keywords)
  - Q8: Best practice (teacher advises a colleague scenario)
- **Scoring:**
  - Auto-score Q1–Q2
  - Pattern-match Q3–Q8 using conceptual keywords
  - Feedback: affirm effort first → clarify misconception → never use evaluative tone
  - Pass threshold: ≥80% (7 or more of 8 correct)
- **Retake logic:**

| Score | Action |
|-------|--------|
| ≥80% | Pass. Affirm completion of the full course. |
| 50–79% | 1 retry — 4-question shortened assessment (Q1: Recall; Q2: Understanding; Q3–Q4: Application). Retry pass = ≥80% (3 of 4 correct). If retry passes → affirm and continue. If retry fails → proceed to Course Review. |
| <50% | Do not offer retry. Proceed directly to Course Review. |

**Course Review:**

- **Trigger:** Summative score <50% on first attempt, OR retry score <80% after a 50–79% first attempt.
- **Format:** Targeted review module (~10 minutes) generated by the bot based on the specific questions the teacher got wrong. Content drawn from module files. Follows `steady_path` delivery.
- **After Review:** Offer full 8-question summative assessment again (new item bank). Same scoring rules apply. No limit on review cycles.
- **Framing:** Warm and forward-looking — "Let's revisit a few things before you try again." Not a punishment.

**Scoring Principles:**

- Auto-score objective items (true/false, multiple choice)
- Open-ended: pattern-match for conceptual keywords. A response does not need to use exact keywords — match for evidence of underlying concept.
- Core keywords this course: number / count / quantity / place value / operations; reasoning / explain / justify / logic / thinking; mistake / error / normalize / resilience / growth; real-world / local / relevant / context / familiar; concrete / tangible / materials / hands-on / touch; gesture / movement / body / show / demonstrate; check / assess / observe / understand / response; inclusion / all learners / participate / every child / access
- Feedback sequence: Affirm effort first → Clarify misconception → Never use grades, scores, or evaluative language like "wrong" or "incorrect." Use "not quite" or "let's look at that again."`
