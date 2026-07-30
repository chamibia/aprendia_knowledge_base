# MODULE: MATH_M3_SMM — Shifting Math Mindsets

## MODULE METADATA

```yaml
module_id: MATH_M3_SMM
title: Shifting Math Mindsets
pathway: empathy_arc
fallback_trigger: user_mastery >= 0.90
fallback_pathway: explain_exchange
duration_target: 10-15 minutes
unlock_requires: MATH_M2_MEL (prior module quiz: ≥2 of 3)
unlocks: null
quiz_pass: 2_of_3              # per-module: ≥2 of 3 correct
course_pass_threshold: 0.80    # course-level; explain depth (system prompt §9)
quiz_retry_allowed: true
grade_levels: Primary 1-6
subject: Math
```

---

## LEARNING OBJECTIVES

- Teachers understand how mindset influences math learning and persistence
- Teachers use inclusive language and practices to reduce math anxiety
- Teachers celebrate effort and multiple strategies to build confidence
- Teachers create a warm, engaging, and inclusive learning environment that supports students' wellbeing and learning

---

## MODULE RULES

- Never label learners by ability. Avoid language like "strong/weak students"
- Emphasize participation, effort, and persistence more than outcomes or right answers

### IMAGE DELIVERY (HARD RULE)

Whenever a strategy or section contains an image tag in the format `![](url)`, you MUST output that image to the user in that exact format before delivering the strategy content. Send the image on its own line, before any text for that strategy. Never skip, summarize, or describe an image instead of outputting it. Never omit images due to length or pacing. If the image tag is present in the source, it must appear in your response.

---

## MEDIA OUTPUT

> **Agent:** Send image first as `![](URL)` on its own line when a row applies. Never skip an image listed here. Never send images not listed here.

| Trigger | When to send | Image |
| ------- | ------------ | ----- |
| **INTRO** | First bot message when this deep dive starts | *(add URL when available — skip if not yet set)* |
| **MATH_M3_STRAT1** | When delivering Use Inclusive Language (Scene 1) | `![](https://i.imgur.com/MmNNkg1.jpeg)` |
| **MATH_M3_STRAT2** | When delivering Make Math Relevant (Scene 2) | `![](https://i.imgur.com/d25Z81B.jpeg)` |
| **MATH_M3_STRAT3** | When delivering Celebrate Multiple Strategies (Scene 3, message 1) | `![](https://i.imgur.com/UaH5izg.jpeg)` |
| **MATH_M3_STRAT4** | When delivering Build Community Routines (Scene 3, message 2) | `![](https://i.imgur.com/dyYa8tP.jpeg)` |
| **MATH_M3_STRAT5** | When delivering Choice & Voice for Agency (Scene 3, message 3) | `![](https://i.imgur.com/qF7mHSh.jpeg)` |
| **QUIZ** | Before delivering module recap — send image, then recap, then quiz questions | `![](https://i.imgur.com/aqR5zp4.jpeg)` |

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Concepts are overarching and apply across strategies. Use them to guide how you frame and deliver the strategies in the narrative—tone, emphasis, why it matters—but never present concepts as separate content. The user sees only strategies in action.

### MATH_M3_CON1 — Belief Shapes Engagement

A child's belief in their ability to learn math directly affects engagement. In crisis settings, instability and interrupted schooling can damage confidence and focus. Short, predictable routines and affirming language rebuild children's senses of capability. Frequent, small wins restore trust and belief in themselves as worthy learners.

### MATH_M3_CON2 — Celebrating Mistakes Promotes Resilience

Celebrating mistakes and growth promotes resilience. Many learners associate errors with embarrassment or punishment, which can be intensified by stress or trauma. When teachers reframe mistakes as information, students feel safer to try again and persist through challenges. Publicly valuing mistakes and revisions normalizes productive struggle and keeps learners focused rather than opting out when a task becomes difficult.

### MATH_M3_CON3 — Inclusive Language and Culture

Classroom language and culture should be inclusive and supportive. Labels like "slow" or "weak" push marginalized or newly arrived learners further to the edges of the class community. Using respectful language, linking lessons to local context, and welcoming all learners of all abilities signals that everyone belongs, which can reduce dropout risk and improve attendance. Inclusive classroom norms also help classes function when materials are limited because peers see each other as a team that can support and uplift each other to learn together.

### MATH_M3_CON4 — Safe, Predictable, Joyful Environments

Safe, predictable, and joyful math environments support wellbeing and learning. Short routines, clear norms, and warm feedback create the safety learners need to try, revise, and keep going. Joyful elements like movement, opportunities for success, and local examples can lower stress and make math feel doable. Offer small choices to build agency and use inclusive entry points so that everyone feels math learning is accessible. When children experience belonging, control, and meaningful challenge, they engage more deeply and learn more, even under challenging conditions.

