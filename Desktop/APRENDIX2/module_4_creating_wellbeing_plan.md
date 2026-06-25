# MODULE: TWB_M4_CWP — Creating a Wellbeing Plan

## MODULE METADATA

```yaml
module_id: TWB_M4_CWP
title: Creating a Wellbeing Plan
pathway: explain_exchange
fallback_trigger: user_struggles_with_socratic
fallback_pathway: steady_path
duration_target: 12-15 minutes
unlock_requires: TWB_M3_BRB (prior module quiz: ≥2 of 3)
unlocks: null
quiz_pass: 2_of_3              # per-module: ≥2 of 3 correct
course_pass_threshold: 0.80    # course-level; explain depth (system prompt §9)
quiz_retry_allowed: true
grade_levels: Primary 1-6 (teachers)
subject: Teacher Wellbeing
```

---

## DELIVERY INSTRUCTIONS

**Pathway:** `explain_exchange` (see Global Pathway Instructions for Socratic flow). Fallback to `steady_path` if user struggles with dialogue.

**When using explain_exchange:** Lead with questions about wellbeing planning. Draw out the five components (Wellbeing Moments, Stressors/Responses, Growth Mindset Reminder, Weekly Check-In, Peer Connection) through Socratic dialogue—do not deliver them as a checklist. After dialogue, summarize the teacher's plan and offer PDF if applicable.

**When fallback is steady_path:** Use the DIY_KIT FLOW and BUILD COMPONENTS below to co-create the plan step by step.

---

## LEARNING OBJECTIVES

- Teachers create a simple, personalized wellbeing plan that fits their daily routines
- Teachers identify supportive responses for common stressors and difficult moments
- Teachers strengthen resilience by planning for a growth mindset and peer connection

---

## MODULE RULES

- Reinforce that the plan should be short, personal, and usable—not perfect or comprehensive
- Plan with the teacher, offering prompts and examples; don't dictate content
- Encourage the teacher to choose a small number of actions to keep the plan manageable
- Guide co-creation, not explanation; use structured prompts and sentence stems
- Limit choices to prevent overload
- If the teacher expresses hopelessness, emotional distress, or thoughts of harm to self or others, pause plan-building and trigger safeguarding guidance

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Use them to guide how you co-create the tool—tone, emphasis, what to include. The user receives a practical plan they can use.

### TWB_M4_CON1 — Planning Supports Action

Wellbeing strategies are more likely to be used when planned in advance. A simple plan reduces decision-making during stressful moments and makes supportive actions easier to recall when energy is low.

### TWB_M4_CON2 — Small Plans Are More Sustainable

Plans that are short and realistic are more likely to be used over time. A few well-chosen actions can have more impact than a long list that feels overwhelming or unattainable.

### TWB_M4_CON3 — Preparation Builds Resilience

Preparing for difficult moments before they happen helps teachers respond with care rather than react under pressure. This strengthens emotional resilience and protects wellbeing over time.

---

## DIY_KIT FLOW

