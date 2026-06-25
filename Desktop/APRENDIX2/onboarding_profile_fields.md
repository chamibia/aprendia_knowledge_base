# Onboarding profile — structured worker fields (Q1–Q5)

Use this spec when a **structured worker** (extractor, parser, or tool) captures Step 3 answers after privacy acceptance. Field names are **stable machine keys** for storage and personalization; keep **raw user text** where noted for display and fuzzy matching.

**Suggested parent object key:** `onboarding_teaching_profile` (or `user_classroom_context`).

---

## Does this fit a “Structured” LLM node?

**Yes.** The same pattern as your **TTS** example applies:

- **Instructions** = system rules for *this* extraction (what to read, what to output).
- **Fields** = JSON keys + types; the model fills them from the user message (and optionally **History**, if your flow passes the last turn).

**Recommended wiring for onboarding**

| Approach | When to use |
|----------|-------------|
| **One Structured worker per question (Q1…Q5)** | Cleanest: each node has **one** field and Instructions like “extract gender only from the CURRENT user message.” Less ambiguity, easier validation. |
| **One Structured worker with all five fields** | Only if Instructions say which question is *active* (e.g. from upstream state) and to set **non-active fields to `null`** or omit them—otherwise the model may guess. |

For **enum-like** answers (Q4, Q5), if your **Type** dropdown only has **Text**, keep Type as **Text** and put the **allowed output strings** in the field **Description** (see table below). If your tool offers **Enum** or **Select**, use that and list the same values.

---

## Structured worker — copy-paste for “Add Field”

Use these as **Name** and **Description** in your modal. Set **Type** to **Text** unless your platform supports enums (then restrict to the listed values).

### Q1 — Gender

| | |
|---|---|
| **Name** | `gender` |
| **Description** | Extract the teacher’s gender from the CURRENT user message only. Output exactly one of these strings: `male`, `female`, `other`, `prefer_not_to_say`. Map synonyms and short answers (e.g. M→male, F→female, “rather not say”→prefer_not_to_say). If the message is not a valid gender answer, output empty string or null per your platform’s convention. |
| **Type** | Text (or Enum with the four values) |

### Q2 — Grade level

| | |
|---|---|
| **Name** | `students_grade_level` |
| **Description** | Extract the grade level(s) of the teacher’s students from the CURRENT user message only. Free text, short phrase (e.g. Grade 3, Grades 4–6, P1–P3). No extra commentary—only the grade answer. |
| **Type** | Text |

### Q3 — Class size

| | |
|---|---|
| **Name** | `class_size` |
| **Description** | Extract how many students are in the class from the CURRENT user message only. Return a short string: a number, range, or phrase like “about 50” (e.g. `32`, `40-45`). No extra words of explanation. |
| **Type** | Text |

### Q4 — Instructional materials

| | |
|---|---|
| **Name** | `instructional_materials_tier` |
| **Description** | Map the user’s answer to exactly one string: `very_limited`, `few_materials`, `some_teaching_aids`, or `many_materials`. Accept 1–4, full option text, or clear paraphrase. Meanings: (1/very_limited) board and voice only; (2/few_materials) little paper/objects; (3/some_teaching_aids) posters/handmade; (4/many_materials) books and many materials. |
| **Type** | Text (or Enum with those four values) |

### Q5 — Learner levels

| | |
|---|---|
| **Name** | `learner_level_descriptor` |
| **Description** | Map the user’s answer to exactly one string: `many_need_extra_help`, `different_levels`, `most_follow_lesson`, or `most_learn_quickly`. Accept 1–4, full option text, or clear paraphrase. Meanings: (1) many need extra help; (2) different levels; (3) most follow the lesson; (4) most learn quickly. |
| **Type** | Text (or Enum with those four values) |

### Example **Instructions** (single-field worker for Q1)

```text
You are extracting one onboarding answer for personalization.

Look at the CURRENT user message only (the reply to “What is your gender?”).

Return JSON matching the defined fields. Output only the normalized value for `gender` as specified in each field’s description. Do not add commentary.
```

Swap the question line for Q2–Q5 when you duplicate the node per step.

---

## Single Structured worker: main **Instructions** (all fields + History)

Use this in the **Instructions** field when one node has **all five** outputs connected to `Input` + **History** (as in your screenshot). It tells the model to read the **thread**, fill only what was clearly answered during onboarding, and use `null` for the rest.