---

## EMPATHY_ARC SCENE MAPPING

> **Agent:** Generate narrative scenes at runtime. **Show only strategies to the user.** Concepts guide your framing but are never delivered explicitly. Use this mapping to know which strategy belongs in each scene. **Pacing:** Scene 3 has 3 strategies—deliver one strategy per message; do not compress into one scene. Use `<break>` between them.

**Per-scene delivery structure (apply to every strategy in every scene):**
1. Open with the strategy name and a relevant emoji (e.g. "💬 Use Inclusive Language"). This is the first line of the message.
2. Deliver the narrative scene — a story showing the strategy in action (3–4 sentences, plain text, no definitions).
3. Add one short sentence on how this strategy helps in the classroom (practical benefit — not a definition).
4. Ask the reflection question for that scene. Wait for the teacher's response before moving to the next scene.

Use `<break>` tags between steps if the combined message exceeds 400 characters. Never skip or compress any of the four steps. Scene 3 has 3 strategies — deliver one per message; do not compress into one turn.

| Scene | Strategy | Concept (guides delivery; do not show) | Narrative brief |
|-------|----------|----------------------------------------|-----------------|
| Scene 1 | STRAT1 (Use Inclusive Language) | CON1 | A teacher shifts from identity labels to process-focused language when students struggle. Include sentence frames ("I noticed…," "I tried…," "Next time I will…") and Stars & Steps feedback. Show the strategy in action—no concept definitions. |
| Scene 2 | STRAT2 (Make Math Relevant) | CON2 | A teacher uses a local, real-world problem (market, sharing food, measurement) instead of textbook examples. Students see math as useful and connected to their daily lives. Show the strategy in action. |
| Scene 3 | STRAT3 + STRAT4 + STRAT5 (Celebrate Multiple Strategies, Build Community Routines, Choice & Voice) | CON3 + CON4 | Weave together: multiple strategies for one problem (e.g., 15-8), think-pair-share with roles and norms, and students choosing their tools (stones, drawing, number line). Show strategies in action—no concept definitions. |

---

## EMPATHY_ARC REFLECTION PROMPTS

> **Agent:** Use these prompts at the specified points. Wait for user response before continuing.

| Step | Prompt |
|------|--------|
| Reflection #1 (after Scene 1) | Have you experienced something like this—students labeled by ability, or a moment when changing your language shifted how learners responded? |
| Reflection #2 (after Scene 3) | What part of this story stood out to you? |

---

## STRATEGIES (User-facing)

> **Agent:** These are what the user sees—through the narrative. Deliver strategies in action; never deliver concepts as separate content.

### MATH_M3_STRAT1 — Use Inclusive Language
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/MmNNkg1.jpeg)

**Description:** Avoid labeling children based on perceived ability and focus on growth over time.

**Expanded explanation:** Avoid identity labels (e.g., "You're not good at math," or putting children in a "fast group" or "slow group"). Replace with process-focused language (e.g., "You used a smart strategy. What is your next step?" or "You're improving! Let's try it again with these beans to help us count."). Post and practice sentence frames like "I noticed…," "I tried…," and "Next time I will…," while redirecting children from statements like "I failed" to "I need help." Especially in emergency settings, inclusive language reduces stigma, which can lower absenteeism and dropout.

**Examples / Variations:**
- Revise "You're wrong" to "Let's check another way"
- Revise "Be fast" to "Be clear and show your thinking"
- "Stars & Steps" feedback: share one strength and one next step

**Reflection prompt:** What is one phrase you could replace with more supportive language?

---

### MATH_M3_STRAT2 — Make Math Relevant
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/d25Z81B.jpeg)

**Description:** Use local examples, names, games, and materials that reflect children's real lives.

**Expanded explanation:** Tie problems to daily tasks that use no special materials, for example: 1) market counting—determine prices and change with beans or bottle caps; 2) water measurement—how many cups fill a bucket—estimate first, then test; 3) skip-counting—count steps or sweeps in 2s/5s/10s while cleaning or lining up. Use local names, places, and objects so children see math as a tool for fairness, planning, safety, and fun.

**Examples / Variations:**
- Count beans at lunch
- Share snacks fairly
- Football scores for addition/comparison
- Hopscotch for skip-counting
- Clap patterns

**Reflection prompt:** What local example could you use for your next math lesson?

---

### MATH_M3_STRAT3 — Celebrate Multiple Strategies
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/UaH5izg.jpeg)

**Description:** Learning is strongest when children explore different ways to solve problems. Valuing diverse strategies teaches children that there is more than one path to understanding.

**Expanded explanation:** Show that there are many paths to one answer. For example, 15-8=?: 1) gather 15 stones then take away 8; 2) Use a number line to count back 8 spaces from 15; 3) Chunking 15-5=10, then 10-3=7. Invite small groups or pairs of students to solve, then present their findings by saying "Our method was… because…". Praising strategy use, not just speed, builds confidence, reduces fear of being "wrong," and helps learners choose methods that fit the materials they have.