> **Agent:** Follow the diy_kit pathway. Co-create a personalized Wellbeing Plan with the teacher. Flow: INTRO → CONTEXT_CHECK → BUILD_STEPS (Reflection #1 mid-build) → REFINEMENT → FINAL_PLAN → Reflection #2 → CONFIRMATION & PDF

### TOOL OPTIONS

The primary tool is a **Wellbeing Plan**. Offer focus based on user preference:

| Focus | Description |
|-------|-------------|
| **Full Wellbeing Plan** | All 5 components. Best when user wants comprehensive coverage. |
| **Daily Moments Focus** | Emphasize Wellbeing Moments + Stressors/Responses + Growth Reminder. For users who want in-the-moment support. |
| **Weekly Structure Focus** | Emphasize Weekly Check-In + Peer Connection + Stressors/Responses. For users who want routine and connection. |

### CONTEXT CHECK QUESTIONS

Ask 1–2 questions before building. Wait for response.

- What is a common stressful moment during your day?
- When do you feel most stretched—mornings, between lessons, or after school?
- Do you have regular contact with a colleague, or is connection limited?
- What kind of plan feels most doable: short daily reminders or a weekly check-in structure?

### BUILD COMPONENTS (from strategies)

Draw on these when constructing the plan. Adapt to user's context. Capture outputs in formats suitable for PDF generation.

- **Wellbeing Moments:** Sentence stems—"When I have 1 minute, I can…" / "When I have 5 minutes, I can…" / "When I feel overwhelmed, I can…" / "When I feel isolated, I can…" Brief, realistic actions (belly breathing, stretch, short walk, quiet pause).
- **Stressors and Responses:** Max 2–3 pairs. Match each stressor with one protective response (e.g., delayed pay → grounding & colleague connection; large class → simplified planning; fatigue → pause with water).
- **Growth Mindset Reminder:** Invite user to draft their own phrase first; offer suggestions if needed (e.g., "I can grow with practice," "Challenges help me improve"). One simple phrase only.
- **Weekly Wellbeing Check-In:** Rate energy, emotions, physical tension, workload (low/medium/high or 1–5). One thing that went well. One supportive action for next week.
- **Peer Connection Plan:** One low-effort, non-identifying habit. No colleague names—roles only (e.g., "Weekly message to one colleague," "Brief check-in with a teaching partner"). Remind users not to share names.

### REFLECTION PROMPTS

| Step | Prompt |
|------|--------|
| Reflection #1 (after step 2 or 3) | Would this work for you? |
| Reflection #2 (after Final Plan) | What might you change? |

### CONSTRAINTS

- **One build component per message.** Do not rush—allow the user to absorb each part before moving on.
- ≤2 required user inputs during build phase
- Final plan must be suitable for PDF generation (copy-paste ready, formatted)
- Always emphasize plans as support, not pressure
- Do not request names or identifying details (e.g., colleague names)

### END OF MODULE

- Confirm plan completeness with the teacher
- Generate and offer Wellbeing Plan PDF
- Optional revision prompt: "Is there anything you'd like to edit?"
- **Primary completion:** Plan generated and confirmed OR teacher confirms plan is usable

---

## STRATEGIES (Reference for Build)

> **Agent:** Use these when constructing the plan. Do not deliver as separate content—incorporate into the co-created tool.

### STRAT1 — Wellbeing Moments

Short actions for common situations. Sentence stems: "When I have 1 minute…" "When I have 5 minutes…" "When I am overwhelmed…" "When I feel isolated…" Examples: belly breathing, stretch, short walk, quiet pause, sip water. Plan ahead so actions are easy to recall when stressed.

### STRAT2 — Identify Stressors and Responses

Match 2–3 major stressors with one protective response each. Response can be emotional (grounding), practical (simplifying), or relational (colleague connection). Goal is not to eliminate stressors but to reduce their impact. Examples: delayed pay → grounding & colleague chat; large class → adjusted planning; fatigue → pause with water.

### STRAT3 — Growth Mindset Reminder

One simple phrase that reinforces learning, effort, and self-compassion. Invite user to draft first; offer suggestions if needed. Examples: "I can grow with practice," "Challenges help me improve." Include in plan for easy recall during difficult moments.

### STRAT4 — Weekly Wellbeing Check-In

Brief structured check-in. Rate: energy, emotions, physical tension, workload (simple scale). One thing that went well. One supportive action for next week. Notice trends without judgement; turn awareness into a gentle plan.

### STRAT5 — Peer Connection Plan

One low-effort way to connect with a colleague. No names—roles only. Examples: weekly "small win" message, short voice note, brief in-person check-in. Planning in advance reduces isolation and increases follow-through.

---

## QUIZ

> **Agent:** Primary completion is plan confirmation. Quiz is optional reinforcement after plan is confirmed. Deliver all 3 items if quiz is used. User must get **≥2 of 3** correct to pass the optional quiz (system prompt §9).

### QUIZ_ITEM_1

| Field | Value |
|-------|-------|
| **Type** | Multiple choice |
| **Question** | You feel overwhelmed transitioning between lessons. Which planned wellbeing moment fits best? |
| **Options** | A: Writing a long reflection / B: A few belly breaths / C: Ignoring the feeling / D: Leaving school early |
| **Correct** | B |
| **Feedback** | Brief, planned actions like belly breathing can help in moments of overwhelm. |

### QUIZ_ITEM_2

| Field | Value |
|-------|-------|
| **Type** | Multiple choice |
| **Question** | Which phrase reflects a growth mindset? |
| **Options** | A: "I should already know this" / B: "This is hard, but I'm learning" / C: "I'm not cut out for this" / D: "There's no point in trying" |
| **Correct** | B |
| **Feedback** | A growth mindset emphasizes learning and effort over fixed ability. |

### QUIZ_ITEM_3

| Field | Value |
|-------|-------|
| **Type** | Short answer (accept keywords) |
| **Question** | Why is it helpful to plan responses to stressors in advance? |
| **Accept keywords** | reduce, impact, intentional, recall, energy, decision |
| **Feedback** | Planning ahead reduces decision-making when stressed and makes supportive actions easier to recall. |

---

## QUIZ_BANK_ALT

> **Agent:** Use these items if retry is needed.

### ALT_ITEM_1

| Field | Value |
|-------|-------|
| **Question** | Why are small plans more sustainable? |
| **Accept keywords** | manageable, realistic, use, overwhelming, attainable |

### ALT_ITEM_2

| Field | Value |
|-------|-------|
| **Question** | Why is connecting with colleagues important for wellbeing? |
| **Accept keywords** | support, resilience, isolation, sharing, connection |

### ALT_ITEM_3

| Field | Value |
|-------|-------|
| **Question** | What does a weekly wellbeing check-in help teachers do? |
| **Accept keywords** | notice, patterns, awareness, trends, plan |
