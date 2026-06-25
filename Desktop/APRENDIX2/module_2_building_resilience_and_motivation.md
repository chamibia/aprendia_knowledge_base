# MODULE: TWB_M2_BRM — Building Resilience & Motivation

## MODULE METADATA

```yaml
module_id: TWB_M2_BRM
title: Building Resilience & Motivation
pathway: empathy_arc
fallback_trigger: user_expresses_confusion
fallback_pathway: steady_path
duration_target: 10 minutes
unlock_requires: TWB_M1_UTWB (prior module quiz: ≥2 of 3)
unlocks: TWB_M3_BRB
quiz_pass: 2_of_3              # per-module: ≥2 of 3 correct
course_pass_threshold: 0.80    # course-level; explain depth (system prompt §9)
quiz_retry_allowed: true
grade_levels: Primary 1-6 (teachers)
subject: Teacher Wellbeing
```

---

## LEARNING OBJECTIVES

- Teachers understand that motivation and energy naturally fluctuate in crisis-affected contexts
- Teachers identify small, meaningful moments that help sustain motivation and commitment to teaching
- Teachers use growth-oriented thinking to continue learning and adapting over time

---

## MODULE RULES

- Reinforce that low motivation is a normal response to prolonged stress and uncertainty, not a personal failure
- Do not push optimism over all else; emphasize meaning, effort, and persistence even when things are challenging
- Keep each strategy ≤2–3 minutes
- Avoid "stay positive" framing
- If a teacher expresses hopelessness, loss of meaning, or statements suggesting harm to self or others, pause the module and trigger safeguarding guidance

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Concepts are overarching and apply across strategies. Use them to guide how you frame and deliver the strategies in the narrative—tone, emphasis, why it matters—but never present concepts as separate content. The user sees only strategies in action.

### TWB_M2_CON1 — Resilience Supports Persistence

Resilience is the ability to continue teaching and caring after difficult moments, not the absence of stress or struggle. In crisis settings, resilience can mean finding ways to recover, refocus, and keep going without burning out.

### TWB_M2_CON2 — Motivation Naturally Fluctuates

Low motivation is a common response to prolonged stress, uncertainty, or fatigue. Recognizing this helps teachers avoid self-judgement and focus on rebuilding motivation gradually through small actions and meaningful moments.

### TWB_M2_CON3 — Growth Mindset Is Key

A growth mindset emphasizes learning, effort, and improvement over time. This mindset supports self-compassion and persistence when progress feels slow or conditions remain challenging.

---

## EMPATHY_ARC SCENE MAPPING

> **Agent:** Generate narrative scenes at runtime. **Show only strategies to the user.** Concepts guide your framing but are never delivered explicitly. Use this mapping to know which strategy belongs in each scene. **Pacing:** Scene 3 has 2 strategies—deliver one strategy per message; do not compress into one scene. Use `<break>` between them. Do not send Scene 2 and Scene 3 back-to-back; allow user to absorb each scene.

