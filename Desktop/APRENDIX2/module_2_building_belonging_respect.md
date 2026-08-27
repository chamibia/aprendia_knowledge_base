# MODULE: HC_M2_BBR — Building Belonging & Respect

## MODULE METADATA

```yaml
module_id: HC_M2_BBR
title: Building Belonging & Respect
pathway: empathy_arc
duration_target: 12-15 minutes
unlock_requires: HC_M1_CSP
unlocks: HC_M3_RPS
quiz_pass: 2_of_3              # per-module: ≥2 of 3 correct
course_pass_threshold: 0.80    # course-level; explain depth (system prompt §9)
quiz_retry_allowed: true
grade_levels: Primary 1-6
subject: Healing Classrooms
```

---

## LEARNING OBJECTIVES

- Teachers implement inclusive participation strategies to ensure every child feels known and involved
- Teachers use effective teacher language to establish a positive learning environment
- Teachers develop shared responsibility and hope through classroom roles and achievable goals

---

## TEACHER MOTIVATIONS & PAIN POINTS

- "I correct behavior, but I don't feel like it is improving."
- "The same few students are always participating while others stay silent."
- "My students don't take responsibility for the classroom."
- "I want every student to feel valued, but I'm not sure how to do that with a big class."

---

## MODULE RULES

- Avoid ranking or public comparison between students.
- Support positive behavior without using punishment or shame.
- Reinforce that small moments of inclusion matter.
- Classroom jobs should be safe, equitable, non-exploitative, and appropriate — they should never cause harm or compromise learning.

---

## MEDIA OUTPUT

> **Agent:** When a row below applies, send the image **first** as `![](URL)` on its own line, then deliver the related content. Never skip an image listed here. Never send images not listed here.

| Trigger | When to send | Image |
| ------- | ------------ | ----- |
| **INTRO** | First bot message when this module starts | `![](https://i.imgur.com/afjtNh6.jpeg)` |
| **HC_M2_STRAT1** | When delivering Scene 1 (Meaningful Classroom Jobs) | `![](https://i.imgur.com/0PSjpRj.jpeg)` |
| **HC_M2_STRAT3** | When delivering Scene 3 (Specific Positive Feedback) | `![](https://i.imgur.com/rCS3u1z.jpeg)` |
| **HC_M2_STRAT5** | When delivering Scene 5 (Respectful Language for All) | `![](https://i.imgur.com/BduvZZX.jpeg)` |

---

## INTRO

