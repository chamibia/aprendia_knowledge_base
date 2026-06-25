# Course Instruction – Classroom Management (also known as Healing Classrooms)

**Course ID:** `HC_COURSE_01`

---

## 1. Course Manifest

| Field | Value |
|-------|-------|
| **Title** | Classroom Management |
| **Description** | A short, sequential course supporting teachers in crisis-affected, low-resource settings to prevent behavior challenges and create calm, inclusive, and engaging classrooms. Module 1 builds safety and predictability (required) → Module 2 strengthens belonging and respect (required). Completion of Modules 1-2 unlocks two additional deep dive modules that are optional and can be completed in any order: Module 3 deepens peer relationships and support, Module 4 focuses on engagement, inclusion, and learning readiness. This course emphasizes prevention, consistency, and teacher calm over punishment and control. |
| **Target Experience** | Beginner to experienced |
| **Target Tech Literacy** | Low to medium |
| **Teaching Context** | Crisis-affected, low-resource |
| **Typical Class Size** | 40–100 students |
| **Known Constraints** | Overcrowding, mixed-age classes, limited materials, high stress, limited time, limited professional support |

### Learning Objectives

- Establish predictable routines and responses that help students feel safe and ready to learn.
- Build belonging, responsibility, and respect through inclusive classroom practices.
- Use structured peer interaction to reduce conflict and expand learning support.
- Increase engagement and learning readiness to prevent disruption before it starts.

### Pedagogical Frame

This course builds classroom management fluency through clear routines, modeling, inclusive participation, and structured peer interaction. Emphasis is on prevention, emotional safety, and easy-to-use practices that reduce stress and support wellbeing for both teachers and students while improving learning environments.

### Design Scope

- **Includes:** routines, constructive rules, consistent and safe consequences, calm teacher responses, belonging, teacher language, peer support, engagement, differentiation, active learning.
- **Excludes:** corporal punishment, exclusionary discipline, public shaming, behavior ranking systems, or compliance-only approaches.

### Microlearning Contract

| Constraint | Value |
|------------|-------|
| Per-interaction time cap | 90–120 seconds |
| Each module total | ≤12–15 minutes |
| Input types | Buttons, short text (≤25 words), quick polls, scenario choices, brief reflections |
| End-of-module quiz (M1–M3) | 3 items: recall → understanding → application; pass = 2 of 3; 1 retake per item; see **End-of-module quizzes (system prompt §9)** under §1 and `system_prompt.md` §9 |

### Tone Guidance

Calm, practical, and respectful. Emphasize prevention over correction. Normalize classroom challenges without blaming teachers or students. Reinforce teacher authority through consistency and care, not punishment.

### End-of-module quizzes (system prompt §9)

| Rule | Detail |
|------|--------|
| **Structure** | **3 items** per module (where a quiz applies), fixed order: **Q1 recall** (MC/TF) → **Q2 understanding** (open-ended; hidden keywords) → **Q3 application** (scenario) |
| **Pass module / unlock** | **≥2 of 3** correct; up to **1 retake per item** (new question, same type, alternate items). See `quiz_rationale.md` |
| **Course pass** | **≥80%** of all quiz items in the course for course pass and explain-style depth; system prompt §9 and module `course_pass_threshold` govern details |
| **Module YAML** | `quiz_pass: 2_of_3` and `course_pass_threshold: 0.80` in module files; legacy `quiz_threshold: 0.80` = course-level only if still present |
| **Key Concepts** | For agent only; not for quiz copy (§9) |

M4 (plan + PDF) does not use the same end quiz pattern; see that module’s completion row.

### AI Guidance Notes

- **Concepts vs Strategies:** Module content includes both **concepts** (e.g. "Routines create safety") and **strategies** (e.g. "Daily Routine & Agenda"). **Concepts are for AI reference only—do NOT show them to the user.** Use concepts to guide tone, emphasis, and framing. **Strategies are what users see**—deliver them through examples, stories, and actions. Never present concepts as separate content or labels.
- Do not recommend punitive, violent, or exclusionary discipline.
- Always frame behavior as communication, not defiance.
- Reinforce consistency and predictability as stress-reducing.
- If frustration or overwhelm appears, slow pacing and emphasize one small shift.
- Use teacher voice examples after no more than two reflections.

---

## 2. Level Structure & Unlock Rules

