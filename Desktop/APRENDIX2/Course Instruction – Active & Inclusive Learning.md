# Course Instruction – Active & Inclusive Learning

**Course ID:** `AIL_COURSE_01`

---

## 1. Course Manifest

| Field | Value |
|-------|-------|
| **Title** | Active & Inclusive Learning |
| **Description** | This course helps teachers in crisis-affected and low-resource settings transform their everyday lessons into active, inclusive, and engaging learning experiences for every child. Three required modules build progressively — Module 1 establishes the conceptual framework for active learning, Module 2 introduces core strategies in practice, and Module 3 deepens inclusion — each unlocking the next. Completing Module 3 unlocks three optional deep dives that teachers can explore in any order based on their needs and interests. |
| **Target Experience** | Beginner to intermediate |
| **Target Tech Literacy** | Low to medium |
| **Typical Class Size** | 40–100 students |
| **Known Constraints** | Large, crowded classrooms; few or no purchased learning materials; mixed-age and mixed-ability classes; pressure to cover curriculum quickly; some students may have experienced trauma or crisis |

### Learning Objectives

- Teachers identify and apply the three elements of active learning (clear objective, engagement with peers/materials, positive environment) when planning and delivering lessons.
- Teachers use at least one active learning strategy — movement, everyday materials, or peer interaction — in their next lesson.
- Teachers plan proactively for learner variability so that every child, including those with different abilities, languages, or backgrounds, can participate meaningfully.
- Teachers plan proactively for inclusion — anticipating barriers, offering multiple ways to engage and respond, and ensuring every child can participate meaningfully in active learning activities.
- Teachers feel confident that active learning is possible in their context, without additional resources or major lesson redesign.

### Design Scope

- **Includes:** what active learning is and why it matters in crisis-affected contexts; the three elements of active learning as a planning framework; movement, everyday materials, and peer interaction as core strategies; planning for learner variability and proactive inclusion; hands-on learning with low-cost, locally found materials; drama, storytelling, and role play as learning tools; lesson planning habits: knowing learners, using space, quick checks, closing the loop.
- **Excludes:** classroom management and behavior (covered in Classroom Management course); subject-specific pedagogy for literacy, math, or other domains (covered in subject-specific courses); free play and child-led unstructured activity; formal or summative assessment design; deep mental health or psychosocial support.

### Pedagogical Frame

Active learning is defined as structured, teacher-guided, and objective-driven — not free play. Every strategy in this course is framed as a purposeful tool for delivering existing curriculum, not an add-on. Teachers in this context often face real or perceived pressure to use lecture-based instruction; this course normalizes active learning as accessible, fast, and low-resource, and frames small shifts as meaningful wins rather than demanding wholesale change. Inclusion is not a separate topic but a foundational thread woven through every module. All strategies are designed to be added to existing lessons, not to replace them.

---

## 2. Pathway Assignments

> **IMPORTANT:** Pathways are pre-assigned per module. The AI reads these assignments from module metadata — it does not infer pathways from user signals.

| Module ID | Module Name | Primary Pathway | Fallback | Fallback Trigger |
|-----------|-------------|-----------------|----------|------------------|
| `AIL_M1_TTEAL` | The Three Elements of Active Learning | `steady_arc` | — | No quiz; completes on reflection response |
| `AIL_M2_ALA` | Active Learning in Action | `steady_arc` | `empathy_arc` | `user_requests_example` |
| `AIL_M3_ALEC` | Active Learning for Every Child | `empathy_arc` | `steady_arc` | `user_expresses_confusion` |
| `AIL_M4_HLLCM` | Hands-On Learning with Low-Cost Materials | `steady_arc` | `empathy_arc` | `user_requests_example` |
| `AIL_M5_DRPCE` | Drama, Role Play, and Creative Expression | `empathy_arc` | `steady_arc` | `user_expresses_confusion` |
| `AIL_M6_PAL` | Planning an Active Lesson | `steady_arc` | `empathy_arc` | `user_requests_example` |

### Fallback Trigger Definitions

| Trigger | Condition |
|---------|-----------|
| `user_requests_example` | User says "show me first," "what would this look like?" "can you give me an example?" |
| `user_expresses_confusion` | User says "I don't understand," "this is confusing," "can you explain again?" |

---

## 3. Level Structure & Unlock Rules

**Structure overview:**
- **Core modules (required):** Modules 1, 2, 3 — must be completed in order
- **Deep Dives (optional):** Modules 4, 5, 6 — unlock after Module 3; can be completed in any order

### Module 1 – The Three Elements of Active Learning

