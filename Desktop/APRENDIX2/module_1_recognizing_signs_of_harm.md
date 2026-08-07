# MODULE: SAFEGUARDING_M1_RSH — Recognizing Signs of Harm

## MODULE METADATA

```yaml
module_id: SAFEGUARDING_M1_RSH
title: Recognizing Signs of Harm
pathway: empathy_arc
duration_target: 10-12 minutes
unlock_requires: none              # first module in the course
unlocks: SAFEGUARDING_M2_BSC
quiz_pass: 3_of_3                  # per course instructions: >80% required (3 items ⇒ all 3 correct)
quiz_retry_allowed: true           # one retry with alternate item bank if <80%
grade_levels: Primary 1-6
subject: Safeguarding
```

---

## LEARNING OBJECTIVES

- Identify behavioral, emotional, and physical signs that a child may be experiencing harm
- Respond to disclosures and signs of distress with calm, empathetic, non-investigative presence
- Document observations accurately to support safe referral and protect the child

---

## TEACHER MOTIVATIONS & PAIN POINTS

- "I want to help my students, but I'm not always sure if what I'm seeing is serious or just a bad day."
- "I worry that if I say the wrong things, I'll make the situation worse for the child."
- "With 80 students in my class, it's hard to notice individual children unless something is very obvious."
- "These issues feel private — what happens in a family is for the family to deal with, not for me to get involved in."
- "I'm afraid of what might happen to me — or to the child — if I report something and the wrong person finds out."

---

## MODULE RULES

- This module covers safe identification and referral of children at risk of protection or safeguarding concerns. Do not introduce reporting procedures, referral chains, or external services — those belong in Module 3.
- Teachers should be encouraged to observe with empathy, not act as investigators or counselors. Teachers should not investigate, diagnose, question deeply, or handle safeguarding concerns on their own.
- Children who demonstrate signs of risk need to be safely identified and referred onto the relevant safeguarding focal point or child protection agency.
- Signs of harm must always be presented as signals that warrant attention — not as proof of abuse. Avoid language that implies certainty.
- Content delivery must consistently reinforce that a calm, trusting relationship is itself a protective factor, not just a precondition for noticing harm.
- Do not include examples or language that could stigmatize families, communities, or specific groups as inherently harmful.

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Concepts are overarching and apply across strategies. Use them to guide how you frame and deliver the strategies in the narrative — tone, emphasis, why it matters — but never present concepts as separate content. The user sees only strategies in action.

### CON1 — Teachers Are a First Line of Protection

In many crisis-affected settings, teachers are among the few consistent, trusted adults in a child's life. This means they are often the first — and sometimes the only — person positioned to notice when something is wrong. Safeguarding is not a specialist role separate from teaching; it is part of showing up for every child every day.

### CON2 — Some Signs Build Over Time, and Some Cannot Wait

No single observation confirms that a child is being harmed — with the exception of physical or sexual assault, which always warrants immediate referral. What matters is staying attentive to any change, whether it appears once or builds into a pattern. If a child shows ongoing signs of distress — even without a clear cause — it is always safer to refer than to wait.

### CON3 — How You Respond Matters as Much as What You Notice

When a child discloses or shows signs of distress, responding with calm, empathy, and without judgement builds trust and helps the child feel safe enough to accept help. A shocked, probing, or dismissive response can cause re-traumatization, prevent the child from sharing further, and make it harder to reach them in the future.

### CON4 — Documentation Protects Children and Teachers

Written observations — factual, specific, and dated — create a record that supports referral and ensures continuity if the concern is escalated. Teachers do not need to build up days of records before acting; one clear, specific observation is enough to refer, and referring promptly is always most important.

---

## EMPATHY_ARC SCENE MAPPING

> **Agent:** Generate narrative scenes at runtime — do not retrieve or reuse a fixed story. **Show only strategies to the user.** Concepts guide your framing but are never delivered explicitly. This module covers **4 strategies**, so pacing is critical — see below.

