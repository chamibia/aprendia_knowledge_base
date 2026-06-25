# MODULE: AIL_M1_TTEAL — The Three Elements of Active Learning

## MODULE METADATA

```yaml
module_id: AIL_M1_TTEAL
title: The Three Elements of Active Learning
pathway: steady_arc
duration_target: ≤5 minutes
unlock_requires: null
unlocks: AIL_M2_ALA   # unlocks immediately on reflection response — no quiz
quiz_pass: none        # Module 1 has no quiz; see Course Instruction §Module 1
course_pass_threshold: 0.80
quiz_retry_allowed: false
grade_levels: Primary 1-6
subject: Active and Inclusive Learning
```

---

## LEARNING OBJECTIVES

- Teachers understand what active learning is and distinguish it from free play.
- Teachers can name the three elements of active learning as a planning framework.
- Teachers reflect on which element they feel most and least confident about.

---

## TEACHER MOTIVATIONS & PAIN POINTS

- "I do not have enough materials or resources for activities."
- "I feel pressure to lecture because it seems faster and easier to manage."
- "I have too much content to cover, but I want my students to enjoy learning."
- "I want my students to feel safe and confident enough to join classroom activities."

---

## MODULE RULES

- This module is foundational and informational — it does not deliver strategies.
- Concepts should be presented linearly and briefly. They establish the shared understanding teachers need before applying strategies in later modules.
- **Even though this module has no strategies, treat each concept exactly like a strategy delivery turn: one concept per message, then stop and wait for any user response before sending the next concept.**
- Address the free-play misconception directly in CON1 — this is a common barrier.
- Surface the three elements as a named, memorable framework in CON3.
- Keep every concept to 1 bot turn (≤4 sentences). This module is ≤5 minutes total.

---

## DELIVERY INSTRUCTIONS

**Pathway:** `steady_arc`

**⚠️ No mini-quiz for this module.** Module 2 unlocks immediately when the teacher responds to the closing reflection. Do not deliver a quiz.

**Flow:** INTRO → CON1 → CON2 → CON3 → CLOSING REFLECTION → unlock AIL_M2_ALA

**Bot behavior (step by step):**

1. Send intro message: "Before we look at how to make your lessons more active, let's make sure we understand what active learning is. This will only take about 5 minutes."
2. Wait for any acknowledgment, then deliver AIL_M1_CON1 (1 bot turn — address the free-play misconception).
3. Wait for any response, then deliver AIL_M1_CON2 (1 bot turn — why active learning matters, 2–3 sentences).
4. Wait for any response, then deliver AIL_M1_CON3 (1 bot turn — surface the three elements explicitly as a named framework).
5. Ask the closing reflection (see CLOSING REFLECTION section below). Wait for response.
6. Accept any response warmly. Acknowledge in 1–2 sentences. Store response as `weakest_element` signal for Module 2 personalization. Transition: "Let's move on to what this looks like in practice." Unlock Module 2 (AIL_M2_ALA) immediately.

**Chunking rules:**
- Each concept ≤4 sentences OR ≤400 characters
- One concept per message — never combine
- **After each concept, stop and wait for any user response before sending the next concept. Do not send CON2 in the same turn as CON1, and do not send CON3 in the same turn as CON2.**
- Deliver in order: CON1 → CON2 → CON3
- Do not insert reflection prompts between concepts — one closing reflection only

---

## CONCEPTS

### AIL_M1_CON1 — What Active Learning Is and Isn't

**Key distinction to surface:** Not all classroom activity is active learning. Free play lets children explore without a goal (e.g. "Go outside for break"). Active learning is purposeful and teacher-guided — every game, movement, or discussion is designed to reach a specific learning objective (e.g. "Walk around the room, find the letter card, and practice the sound with a partner"). Active learning is not free time — it is a purposeful method for delivering the curriculum children are already learning.

**Teacher Voice:** "I used to think active learning meant letting students play. Understanding that it still has a clear goal changed how I plan."

---

### AIL_M1_CON2 — Why Active Learning Matters

**Key point to surface:** Children's brains learn better when they are actively doing — not passively listening. In large, low-resource, or crisis-affected classrooms, active learning supports both understanding and wellbeing. It does not require special materials or a perfectly managed classroom — small, purposeful shifts make a real difference.

**Teacher Voice:** "Even small moments of participation help my students feel included and stay focused."

---

### AIL_M1_CON3 — The Three Elements of Active Learning

**Surface explicitly as a named, memorable framework — number each element clearly:**

Every active learning lesson has three core elements:

1. **A clear learning objective** — Students know what they are learning and why. Every activity connects to a specific goal.
2. **Active engagement with peers and/or materials** — Students think, discuss, explore, or create — not just listen. Local objects, movement, and peer interaction are all tools.
3. **A positive, safe, inclusive environment** — Students feel confident enough to participate, make mistakes, and take risks. Every child has a way to join in.

These three elements work together in any lesson, any subject, and any grade level — even in a crowded, low-resource classroom.

---

## CLOSING REFLECTION

> **Agent:** After delivering CON3, ask this question. Wait for the teacher's response before proceeding. Accept any answer warmly — do not score or evaluate.

**Prompt:** "Think about a lesson you taught recently. Which of the three elements do you feel most confident about — and which would you most like to strengthen?"

**On response:**
- Acknowledge warmly in 1–2 sentences (affirm what they named; do not correct or evaluate).
- Store the teacher's answer as `weakest_element` signal for Module 2 personalization (see Course Instruction §3 Personalization & Routing Rules).
- Transition: "Let's move on to what this looks like in practice."
- **Unlock Module 2 (AIL_M2_ALA) immediately.**

---

## REFERENCE CONTENT (Agent Use Only)

> The following expanded content supports the concepts above. Use it to inform tone, generate examples, and respond to teacher questions — but do not deliver it as separate content blocks. Each concept must remain ≤4 sentences in delivery.

**On CON1 (Clear Learning Objective):**
Learning objectives do not need to be long or complicated. They are simple "I can…" statements describing what students should be able to do by the end of a lesson (e.g. "I can write the names of the plane shapes" or "I can match the word to the picture card"). Clear objectives help teachers think creatively about playful activities that support learning, ensuring lessons are engaging and academically meaningful.

**On CON2 (Why It Matters):**
Active engagement allows students to think, question, practice, discuss, explore, and apply ideas in meaningful ways. Playful learning experiences help students stay motivated throughout a lesson. In stressful environments, being actively engaged also supports emotional safety and a sense of belonging.

**On CON3 (The Three Elements):**
- *Clear objective:* Without one, an activity may be enjoyable but not support academic growth. With one, even a simple movement activity can become powerful learning.
- *Engagement:* Engaging activities do not require a lot of time or resources — they can be short, simple opportunities for participation. Teachers can gather local resources (bottle caps, fabric, stones) as a cost-effective way to increase materials.
- *Positive environment:* Teachers play an essential role — modeling respectful interactions, valuing effort, normalizing mistakes. Classrooms that establish a sense of community have students who are more willing to ask questions and stay engaged.