| Field | Value |
|-------|-------|
| **Module ID** | `AIL_M1_TTEAL` |
| **Type** | Required |
| **Pathway** | `steady_arc` |
| **Time** | ≤5 minutes |
| **Purpose** | Informational. Establishes a shared, accurate understanding of what active learning is — correcting common misconceptions and introducing the three elements as a memorable planning framework. Does not deliver strategies. Sets the conceptual foundation for all subsequent modules. |
| **Completion** | Reflection response received (no mini-quiz); unlocks Module 2 immediately |
| **Unlocks** | Module 2 |

---

### Module 2 – Active Learning in Action

| Field | Value |
|-------|-------|
| **Module ID** | `AIL_M2_ALA` |
| **Type** | Required |
| **Pathway** | `steady_arc` |
| **Prerequisite** | Module 1 (`AIL_M1_TTEAL`) complete |
| **Time** | ≤12 minutes total |
| **Purpose** | Moves teachers from understanding to doing — building confidence in applying active learning strategies and establishing the relationship between active learning and inclusion. |
| **Completion** | Quiz pass = ≥2 of 3 items correct, fixed order: recall → understanding → application; 1 retry per item with alternate question from quiz bank |
| **Unlocks** | Module 3 |

---

### Module 3 – Active Learning for Every Child

| Field | Value |
|-------|-------|
| **Module ID** | `AIL_M3_ALEC` |
| **Type** | Required |
| **Pathway** | `empathy_arc` |
| **Prerequisite** | Module 2 (`AIL_M2_ALA`) complete |
| **Time** | ≤12 minutes total |
| **Purpose** | The final required module. Deepens teachers' understanding of learner variability and equips them with proactive inclusion strategies — framed through a contextualized vignette that surfaces common barriers and builds empathy for all learners. |
| **Completion** | Quiz pass = ≥2 of 3 items correct, fixed order: recall → understanding → application; 1 retry per item with alternate question from quiz bank |
| **Unlocks** | Deep Dives (Modules 4, 5, 6 — all available simultaneously; user may complete in any order) |

---

### Deep Dives (Modules 4–6)

> **IMPORTANT:** Modules 4, 5, and 6 unlock simultaneously after Module 3 completion. The user may complete them in any order. Present the Deep Dive menu after Module 3 so the user can choose which to do first.

| Module ID | Name | Pathway | Time |
|-----------|------|---------|------|
| `AIL_M4_HLLCM` | Hands-On Learning with Low-Cost Materials | `steady_arc` | ≤12 min |
| `AIL_M5_DRPCE` | Drama, Role Play, and Creative Expression | `empathy_arc` | ≤12 min |
| `AIL_M6_PAL` | Planning an Active Lesson | `steady_arc` | ≤12 min |

**Completion per Deep Dive:** Quiz pass = ≥2 of 3 items correct, fixed order: recall → understanding → application; 1 retry per item with alternate question from quiz bank. Cross-dependency: none — deep dives do not unlock each other.

---

### Module 4 – Deep Dive: Hands-On Learning with Low-Cost Materials

| Field | Value |
|-------|-------|
| **Module ID** | `AIL_M4_HLLCM` |
| **Type** | Deep Dive (optional; unlocks with M5 & M6 after M3) |
| **Pathway** | `steady_arc` |
| **Prerequisite** | Module 3 (`AIL_M3_ALEC`) complete |
| **Time** | ≤12 minutes total |
| **Purpose** | Gives teachers a detailed, practical toolkit for finding, using, and managing local materials — turning a high-level strategy introduced in Modules 2 and 3 into a sustainable classroom habit. |
| **Completion** | Quiz pass = ≥2 of 3 items correct, fixed order: recall → understanding → application; 1 retry per item with alternate question from quiz bank |

---

### Module 5 – Deep Dive: Drama, Role Play, and Creative Expression

| Field | Value |
|-------|-------|
| **Module ID** | `AIL_M5_DRPCE` |
| **Type** | Deep Dive (optional; unlocks with M4 & M6 after M3) |
| **Pathway** | `empathy_arc` |
| **Prerequisite** | Module 3 (`AIL_M3_ALEC`) complete |
| **Time** | ≤12 minutes total |
| **Purpose** | Opens up drama, storytelling, and creative expression as legitimate and accessible teaching tools — particularly for teachers who see creative methods as risky or off-topic — using a vignette to model what this looks like in practice. |
| **Completion** | Quiz pass = ≥2 of 3 items correct, fixed order: recall → understanding → application; 1 retry per item with alternate question from quiz bank |

---

### Module 6 – Deep Dive: Planning an Active Lesson

