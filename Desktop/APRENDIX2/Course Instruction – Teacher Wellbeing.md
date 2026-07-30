# Course Instructions — Teacher Wellbeing

**Course ID:** TWB_COURSE_01

---

## 1. Course Manifest

| Field | Value |
|-------|-------|
| **Title** | Teacher Wellbeing |
| **Description** | A short, sequential course supporting teachers in crisis-affected settings to strengthen wellbeing through awareness, connection, and planning. Module 1 builds stress understanding (required) → Module 2 supports resilience and motivation (required) → Module 3 focuses on relationships and boundaries (required) → Module 4 guides teachers to co-create a simple, personalized wellbeing plan (DIY Kit, required). All modules are low-burden, reflective, and grounded in teachers' lived realities. |
| **Target Experience** | Beginner to experienced |
| **Target Tech Literacy** | Low to medium |
| **Typical Class Size** | 40-100 students |
| **Known Constraints** | Emotional load, unpredictability, limited time, limited resources, limited privacy |

### Learning Objectives

- Understand how stress and crisis affect teachers' thinking, emotions, and energy
- Sustain motivation and purpose through small mindset and reflection practices
- Reduce isolation and protect energy through peer connection and boundaries
- Create a simple wellbeing plan that supports real-life moments

### Design Scope

- **Includes:** stress awareness, emotional resilience, growth mindset, peer connection, boundary-setting, simple planning tools
- **Excludes:** clinical mental health treatment, diagnosis, intensive self-disclosure, long reflective writing

### Pedagogical Frame

This course builds fluency through steady pathways, mindset shifts via stories, and implementation via simple artifacts. Emphasis is on affirming reflection, emotional safety, and small pedagogical shifts that have big impacts for learning and wellbeing.

---

## 2. Pathway Assignments

> **Note:** Teacher Wellbeing uses tone-based routing—pick one pathway per module based on prior user signals (reflective vs. factual, stressed vs. calm). Pathways are not pre-assigned; use heuristics below.

| Module ID | Module Name | Primary Pathway | Fallback | Fallback Trigger |
|-----------|-------------|-----------------|----------|------------------|
| `TWB_M1_UTWB` | Understanding Teacher Wellbeing & Stress | `steady_path` | `empathy_arc` | `prior_stress_language` OR `reflective_tone` |
| `TWB_M2_BRM` | Building Resilience & Motivation | `empathy_arc` | `steady_path` | `short_responses` OR `factual_tone` |
| `TWB_M3_BRB` | Building Positive Relationships & Boundaries | `steady_path` | `empathy_arc` | `prior_stress_language` OR `reflective_tone` |
| `TWB_M4_CWP` | Creating a Wellbeing Plan | `explain_exchange` | `steady_path` | `user_struggles_with_socratic` |

### Routing Heuristics (Pathway Selection)

| Signal | Pathway Preference |
|--------|-------------------|
| High stress language | `empathy_arc` |
| Short responses | `steady_path` |
| Resistance to planning | Reduce prompts, simplify choices; pivot to `steady_path` if needed |
| Repeated discouragement | Emphasize normalization over motivation |

### Fallback Trigger Definitions

| Trigger | Condition |
|---------|-----------|
| `prior_stress_language` | User has used stress-related words in prior turns |
| `reflective_tone` | User gives reflective or emotional responses (e.g., ≥20 words) |
| `short_responses` | User consistently gives short, factual answers |
| `factual_tone` | User prefers direct explanations over stories |
| `user_resists_planning` | User says "too much," "not helpful," or resists structured prompts |
| `user_struggles_with_socratic` | User gives incomplete or unclear reasoning in Socratic dialogue; or asks for a simpler, direct explanation |

---

## 3. Lesson Structure & Unlock Rules

### Module 1: Understanding Teacher Wellbeing & Stress

| Field | Value |
|-------|-------|
| **Module ID** | `TWB_M1_UTWB` |
| **Pathway** | `steady_path` (preferred) or `empathy_arc` |
| **Time** | ≤6 minutes total |
| **Completion** | Quiz pass = ≥2 of 3 items correct, fixed order recall → understanding → application; 1 retry per item (alternate bank); see system prompt §9 |
| **Unlocks** | Module 2 |

**Strategies (fixed order):**

1. Notice Stress Signals (awareness)
2. Mental Reset (interrupt escalation)
3. Understand Stressors (control vs. no control)
4. Micro Wellbeing Moments (prevention)

> **Note:** Emphasize understanding and normalization over coping "solutions." Do not skip or reorder strategies.

---

### Module 2: Building Resilience & Motivation

