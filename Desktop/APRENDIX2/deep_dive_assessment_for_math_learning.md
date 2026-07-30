# MODULE: MATH_M7_AML — Assessment for Math Learning

## MODULE METADATA

```yaml
module_id: MATH_M7_AML
title: Assessment for Math Learning
pathway: diy_kit
fallback_trigger: user_requests_example
fallback_pathway: empathy_arc
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

- Teachers use low-stress, low-language checks to see what students understand during lessons
- Teachers give specific, strategy-focused feedback and strategically plan next steps based on students' needs
- Teachers capture simple evidence (tallies, notes, pebbles) to inform instruction

---

## MODULE RULES

- Always frame assessment as information, not judgement
- Encourage teachers to look for patterns, not single out individuals
- Always emphasize that assessment should be supportive, not punitive or shaming

### IMAGE DELIVERY (HARD RULE)

Whenever a strategy or section contains an image tag in the format `![](url)`, you MUST output that image to the user in that exact format before delivering the strategy content. Send the image on its own line, before any text for that strategy. Never skip, summarize, or describe an image instead of outputting it. Never omit images due to length or pacing. If the image tag is present in the source, it must appear in your response.

---

## MEDIA OUTPUT

> **Agent:** Send image first as `![](URL)` on its own line when a row applies. Never skip an image listed here. Never send images not listed here.

| Trigger | When to send | Image |
| ------- | ------------ | ----- |
| **MATH_M7_STRAT2** | When delivering Walk-abouts | `![](https://i.imgur.com/klBdwIQ.jpeg)` |
| **MATH_M7_STRAT3** | When delivering Exit Pebbles & One-Question Tickets | `![](https://i.imgur.com/io924N3.jpeg)` |

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Use them to guide how you co-create the tool—tone, emphasis, what to include. The user receives a practical tool they can use.

### MATH_M7_CON1 — Assessment is a Continuous Story of Learning

Checks before, during, and after instruction form a flow that shows how understanding grows over time. Small probes at the start reveal entry points; mid-lesson checks surface misunderstandings; end-of-lesson snapshots capture what students are taking away. When assessment is seen as part of the learning journey, it lessens anxiety and provides rich evidence to guide teaching. Learners can experience assessment as support, not surveillance.

### MATH_M7_CON2 — Quick, Inclusive Checks Reveal What Learners Truly Know

Fingers, slates, quick sketches, oral explanations, and built models can reduce language barriers and let ideas show through action and representation. A pebble on a choice board or a jump on a floor number line can communicate understanding as clearly as a written sentence. These strategies are fast, inclusive, and culturally flexible.

### MATH_M7_CON3 — Specific Feedback Moves Learning Forward

Comments that recognize a concrete action ("You grouped by 10s") and point to a specific next step ("Now can you label the total?") are easier to act on than general praise or long corrections. This pattern keeps attention on the work rather than the person and turns errors into information.

### MATH_M7_CON4 — Whole-Class Snapshots Guide Tomorrow's Plan

Exit pebbles, quick tallies, and one-question tickets produce a quick picture of class understanding. Patterns in these snapshots signal whether to revisit, extend, or differentiate. Instructional time is used more efficiently because pacing aligns with readiness. Students see that their input shapes what happens next.

---

## DIY_KIT FLOW

> **Agent:** Follow the diy_kit pathway. Co-create a practical assessment tool with the teacher. Flow: INTRO → CONTEXT_CHECK → BUILD_STEPS (Reflection #1 mid-build) → REFINEMENT → FINAL_TOOL → Reflection #2 → QUIZ

### TOOL OPTIONS

Offer to build one of these (or let the user choose):

| Tool | Description |
|------|-------------|
| **Assessment Checklist** | Quick checks to use before/during/after lessons: Fix & Explain, Walk-about, Exit Pebble, Demonstration, Estimation. Copy-paste ready. |
| **Walk-about Recording Template** | Class list with checkmark/question mark/dot system. Simple observation template. Copy-paste ready. |
| **Quick Check Template** | Exit pebble setup, one-question ticket prompt, demonstration prompt, estimation line. Steps and prompts for a lesson. Copy-paste ready. |

### CONTEXT CHECK QUESTIONS

Ask 1-2 questions before building. Wait for response.

- What is your class size? How do you typically record observations?
- What materials do you have for quick checks? (e.g., slates, pebbles, scrap paper)
- When do you most want to check understanding—before, during, or at the end of a lesson?

### BUILD COMPONENTS (from strategies)

Draw on these when constructing the tool. Adapt to user's context.

- **Fix & Explain:** pre-planned example with purposeful error; students decide, fix with model/sketch; observe
- **Walk-abouts:** one focus per walk; checkmark (secure) / question mark (unsure) / dot (needs help) on class list; brief questions
- **Exit Pebbles:** 3 options A/B/C on board; pebble on paper; or one-question ticket on slip
- **Demonstration prompts:** short prompt; students draw/build on slate/notebook; hold up at signal; scan for patterns
- **Estimation line:** Too Small / About Right / Too Big; point, pebble, or stand; turn-and-talk reason

### REFLECTION PROMPTS

| Step | Prompt |
|------|--------|
| Reflection #1 (after step 2 or 3) | Would this work in your class? |
| Reflection #2 (after Final Tool) | What might you change? |

### CONSTRAINTS

- ≤2 required user inputs during build phase
- Final tool must be copy-paste ready
- Always emphasize assessment as information, not judgement

---

## STRATEGIES (Reference for Build)

> **Agent:** Use these when constructing the tool. Do not deliver as separate content—incorporate into the co-created tool.

### STRAT1 — Fix & Explain

Post a pre-planned example with a purposeful error. Students decide if it's correct, fix it with a model or sketch. Walk around to observe. Examples: number line error, regrouping error, wrong operation. Accessible for language learners; turns mistakes into information.

### STRAT2 — Walk-abouts
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/klBdwIQ.jpeg)
Move through the room while students work. Choose one thing to look for. Record quick marks on a class list: checkmark (secure), question mark (unsure), dot (needs help). Ask brief questions. In large classes, sample strategically. If patterns emerge, pause for a short reteach.

### STRAT3 — Exit Pebbles & One-Question Tickets
📷 Send this image first, then deliver strategy content:
![](https://i.imgur.com/io924N3.jpeg)

Pebble vote: 3 options A/B/C on board, papers on table, students place pebble. Or one quick prompt—students write on slip. Low-stakes snapshot to plan next steps. Examples: "Draw equal groups for 12"; "Write a number close to 50 but not 50."

### STRAT4 — Demonstration Prompts

Short prompt; students draw/build on slate or notebook. At signal, hold up. Scan for patterns—not who is right/wrong. Fast, inclusive, whole-class. Examples: "Show 14 on place value chart"; "Model 4+3 with pictures"; "Draw a shape with 4 sides."

### STRAT5 — Class Estimation

Line labeled Too Small / About Right / Too Big. Students point, place pebble, or stand. Turn-and-talk for reason. Patterns guide revisit, proceed, or differentiate. Examples: "Is 15-7=3 too small/about right/too big?"; "Is 11+6 closer to 15 or 20?"

---

## 7. Quiz Questions

> **Deliver exactly one item per type, in this fixed order: Q1 recall → Q2 understanding → Q3 application. User must get ≥2 of 3 correct to pass. If an answer is incorrect, offer one retake using a different item of the same type from this bank — never re-ask the same question.**

#### Question 1: Recall

- **The purpose of a walk-about is to gather evidence of student learning.**
  - Options: True / False

- **Demonstration prompts are useful in large classes because:**
  - Options: They increase writing / They entertain students / They show thinking

- **Estimation replaces calculation.**
  - Options: True / False

#### Question 2: Understanding

- **How can exit pebbles help teachers plan their next lesson?**
  - Keywords: data, understanding, evidence, review

- **What does having students analyze an error do for you as a teacher?**
  - Keywords: misunderstanding, misconception, reasoning, next steps

- **What is the purpose of a walk-about?**
  - Keywords: evidence, adjustment, support

#### Question 3: Application

- **Scenario 1:**
  During a busy math lesson on multiplication, students are working in groups using bottle caps to make equal groups. The teacher cannot sit with every group, but wants to understand who is correctly forming groups of 4.
  *What should the teacher do during their walk-about to gather useful data?*

- **Scenario 2:**
  In a large classroom, students are learning how to represent four-digit numbers using a place value chart. The teacher wants to quickly see everyone's thinking at the same time without calling on students individually.
  *How can this teacher use a demonstration prompt to understand student thinking?*

- **Scenario 3:**
  During a warm-up activity, a teacher writes "12 x 7 = 104" on the board and asks students to label it as "too small," "about right," or "too big" without solving it. Then students explain their thinking to a partner.
  *What could this estimation activity tell teachers about student thinking?*

---

## OPTIONAL_ENRICHMENT

> **Agent:** Offer only after quiz is passed. Not required for completion.

### DIY_ACTIVITY_1: Exit Pebble Setup

| Field | Value |
|-------|-------|
| **Time** | ~5 minutes |
| **Materials** | 3 papers labeled A, B, C; pebbles or similar |
| **Steps** | 1. Create 3 answer options on the board for one problem / 2. Place papers A, B, C on a table / 3. Students place a pebble on their answer / 4. Review results together |
| **Observation** | Quick snapshot of class understanding |

### DIY_ACTIVITY_2: Estimation Line Practice

| Field | Value |
|-------|-------|
| **Time** | ~5 minutes |
| **Materials** | Chalk or tape for line |
| **Steps** | 1. Draw a line labeled Too Small / About Right / Too Big / 2. Pose a problem (e.g., "Is 12+7 closer to 18 or 25?") / 3. Students point or stand at their answer / 4. Pairs share one reason |
| **Observation** | Low-stress check of estimation and reasoning |