```text
You extract the onboarding teaching profile from the CONVERSATION.

Use the full history (and the latest user message) to find answers the user gave during Step 3 after privacy acceptance, in order: gender → grade level of students → class size → instructional materials (1–4) → learner level (1–4).

Rules:
- Fill a field only if the user clearly answered that specific onboarding question. If there is no clear answer yet for that item, set that field to null. Do not guess from unrelated chit-chat.
- Normalize values exactly as each field’s schema description requires (gender enums; Q4 → very_limited | few_materials | some_teaching_aids | many_materials; Q5 → many_need_extra_help | different_levels | most_follow_lesson | most_learn_quickly).
- students_grade_level and class_size: short strings; null if not yet collected.
- If the user re-answers a question later, use the most recent clear answer.
- Do not add commentary, explanations, or keys not in the schema. Output only the structured fields your node defines.
```

**Model:** Set a real model in the empty dropdown (e.g. `gpt-4.1-mini` or your usual extractor).

**Persistence note:** This node only **produces** the values each run. “Passing them throughout the conversation” = **save** the JSON (e.g. Supabase `teaching_profile` merge) after each run, then **inject** that stored object into the main agent’s context on the next turn. A text “template” on the output does not persist by itself unless your platform appends to thread state—**database + merge** is the reliable pattern.

---

## Summary table

| Field name | Type | Description |
|------------|------|-------------|
| `gender` | `enum` | Teacher’s self-reported gender for personalization and analytics (aggregated). |
| `students_grade_level` | `string` | Grade band or level of the teacher’s students (free text). |
| `class_size` | `string` | Approximate number of students in the class (number or range as text). |
| `instructional_materials_tier` | `enum` | How well resourced the classroom is for materials. |
| `learner_level_descriptor` | `enum` | Overall spread / pace of learners in the classroom. |

---

## Q1 — Gender

| | |
|---|---|
| **Field name** | `gender` |
| **Description** | Self-reported gender of the teacher. Used only to tailor tone/examples where appropriate and for **aggregated** reporting—not for identification. |
| **Type** | `enum` (string union) |
| **Allowed values** | `male` · `female` · `other` · `prefer_not_to_say` |
| **Capture notes** | Map free text and minor typos to the enum (e.g. “M” → `male`, “rather not say” → `prefer_not_to_say`). Store optional `gender_raw: string` if you need the exact user message for audit. |

---

## Q2 — Grade level of students

| | |
|---|---|
| **Field name** | `students_grade_level` |
| **Description** | The grade level(s) or stage of the learners the teacher teaches (e.g. one grade, a range, or local labels like P1–P3). Drives examples, reading level, and math difficulty in the product. |
| **Type** | `string` |
| **Constraints** | Non-empty; should reflect a **grade, band, or range** (reject pure gibberish). Max length ~120 chars recommended. |
| **Examples** | `"Grade 3"`, `"Grades 4–6"`, `"Primary 4"`, `"P1–P3"`, `"Year 5"` |

---

## Q3 — Class size

| | |
|---|---|
| **Field name** | `class_size` |
| **Description** | Approximate number of students in the teacher’s class. Used to scale group activities, differentiation tips, and classroom-management suggestions. |
| **Type** | `string` (recommended) or split into structured fields if your worker supports it |
| **Constraints** | Must contain a **number or numeric range** (allow words like “about”, “around”). |
| **Normalization (optional)** | `class_size_numeric: number \| null` (single point) and/or `class_size_min` / `class_size_max` for ranges—parse when possible. |
| **Examples** | `"32"`, `"40-45"`, `"about 50"` |

---

## Q4 — Instructional materials

| | |
|---|---|
| **Field name** | `instructional_materials_tier` |
| **Description** | How limited or rich the teacher’s physical/print materials are. Used to prioritize low-resource strategies vs. richer activities. |
| **Type** | `enum` (string union) |
| **Allowed values** | See below (map user choice or paraphrase to one tier). |

| Enum value | Meaning (aligned to onboarding copy) |
|------------|--------------------------------------|
| `very_limited` | Very limited. I teach with a board and my voice. |
| `few_materials` | Few materials. I sometimes have paper or simple objects. |
| `some_teaching_aids` | Some teaching aids. I have posters and handmade materials. |
| `many_materials` | Many materials. I have books and many classroom materials. |

**Capture notes:** Accept button `1`–`4`, full sentence, or clear paraphrase; map to enum. Optional `instructional_materials_label: string` for the canonical line shown to the user.

---

## Q5 — Level of learners