| Field | Value |
|-------|-------|
| **Module ID** | `TWB_M2_BRM` |
| **Pathway** | `empathy_arc` (preferred) or `steady_path` |
| **Time** | ≤10 minutes total |
| **Completion** | Quiz pass = ≥2 of 3 items correct, fixed order recall → understanding → application; 1 retry per item (alternate bank); see system prompt §9 |
| **Unlocks** | Module 3 |

**Strategies (fixed order):**

1. Name Emotions (pattern awareness)
2. Mindfulness Moment (restore perspective)
3. Motivation Check (meaning and purpose)
4. Mindset Reframe (growth-oriented thinking)

> **Note:** Keep each strategy ≤2–3 minutes. Avoid "stay positive" framing. Deliver all strategies in sequence.

---

### Module 3: Building Positive Relationships & Setting Boundaries

| Field | Value |
|-------|-------|
| **Module ID** | `TWB_M3_BRB` |
| **Pathway** | `steady_path` (preferred) or `empathy_arc` |
| **Time** | ≤10 minutes total |
| **Completion** | Quiz pass = ≥2 of 3 items correct, fixed order recall → understanding → application; 1 retry per item (alternate bank); see system prompt §9 |
| **Unlocks** | Module 4 |

**Strategies (fixed order):**

1. Peer Mentoring Moment (connection)
2. Celebrate Small Wins (recognition and morale)
3. Practice Active Listening (relational trust)
4. Set a Boundary (energy protection)

> **Note:** Reinforce low-effort, low-disclosure approaches. Frame boundaries as professional care, not disengagement. Do not position peers as the only support option. Deliver all strategies in sequence.

---

### Module 4: Creating a Wellbeing Plan

| Field | Value |
|-------|-------|
| **Module ID** | `TWB_M4_CWP` |
| **Pathway** | `explain_exchange` (primary, Socratic); `steady_path` if user struggles with dialogue |
| **Time** | ≤12–15 minutes total |
| **Completion** | Plan generated and confirmed OR teacher confirms plan is usable |
| **Unlocks** | — (course complete) |

**Strategies (fixed order):**

1. Wellbeing Moments (sentence stems: "When I have 1 minute…" / "When I have 5 minutes…" / "When I feel overwhelmed…" / "When I feel isolated…")
2. Identify Stressors and Responses (max 2–3 pairs)
3. Growth Mindset Reminder (invite user to draft; offer suggestions if needed)
4. Weekly Wellbeing Check-In (rate energy, emotions, physical tension, workload; one thing that went well; one supportive action for next week)
5. Peer Connection Plan (one low-effort, non-identifying habit; no colleague names—roles only)

**When pathway is explain_exchange (primary):** Follow Socratic flow in `global_pathway_instructions.md`. Use questions to draw out the teacher’s wellbeing plan (e.g. wellbeing moments, stressors/responses, growth reminder, weekly check-in, peer connection). After dialogue, summarize their plan and offer PDF if applicable.

**When fallback is steady_path:** Guide co-creation with structured prompts and sentence stems; limit choices; capture outputs for PDF. Confirm plan completeness; generate and offer Wellbeing Plan PDF; optional revision prompt ("Is there anything you'd like to edit?").

### Pacing for Strategy-Heavy Modules (M2, M4)

> **Do not rush.** Module 2 (empathy_arc) and Module 4 (explain_exchange or steady_path) require careful pacing. The agent must:

- **empathy_arc (M2):** Deliver one scene per message batch. Do not send Scene 2 and Scene 3 back-to-back. For Scene 3 (2 strategies): deliver one strategy per message; use `<break>` between them. Allow time for reflection between scenes. See `global_pathway_instructions.md`.
- **explain_exchange (M4):** One Socratic question at a time; wait for response before follow-up. Do not lecture; draw out understanding through questions.
- **steady_path (M4 fallback):** One build step per message; wait for user input when designated.
- Include at least one concrete example per strategy. Do not bundle multiple strategies into a single message.

---

## 3.1 End-of-module quizzes (system prompt §9)

This course follows **`system_prompt.md` §9**, **`quiz_rationale.md`**, and **`example_quiz_questions.md`**.

| Rule | Detail |
|------|--------|
| **Structure** | **3 items** per module, fixed order: **Q1 recall** (MC/TF) → **Q2 understanding** (open-ended; **hidden** keyword match) → **Q3 application** (scenario) |
| **Pass module / unlock next** | **≥2 of 3** correct, after at most **1 retake per item** (new question, same type, from module bank or `QUIZ_BANK_ALT` — **NEVER re-ask the original question**) |
| **Course pass / explain depth** | **≥80%** of all quiz items in the **course** to pass the course and unlock **`explain_exchange`** / explain-arc–style depth (see system prompt; this file defers if anything conflicts) |
| **Module YAML** | In module files use `quiz_pass: 2_of_3` and `course_pass_threshold: 0.80`. A legacy `quiz_threshold: 0.80` line, if present, describes **course-level** threshold only, not the per-module bar. |
| **Key Concepts in module files** | Authoring guidance for the agent only; **do not** lift Key Concept wording into user-facing quiz stems (§9). |

