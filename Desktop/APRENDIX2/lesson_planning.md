# Lesson Planning in Classroom Toolkit

## Overview

Lesson Planning is a **Classroom Toolkit tool** that helps a teacher generate a **ready-to-teach plan for an upcoming lesson** in WhatsApp, with an optional **PDF export**. It is designed for crisis/low-resource contexts and interrupted use.

## Objective

Reduce planning time and decision fatigue while increasing teacher confidence and classroom readiness, by delivering a plan that is:

* usable tomorrow (not abstract)
* low-resource by default
* WhatsApp-scannable (one screen)
* fast to generate (teacher answers in under a minute)

## Engagement hooks

* Teachers get value quickly: "one lesson plan you can run tomorrow."
* Retention loop: **Generate → Save → Reuse → Another version**
* No scheduled reminders required (Save/Reuse is the mechanic).

## Entry

Classroom Toolkit → Lesson Planning

Mentor opener:
"Let's plan one lesson you can teach soon. Keep it short and practical."

## Q1 (open-ended, bounded)

**Question:** "What is the performance objective of the lesson?"
Instruction: "Share your own objective or one from curriculum."
Examples:

• Place numbers values appropriately
• Use contextual clues to get the meaning of unfamiliar words
• Name the main character in a story

**Guardrail:** If the answer is general, missing a specific topic or student outcome, ask one quick follow-up (only once):
"Thank you for sharing. Can you be more specific? Here is an example: Explain the meaning of a verb"

## Q2 (open-ended, bounded)

**Question:** "How much time do you have for the lesson?"
Instruction: "Reply in one short line with time."
Examples:

• 60 minutes
• 40 minutes
• 20 minutes

**Guardrail:** If time is missing, ask one quick follow-up (only once):
"How long?"

## Q3 (options provided, bounded)

**Question:** "Do you have any materials for this lesson?"
Instruction: "Respond with the number that best represents your classroom."
Options:

1. Very limited - I only have the board and my voice.
2. Few materials - I have some paper and simple objects.
3. Some teaching aids - I have posters and handmade materials.
4. Many materials - I have books and many classroom materials.

**Guardrail:** If number is missing, ask one quick follow-up (only once):
"Which number reflects your classroom?"

## Q4 (options provided, bounded)

**Question:** "How ready are your students for this objective?"
Instruction: "Respond with the number that best represents your students."
Options:

1. Students are new to this topic.
2. Students need significant support and background knowledge.
3. Students have some familiarity but struggled before.
4. Students understand the basics and need more practice.
5. Students already understand the basics and are ready to go deeper.

**Guardrail:** If number is missing, ask one quick follow-up (only once):
"Which number reflects your students?"

## Q5 (open-ended, bounded)

**Question:** "What challenges should we plan ahead for to ensure all students can participate in the lesson?"
Instruction: "Share a challenge like language, skill level, student wellbeing, or something else."
Examples:

• Some students speak different languages than the rest of the class
• My students get nervous speaking in front of the whole class
• I have students who cannot write yet

**Guardrail:** If challenge is not provided or too general, ask one quick follow-up (only once):
"Take a moment to reflect on your class. We can even plan ahead for small barriers." or
"Thank you for sharing. Can you be more specific? Here is an example: My students get stressed during math tests"

## Output (WhatsApp-first, one-screen plan)

The plan must use this exact structure every time:

> Thank you for answering those questions! Let's build the lesson plan together, step by step — I'll suggest, and you can accept, change, or add your own ideas before we move on. Ready?

**Step 1: Warm-up**
How would you like to introduce the topic or access students' background knowledge?

1. ...
2. ...
3. Another idea you have?

Which warm-up do you like best, or do you have a different idea?

**Step 2: I Do (Teacher Modeling)**
How would you like to model this to students? Here are two ideas:

1. ...
2. ...
3. Another idea you have?

Which option do you like?

**Step 3: We Do (Practice Together)**
How would you like to practice with your students here?

1. ...
2. ...
3. Another idea that you have?

Which one of these would you like to use, or do you want to combine ideas?

**Step 4: You Do (Independent Practice)**
How would you like students to show their understanding? For example:

1. ...
2. ...
3. Another idea that you have?

Which option do you like, or would you like different ideas?

**Step 5: Wrap-up**
Let's build your wrap-up so you can close the lesson. Which best fits your style or class, or add your own idea!

