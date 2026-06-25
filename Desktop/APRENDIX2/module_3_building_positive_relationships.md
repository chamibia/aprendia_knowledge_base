# MODULE: TWB_M3_BRB — Building Positive Relationships & Setting Boundaries

## MODULE METADATA

```yaml
module_id: TWB_M3_BRB
title: Building Positive Relationships & Setting Boundaries
pathway: steady_path
fallback_trigger: user_requests_example
fallback_pathway: empathy_arc
duration_target: 10 minutes
unlock_requires: TWB_M2_BRM (prior module quiz: ≥2 of 3)
unlocks: TWB_M4_CWP
quiz_pass: 2_of_3              # per-module: ≥2 of 3 correct
course_pass_threshold: 0.80    # course-level; explain depth (system prompt §9)
quiz_retry_allowed: true
grade_levels: Primary 1-6 (teachers)
subject: Teacher Wellbeing
```

---

## LEARNING OBJECTIVES

- Teachers strengthen supportive connections with colleagues through simple, realistic actions
- Teachers use peer interaction to reduce isolation and share encouragement
- Teachers set one clear boundary to protect energy and prevent burnout

---

## MODULE RULES

- Reiterate that boundaries are a form of care, not selfishness
- Reinforce that feeling alone or stretched thin is common in crisis contexts; avoid language that suggests teachers are unsupported or abandoned
- Reinforce that support does not require long conversations, formal meetings, or emotional disclosure
- Encourage peer connection, but do not frame colleagues as the only source of support
- Reinforce low-effort, low-disclosure approaches
- If a teacher expresses hopelessness, extreme withdrawal, or statements suggesting harm to self or others, trigger safeguarding guidance and shift away from peer-based strategies

---

## DELIVERY INSTRUCTIONS

**Pathway:** `steady_path` (see Global Pathway Instructions for full execution spec)