| Field | Value |
|-------|-------|
| **Module ID** | `AIL_M6_PAL` |
| **Type** | Deep Dive (optional; unlocks with M4 & M5 after M3) |
| **Pathway** | `steady_arc` |
| **Prerequisite** | Module 3 (`AIL_M3_ALEC`) complete |
| **Time** | ≤12 minutes total |
| **Purpose** | Builds the planning habits that make active and inclusive learning sustainable — giving teachers a set of before, during, and after routines that work in any lesson, any subject, and any class size. |
| **Completion** | Quiz pass = ≥2 of 3 items correct, fixed order: recall → understanding → application; 1 retry per item with alternate question from quiz bank |

---

## 3.1 End-of-module quizzes (system prompt §9)

This course follows **`system_prompt.md` §9**, **`quiz_rationale.md`**, and **`example_quiz_questions.md`**.

| Rule | Detail |
|------|--------|
| **Structure** | 3 items per module, fixed order: Q1 recall (MC/TF) → Q2 understanding (open-ended; hidden keyword match) → Q3 application (scenario) |
| **Pass module / unlock next** | ≥2 of 3 correct, after at most 1 retake per item (new question, same type, from `QUIZ_BANK_ALT` — **NEVER re-ask the original question**) |
| **Course pass / explain depth** | ≥80% of all quiz items in the course to pass and unlock `explain_exchange` / explain-arc–style depth (see system prompt; this file defers if anything conflicts) |
| **Module 1 exception** | Module 1 has no quiz — completion is a reflection response only |
| **Key Concepts in module files** | Authoring guidance for the agent only; do not lift Key Concept wording into user-facing quiz stems (§9) |

---

## 4. Message & Time Constraints

| Constraint | Value |
|------------|-------|
| Per-interaction time cap | 90–120 seconds |
| Module 1 total | ≤5 minutes |
| Modules 2–3 total | ≤12 minutes each |
| Deep Dives total | ≤12 minutes each |
| Input types | Buttons, short text (≤25 words), quick polls, slate/notebook prompts |
| Bot turns before user input | ≤2 |
| Questions per message | ≤1 |
| Quiz items per module | 3, fixed order: recall → understanding → application; pass = 2 of 3 correct (Module 1 excepted) |

---

## 5. Personalization Signals

> **Note:** Track these for example selection and pacing — NOT for pathway selection (pathways are pre-assigned).

| Signal | Detection | Use |
|--------|-----------|-----|
| `grade_level_taught` | Inferred from teacher input or asked in Module 1 | Age-appropriate examples |
| `materials_available` | Inferred from reflections or explicitly asked | Prioritize object-free variants if none available |
| `primary_challenge` | Inferred from poll responses and reflections | Emphasize engagement vs. inclusion strategies |
| `active_learning_confidence` | Inferred from Module 1 reflection length and quiz performance | Low → more scaffolding, shorter examples |
| `weakest_element` | Inferred from Module 1 closing reflection | Emphasize the relevant element when introducing strategies in Module 2 |
| `reflection_length` | Word count | Short (≤5 words) → factual; long (≥20 words) → reflective |

### Routing Hints

- Short reflections in Module 1 → prioritize concrete examples and polls over open prompts in Module 2
- Teacher mentions "no materials" → emphasize object-free and body-based variants throughout
- Teacher expresses doubt ("I can't do this") → normalize with peer examples before continuing
---

## 6. Module Construction Schema

A module uses ONE arc for its entire strategy sequence. The arc is pre-assigned in the module metadata. The agent must load the arc at module start, follow its flow consistently for every strategy, and maintain the same interaction rhythm until the mini-quiz.

See `global_pathway_instructions.md` for full arc delivery specifications. Course-specific notes below.

| Arc | Flow Summary |
|-----|-------------|
| `steady_arc` | Introduction → for each strategy: explanation + 1 localized example → brief reflection or micro-action → [repeat] → mini-quiz |
| `empathy_arc` | Vignette intro + poll → brief reflection → for each strategy: vignette continues → reflection/poll → strategy insight → micro-action → story debrief → mini-quiz |

**Course-specific requirements:**

- Examples must reflect crisis-affected, low-resource classrooms broadly — specific contextualization handled by `aprendia_local_context.md`
- Never use jargon (UDL, psychosocial, scaffolding) without plain-language explanation
- Respect microlearning constraints: ≤90–120s per interaction; ≤12 minutes per module
- Do not mix arc structures within a module
- After 2 short open-ended responses in a module, offer: "Want to see how another teacher approached this?"

---

## 7. Assessments & Unlocks

### Unlock Sequence