1. Closing reflection (relating to real-world or classroom learning)
2. Challenge (optional practice for outside the classroom)
3. Another idea that you have?

**Final plan:**

> Here is your complete lesson plan:
>
> Title (≤6 words)
> Performance objective (1 sentence)
>
> 1. Warm-up: ... (≤25 words; include time)
> 2. I do: ... (≤25 words; include time)
> 3. We do: ... (≤25 words; include time)
> 4. You do: ... (≤25 words; include time)
> 5. Wrap-up: ... (≤25 words; include time)
> 6. Differentiation (Support 1 line; Extension 1 line)
>
> Great work planning this lesson! This will help your students…

## Options loop (always)

Save | Another version | Export PDF | Back

# Builder Implementation Checklist (Bianca)

## A) Flow nodes

1. Toolkit menu → Lesson Planning
2. Q1 capture → store
3. Q1 follow-up only if missing a specific topic/outcome
4. Q2 capture → store
5. Q2 follow-up only if time is missing
6. Q3 capture → store
7. Q3 follow-up only if number is missing
8. Q4 capture → store
9. Q4 follow-up only if number is missing
10. Q5 capture → store
11. Q5 follow-up only if challenge is missing or too general
12. Direct LLM generation (no retrieval) — only after Q1–Q5 are all captured
13. Render output contract
14. Options loop

## B) PDF export

* Trigger: user selects Export PDF
* Use `lp.plan_text` + metadata (topic/learners, time) as header
* Output: 1-page PDF with the same headings as WhatsApp plan
* Failure fallback (single line):
  "I couldn't generate a PDF right now. Your plan is still here in chat."

## C) Telemetry (minimum)

* `toolkit_lesson_planning_started`
* `toolkit_lesson_planning_q1_captured`
* `toolkit_lesson_planning_q2_captured`
* `toolkit_lesson_planning_q3_captured`
* `toolkit_lesson_planning_q4_captured`
* `toolkit_lesson_planning_q5_captured`
* `toolkit_lesson_planning_generated`
* `toolkit_lesson_planning_saved`
* `toolkit_lesson_planning_regenerated`
* `toolkit_lesson_planning_pdf_exported`
* `latency_seconds`

# Builder Prompt Set

## 1) Agent prompt (orchestration)

**Name:** `TOOLKIT_LESSON_PLANNING_AGENT_PROMPT_V4`

You are aprendIA running Lesson Planning inside Classroom Toolkit on WhatsApp.

Objective: deliver one classroom-ready plan the teacher can teach soon, optimized for low resources and interrupted use.

Mandatory flow:

1. Ask all 5 questions, in order (Q1–Q5) — one at a time, waiting for a reply before moving to the next. Do not skip a question, reorder them, or generate the plan until every one of Q1–Q5 has been answered (each may have used its one allowed guardrail follow-up).
2. Call the Direct LLM prompt (no retrieval) — only once Q1–Q5 are all captured.
3. Show the plan exactly as returned.
4. Always show options: Save | Another version | Export PDF | Back.

Step options format (Warm-up, I Do, We Do, You Do):
For each of these steps, generate exactly 2 original options (numbered 1–2) tailored to the teacher's inputs from Q1–Q5. Always append a fixed 3rd option inviting the teacher's own idea (e.g. "Another idea you have?"). Never label the generated options as AI-generated in the output shown to the teacher.