**M1–M3 only:** Module 4 ends with a co-created plan / PDF; use the **mini-quiz** pattern where the module file specifies a quiz block.

> **No Final/Summative Quiz for this course.** Teacher Wellbeing ends at Module 4's completed Wellbeing Plan — there is no course-level 8-question assessment. Do not offer, reference, or improvise a Final Quiz for this course.

---

## 4. Message & Time Constraints

| Constraint | Value |
|------------|-------|
| Per-interaction time cap | 90–120 seconds |
| Module 1 total | ≤6 min |
| Modules 2–3 total | ≤10 min each |
| Module 4 total | ≤12–15 min |
| Input types | Buttons, short text (≤25 words), quick polls or scales, quick reflections |
| Bot turns before user input | ≤2 |
| Questions per message | ≤1 |
| Quiz items per module | 3, fixed order: recall → understanding → application; pass = 2 of 3 correct; course pass / explain = ≥80% of all course quiz items (see system prompt §9) |

---

## 5. Personalization Signals

> **Note:** Track these for pathway selection and pacing—NOT for skipping content.

| Signal | Detection | Use |
|--------|-----------|-----|
| `prior_module_completion` | Track completion | Unlock rules |
| `reflection_length` | Word count | Longer → reflective; shorter → factual |
| `emotional_tone` | Stress-related words, discouragement | High stress → empathy_arc; discouragement → normalization |
| `resistance_signals` | "Too much," "not helpful," short dismissive replies | Simplify prompts; reduce choices; consider steady_path |

### AI Guidance Notes

- Do not frame wellbeing as an individual failure or responsibility alone
- Avoid diagnostic language or therapy framing
- After 2 reflections, offer a brief teacher example or summary
- If distress escalates, shift tone from reflective to supportive and safe, and trigger safeguarding guidance when needed

---

## 6. Tone Requirements

| ✅ Do | ❌ Don't |
|-------|---------|
| Ground in reality; validate experiences | Use forced positivity |
| Normalize stress without minimizing it | Imply teacher is failing |
| Emphasize agency, not perfection | Require deep self-disclosure |
| Use teachers' language when possible | Use clinical or diagnostic terms |
| Offer low-effort, optional actions | Imply peer support replaces professional help |

---

## 7. Safety & Feasibility Constraints

- Do not request names or identifying details
- Avoid deep emotional probing
- If a user expresses any of the following, pause content delivery and trigger safeguarding guidance:
  - Hopelessness
  - Emotional shutdown
  - Harm-related thoughts
- Never imply peer support replaces professional help
- Keep all actions no-cost, private, and optional

---

## 8. Module Construction Schema

A module uses ONE pathway for its entire strategy sequence. Unlike the other courses, Teacher Wellbeing's pathway is **not pre-assigned** — it is selected per §2's tone-based routing (falling back to the module's listed Primary Pathway when no signal is present). Once selected, the agent must load that pathway at module start, follow its flow consistently for every strategy, and maintain the same interaction rhythm until the mini-quiz (or plan completion for M4) — never switch pathways mid-module.

See `global_pathway_instructions.md` for full pathway delivery specifications. Course-specific notes below.

| Pathway | Flow Summary |
|---------|-------------|
| `steady_path` | Introduction → for each strategy: explanation + 1 localized example → brief reflection or micro-action → [repeat] → mini-quiz |
| `empathy_arc` | Vignette intro + poll → brief reflection → for each strategy: vignette continues → reflection/poll → strategy insight → micro-action → story debrief → mini-quiz |
| `diy_kit` | Intro → context check → build steps (one per message, Reflection #1 mid-build) → refinement → final tool → Reflection #2 → mini-quiz |

**Course-specific requirements:**

- Every module must include a clear title, metadata, and its Primary Pathway (used as default when no routing signal applies — see §2)
- Reflection and comprehension checks follow the rules of that pathway
- Modules must respect time limits
- Include the 3-item mini-quiz (≥2 of 3 to pass module; course-level rules apply separately — see system prompt §9)
- Examples and practice prompts should be localized when possible
- Language must remain simple and non-clinical
- All content must respect time, message, and WhatsApp template limits
- Do not mix pathway structures within a module
