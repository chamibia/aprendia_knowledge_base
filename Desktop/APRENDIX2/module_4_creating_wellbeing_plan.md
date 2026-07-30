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
- **Save the final plan text to the `wellbeing_plan` user state field** (see system prompt §13). This is what makes the plan available under "My Teacher Wellbeing Plan" in the Classroom Toolkit — write it every time the plan is confirmed or revised here, so the Toolkit always reflects the latest version.
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

## 7. Quiz Questions

> **Agent:** Primary completion is plan confirmation. Quiz is optional reinforcement after plan is confirmed. Deliver exactly one item per type, in this fixed order: Q1 recall → Q2 understanding → Q3 application. If an answer is incorrect, offer one retake using a different item of the same type from this bank — never re-ask the same question.

#### Question 1: Recall

- **Which is a good planned wellbeing moment when feeling overwhelmed between lessons?**
  - Options: Writing a long reflection / A few belly breaths / Ignoring the feeling / Leaving school early

- **Which phrase reflects a growth mindset?**
  - Options: "I should already know this" / "This is hard, but I'm learning" / "I'm not cut out for this" / "There's no point in trying"

- **Regular self-assessment focuses on energy, emotions, physical tension, and workload.**
  - Options: True / False

#### Question 2: Understanding

- **Why is it helpful to plan wellbeing responses ahead of stressors?**
  - Keywords: ready, calm, effort, prepared

- **Why is connecting with colleagues important?**
  - Keywords: support, resilience, commiserating, sharing, friendship, advice, guidance

- **How can planning a low-effort peer connection support wellbeing?**
  - Keywords: community, encourage, support, understanding

#### Question 3: Application

- **Scenario 1:**
  A teacher has not received their salary for the month and is distracted with worry. They know this is out of their control and want to manage this stress so it does not affect their teaching.
  *How can they use the stressor and response strategy in this situation?*

- **Scenario 2:**
  A teacher has back to back lessons every morning and starts to lose patience with each lesson. They have less than two minutes before the next group of students arrives for class.
  *How could the teacher use a wellbeing moment to reset?*

- **Scenario 3:**
  A teacher tried a new classroom activity that did not go as planned and keeps thinking "I am not a good teacher." They want to stop this thinking before it affects their confidence.
  *What could the teacher include in their wellbeing plan to support a moment like this?*