**Examples / Variations:**
- Ask learners to show 2–3 ways to solve the same problem
- Strategy poster showing options: model, draw, write, act

**Reflection prompt:** How could you show your class there are many ways to solve a problem?

---

### MATH_M3_STRAT4 — Build Community Routines
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/dyYa8tP.jpeg)
**Description:** Structured collaboration and shared roles in math tasks help children trust each other and take academic risks. These routines also promote social-emotional growth.

**Expanded explanation:** Shared routines make risk-taking feel safe and reduce teacher load in crowded classrooms. Establish quick roles (e.g., speaker, checker, timekeeper) for group tasks. During pair work, use "think-pair-share" to encourage children to think about a problem, answer it with a partner, then share their methods with another pair or the whole class. Create norms (e.g., "Always ask why," "help first, tell later," "kind feedback only") to encourage a supportive classroom environment. These structures need no special materials, work with mixed ages, and build SEL skills (listening, turn-taking, empathy), along with math skills.

**Examples / Variations:**
- Math circles
- Partner coaching with sentence frames
- Roles like 'timekeeper,' 'reporter'
- Pair-share → pair-pair-share (two pairs combine to compare responses and provide support)

**Reflection prompt:** What classroom routine could help your students work together?

---

### MATH_M3_STRAT5 — Choice & Voice for Agency
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/qF7mHSh.jpeg)

**Description:** Offer small choices (method, materials, problem order) so learners feel ownership and are more willing to try.

**Expanded explanation:** Agency lowers anxiety. Let students choose to model with stones, draw, or use a number line; choose which problem to start with; or pick a check method (recount, draw, jump on a number line). Small choices restore a sense of control and encourage persistence, especially in overcrowded and/or resource-lean settings.

**Examples / Variations:**
- "Choose your tool": students choose which manipulative to use
- Menu of checks: recount/redraw/number line jump

**Reflection prompt:** Where could you add a student choice in tomorrow's lesson?

---

## 7. Quiz Questions

📷 Send this image first, then deliver the module recap, then the quiz:
![](https://i.imgur.com/aqR5zp4.jpeg)

> **Deliver exactly one item per type, in this fixed order: Q1 recall → Q2 understanding → Q3 application. User must get ≥2 of 3 correct to pass. If an answer is incorrect, offer one retake using a different item of the same type from this bank — never re-ask the same question.**

#### Question 1: Recall

- **Giving students small choices in math helps them:**
  - Options: Avoid work / Feel ownership / Ask the teacher more questions

- **Teachers should encourage multiple ways to solve a problem.**
  - Options: True / False

- **What is the effect of using inclusive math language?**
  - Options: Builds motivation / Focuses on the current answer / Reduces participation

#### Question 2: Understanding

- **Why should students learn multiple ways to solve a problem?**
  - Keywords: different strategies, confidence, connections, understanding

- **How do shared routines support student learning?**
  - Keywords: trust, collaboration, risk-taking, participation

- **How can you rephrase "you are wrong" using inclusive language?**
  - Keywords: try another way, check your answer again

#### Question 3: Application

- **Scenario 1:**
  A class is practicing addition using examples from a textbook. The students seem bored and ask why this lesson matters.
  *What could the teacher do to make this math lesson more relevant to students' lives?*

- **Scenario 2:**
  A teacher gives all students the same math problem and tells them to solve it one specific way. Some students become frustrated and stop trying.
  *How would you advise the teacher to give students more choice?*

- **Scenario 3:**
  A teacher has started using group work in their math class, but noticed students do not know how to work together. The teacher wants students to participate more.
  *What could the teacher do to build community routines so all students can participate?*

---

## OPTIONAL_ENRICHMENT

> **Agent:** Offer only after quiz is passed. Not required for completion.

### DIY_ACTIVITY_1: Growth Mindset Wall

| Field | Value |
|-------|-------|
| **Time** | ~15 minutes |
| **Materials** | Paper, chalk |
| **Steps** | 1. Students share a mistake they made / 2. Class reframes it positively / 3. Add to wall display |
| **Variation (younger)** | Drawings of mistakes |
| **Variation (older)** | Short written notes |

### DIY_ACTIVITY_2: Kind Math

| Field | Value |
|-------|-------|
| **Time** | 10-15 minutes |
| **Materials** | Board, chalk |
| **Steps** | 1. Create two columns on the board: "Unhelpful" and "Helpful" / 2. Elicit common hurtful phrases learners hear during math; write under "Unhelpful" / 3. Lead the class to create "Helpful" alternatives / 4. Leave the list on the board or post on a class wall |
| **Variation** | Students use helpful phrases during math lessons |
