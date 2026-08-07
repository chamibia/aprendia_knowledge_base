# MODULE: TWB_M1_UTWB — Understanding Teacher Wellbeing & Stress

## MODULE METADATA

```yaml
module_id: TWB_M1_UTWB
title: Understanding Teacher Wellbeing & Stress
pathway: steady_path
fallback_trigger: user_requests_example
fallback_pathway: empathy_arc
duration_target: 6 minutes
unlock_requires: null
unlocks: TWB_M2_BRM
quiz_pass: 2_of_3              # per-module: ≥2 of 3 correct
course_pass_threshold: 0.80    # course-level; explain depth (system prompt §9)
quiz_retry_allowed: true
grade_levels: Primary 1-6 (teachers)
subject: Teacher Wellbeing
```

---

## LEARNING OBJECTIVES

- Teachers recognize how stress affects thinking, emotions, and teaching behaviors in crisis settings
- Teachers distinguish between stressors they can influence and those they cannot, reducing blame and overload
- Teachers practice one small, protective action to protect wellbeing

---

## MODULE RULES

- This module is about understanding wellbeing and stress, not fixing everything
- Reinforce that stress reactions are normal, not a personal failure
- Reinforce that one small change is enough; teachers do not need to use all strategies at once
- Consistently guide teachers back to distinguishing what they can control and what they cannot
- If a teacher expresses extreme distress, hopelessness, inability to function, or thoughts of harming self or others, shift away from self-reflection prompts and trigger safeguarding guidance

---

## DELIVERY INSTRUCTIONS

**Pathway:** `steady_path` (see Global Pathway Instructions for full execution spec)

