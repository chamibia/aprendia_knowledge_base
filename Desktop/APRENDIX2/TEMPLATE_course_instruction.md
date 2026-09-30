# Course Instruction – [Course Title]

**Course ID:** `[PREFIX]_COURSE_01`

---

## 1. Course Manifest

| Field | Value |
|---|---|
| Title | [Course title] |
| Description | [1–2 sentence description of who this is for and what it covers] |
| Target Experience | [e.g. Beginner to intermediate] |
| Target Tech Literacy | [e.g. Low to medium] |
| Teaching Context | [e.g. Crisis-affected, low-resource classrooms] |
| Typical Class Size | [e.g. 40–100 students] |
| Known Constraints | [e.g. limited materials, interrupted attendance, mixed grade levels] |

### Learning Objectives

- [Objective 1 — short imperative statement: "Teachers can / understand / recognize…"]
- [Objective 2]
- [Objective 3]
- [Objective 4 — optional]

### Design Scope

- **Includes:** [comma-separated list of topics/skills covered]
- **Excludes:** [comma-separated list of topics explicitly out of scope]

### Pedagogical Frame

[One paragraph describing the instructional philosophy underpinning this course — e.g. sense-making over memorization, trauma-informed, strengths-based.]

### Microlearning Contract

| Constraint | Value |
|---|---|
| Time per interaction | [e.g. ≤2 minutes] |
| Time per module | [e.g. ≤10–15 minutes] |
| Input types accepted | [e.g. free text, single-word replies, button/list selections] |
| Bot turns before user input | 2 max |
| End-of-module quiz rule | [1-line summary — full rule is in the subsection below] |

### Tone Guidance

[One short paragraph describing the voice: e.g. warm, direct, colleague-to-colleague, no jargon, no cheerleading.]

### End-of-module quizzes (system prompt §9)

| Rule | Detail |
|---|---|
| Structure | 3 items: 1 recall, 1 understanding, 1 application |
| Pass → unlock next module | Value of each module's `quiz_pass` field (e.g. `2_of_3`) |
| Course pass / explain depth | Value of each module's `course_pass_threshold` field (e.g. `0.80`) — every module file in this course must declare this key |
| Retry rule | One retake per missed item, using a different item of the same type from that module's quiz bank — never re-ask the same item |
| Key concepts note | [any course-specific note on what must be tested] |

### AI Guidance Notes

- [Bulleted do/don't rules for the agent's behavior specific to this course]
- [Routing hint examples]

---

## 2. Pathway Assignments

| Module ID | Module Name | Pathway | Fallback | Fallback Trigger |
|---|---|---|---|---|
| `[MODULE_ID]` | [Name] | [steady_path / steady_arc / empathy_arc / diy_kit] | [fallback pathway, or "—"] | [trigger key, or "—"] |

> If this course has no fallback-pathway system, write "Not used in this course" under the table instead of leaving rows blank.

### Fallback Trigger Definitions

| Trigger | Condition |
|---|---|
| `[trigger_key]` | [condition description, e.g. `user_mastery >= 0.90`] |

---

## 3. Level Structure & Unlock Rules

[One paragraph: how many required modules, how many deep dives (if any), overall unlock logic.]

### Module 1 – [Name]

| Field | Value |
|---|---|
| Module ID | `[MODULE_ID]` |
| Type | Required |
| Pathway | [pathway] |
| Prerequisite | None — first module in the course |
| Time | [e.g. ≤10 minutes] |
| Purpose | [1 sentence] |
| Completion | Quiz: [quiz_pass value] |
| Unlocks | `[next Module ID]` |

[Repeat one block per required module, in order.]

### Deep Dives ([Module ID range])

| Module ID | Name | Pathway | Time |
|---|---|---|---|
| `[MODULE_ID]` | [Name] | [pathway] | [time] |

[Unlock/completion prose for deep dives — e.g. "All deep dives unlock simultaneously once required modules are complete." If this course has no deep dives, delete this subsection and state so in the paragraph above instead.]

### Pacing for Strategy-Heavy Modules

- [Delivery pacing rules for any module with 3+ strategies/concepts — e.g. one strategy per message, full Expanded Explanation before advancing]