**Flow:** INTRO → STRATEGIES (Reflection #1 after STRAT2, Reflection #2 after STRAT4) → RECAP → QUIZ

**Chunking rules:**
- Each message ≤4 sentences OR ≤400 characters
- Wait for user response after each reflection prompt
- One strategy per message (never combine)
- Frame boundaries as professional care, not disengagement
- **Do NOT deliver concepts as separate content**—use them to guide tone and framing only

---

## INTERNAL: Concepts (Agent Guidance Only)

> **Do NOT show these concepts to the user.** Concepts are overarching and apply across strategies. Use them to guide how you frame and deliver the strategies—tone, emphasis, why it matters—but never present concepts as separate content. The user sees only strategies.

### TWB_M3_CON1 — Connection Reduces Isolation

Teaching in crisis-affected settings can feel isolating, especially when resources are limited and stress is high. Even brief, supportive interactions with colleagues help teachers feel seen and less alone. Connection does not always require deep conversations—small moments of sharing and encouragement can significantly reduce emotional burden.

### TWB_M3_CON2 — Peer Support Strengthens Resilience

Peer support allows teachers to share challenges, ideas, and encouragement with someone who understands their reality. These exchanges build shared resilience by normalizing difficulty and reminding teachers they are not carrying challenges alone.

### TWB_M3_CON3 — Boundaries Protect Energy

Without clear boundaries, teachers may overextend themselves and experience burnout. Boundaries protect time, energy, and emotional capacity so teachers can continue teaching sustainably over time.

---

## STRATEGIES (User-facing)

### TWB_M3_STRAT1 — Peer Mentoring Moment

**Description:** Connect with a colleague once a week to exchange one challenge, one idea, or one small win.

**Expanded explanation:** Peer mentoring does not require formal programs or scheduled meetings. A simple weekly connection can provide meaningful support. Sharing one challenge helps normalize difficulty; sharing one idea or small win reinforces competence and growth. The focus is not solving every problem, but offering presence, encouragement, and shared understanding.

**Examples / Variations:**
- Short WhatsApp message of encouragement
- Brief end-of-day chat
- Weekly voice note

**Reflection prompt:** Who could you check in with this week?

**Quiz item:** A colleague says, "I don't have time for meetings." Which option best fits a peer mentoring moment? (Options: A: Schedule a weekly discussion / B: Send a short message / C: Write a long note / D: Wait until less busy | Correct: B)

---

### TWB_M3_STRAT2 — Celebrate Small Wins

**Description:** Take a moment to recognize a positive classroom interaction or improvement, and share it with a colleague.

**Expanded explanation:** In challenging contexts, progress is often slow and easy to overlook. Celebrating small wins helps teachers recognize effort, growth, and positive moments that might otherwise go unnoticed. These wins can include a calm transition, a child's effort, or simply getting through a difficult day. Sharing with a colleague strengthens connection and builds a more supportive school culture.

**Examples / Variations:**
- Quiet self-acknowledgement
- Share a win with a colleague
- Write one positive note to your future self
- End-of-week reflection

**Reflection prompt:** What small success happened this week?

**Quiz item:** Celebrating small wins helps teachers notice _____, even when challenges remain. (Keywords: progress, motivation, growth, success)

---

### TWB_M3_STRAT3 — Practice Active Listening

**Description:** Offer full attention in conversations to strengthen trust, teamwork, and emotional safety.

**Expanded explanation:** Active listening means giving full attention without interrupting, judging, or immediately offering solutions. Being truly heard can reduce emotional burden and strengthen trust. This does not require long conversations—short moments of focused listening can have a strong impact. It also models respect and empathy, promoting teamwork and emotional safety.

**Examples / Variations:**
- Eye contact and attentive posture
- Asking clarifying questions

**Reflection prompt:** How do you show others you are listening to them?

**Quiz item:** A colleague is sharing frustration about a difficult class. Which response shows active listening? (Options: A: "That happened to me—here's what I did." / B: "It will get better, don't worry." / C: "That sounds exhausting. What felt hardest?" / D: "You should try a new strategy." | Correct: C)

---

### TWB_M3_STRAT4 — Set a Boundary

**Description:** Choose one realistic limit that protects energy (e.g., reserving the first 10 minutes after school for quiet reset).

**Expanded explanation:** Boundaries help teachers manage workload and emotional demands. Setting a boundary does not mean caring less—it means protecting the energy needed to keep teaching. A boundary might involve time (e.g., a few minutes alone after school) or communication (e.g., not responding to work messages after a certain hour). Choosing one clear, realistic boundary makes it easier to maintain.

**Examples / Variations:**
- Quiet reset time after school
- Limit work messages at night
- Say no to an extra task

**Reflection prompt:** What boundary would help you most right now?

**Quiz item:** Which boundary is most realistic for protecting energy in a busy school setting? (Options: A: Never thinking about work at home / B: Taking a full day off each week / C: Protecting 10 minutes after school for a reset / D: Saying yes to every request for help | Correct: C)

---

## REFLECTION PROMPTS

> **Agent:** Use these prompts at the specified points. Wait for user response before continuing.

| Step | Prompt |
|------|--------|
| Reflection #1 (after STRAT2) | What small success happened this week? |
| Reflection #2 (after STRAT4) | Which of these four strategies would you try first—or what stands out to you from what we covered? |

---

## RECAP

> **[Deliver: 2–3 sentences summarizing key takeaways]**

You explored four ways to strengthen connections and protect energy: peer mentoring moments, celebrating small wins, practicing active listening, and setting boundaries. Support does not require long meetings or deep disclosure—brief, simple actions can reduce isolation and build resilience. Next, we'll co-create a simple wellbeing plan.

---

## QUIZ

> **[Deliver all 3 items. User must get ≥2 of 3 correct to unlock the next module.]**  
> **[Provide correct answer + 1-sentence explanation after each item.]**  
> **[If not passed, offer one retry per item with alternate items from QUIZ_BANK_ALT (§9)]**

### QUIZ_ITEM_1

| Field | Value |
|-------|-------|
| **Type** | Multiple choice |
| **Question** | A colleague says, "I don't have time for meetings." Which option best fits a peer mentoring moment? |
| **Options** | A: Schedule a weekly discussion / B: Send a short message / C: Write a long note / D: Wait until less busy |
| **Correct** | B |
| **Feedback** | Peer mentoring moments can be brief—a short message or quick chat is enough to build connection. |

### QUIZ_ITEM_2

| Field | Value |
|-------|-------|
| **Type** | Short answer (accept keywords) |
| **Question** | Celebrating small wins helps teachers notice _____, even when challenges remain. |
| **Accept keywords** | progress, motivation, growth, success, effort |
| **Feedback** | Celebrating small wins helps teachers recognize progress and growth, even in difficult conditions. |

### QUIZ_ITEM_3

| Field | Value |
|-------|-------|
| **Type** | Multiple choice |
| **Question** | A colleague is sharing frustration about a difficult class. Which response shows active listening? |
| **Options** | A: "That happened to me—here's what I did." / B: "It will get better, don't worry." / C: "That sounds exhausting. What felt hardest?" / D: "You should try a new strategy." |
| **Correct** | C |
| **Feedback** | Active listening involves acknowledging the feeling and inviting more—not immediately offering advice or solutions. |

---

## QUIZ_BANK_ALT

> **[Use these items if retry is needed]**

### ALT_ITEM_1

| Field | Value |
|-------|-------|
| **Question** | Which boundary is most realistic for protecting energy in a busy school setting? |
| **Options** | A: Never thinking about work at home / B: Taking a full day off each week / C: Protecting 10 minutes after school for a reset / D: Saying yes to every request for help |
| **Correct** | C |

### ALT_ITEM_2

| Field | Value |
|-------|-------|
| **Question** | Why are boundaries a form of care? |
| **Accept keywords** | protect, energy, sustain, burnout, continue, teaching |

### ALT_ITEM_3

| Field | Value |
|-------|-------|
| **Question** | What does peer support NOT require? |
| **Options** | A: Long conversations or formal meetings / B: Brief connection / C: Sharing one small win / D: Presence and encouragement |
| **Correct** | A |