**Structure overview:**
- **Core modules (required):** Module 1, Module 2 — must be completed in order
- **Deep Dives (optional):** Module 3, Module 4 — unlock after Module 2; can be completed in any order

### Module 1 – Creating Safety & Predictability

| Field | Value |
|-------|-------|
| **Module ID** | `HC_M1_CSP` |
| **Purpose** | Establish routines, consistency, and calm responses; must complete to unlock Module 2 |
| **Time** | ≤12–15 minutes total |
| **Pathway** | `steady_path` |
| **Completion** | Mini-quiz (3 items, fixed order: recall → understanding → application); pass = ≥2 of 3; 1 retry per item with alternative items; see system prompt §9 |

**Strategies (must include all; fixed order; bot may vary examples):**

1. Daily Routine & Agenda
2. Morning Greeting
3. Teacher Modeling
4. Co-Create Classroom Rules
5. Consistent, Non-Violent Consequences
6. Calm Teacher Responses

> **Strategy delivery guidance:**
>
> - Do not include punitive, violent, or exclusionary discipline examples.
> - Prioritize prevention over reaction to challenging behavior.
> - Reinforce the importance of consistency when establishing routine and how predictability reduces stress.
> - When introducing co-creating classroom rules, always encourage the teacher to make the rules positive (positive phrasing like "Be a good listener" is more effective than negative phrasing like "Do not speak while others are talking").

---

### Module 2 – Building Belonging & Respect

| Field | Value |
|-------|-------|
| **Module ID** | `HC_M2_BBR` |
| **Purpose** | Increase inclusion, responsibility, and positive behavior; must complete to unlock Deep Dives (M3 & M4) |
| **Time** | ≤12–15 minutes total |
| **Pathway** | `empathy_arc` |
| **Completion** | Mini-quiz (3 items, fixed order: recall → understanding → application); pass = ≥2 of 3; 1 retry per item with alternative items; see system prompt §9 |

**Strategies (must include all; bot may vary examples):**

1. Meaningful Classroom Jobs
2. Whole-Class Responses
3. Specific Positive Feedback
4. Goal Setting
5. Respectful Language for All

> **Strategy delivery guidance:**
>
> - Avoid ranking or public comparison between students.
> - Support positive behavior without using punishment or shame.
> - Reinforce that small moments of inclusion matter.
> - Classroom jobs should be safe, equitable, non-exploitative, and appropriate. They should never cause harm or compromise learning.

---

### Deep Dives (M3–M4)

> **IMPORTANT:** Modules 3 and 4 are **Deep Dives**. They unlock simultaneously after Module 2 completion. The user may complete them in any order. Present the Deep Dive menu after Module 2 so the user can choose which to do first.

| Module ID | Name | Pathway | Time | Completion |
|-----------|------|---------|------|------------|
| `HC_M3_RPS` | Relationships & Peer Support | `steady_path` | ≤12–15 min | Mini-quiz: ≥2 of 3 (1 retry) |
| `HC_M4_EILR` | Engagement, Inclusion & Learning Readiness | `steady_path` | ≤12–15 min | Plan completeness + PDF generation |

**Unlock:** Both Deep Dives unlock after Module 2 completion (no fixed order between M3 and M4)

**Completion per Deep Dive:** Mini-quiz: ≥2 of 3 to pass (see system prompt §9) for M3; plan completeness + PDF for M4. Course completes when both Deep Dives are done.

---

### Module 3 – Deep Dive: Relationships & Peer Support

| Field | Value |
|-------|-------|
| **Module ID** | `HC_M3_RPS` |
| **Type** | **Deep Dive** (optional; unlocks with M4 after M2) |
| **Purpose** | Reduce conflict and expand learning through structured peer interaction |
| **Time** | ≤12–15 minutes total |
| **Pathway** | `steady_path` |
| **Completion** | Mini-quiz (3 items, fixed order: recall → understanding → application); pass = ≥2 of 3; 1 retry per item with alternative items; see system prompt §9 |

**Strategies (must include all; fixed order; bot may vary examples):**

1. Structured Groups
2. Mixed-Ability Grouping
3. Turn-and-Talk
4. Structured Peer Support
5. Connect Lessons to Children's Lives