---

## 4. Personalization Signals

| Signal | Detection | Use |
|---|---|---|
| `[signal_key]` | [how it's detected] | [how it changes delivery] |

### Routing Hints (Suggestive, Not Mandatory)

- [Bulleted routing hints — these inform tone/pacing, they never override the pre-assigned pathway]

---

## 5. Module Construction Schema

| Pathway | Flow Summary |
|---|---|
| steady_path / steady_arc | `INTRO → STRATEGIES (reflection checkpoints) → RECAP → QUIZ` |
| empathy_arc | `[Opening poll (optional)] → per-scene story/insight/reflection → VIGNETTE DEBRIEF → QUIZ` |
| diy_kit | `INTRO → CONTEXT_CHECK → BUILD_STEPS → REFINEMENT → FINAL_PLAN → CONFIRMATION` |

[List only the pathways actually used in this course — delete rows for pathways not used. `explain_exchange` is a fallback-only pathway; do not list it here unless a module in this course uses it as its primary pathway.]

### Course-specific requirements

- [Any deviations from the standard pathway flows above, specific to this course]

---

## 6. Message & Time Constraints

| Constraint | Value |
|---|---|
| Characters per message | 300–400 max |
| Sentences per message | 3–4 max |
| Concepts per message | 1 only |
| Strategies per message | 1 only |
| Bot turns before user input | 2 max |
| Questions per message | 1 only |
| Examples per message | 1 only |

---

## 7. Tone Requirements

| ✅ Do | ❌ Don't |
|---|---|
| [do] | [don't] |

---

## 8. Safety & Feasibility Constraints

### Content Safety
- [Bulleted hard constraints — e.g. no PII collection, no medical/legal/diagnostic advice]

### Feasibility Constraints
- [Bulleted hard constraints — e.g. no materials required, works in overcrowded classrooms, non-contact activities only]

---

## 9. Media & Image Output

[Only include this section if the course uses images. State the rule for when/how images are sent (e.g. "send the image URL on its own line, followed by the caption on the next line"). Otherwise, delete this section entirely — do not leave it as a placeholder.]

---

## 10. Assessments & Unlocks

### Module Unlock Rules
- [Unlock rule per module, or "See §3 Level Structure tables above."]

### Summative Assessment

[Include only if this course has a final/summative quiz. If it does not, delete everything below this line and write instead: "No summative quiz for this course."]

| Field | Value |
|---|---|
| Trigger | [e.g. after all required modules + deep dives are complete] |
| Format | 8 questions: Q1–Q2 Recall, Q3–Q4 Understanding, Q5–Q6 Application, Q7 Observation (image), Q8 Best Practice |
| Pass | 7–8 of 8 |
| Retry (5–6 of 8) | 4-question shortened retry; pass = 3–4 of 4 |
| Fail (0–4 of 8) | Review & Choice |
| Source file | `summative_quiz_[course_slug].md` |

### Review & Choice
- [What options the user gets after failing the summative assessment]

### Scoring Principles
- [General scoring philosophy for this course]

---

<!--
AUTHOR NOTES — delete this block before publishing a finished course instruction file.

Standardization decisions this template enforces (resolved from inconsistencies found across
the 6 existing Course Instruction files — flag to Bianca if you want to change one):
- Title line: "Course Instruction – [Title]" (singular, en dash). Do not use "Course Instructions —".
- Course ID is always backtick-wrapped: `PREFIX_COURSE_01`.
- Per-module metadata is always a `| Field | Value |` table — never a bullet list of `key: value` lines.
- Section names are fixed as written above (e.g. always "Level Structure & Unlock Rules", never
  "Lesson Structure"; always "Safety & Feasibility Constraints", never "Safety/Feasibility Constraints").
- Section numbers (## 1., ## 2., …) are sequential in this file regardless of which optional
  sections a given course uses — renumber if you delete a section.
- Every module referenced in §3 must have a matching module content file using
  TEMPLATE_module_content.md, with matching module_id.
- If a course has no deep dives, no fallback system, or no summative quiz, do not leave an
  empty section — delete it and state the opt-out in the surrounding prose (as TWB and
  Keeping Children Safe do today).
-->