Inputs available from system (use them, don't ask the teacher):
`teacher_language`, `profile_tags`, `context_assessment_summary`, `interaction_history_summary`, `recent_outputs_same_tool` (last 2), `saved_items_same_tool_summary` (last 2).

Quality gate (required):
Before sending the plan, verify:

* All of Q1–Q5 were answered before generation was triggered — including student readiness (Q4) and the challenge to plan for (Q5)
* It matches Q1–Q5
* It follows the output contract exactly
* It assumes low resources appropriately
* It is culturally portable
* It is not a near-duplicate of the last 2 delivered or last 2 saved plans

If it fails, rerun the Direct LLM prompt once.

Action handling:

* **Save:** store exact `plan_text` + metadata; reply "Saved." then show options again.
* **Another version:** regenerate using same inputs; must be meaningfully different.
* **Export PDF:** call PDF tool with `plan_text`; if it fails, send fallback line.
* **Back:** return to Classroom Toolkit menu.

Non-negotiables:
No personal identifiers. No official curriculum sequencing claims unless validated local overlay is provided.

## 2) Direct LLM prompt (generation)

**Name:** `LESSON_PLANNING_DIRECT_LLM_PROMPT_PRO_V4`

Generate ONE lesson plan a teacher can run tomorrow in a low-resource classroom. Direct LLM (no retrieval). Use only the provided context.

Provided context (use it, don't repeat it):
Language: `{{teacher_language}}`
Teacher tags: `{{profile_tags}}`
Context assessment: `{{context_assessment_summary}}`
Interaction history: `{{interaction_history_summary}}`
Recent plans delivered (last 2): `{{recent_outputs_same_tool}}`
Saved plans (last 2): `{{saved_items_same_tool_summary}}`

Teacher inputs (raw) — all 5 must be present; do not generate if any are missing:
Q1 (performance objective): `{{lp.objective_raw}}`
Q2 (time available): `{{lp.time_raw}}`
Q3 (materials available): `{{lp.materials_raw}}`
Q4 (student readiness): `{{lp.readiness_raw}}`
Q5 (challenges to plan for): `{{lp.challenges_raw}}`

Hard constraints:

* Total length 220–280 words max
* Steps: exactly 5 steps (Warm-up, I do, We do, You do, Wrap-up); each step line ≤25 words
* Low-resource by default; include alternatives
* No jargon; no long explanations
* Must not be a near-duplicate of last 2 delivered or last 2 saved
* No personal data requests
* No curriculum sequencing claims

### Output template

**Title:**

**Performance Objective:**

**Materials:**

|  | Teacher's Actions | Pupils' Actions | Teaching Strategies |
| :---- | :---- | :---- | :---- |
| Warm-up |  |  |  |
| Teacher Presentation (I do) |  |  |  |
| Whole Class Practice (We do) |  |  |  |
| Independent Practice (You do) |  |  |  |
| Wrap-up |  |  |  |
| Differentiation |  |  |  |
| What went well… Even better if… | *Reflect on what worked during your lesson and what could have been improved!* |  |  |

Silent self-check:
Confirm it matches the teacher's inputs and is runnable tomorrow. Rewrite once if needed.

---

# Instructional Design blanks (Mackenzie + Shelby fill)

1. Topic examples per subject that are culturally portable and low-resource (2–3 each): ______
2. What "good lesson plan" means for aprendIA (5 bullet checklist):
   * **Prepare teachers for the lesson.** Lesson plans should be thorough yet adaptable, so that teachers have confidence in what they are teaching but also can readjust in the moment. Lesson plans should anticipate barriers that might present during teaching.
   * **Center active learning strategies.** Lesson plans should always reflect the core elements of active learning: a clear learning objective, engagement with peers and learning materials, and a positive, safe learning environment.
   * **Reflect the realities of each classroom.** Lesson plans should allow teachers to choose strategies and practices that are possible for their particular circumstances and students. Lesson plans should provide locally contextualized examples and languages, and utilize country-specific curriculum when available.
   * **Include all students.** Lesson plans should be accessible for all students to participate despite academic level, language, or abilities. Lesson plans should offer differentiation strategies that allow students to be part of the learning process and demonstrate understanding.
   * **Promote curiosity.** Lesson plans should enable students to explore, problem solve, discover, take risks, make connections, try new things, and/or make mistakes.
3. Do/Don't content constraints (safeguarding + cultural risk):
   * **Do:**
     * Reflect the diverse representation of cultures, families, and abilities
     * Emphasize the importance of inclusion (language, ethnicity, culture, ability level, learning level, religion)
     * Use local curriculum/standards when available for guidance
     * Offer varied options for users that reflect strategies from courses
       * Use user onboarding answers to tailor options
     * Suggest local/environmental resources and materials
     * Validate users pushing back on ideas if they will not work in a user's classroom
   * **Don't:**
     * Include content that could shame or single out students based on background, ability, or identity
     * Assume single cultural, religious, or family norm as universal
     * Suggest resources/materials that are expensive or unavailable to users
     * Assume the learning level of students based off grade level alone
4. PDF format preference (one page vs two; include title/date or not):
   * PDFs should be two pages maximum
   * Include title, performance objective, and materials needed.
     * Reach out to the Nigeria team about what other key things headmasters/teachers would like to see (e.g. grade level, subject, topic…)?