| Scene | Strategy | Concept (guides delivery; do not show) | Narrative brief |
|-------|----------|----------------------------------------|-----------------|
| Scene 1 | STRAT1 (Name Emotions) | CON1 | A teacher feels overwhelmed after a difficult morning. She pauses to name what she feels ("frustrated," "tired"). She notices a pattern—certain situations lower her energy. Naming creates space to choose her next step. Show the strategy in action—no concept definitions. |
| Scene 2 | STRAT2 (Mindfulness Moment) | CON2 | The same teacher (or another) feels low motivation. She does a brief mindfulness practice (e.g., belly breathing, contract and release). She regains perspective and recognizes that motivation fluctuates—and that's normal. Show the strategy in action. |
| Scene 3 | STRAT3 + STRAT4 (Motivation Check, Mindset Reframe) | CON3 | Weave together: she identifies one small meaningful moment from her day (a child's progress, a moment of connection). Then she reframes a discouraging thought ("I'm not good enough") with a growth-oriented alternative ("This is difficult, but I can improve with practice"). Show strategies in action—no concept definitions. |

---

## EMPATHY_ARC REFLECTION PROMPTS

> **Agent:** Use these prompts at the specified points. Wait for user response before continuing.

| Step | Prompt |
|------|--------|
| Reflection #1 (after Scene 1) | What emotions show up most often during your day? |
| Reflection #2 (after Scene 3) | What part of this story stood out to you? |

---

## STRATEGIES (Reference for Narrative)

> **Agent:** Use these when constructing the narrative. Do not deliver as separate content—embody them in the story scenes.

### TWB_M2_STRAT1 — Name Emotions

Use short statements that identify feelings ("feeling overwhelmed," "feeling discouraged") to reduce intensity and guide responses. Naming emotions helps teachers understand what they are experiencing, reveals patterns over time, and creates space between feeling and response. Examples: silent emotion naming, end-of-day emotion check, connecting with a colleague.

### TWB_M2_STRAT2 — Mindfulness Moment

Select a brief mindfulness activity (e.g., belly breathing, contract and release) to settle the mind and body. Short practices help restore perspective, reduce mental noise, and create clarity to continue teaching with intention. Examples: belly breathing, contract and release muscles, focus on one sound.

### TWB_M2_STRAT3 — Motivation Check

Identify one daily moment that strengthens purpose or hope (e.g., a child's progress or a small success). Motivation grows from noticing small, meaningful moments rather than waiting for major changes. Examples: notice progress, end-of-day reflection, write one positive moment, share a small win with a colleague.

### TWB_M2_STRAT4 — Mindset Reframe

Replace discouraging thoughts with growth-oriented alternatives (e.g., "This is challenging, but I can improve with practice"). Stress and fatigue can trigger negative thoughts; reframing helps respond with persistence and self-compassion. Examples: personal mantra ("I can do hard things"), journaling, coping ahead.

---

## QUIZ

> **Agent:** Deliver all 3 items (recall → understanding → application). User must get **≥2 of 3** correct to unlock the next module. Provide correct answer + 1-sentence explanation after each item. If not passed, offer one retry per item with alternate items from QUIZ_BANK_ALT (system prompt §9).

### QUIZ_ITEM_1

| Field | Value |
|-------|-------|
| **Type** | Multiple choice |
| **Question** | Over time, naming emotions helps teachers notice… |
| **Options** | A: Which emotions are acceptable / B: Emotional patterns that impact energy and motivation / C: How to avoid hard feelings / D: Which emotions to ignore |
| **Correct** | B |
| **Feedback** | Naming emotions over time reveals patterns that affect energy and motivation, helping teachers make more intentional choices. |

### QUIZ_ITEM_2

| Field | Value |
|-------|-------|
| **Type** | Short answer (accept keywords) |
| **Question** | What can mindfulness support? |
| **Accept keywords** | calm, focus, perspective, balance, clarity |
| **Feedback** | Mindfulness can support calm, focus, and perspective—helping teachers regain steadiness and clarity. |

### QUIZ_ITEM_3

| Field | Value |
|-------|-------|
| **Type** | Multiple choice |
| **Question** | Which statement reflects a growth mindset? |
| **Options** | A: "I should already know how to do this" / B: "If this is hard, I must be bad at my job" / C: "This is difficult, but I can improve with practice" / D: "There's no point in trying" |
| **Correct** | C |
| **Feedback** | A growth mindset emphasizes that effort and practice lead to improvement over time. |

---

## QUIZ_BANK_ALT

> **Agent:** Use these items if retry is needed.

### ALT_ITEM_1

| Field | Value |
|-------|-------|
| **Question** | A motivation check helps teachers remember that their work has _____, even when it's hard. |
| **Accept keywords** | meaning, purpose, value, impact, support |

### ALT_ITEM_2

| Field | Value |
|-------|-------|
| **Question** | What is one benefit of naming emotions? |
| **Accept keywords** | understand, pattern, space, choose, manage, intensity |

### ALT_ITEM_3

| Field | Value |
|-------|-------|
| **Question** | Why is a brief mindfulness moment helpful for teachers? |
| **Options** | A: It replaces the need for rest / B: It can help restore perspective and create clarity / C: It only works when stress is low / D: It requires special training |
| **Correct** | B |