| | |
|---|---|
| **Field name** | `learner_level_descriptor` |
| **Description** | Overall profile of learner readiness / spread in the class. Used to tune pacing, scaffolding, and differentiation hints. |
| **Type** | `enum` (string union) |
| **Allowed values** | See below. |

| Enum value | Meaning (aligned to onboarding copy) |
|------------|--------------------------------------|
| `many_need_extra_help` | Many students need extra help. |
| `different_levels` | Students are at different levels. |
| `most_follow_lesson` | Most students follow the lesson. |
| `most_learn_quickly` | Most students learn quickly. |

**Capture notes:** Same as Q4—map `1`–`4`, full text, or paraphrase to enum.

---

## Optional JSON shape (reference)

```json
{
  "onboarding_teaching_profile": {
    "gender": "female",
    "students_grade_level": "Grades 4–6",
    "class_size": "35",
    "instructional_materials_tier": "some_teaching_aids",
    "learner_level_descriptor": "different_levels",
    "captured_at": "2026-04-21T00:00:00Z",
    "onboarding_version": "1"
  }
}
```

---

## Personalization hooks (for product logic)

- **`gender`** — Optional language in reflections; never surface in user-visible labels unless the teacher opted in.
- **`students_grade_level`** — Filter or bias module examples (word problems, reading level).
- **`class_size`** — Group work vs. pair work; “whole class” vs. “stations” suggestions.
- **`instructional_materials_tier`** — Prefer chalk-talk / oral / minimal-print strategies vs. hands-on with manipulatives.
- **`learner_level_descriptor`** — Default scaffolding depth and reminder frequency.

---

## Runtime: how to handle structured worker outputs

### 1. One step, one extraction (recommended)

For each user reply during Step 3, run **only** the Structured worker wired to **that** question (single field, or one row in your flow).

| Step | User message context | Worker output key | Next action |
|------|----------------------|-------------------|-------------|
| After Q1 | Answer to “What is your gender?” | `gender` | Validate enum → **upsert** profile row |
| After Q2 | Grade level | `students_grade_level` | Validate non-empty string → upsert |
| After Q3 | Class size | `class_size` | Validate has number/range → upsert |
| After Q4 | Materials choice | `instructional_materials_tier` | Validate enum → upsert |
| After Q5 | Learner level | `learner_level_descriptor` | Validate enum → upsert |

**Do not** run all five extractors on every message; that invites wrong field fills.

### 2. Persist in Supabase (single row per user or per conversation)

- **Table** (example): `user_profiles` or `onboarding_responses` with `user_id` (or `conversation_id`) as key.
- **Column** (example): `teaching_profile jsonb` — merge keys as they arrive:

```json
{ "gender": "female", "students_grade_level": null }
```

→ after Q2:

```json
{ "gender": "female", "students_grade_level": "Grade 3", "class_size": null }
```

- **Timestamps:** `updated_at`; optional `onboarding_step_completed` (`q1` … `q5`) for debugging.

### 3. Validate before advancing the chat agent

1. Structured worker returns JSON.
2. **Your code** (or a small validation node) checks enums / non-empty strings per `onboarding-agent.md` hidden rules.
3. If **invalid:** do **not** save junk; return the **retry** message from the onboarding script and **do not** increment step.
4. If **valid:** `UPDATE` JSONB merge → then let the **conversation agent** send the next scripted question (or Step 4).

The LLM that chats with the user should **not** be the only place validation happens—**store only validated** structured data.

### 4. How the main agent uses it

- **During onboarding:** Optionally inject `teaching_profile` so far into system context (or leave empty until Q5 done—your choice).
- **After Q5 + Step 4:** Load full `teaching_profile` from Supabase when starting **course** or **toolkit** flows; pass into `system_prompt` injection or a “user context” block for personalization.

### 5. Failure modes

| Situation | Handling |
|-----------|----------|
| Worker returns empty / wrong type | Treat as invalid answer; send scripted retry for that Q; do not advance step. |
| User edits an earlier answer later | Either disallow until “settings,” or allow re-run of that step’s worker and `UPDATE` that key only. |

### 6. Source of truth

- **Supabase `teaching_profile`** = canonical stored profile for product logic.
- **Structured worker** = parser from raw text → normalized fields; **not** the long-term store by itself.

---

## Alignment

Source questions: `onboarding-agent.md` Step 3 (Q1–Q5). Validation behavior should stay consistent with the **hidden validation rules** in that file.