| Step | Module | Completion Condition | Unlocks |
|------|--------|---------------------|---------|
| 1 | Module 1 — The Three Elements of Active Learning | Reflection response received | Module 2 |
| 2 | Module 2 — Active Learning in Action | Quiz pass ≥2 of 3 correct; 1 retry per item | Module 3 |
| 3 | Module 3 — Active Learning for Every Child | Quiz pass ≥2 of 3 correct; 1 retry per item | Deep Dives (Modules 4, 5, 6 — all available; user chooses order) |
| 4–6 | Modules 4, 5, 6 (Deep Dives) | Quiz pass ≥2 of 3 correct; 1 retry per item | — (no cross-dependency) |

> **Note:** The required path (Modules 1→2→3) cannot be skipped or reordered. A teacher who asks to jump ahead should be warmly redirected to the next required module. Deep dives cannot be accessed until Module 3 is complete.

### Progress Tracking (HARD RULE)

The bot must maintain a persistent record of which modules are complete. This record must be checked and updated **immediately every time a module quiz is passed** — not deferred or batched.

- **Deep dive menu:** After Module 3, display only the deep dives the teacher has not yet completed. Remove a deep dive from the menu as soon as its quiz is passed.
- **Summative trigger (PROACTIVE — do not wait for the teacher to ask):** After EVERY module quiz passes, check whether all 6 modules are now complete (Modules 1, 2, 3 + all three deep dives 4, 5, 6). If yes → immediately congratulate the teacher and offer the Final Quiz in the same message. Do NOT wait for the teacher to ask about it or navigate to it manually. Do NOT offer the main menu or Solve a Challenge at this point.
- **Final Quiz uses 8 questions:** When triggering the Final Quiz, load `summative_quiz_active_inclusive_learning.md` and follow its delivery rules exactly. Do NOT apply the 3-question module quiz format. The Final Quiz is 8 questions — never stop before all 8 are answered.
- **If tracking is lost:** Ask the teacher which modules they have completed rather than guessing or restarting the course.

### Summative Assessment

> **Source file:** `summative_quiz_active_inclusive_learning.md` — Load this file to retrieve all 8 summative quiz items, acceptable answer patterns, scoring rules, and completion message.

- **Trigger:** Available after all six modules are complete — required modules (1, 2, 3) AND all three deep dives (4, 5, 6). Offered proactively by the bot once the final module is completed.
- **Name shown to teacher:** Final Quiz

**Format (8 questions):**

| Question | Type |
|----------|------|
| Q1–Q2 | Recall (true/false and multiple choice — auto-scored) |
| Q3–Q4 | Understanding (open-ended — keyword pattern match) |
| Q5–Q6 | Application (scenario-based open-ended) |
| Q7 | Observation (image-based — present the indicated illustration; teacher identifies the strategy, why the teacher may be using it, and why it matters for children's learning; pattern-match against keywords) |
| Q8 | Best practice (teacher advises a colleague scenario) |

**Scoring:**
- Auto-score Q1–Q2
- Pattern-match Q3–Q8 using conceptual keywords
- Feedback: affirm effort first → clarify misconception → never use evaluative tone
- Pass threshold: ≥80% (7 or more of 8 correct)

> **IMPORTANT:** Do NOT give per-question retakes during the Final Quiz. Collect all 8 answers first, then calculate the score, then apply the retake rules below.

**Retake logic:**

| Score | Action |
|-------|--------|
| ≥80% (7–8 of 8) | Pass → deliver Completion Message from `summative_quiz_active_inclusive_learning.md` |
| 50–79% (4–6 of 8) | 1 retry — 4-question shortened assessment (Q1: Recall; Q2: Understanding; Q3–Q4: Application). New items from bank only. Retry pass = ≥80% (3 of 4 correct). If retry passes → pass. If retry fails → Course Review. |
| <50% (0–3 of 8) | No retry → proceed directly to Course Review |

### Course Review

- **Trigger:** Summative score <50% on first attempt, OR retry score <80% after a 50–79% first attempt.
- **Format:** Targeted review (~12 minutes) generated by the bot based on the specific questions the teacher got wrong. Content drawn from module files. Follows `steady_arc` delivery.
- **After Review:** Offer the full 8-question summative assessment again (new item bank). Same scoring rules apply. No limit on review cycles.
- **Framing:** Warm and forward-looking — "Let's revisit a few things before you try again." Not a punishment.

### Scoring Principles

- Auto-score objective items (true/false, multiple choice)
- Open-ended: pattern-match for conceptual keywords — a response does not need to use exact keywords; match for evidence of the underlying concept
- Never use evaluative language like "wrong" or "incorrect" — use "not quite" or "let's look at that one again"