**Vignette setup:** Feature a teacher with a realistic class size and setting, drawn from what the bot knows about the user's context from chat history (grade level, class size, location) — the same details should carry through every scene, not just the opening. If context is limited, use broadly plausible details for a large primary class. Open with a concrete classroom moment where a child's behavior or appearance has changed in a way that is noticeable but ambiguous — the teacher sees something but isn't sure what it means or what to do. The teacher wants to help but has not yet identified the concern as a safeguarding issue or taken any action. Keep the opening to 2–3 sentences — specific and grounded, not generic.

**⚠️ NARRATIVE VOICE (HARD RULE):** The vignette is about a fictional teacher, told in **third person** ("the teacher," "she," or a name) — never in second person ("you"). Do not address the real teacher as if the story is happening to them. **Second person is reserved exclusively for the poll and reflection prompts**, which speak directly to the real teacher about their own classroom. Do not blend the two — a scene should never slide from narrating "the teacher" into asking "you" mid-story.

**⚠️ VIGNETTE CONTINUITY (HARD RULE):** This is one continuous story about one teacher, running across all 4 strategy scenes — not a fresh example per strategy. Scene 2, 3, and 4 must pick up where the previous scene left off (same teacher, same class, same unfolding situation). Never let the module quietly drop the story and start delivering strategies as plain, story-free content after Scene 1 — if that happens, it is a failure of this module, not an acceptable shortcut.

**Opening poll (after the vignette intro):** "Have you ever noticed something concerning about a child and felt unsure what to do next?"
- A: Yes, fairly often
- B: Sometimes
- C: Not yet, but I want to be ready

**Reflection after poll (based on response):**
- A: "You're already noticing. This module will help you know what to do with what you see."
- B: "Those moments matter more than they might seem. Let's look at what you do when they arise."
- C: "Being prepared before it happens is exactly the right instinct. Let's build that readiness now."

**⚠️ CRITICAL PACING RULE: This module has 4 strategies — one strategy scene per message. Never combine two strategies into one message, and never compress the story into a single block. Complete the full cycle (strategy name → scene → insight → reflection) for one strategy, wait for the teacher's response, then move to the next. Use `<break>` between steps if a message would otherwise exceed 400 characters.**

**Per-scene delivery structure (apply to every strategy — all 4, not just the first).** Use this exact template, in this exact order, for every scene:

> 📍 **Strategy [N] of 4: [Strategy Name]**
> <break>
> [Story — 3–4 sentences, third person, continuing the same ongoing vignette: what does the teacher in the story notice, try, or decide at this moment? Show the strategy in action, don't define it abstractly.]
> <break>
> 💡 [Insight — 1–2 lines, plain language, no jargon. This is the teaching content. It must appear here, before the reflection — never after.]
> <break>
> ❓ [Reflection — the prompt for that strategy, addressed directly to the teacher ("you"/"your classroom"), asked only now that they have the story and insight needed to answer it. Wait for the teacher's response before moving to the next strategy.]

**Do not reorder these four parts.** In particular: never ask the ❓ reflection question before the 💡 insight has been delivered — the teacher can't meaningfully reflect on content they haven't been taught yet. The 📍 "Strategy N of 4" header must appear on every one of the 4 scenes, not just the first, so the teacher always knows both which strategy they're on and how many remain.

| Scene | Strategy | Concept (guides delivery; do not show) | Narrative brief |
|-------|----------|----------------------------------------|-----------------|
| Scene 1 | STRAT1 (Know the Signs) | CON1, CON2 | The teacher looks more closely at the ambiguous change from the opening vignette — a behavioral, emotional, or physical signal — and starts to recognize it as a possible sign of harm rather than "just a bad day." Show the noticing in action — no definitions. |
| Scene 2 | STRAT2 (Create a Safe Arrival Moment) | CON1 | Continuing directly from Scene 1: the same teacher introduces, or reflects on, a simple daily check-in — a greeting, a look, a question — and uses it to observe the same child more closely over the following day(s) without singling them out. |
| Scene 3 | STRAT3 (Respond without Probing) | CON3 | Continuing the same story: the same child discloses something, or shows visible distress, and the teacher responds with calm empathy — listening, reassuring, and explaining they will get the child help — without asking investigative questions. |
| Scene 4 | STRAT4 (Document What You See) | CON4 | Continuing the same story: after the moment passes, the teacher privately writes down (or verbally reports, if writing isn't safe or possible) exactly what was seen and heard — facts only, dated — as a first step toward referral. |

---

## EMPATHY_ARC REFLECTION PROMPTS

> **Agent:** Use these prompts at the specified points, tied to the story moment — not as abstract questions. Wait for the teacher's response before continuing.

| Step | Prompt |
|------|--------|
| Scene 1 | What in your classroom might make it harder to notice if one child's behavior or appearance changed? |
| Scene 2 | What is one small greeting or check-in ritual you could introduce tomorrow that would take less than five minutes? |
| Scene 3 | If a child disclosed something difficult to you today, what is the first thing you would say? |
| Scene 4 | What can you use to privately record a concern about a child? |

---

## STRATEGIES (Reference for Narrative)

> **Agent:** Use these when constructing the narrative. Do not deliver as separate content — embody them in the story scenes.

### SAFEGUARDING_M1_STRAT1 — Know the Signs

**Description:** Recognize the behavioral, emotional, and physical signals that may indicate a child is experiencing harm.

**Expanded explanation:** Signs of harm often appear before a child is able or willing to speak about what is happening. Behavioral changes — sudden withdrawal, increased aggression, regression to younger behaviors (e.g. thumb-sucking), or overtly sexual behavior — can signal that something has disrupted a child's sense of safety. Emotional signals such as persistent sadness, fearfulness around specific adults, or a flat/disengaged affect are equally important to notice. Physical signs like unexplained injuries old and new, frequent absence, unattended medical needs, or deteriorating hygiene may point to neglect or abuse, particularly when they appear repeatedly. In large, crowded classrooms, these signs can be easy to miss, which is why building a habit of attentive, consistent observation matters.

**Examples / Variations:**
- A child who normally participates stops volunteering answers and avoids eye contact for several days running.
- A child flinches or becomes visibly distressed when a particular adult enters the classroom or school grounds.
- A younger child begins wetting themselves again after a period of normal development with no apparent illness.
- In a multi-age classroom, an older child takes on an unusually adult role (e.g. managing younger siblings, appearing exhausted, missing school during harvest or market days), which may signal economic exploitation or neglect at home.

**Reflection prompt:** What in your classroom might make it harder to notice if one child's behavior or appearance changed?

**Teacher Voice:** "I used to think something had to be very obvious before I could say anything — now I understand that noticing a pattern early is part of my job."

---

### SAFEGUARDING_M1_STRAT2 — Create a Safe Arrival Moment

**Description:** Use a brief, consistent daily check-in at the start of class to build trust and notice changes in how children present each day.

**Expanded explanation:** A safe arrival moment is a simple, repeatable routine — a greeting, a look, a question — that signals to every child that they are seen and that their teacher is present for them. Over time, consistency builds the kind of trust that makes children more likely to signal distress or accept support. In crisis-affected contexts where home environments may be unpredictable, the predictability of a warm daily greeting can itself be stabilizing. It also gives teachers a low-pressure opportunity to notice changes in a child's mood, energy, or appearance before the demands of the lesson begin.

**Examples / Variations:**
- Stand at the door each morning, greet each child by name, and make brief eye contact as they enter.
- Begin class with a simple whole-group question: "Show me how you're feeling using your fingers — one finger if you're feeling okay, two if you're feeling good, three if you're feeling great." Notice who doesn't respond or who looks away.
- For very large classes, rotate focus — make a point of greeting a different group of 10–15 children closely each day so every child receives individual attention across the week.
- For multi-grade groups, ask older children to help welcome younger ones — this builds peer connection while freeing the teacher to observe.

**Reflection prompt:** What is one small greeting or check-in ritual you could introduce tomorrow that would take less than five minutes?

**Teacher Voice:** "I already say good morning — I didn't realize that moment could be so important if I actually use it to observe each child."

---

### SAFEGUARDING_M1_STRAT3 — Respond without Probing

**Description:** When a child discloses distress or shows signs of harm, respond with calm empathy — acknowledging feelings, thanking the child for sharing, and explaining that you will need to share this with a trained person who can help — without asking leading questions or investigating.

**Expanded explanation:** A child who chooses to disclose is taking a significant risk, and the teacher's response in that moment can either open or close the door to further support. The goal is not to find out what happened — that is the role of trained specialists — but to make the child feel heard, safe, and not alone. Asking probing questions ("Who did this?" "What exactly happened?") can distress the child further, compromise future investigations, and place the teacher in a role they are not equipped to fill. In crisis contexts where children may have experienced multiple overlapping traumas, a calm adult — who believes the child — is what the child needs in the moment. Believing the child, and being transparent that you will seek help for them, is itself an act of protection.

**Examples / Variations:**
- A child says "Uncle hurts me when I come home." Respond: "Thank you for telling me. That was brave. You are safe here, and I am going to make sure someone helps you." Do not ask follow-up questions about the uncle. You can add: "I will need to share this with someone whose job it is to keep children safe — they will support you directly, and I can be with you when we meet them."
- A child is crying and won't say why. Respond: "I can see you're having a hard time. I'm here. You don't have to talk right now." Sit nearby, stay calm, and observe.
- If a child begins to describe an incident in detail, gently say: "I hear you, and I believe you. I don't need to know everything right now — what matters is that you're safe."
- For younger children, physical reassurance (a hand on the shoulder, crouching to eye level) can communicate safety when words are hard.

**Reflection prompt:** If a child disclosed something difficult to you today, what is the first thing you would say?

**Teacher Voice:** "I used to think I needed to get the full story so I could help. Now I understand that just staying calm and believing them is the most important thing I can do."

---

### SAFEGUARDING_M1_STRAT4 — Document What You See

**Description:** Write down specific, factual observations — what the child said, did, or showed — to create an accurate record that supports referral and protects the child.

**Expanded explanation:** Documentation is not about building a case — it is about ensuring that a child's situation is not forgotten, misremembered, or dismissed. A factual record (what was observed, when, and in what context) gives whoever receives the referral the clearest possible picture. It also protects the teacher by showing that they acted appropriately and promptly. In crisis contexts where staff may change frequently or school structures are disrupted, written records ensure continuity of care even when memory cannot be relied upon. A simple, minimum structure is all that is needed: the child's name and the date, what was observed or heard using facts only, and where and when it happened. Writing something down is not the final step — every documented concern must be shared through the referral pathway. If safe storage is not available, share the concern directly with a trusted supervisor or focal point as soon as possible rather than leaving a written record in an unsecured place. If writing is not safe or feasible at all, report verbally to a trusted focal point immediately and ask them to record it.

**Examples / Variations:**
- Write: "Monday 14th: Amina arrived with a bruise on her left arm. When I asked if she was ok, she looked away and said nothing. She did not participate in class." Avoid: "Amina seems to be abused at home."
- Keep a small notebook dedicated to safeguarding observations, stored privately — not in a shared register, on a shared desk, or anywhere visible to students or other community members. If safe private storage is not possible, bring notes directly to a trusted supervisor or focal point rather than leaving a written record unsecured.
- If writing is not possible in the moment, note three specific details immediately after: what you saw, what was said, and the date.
- For teachers with limited literacy, a trusted colleague or school leader can help transcribe observations, but confidentiality must be maintained.

**Reflection prompt:** What can you use to privately record a concern about a child?

**Teacher Voice:** "I never wrote things down because I didn't want to make accusations, but I understand now that I'm just recording what I saw, not making a judgement."

---

## VIGNETTE DEBRIEF (Module End)

> **Agent:** Resolve the vignette generated for this module. Show the teacher taking the right actions across all four scenes — noticing the change, creating a safe check-in, responding with calm empathy, and documenting factually. Name what the teacher did and why it mattered, in 2–3 sentences. End with a one-sentence bridge into the quiz — e.g. "Now that you know how to recognize and respond to signs of harm, let's check what stuck with a few quick questions." **Do NOT bridge into Module 2 here, and do not preview Module 2 content.** Module 2 is locked until the quiz below is passed.

**⚠️ HARD RULE: The mini-quiz below is mandatory and comes immediately after this debrief, before anything else.** Do not transition to Module 2, offer a summary of what's next in the course, or end the module here. The debrief's job is to close out the story — not to close out the module. Module 2 does not unlock until the teacher passes this quiz (see course instructions §5).

---

## 7. Quiz Questions

> **Deliver in this fixed order: Q1 Recall → Q2 Understanding → Q3 Application. This course requires >80% to pass a module quiz — with 3 items, that means all 3 must be correct. If any answer is incorrect, offer one retake using a new item of the same type — never re-ask the same question. If the retake is also incorrect, offer a brief recap of Module 1 key concepts (signs of harm, responding without probing, documentation basics), then allow one more retry.**

#### Question 1: Recall (True/False)

- **The child stays behind after class and begins to cry but doesn't say why. The teacher should ask questions to find out what happened so she can help.**
  - Options: True / False
  - Correct: False

#### Question 2: Understanding (Open-Ended)

- **The teacher notices the child has changed over several days but isn't sure if it is serious. What should she do first?**

#### Question 3: Application (Multiple Choice)

- **After the interaction, the teacher wants to record what happened. Which of these is the best thing to write down?**
  - Options: A: "Something is wrong with this child." / B: "The child stayed after class, was crying, and said nothing when I asked if she was okay." / C: "The child seems to be experiencing abuse." / D: "The child was upset today."
  - Correct: B

---

## OPTIONAL_ENRICHMENT

> **Agent:** Offer only after the quiz is passed. Not required for completion.

### DIY_ACTIVITY_1: The Morning Signal

| Field | Value |
|-------|-------|
| **Materials** | Chalk or a stick to draw on the ground |
| **Steps** | 1. Before students arrive, draw three circles on the ground near the entrance or on the board, labeled 1, 2, 3. / 2. As students enter, ask them to step in or tap the circle that matches how they feel: 1 = not great, 2 = okay, 3 = good. / 3. Observe quietly — notice who hesitates, who avoids, who picks a different spot each day. / 4. After class, take a mental or written note of any children who consistently choose 1 or don't engage. |
| **Variation (younger)** | Use facial expressions drawn in the circle (sad face, neutral face, happy face) |
| **Variation (older)** | Add a fourth option and invite them to name their own feeling out loud |
| **Observation** | Teachers may notice that some children always choose 1 without explanation, or avoid the activity entirely. Both are worth gentle follow-up. |
| **Time** | 3–5 min |

### DIY_ACTIVITY_2: My Observation Note

| Field | Value |
|-------|-------|
| **Materials** | Any paper or small notebook; pen/pencil |
| **Steps** | 1. After a day when you noticed something concerning about a child, find a quiet moment before leaving school. / 2. Write three things: the child's name and the date; exactly what you observed — behavior, appearance, or words; and the context — where it happened and who else was present. / 3. Store the paper somewhere private, or keep a dedicated notebook locked/out of reach of students. / 4. Review your notes at the end of the week and notice patterns. |
| **Variation** | For teachers who find writing difficult, practice with a partner by saying three things aloud first (after confirming confidentiality), then writing. For teachers with no paper, identify a trusted person at school to verbally report to and ask them to record it. |
| **Observation** | Notice patterns across days — they are often more telling than a single incident |
| **Time** | 5–10 min |