> **Strategy delivery guidance:**
>
> - Peer interaction examples must emphasize safety, respect, and emotional regulation.
> - Do not include competitive, shaming, or exclusionary peer practices.
> - Encourage the teacher to model the behavior before asking students to do it independently.
> - Emphasize that teachers should move around the room and observe students during group or pair work.
> - Never suggest that students support each other at the expense of their own learning.
> - When introducing strategies for grouping and peer support, remind the teacher that peer interactions should never position one student as more powerful or smarter than the other. Peer support should encourage positive relationship building, collaboration, and shared learning.

---

### Module 4 – Deep Dive: Engagement, Inclusion & Learning Readiness

| Field | Value |
|-------|-------|
| **Module ID** | `HC_M4_EILR` |
| **Type** | **Deep Dive** (optional; unlocks with M3 after M2) |
| **Purpose** | Prevent disruption and support wellbeing through engagement, clarity, and accessibility |
| **Time** | ≤12–15 minutes total |
| **Pathway** | `steady_path` |
| **Completion** | Confirm plan completeness; generate and offer Classroom Management Plan PDF; optional revision prompt ("Is there anything you'd like to edit?"). Plan generated OR teacher confirms plan is usable. |

**Strategies (must include all; bot may vary examples):**

1. Multiple Ways to Respond
2. Simple Teaching Aids
3. Different Types of Questions
4. Movement-Based Learning
5. Clear Learning Goals

> **Strategy delivery guidance:**
>
> - Emphasize prevention, not correction.
> - Reinforce accessibility for mixed-age and mixed-language classrooms.
> - If teachers use manipulatives or teaching aids from the environment, they must be safe and appropriate.
> - When using movement-based learning strategies, students should have space to move their body without physically hurting themselves or another student.

---

## 3. Personalization & Adaptation Rules

**Signals the bot should track:**

- prior_module_completion
- reflection_length
- emotional_tone
- resistance_signals ("too much," "not helpful," "no time," "too hard," "won't work")

**Adaptation heuristics (within the assigned pathway, not for changing pathways):**

| Condition | Response |
|-----------|----------|
| High stress language | Slow pacing, normalize challenges, and emphasize one small action. |
| Short responses | Simplify prompts, keep choices small, and check understanding. |
| Resistance to planning | Reduce prompts, simplify choices, and offer smaller, low-effort actions. |
| Repeated discouragement | Emphasize normalization over motivation; acknowledge effort before suggesting next steps. |

---

## 4. Module Construction Schema

- Each module uses one learning pathway for the full module.
- Pathway must be loaded at module start and stay consistent.
- Strategy flows must strictly follow pathway definitions.

**Pathway flows:**

| Pathway | Flow |
|---------|------|
| `steady_path` | explanation → example → reflection → check |
| `empathy_arc` | story → normalize → prompt → response → takeaway → check |

**General requirements:**

- Modules must include clear title, metadata, and pathway_type.
- Each strategy must use the exact flow steps defined by the chosen pathway.
- Reflection and comprehension checks follow the rules of that pathway.
- Modules must respect time limits.
- The mini-quiz at module end must include 3 items; pass with ≥2 of 3 correct (see system prompt §9).
- Examples and practice prompts should be localized when possible.
- Language must remain simple and non-clinical.
- All content must respect time, message, and WhatsApp template limits.

---

## 5. Assessments & Unlocks

| Unlock | Requirement |
|--------|-------------|
| Module 1 unlock → Module 2 | 3-item quiz: ≥2 of 3; one retry. |
| Module 2 unlock → Deep Dives (M3 & M4) | 3-item quiz: ≥2 of 3; one retry. Both M3 and M4 unlock simultaneously; user may complete in any order. |
| Module 3 completion | Mini-quiz: ≥2 of 3; one retry. |
| Module 4 completion | Plan completeness + PDF. Course completion when both Deep Dives are done. |

---

## 6. Safety/Feasibility Constraints

- Do not request names or identifying details.
- Avoid shaming, ranking, or public correction.
- Avoid deep emotional probing.
- Never suggest corporal punishment or exclusion.
- Keep teacher authority framed as calm, consistent leadership.
- Never imply peer support replaces professional help.
- Keep all actions no-cost, private, and optional.

**If a user expresses any of the following, pause content delivery and trigger safeguarding guidance:**

- Hopelessness
- Emotional shutdown
- Harm-related thoughts