📷 Send this image first, then deliver the module intro text:
![](https://i.imgur.com/afjtNh6.jpeg)

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Concepts are overarching and apply across strategies. Use them to guide how you frame and deliver the strategies in the narrative — tone, emphasis, why it matters — but never present concepts as separate content. The user sees only strategies in action.

### CON1 — Belonging Supports Positive Behavior

Every child wants to feel like they are important and valued. When teachers make belonging a priority, they create a welcoming environment and strong classroom community. Students who feel a sense of belonging want to be at school and have increased positive behaviors that reflect their positive, healthy relationships within the classroom. Feeling included helps children care about learning and each other.

### CON2 — Participation Builds Confidence

Students who are active participants in the classroom see that their ideas and voices matter. All students should be invited to respond, ask questions, and share their thoughts. The classroom is a safe, low-pressure environment where children can participate and take risks, like asking or answering questions. Over time, regular participation builds confidence and helps students stay engaged in learning. Teachers can encourage participation through a variety of activities and inclusive practices that relate to learners with different interests and abilities.

### CON3 — Responsibility Creates Pride

Giving students responsibility helps them feel trusted and capable. Students who are given equitable opportunities to take on roles and tasks that contribute to the classroom develop a stronger sense of responsibility and belonging. Contributing in meaningful ways, such as helping a peer or caring for the learning space, helps students see themselves as important members of the class. This sense of pride in being a student is highly motivating and leads to increased positive behavior and participation.

### CON4 — Teacher Language Shapes Student Self-Belief and Self-Image

The words teachers use matter. Teacher language can help students or hurt them. As teachers, words can influence not only student behavior and learning, but also how they see themselves. Encouraging language from a teacher helps students form their own vision of themselves succeeding. When students hear positive truth about themselves, they will be inspired and motivated on a personal and academic level. Language that focuses on effort and progress helps children believe in their abilities to learn.

---

## EMPATHY_ARC SCENE MAPPING

> **Agent:** Generate narrative scenes at runtime — do not retrieve or reuse a fixed story. **Show only strategies to the user.** Concepts guide your framing but are never delivered explicitly. This module covers **5 strategies**, so pacing is critical — see below.

**Vignette setup:** Feature a teacher with a realistic class size and setting, drawn from what the bot knows about the user's context from chat history (grade level, class size, location). If context is limited, use broadly plausible details for a large primary class. Open with a concrete moment where the teacher notices that participation and belonging aren't evenly shared in the room — a few students always answer first and take the lead, while others (including one child the teacher notices in particular) stay quiet, hang back from group activities, or seem unsure of their place in the class. The teacher wants every child to feel like they belong, but isn't yet sure how to make that consistent. Keep the opening to 2–3 sentences — specific and grounded, not generic.

**Opening poll (after the vignette intro):** "Do you have students in your class who rarely speak up or seem to hang back from the group?"
- A: Yes, a few students come to mind
- B: Sometimes, depending on the activity
- C: Not that I've noticed yet

**Reflection after poll (based on response):**
- A: "You already know who needs this most. Let's look at small ways to bring them in."
- B: "That's a helpful thing to notice — let's build some habits that make belonging more consistent, no matter the activity."
- C: "Great — this module will help you build habits that keep it that way for every child."

**⚠️ CRITICAL PACING RULE: This module has 5 strategies — one strategy scene per message. Never combine two strategies into one message, and never compress the story into a single block. Complete the full cycle (scene → reflection/poll → insight → micro-action) for one strategy, wait for the teacher's response, then move to the next. Use `<break>` between steps if a message would otherwise exceed 400 characters.**

**Per-scene delivery structure (apply to every strategy):**
1. Continue or deepen the vignette — what does the teacher in the story try, notice, or decide at this moment? (3–4 sentences, embedding the strategy in the action, not naming it as a definition)
2. Pose a reflection prompt or quick poll tied to that moment. Wait for the teacher's response.
3. Deliver the strategy insight in 1–2 lines — plain language, no jargon.
4. Offer a micro-action the teacher can try tomorrow.

| Scene | Strategy | Concept (guides delivery; do not show) | Narrative brief |
|-------|----------|----------------------------------------|-----------------|
| Scene 1 | STRAT1 (Meaningful Classroom Jobs) | CON3, CON1 | The teacher gives the quiet or overlooked child from the opening vignette a simple, real classroom job, and notices the child take visible pride in having a role. |
| Scene 2 | STRAT2 (Whole Class Responses) | CON2 | Instead of calling on the same few hands, the teacher shifts to a whole-class response method (thumbs up/down, fingers, slates) and notices students who never volunteer suddenly taking part. |
| Scene 3 | STRAT3 (Specific Positive Feedback) | CON4 | The teacher catches a specific, genuine moment of effort from a student who doesn't usually get noticed, and names it specifically and privately rather than with generic praise. |
| Scene 4 | STRAT4 (Goal Setting) | CON3, CON1 | The teacher and class set one small, shared class goal together, and the teacher notices students — including quieter ones — start to feel ownership over it. |
| Scene 5 | STRAT5 (Respectful Language for All) | CON4 | The teacher notices a student getting discouraged and consciously chooses effort-focused, respectful language instead of a label or correction, and sees the student re-engage. |

---

## EMPATHY_ARC REFLECTION PROMPTS

> **Agent:** Use these prompts at the specified points, tied to the story moment — not as abstract questions. Wait for the teacher's response before continuing.

| Step | Prompt |
|------|--------|
| Scene 1 | What are some classroom tasks that your students can help do as a job? |
| Scene 2 | When during your lessons could you invite all students to respond at once? |
| Scene 3 | When you give feedback to students, what do you typically say? How can you improve? |
| Scene 4 | What is one small goal your class could work on this week? |
| Scene 5 | What is one phrase you could use to highlight a student's effort or progress in class? |

---

## STRATEGIES (Reference for Narrative)

> **Agent:** Use these when constructing the narrative. Do not deliver as separate content — embody them in the story scenes.

### HC_M2_STRAT1 — Meaningful Classroom Jobs

📷 Send this image first, then deliver Scene 1:
![](https://i.imgur.com/0PSjpRj.jpeg)

**Description:** Rotating simple classroom jobs helps students feel responsible and included.

**Expanded explanation:** When students are given meaningful, developmentally appropriate jobs, they see themselves as trusted members of the classroom community. Classroom jobs help children understand that everyone plays a role in keeping the class running efficiently, so that effective learning can occur. Use rotating jobs to ensure that every child has the opportunity to try each job at least once throughout the school year. Not every student needs to have a job at the same time, so the teacher should remind children that everyone will have the opportunity to participate. Encourage teachers to keep track of which students have done which role. Classroom jobs may include line leader, sweeper, cleaning the board, taking attendance, or leading a song. Classroom jobs should be safe, equitable, non-exploitative, and appropriate.

**Examples / Variations:**
- For larger class sizes, some jobs can have multiple students (if students keep their notebooks at school, two or three students can be in charge of collecting them at the end of the day).
- Teachers can rotate the jobs at the end of each day or at the end of each week (make rotating jobs a fun reveal for students).
- Use pictures or symbols to display the different jobs and write student names by the job they are responsible for.

**Reflection prompt:** What are some classroom tasks that your students can help do as a job?

**Teacher Voice:** "When students have jobs, they feel like an important member of the class and learn responsibility."

---

### HC_M2_STRAT2 — Whole Class Responses

**Description:** Whole-class responses invite all students to participate and share their thoughts.

**Expanded explanation:** Whole-class responses reduce pressure by allowing students to answer together instead of one at a time. This helps quieter or less confident students feel safe to participate. This strategy also helps teachers quickly assess who understands a lesson and who may need more support. This teaching strategy needs no pre-made materials and is easy to implement into any lesson for any subject. When using this strategy for answers/choices that have a right or wrong answer, teachers should remind students that it is okay to make mistakes and that mistakes help us learn. Teachers must set clear expectations for students to be encouraging and supportive of all learners and their level of understanding.

**Examples / Variations:**
- Thumbs up, thumbs down, or in the middle to show understanding of content.
- Use fingers to show answer or choice (can be a great strategy for math lessons).
- Reflection time — give students a reflection prompt related to the lesson and allow 5 minutes of silent writing or drawing time; while students write, walk around the room to quietly read their work and offer support.
- Write answers on paper, notebook, or slate, then hold them up to share.
- Stand up or sit down to show agreement, choice, or answer.
- Label four corners/areas of the room to represent different answers or choices; have students move to their respective choice/answer.

**Reflection prompt:** When during your lessons could you invite all students to respond at once?

**Teacher Voice:** "More students try when everyone answers together."

---

### HC_M2_STRAT3 — Specific Positive Feedback

📷 Send this image first, then deliver Scene 3:
![](https://i.imgur.com/rCS3u1z.jpeg)

**Description:** Naming the positive behavior you notice helps students repeat it.

**Expanded explanation:** Specific positive feedback tells students exactly what they did well, instead of general praise. This is reinforcing teacher language and reinforces positive behaviors that promote effective learning. Teachers can name concrete and specific behaviors that they want repeated, like "You remembered to put your pencil away before we have a break." Avoid general phrases like "Nice work." When a teacher sees improvement in a student, ask them to share how they did it, like "You capitalized the beginning of all your sentences today. What helps you remember to do that?" Avoid complimenting individual students in front of the whole class often. Instead, during the school day, tell a student individually the positive feedback. De-emphasize teacher approval — students should be active and engaged learners who are intrinsically motivated.

**Examples / Variations:**
- Use a neutral, calm tone so feedback feels informational, not performative.
- Name the exact behavior you want repeated ("You raised your hand and waited to be called on before speaking").
- Highlight improvement over time ("Yesterday you needed reminders to line up quietly, and today you did it on your own").
- Prompt students to reflect on their behaviors, choices, or success ("You finished your work early and helped clean up. What helped you remember to do that?").
- Give quiet, individual feedback during work time (kneel beside a student and say, "You stayed focused the whole time we were writing").

**Reflection prompt:** When you give feedback to students, what do you typically say? How can you improve?

**Teacher Voice:** "I say exactly what positive things I notice and students repeat them."

---

### HC_M2_STRAT4 — Goal Setting

**Description:** Small, achievable goals help students build confidence and hope.

**Expanded explanation:** Setting goals gives students something positive to work towards, individually or together. Small goals help all students experience success, even when outside school they may be experiencing challenging conditions. Class goals further establish belonging and respect within the learning environment. As goals are set, the whole class should review and share strategies to help them achieve the goal. Teachers should remind students of the goal throughout the school day/week. After students become familiar with the goal setting system, students may begin suggesting class goals they can work together to achieve. Goals should be broad and applicable for all students, should not single out individual students, and should provide a specific time period for a goal (day, week, two weeks, etc.).

**Examples / Variations:**
- Set one simple class goal for the week (e.g. no trash on the floor when we close at the end of the day; treat others the way you want to be treated).
- Track how many goals students complete throughout a term or school year.
- Display class goals with a picture or symbol.
- Reflect briefly at the end of the day/week to gauge student perception of how they are completing the goal.
- Create personal goals with students who have persistent challenges or unwanted behaviors (example goal: "I will take three belly breaths when I start to feel overwhelmed") and check in with the student daily/weekly to check progress.
- Repeat goals if students were unable to meet them and brainstorm as a class how they could try to meet the goal.

**Reflection prompt:** What is one small goal your class could work on this week?

**Teacher Voice:** "Small goals helped my students believe they could succeed."

---

### HC_M2_STRAT5 — Respectful Language for All

📷 Send this image first, then deliver Scene 5:
![](https://i.imgur.com/BduvZZX.jpeg)

**Description:** Using respectful, effort-focused language helps students feel capable and valued.

**Expanded explanation:** The words teachers use influence how students see themselves. Avoiding labels and focusing on effort helps children believe they can improve, reinforcing that they are valued. Use focused statements to motivate students, like "I know you all can be good listeners," that encourage positive behaviors. Teachers need to remind students that school is a safe place to make mistakes, take risks, and try again. Teachers do not expect students to be perfect, but they do expect them to try their best. Respectful, effort-focused language reduces shame and fear, which improves confidence and participation.

**Examples / Variations:**
- Use effort-focused praise ("You kept trying even when it was hard").
- Normalize mistakes ("It's okay to try again" or "Mistakes make us better learners").
- Model respectful self-talk ("This is hard, so I am going to slow down and try a new strategy").
- Replace labels with observations ("Your materials are not out yet" instead of "You do not listen").

**Reflection prompt:** What is one phrase you could use to highlight a student's effort or progress in class?

**Teacher Voice:** "I did not realize how much my words shaped how students see themselves."

---

## VIGNETTE DEBRIEF (Module End)

> **Agent:** Resolve the vignette generated for this module. Show the teacher's classroom becoming a place where every child has a role, a voice, specific recognition, a shared goal, and language that builds them up rather than labels them. Name what the teacher did and why it mattered, in 2–3 sentences. End with a one-sentence bridge into the quiz — NOT into the Deep Dives — e.g. "You've built a classroom where belonging is part of the everyday routine. Before we move on, let's check what stuck with a few quick questions." **Do not preview the Deep Dives here; they unlock only after this quiz is passed.**
>
> **⚠️ HARD RULE:** The mini-quiz below is mandatory and comes immediately after this debrief, before anything else. Do not present Deep Dive options or end the module here.

---

## 7. Quiz Questions

> **Deliver exactly one item per type, in this fixed order: Q1 recall → Q2 understanding → Q3 application. User must get ≥2 of 3 correct to pass. If an answer is incorrect, offer one retake using a different item of the same type from this bank — never re-ask the same question.**

#### Question 1: Recall

- **Why do classroom jobs support positive behavior?**
  - Options: They keep students busy / They build responsibility / They reduce lesson time

- **Whole-class responses can help quieter students participate.**
  - Options: True / False

- **Why should class goals be small and achievable?**
  - Options: To finish quickly / To build confidence / To keep students busy

#### Question 2: Understanding

- **Why is specific feedback more effective than general praise?**
  - Keywords: clear, repeat behavior, specific, understanding

- **How does teacher language influence how students see themselves?**
  - Keywords: motivation, encouragement, self-belief

- **Why is it important to rotate classroom jobs?**
  - Keywords: inclusion, experience, opportunity

#### Question 3: Application

- **Scenario 1:**
  A teacher asks questions during a lesson, but only the same few students raise their hands to answer. Many students stay quiet, even when they know the answer.
  *What could the teacher do to involve more students in responding?*

- **Scenario 2:**
  A student is struggling with a task, and the teacher says, "You are not trying hard enough." The student becomes quiet and stops participating.
  *What could the teacher do differently to better support the student? Why?*

- **Scenario 3:**
  A teacher notices that only a few students help with classroom tasks, like erasing the board and collecting textbooks. The teacher wants more students to feel responsible and included in the classroom.
  *What could the teacher do to increase student responsibility and participation?*

---

## OPTIONAL_ENRICHMENT

> **Agent:** Offer only after the quiz is passed. Not required for completion.

### DIY_ACTIVITY_1: Say It the Helpful Way

| Field | Value |
|-------|-------|
| **Materials** | Board or poster; chalk or marker |
| **Steps** | 1. Write a common classroom phrase on the board that may be discouraging ("You are doing it wrong"). / 2. Ask students how that phrase might make someone feel. / 3. Work together to rephrase the statement in a helpful way ("I see that this is hard. Can I help you?" or "Let's try a different strategy"). / 4. Practice saying the new phrase together as a class. / 5. Encourage students to listen for and use helpful language throughout the day. |
| **Variation (younger)** | For the first few examples, the teacher provides the original phrase and helpful phrase at the same time; writes the phrases on paper and posts them on the class wall. |
| **Variation (older)** | Write about a time someone used helpful language to support them. |
| **Observation** | Students use respectful language. Accountability between students and teacher to use respectful language. |
| **Time** | 8–10 minutes |

### DIY_ACTIVITY_2: Would You Rather?

| Field | Value |
|-------|-------|
| **Materials** | Students |
| **Steps** | 1. Before class, prepare a list of five to ten questions ("Would you rather play football or listen to music?"). / 2. Instruct students to stand for the first option or sit for the second option. / 3. Ask the class each question one at a time. / 4. Prompt students to explain their choice. / 5. Reflect on what it is like to see and hear everyone's choices. |
| **Variation (younger)** | Use pre-made questions. |
| **Variation (older)** | Write down questions and turn them in to the teacher to ask during the activity. |
| **Observation** | Students participate in a fun and engaging way. Students feel safe sharing their choices. |
| **Time** | 10–15 minutes |

---

## MEDIA NOTES

| Media Type | File Name | Notes |
|------------|-----------|-------|
| Image | *(not yet supplied)* | Teacher kneeling by student while class is working — both look happy as the teacher has provided positive feedback. |
| Audio | *(none)* | |