**Flow:** INTRO → STRATEGIES (Reflection #1 after STRAT2, Reflection #2 after STRAT4) → RECAP → QUIZ

**Chunking rules:**
- Each message ≤4 sentences OR ≤400 characters
- Wait for user response after each reflection prompt
- One strategy per message (never combine)
- Emphasize understanding and normalization over coping "solutions"
- **Do NOT deliver concepts as separate content**—use them to guide tone and framing only

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Concepts are overarching and apply across strategies. Use them to guide how you frame and deliver the strategies—tone, emphasis, why it matters—but never present concepts as separate content. The user sees only strategies.

### TWB_M1_CON1 — Wellbeing Shapes Teaching Quality

Teacher wellbeing influences patience, decision-making, and classroom climate. When teachers feel overwhelmed or exhausted, it becomes harder to respond calmly or create predictable learning environments. Understanding this connection helps teachers see wellbeing as part of teaching, not separate from it.

### TWB_M1_CON2 — Stress Impacts the Brain

High or prolonged stress can push the brain into "survival mode," reducing focus, flexibility, and emotional regulation. This response is normal in crisis-affected settings and explains why even experienced teachers may feel reactive or foggy sometimes. Recognizing this helps teachers respond to stress with compassion rather than blame.

### TWB_M1_CON3 — Control Reduces Emotional Load

Not all stressors can be changed immediately. Stressors like delayed salaries or overcrowded classrooms are often outside a teacher's control. Stress increases when teachers try to solve what is outside their control. Wellbeing improves when teachers focus energy on what they can influence.

---

## STRATEGIES (User-facing)

### TWB_M1_STRAT1 — Notice Stress Signals

**Description:** At least once per day, pause briefly to identify tension, emotions, and energy levels.

**Expanded explanation:** Stress often builds gradually. Many teachers only notice stress when patience is gone or exhaustion has set in. Stress signals such as tight shoulders, headaches, irritability, shallow breathing, or mental fog are not signs of weakness; they are information.

**Examples / Variations:**
- Body scan before class begins
- End-of-day energy check
- Silent emotion naming

**Reflection prompt:** What signals in your body or behavior tell you that you are becoming stressed?

---

### TWB_M1_STRAT2 — Mental Reset

**Description:** Use a 1-minute grounding practice (e.g., deep breaths) when feeling overwhelmed, or before beginning a lesson.

**Expanded explanation:** The purpose is not deep relaxation, but interruption—creating a brief pause before stress escalates further. Simple grounding actions such as slow breathing or feeling your feet on the floor can signal safety to the body and help regain focus.

**Examples / Variations:**
- Breathe in count to 4, breathe out count to 6. Repeat 2–3x.
- Place hands flat on desk, feet flat on ground. Notice the structure holding you.
- Name one thing you can see, hear, feel (5 senses).
- Brief pause with eyes closed.

**Reflection prompt:** When would a one-minute reset help most during your day?

---

### TWB_M1_STRAT3 — Understand Stressors

**Description:** List two stressors "within my control" and two "outside my control," then choose one constructive response for each.

**Expanded explanation:** By naming stressors in this way, teachers can redirect energy toward what is realistically possible. For stressors outside control, the goal is not solving the problem, but choosing supportive responses (grounding, simplifying expectations, reaching out to a colleague, or taking a short pause).

**Examples / Variations:**
- Two-column list: Out of my control / In my control
- Delayed salary → grounding breath and colleague chat; large class → simplified lesson plan; no materials → adapt with local objects

**Reflection prompt:** Which stressor drains you the most right now and what can you do to support yourself?

---

### TWB_M1_STRAT4 — Micro Wellbeing Moments

**Description:** Identify 2–3 short actions (e.g., stretching, drinking water, stepping outside, eye rest) to promote wellbeing during the day.

**Expanded explanation:** In busy, high-stress environments, long breaks are often unrealistic. Micro wellbeing moments focus on prevention—short actions that help regulate energy and release tension. While small, they add up when repeated throughout the day.

**Examples / Variations:**
- Shoulder roll between lessons
- Drink water between lessons
- Step outside briefly during breaks
- Rest eyes for 20 seconds

**Reflection prompt:** What small wellbeing action feels most doable today?

---

## REFLECTION PROMPTS

> **Agent:** Use these prompts at the specified points. Wait for user response before continuing.

| Step | Prompt |
|------|--------|
| Reflection #1 (after STRAT2) | What signals in your body or behavior tell you that you are becoming stressed? |
| Reflection #2 (after STRAT4) | Which of these four strategies would you try first—or what stands out to you from what we covered? |

---

## RECAP

> **[Deliver: 2–3 sentences summarizing key takeaways]**

You learned how stress affects teaching, that stress reactions are normal, and that distinguishing what you can control from what you cannot reduces overload. You also explored four small actions: noticing stress signals, mental reset, understanding stressors, and micro wellbeing moments. One small change is enough. Before we move on, let's check what stuck with a few quick questions.

**⚠️ HARD RULE:** The mini-quiz below is mandatory and comes immediately after this recap, before anything else. Do not transition to Module 2, preview its content, or end the module here. Module 2 is locked until this quiz is passed.

---

## 7. Quiz Questions

> **Deliver exactly one item per type, in this fixed order: Q1 recall → Q2 understanding → Q3 application. User must get ≥2 of 3 correct to pass. If an answer is incorrect, offer one retake using a different item of the same type from this bank — never re-ask the same question.**

#### Question 1: Recall

- **Which of the following is an early stress signal for many teachers?**
  - Options: Forgetting lessons / Tight shoulders / Feeling calm and focused / Having extra energy

- **Which stressor is usually outside a teacher's control?**
  - Options: Choosing a calming response / Planning a lesson goal / Delayed salary payments / Taking a short pause

- **Which action best fits a "micro wellbeing moment"?**
  - Options: Taking a full day off / Stretching shoulders between lessons / Attending a training workshop / Writing a long reflection

#### Question 2: Understanding

- **What is one benefit of pausing?**
  - Keywords: calm, focus, reduce anxiety

- **Why does identifying what is in your control reduce stress?**
  - Keywords: focus, energy, action, reduce frustration

- **How can a short mental reset support teachers during stress?**
  - Keywords: pause, calm, focus

#### Question 3: Application

- **Scenario 1:**
  A teacher notices they feel impatient and distracted by the middle of the school day, but they usually ignore these feelings. The teacher wants to better understand their stress earlier.
  *What is a small action the teacher can take during the middle of the day?*

- **Scenario 2:**
  A teacher feels frustrated about large class sizes and their delayed salary. The teacher wants to reduce this stress and focus their energy more effectively.
  *How can the teacher reframe their situation to protect their wellbeing?*

- **Scenario 3:**
  A teacher feels overwhelmed before the start of reading class and notices their heart is beating fast. They want to calm themselves so they can continue with the lesson.
  *What could the teacher do to support themself in that moment?*
