# Classroom Toolkit Agent — Run Conditions

**Production Agent**: Classroom Toolkit

### Run Condition Detection

Analyze the user's message and conversation history to determine if the Classroom Toolkit agent should run.

Set **run_classroom_toolkit** to `"true"` if:

- The current message explicitly selects Classroom Toolkit (e.g. "Classroom toolkit", "Classroom Toolkit", "Build a classroom toolkit", "c)", "option c", "toolkit")
- The user said "Menu" in a prior message and the current message selects Classroom Toolkit
- Chat history shows the user is already in the Classroom Toolkit flow (e.g. last agent was Classroom Toolkit, or last output showed Energizers | Wellbeing menu)
- The current message is a response to a Classroom Toolkit prompt (Q1: "What do you need from your class?" / Q2: "When will you use it?" for Energizers; or Q1: "What would help you most?" / Q2: "Where are you right now?" for Wellbeing)
- The current message selects a post-output action: "Save", "Another", "Remind me", "Back" — and the prior output was an Energizer or Wellbeing moment
- The current message selects ⚡ Energizers or 🌿 Wellbeing from the Toolkit menu

Set **run_classroom_toolkit** to `"false"` if:

- The user has never selected Classroom Toolkit
- The user selected "Learn a Skill" or "Solve Challenge" from the pathway choice (Step 4)
- Chat history shows the user is in a course (Math, Reading, Teacher Wellbeing, Classroom Management) or in Solve a Challenge flow
- The user explicitly asks to leave (e.g. "go back", "main menu", "learn a skill", "solve a challenge") and does not select Classroom Toolkit
- The current message is part of general onboarding (Steps 1–3, Q1–Q5) before pathway choice

**Handoff from onboarding:** When the user selects Classroom Toolkit from Step 4 (Pathway Choice), hand off to the Classroom Toolkit agent immediately. Do not run course selection or any other agent.
