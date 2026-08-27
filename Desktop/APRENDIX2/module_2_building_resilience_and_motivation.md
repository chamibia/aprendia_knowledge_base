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

## MEDIA OUTPUT

> **Agent:** When a row below applies, send the image **first** as `![](URL)` on its own line, then deliver the related content. Never skip an image listed here. Never send images not listed here.

| Trigger | When to send | Image |
| ------- | ------------ | ----- |
| **TWB_M2_STRAT2** | When delivering Scene 2 (Mindfulness Moment) | `![](https://i.imgur.com/wtLhRNS.jpeg)` |
| **TWB_M2_STRAT3** | When delivering Scene 3 (Motivation Check) | `![](https://i.imgur.com/mTrg9ND.jpeg)` |
| **TWB_M2_STRAT4** | When delivering Scene 3 (Mindset Reframe) | `![](https://i.imgur.com/lgF0KHT.jpeg)` |

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

**Per-scene delivery structure (apply to every strategy in every scene):**
1. Open with the strategy name and a relevant emoji (e.g. "💭 Name Emotions"). This is the first line of the message.
2. Deliver the narrative scene — a story showing the strategy in action (3–4 sentences, plain text, no definitions).
3. Add one short sentence on how this strategy helps in the classroom (practical benefit — not a definition).
4. Ask the reflection question for that scene. Wait for the teacher's response before moving to the next scene.

Use `<break>` tags between steps if the combined message exceeds 400 characters. Never skip or compress any of the four steps. Scene 3 has 2 strategies — deliver one per message; do not compress into one turn.

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

**Description:** Use short statements that identify feelings ("feeling overwhelmed," "feeling discouraged") to reduce intensity and guide responses.

**Expanded explanation:** Emotions strongly influence motivation and energy. Naming emotions using simple words ("discouraged," "frustrated," "tired," "overwhelmed," "excited") helps teachers understand what they are experiencing rather than pushing feelings aside. Over time, this practice reveals patterns: certain situations may consistently lower motivation, while others restore it. Naming emotions also creates space between the feeling and the response, so instead of reacting automatically, teachers can pause and choose how to proceed. This supports emotional resilience and helps teachers protect their energy. This strategy is not about fixing emotions or forcing positivity, but rather understanding emotional experiences so they can guide decisions about boundaries, support, and self-care.

**Examples / Variations:**
- Silent emotion naming
- End-of-day emotion check
- Connecting with a colleague

**Reflection prompt:** What emotions show up most often during your day?

**Teacher Voice:** "When I name it, it feels easier to manage."

---

### TWB_M2_STRAT2 — Mindfulness Moment

📷 Send this image first, then deliver Scene 2:
![](https://i.imgur.com/wtLhRNS.jpeg)

**Description:** Select a brief mindfulness activity (e.g. Belly Breathing or Contract & Release) to settle the mind and body.

**Expanded explanation:** Mindfulness can be used to restore perspective. Short mindfulness practices (e.g. slow breathing or gentle body awareness) can help teachers step back from discouragement and reconnect with steadiness and purpose. This can be especially helpful when motivation feels low or challenges feel endless. Mindfulness supports teachers in noticing thoughts and emotions without being overwhelmed by them. Even one or two minutes can help shift perspective, reduce mental noise, and create enough clarity to continue teaching with intention. These practices are quiet, flexible, and require no materials, making them realistic even for busy school days.

**Examples / Variations:**
- Belly breathing
- Contract and release muscles
- Focus on one sound

**Reflection prompt:** Which mindfulness practice helps you regain calm and perspective?

**Teacher Voice:** "Having a mindfulness moment helps me pause and see things more clearly."

---

### TWB_M2_STRAT3 — Motivation Check

📷 Send this image first, then deliver Scene 3:
![](https://i.imgur.com/mTrg9ND.jpeg)

**Description:** Identify one daily moment that strengthens purpose or hope (e.g. a child's progress or a small success).

**Expanded explanation:** Motivation often grows from noticing small, meaningful moments rather than waiting for major changes. In crisis-affected contexts especially, progress may feel slow or difficult to see. Identifying small motivators helps teachers anchor motivation in daily experiences, such as a child's effort, a moment of connection, or completing a challenging task. By intentionally noticing these moments, teachers counter discouragement and remind themselves why their work matters. Over time, this practice builds a sense of purpose that does not depend on constant energy or ideal conditions. The goal is not to ignore difficulties, but to balance them with reminders of meaning and impact.

**Examples / Variations:**
- Notice progress
- End-of-day reflection
- Write one positive moment each day
- Share a small win with a colleague

**Reflection prompt:** What gave you a sense of purpose today?

**Teacher Voice:** "Small wins remind me why I teach."

---

### TWB_M2_STRAT4 — Mindset Reframe

📷 Send this image first, then deliver Scene 3:
![](https://i.imgur.com/lgF0KHT.jpeg)

**Description:** Replace discouraging thoughts with growth-oriented alternatives (e.g. "This is challenging, but I can improve with practice").

**Expanded explanation:** Stress and fatigue can trigger negative thoughts (e.g. "I'm not good enough" or "This will never improve"). These thoughts drain motivation and increase burnout. Mindset reframing helps teachers respond to challenges with persistence and self-compassion rather than self-criticism. Growth-oriented statements (e.g. "This is difficult, but I am learning," "I can improve with practice") reinforce the idea that effort leads to growth over time. This mindset helps teachers stay engaged, adapt strategies, and continue learning even when conditions are hard. Over time, reframing supports a professional identity rooted in growth.

**Examples / Variations:**
- Personal mantra (e.g. "I can do hard things")
- Journaling
- Coping ahead: think of an upcoming stressor and reframe it as an opportunity and/or plan a coping strategy

**Reflection prompt:** What can you tell yourself when you need to persevere through challenges?

**Teacher Voice:** "Reframing helps me be kinder to myself and keep trying."

---

## 7. Quiz Questions

> **Deliver exactly one item per type, in this fixed order: Q1 recall → Q2 understanding → Q3 application. User must get ≥2 of 3 correct to pass. If an answer is incorrect, offer one retake using a different item of the same type from this bank — never re-ask the same question.**

#### Question 1: Recall

- **Over time, naming emotions helps teachers notice:**
  - Options: Which emotions are acceptable / Emotional patterns that impact energy and motivation / How to avoid hard feelings / Which emotions to ignore

- **Which statement reflects a growth mindset?**
  - Options: "I should already know how to do this" / "If this is hard, I must be bad at my job" / "This is difficult, but I can improve with practice" / "There's no point in trying"

- **A motivation check focuses on big achievements only.**
  - Options: True / False

#### Question 2: Understanding

- **What can mindfulness support?**
  - Keywords: calm, focus, perspective, balance

- **How does naming emotions support motivation?**
  - Keywords: awareness, patterns, response

- **How can an end-of-day reflection support a growth mindset?**
  - Keywords: effort, improvement, notice positive

#### Question 3: Application

- **Scenario 1:**
  During a math lesson, several students begin talking and not following directions. The teacher notices they are about to raise their voice.
  *How might naming the emotion change the teacher's reaction?*

- **Scenario 2:**
  At the end of a long day, a teacher feels discouraged and believes their lessons did not go well. Then, they remember that one student who usually struggles in reading class decoded a new word.
  *How could the teacher use this moment for motivation?*

- **Scenario 3:**
  Right before starting a reading lesson, the teacher feels overwhelmed after a noisy transition back from break. They are struggling to focus and give instructions clearly.
  *What could the teacher do to reset and continue the lesson?*
