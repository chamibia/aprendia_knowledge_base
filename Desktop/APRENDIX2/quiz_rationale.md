# Quiz rationale

Canonical definitions for end-of-module quizzes: **three items**, fixed order **recall → understanding → application**.

---

## Question types

### Q1 — Recall

- **Format:** Multiple choice or true/false.  
- **Grading:** One clearly correct answer.  
- **Checks:** *Does the learner remember key information from the module?*

### Q2 — Understanding

- **Format:** Short open-ended response.  
- **Grading:** Multiple acceptable answers are allowed if they are grounded in module content; use **hidden keyword** lists for evaluation only—never expose keywords to the user.  
- **Checks:** *Can the learner explain ideas in their own words?*

### Q3 — Application

- **Format:** Scenario reflecting the teaching environment and classroom.  
- **Task:** Synthesize module content and relate it to realistic practice.  
- **Checks:** *Can the learner apply the content in real-world situations?*

---

## Learning design

| Aspect | Rule |
|--------|------|
| **Items per module** | 3 |
| **Order** | Always recall → understanding → application |
| **Intent** | Surface ordered thinking from lower to higher cognitive demand |

---

## Unlock and pass logic

| Level | Rule |
|--------|------|
| **Next module** | **2 of 3** items correct on that module’s end quiz |
| **Course pass / depth** | **≥80%** of **all** quiz items in the course answered correctly to pass and unlock **explain** pathways (e.g. `explain_exchange` and explain-arc-style depth), unless a course instruction file states otherwise |

---

## Quiz wording vs Key Concepts (authoring)

In module files, **Key Concepts** (and similar blocks with internal IDs like `*_CON*`) exist to guide **how the agent teaches**. They are **not** meant to be copied into quiz stems.

- **Avoid** internal codes, Key Concept **titles as the question**, or **near-verbatim** sentences from those bullets in user-facing quizzes (including retakes).
- **Prefer** the module’s dedicated **quiz bank** / **Quiz Item** lines under strategies, or **new** stems in plain language that match what the learner heard via strategies and examples.

---

## Re-take logic

When a learner answers an item **incorrectly**, the assistant should:

1. **Identify** the missed concept area.  
2. Give a **brief** explanation of the correct idea.  
3. Offer **one** retake with a **new** question of the **same type** (recall / understanding / application).

**Constraints**

- **At most one retake per question.**  
- Tone: **supportive and predictable.**
