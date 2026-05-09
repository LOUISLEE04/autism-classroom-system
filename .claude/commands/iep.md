# /iep [name] — IEP Goal Tracking

Manage Individualized Education Plan goals for a specific student.

## Steps

1. Read the student's profile (`students/S*-[name].md`) — Section 12 IEP Goals Summary
2. Check if `iep/goals-[name].md` exists — if yes, read it; if not, offer to create it

## Modes

Ask which the teacher needs:

### View current goals
- Display all active goals with status and review dates
- Flag any goals that are past their review date

### Add a new goal
Ask for:
1. Goal area (Communication / Social / Academic / Self-care / Behaviour / Motor / Other)
2. What is the goal? (teacher describes in plain language)
3. How will you measure progress? (e.g., "80% accuracy over 3 sessions", "independently 3 out of 5 trials")
4. What is the target date?
5. What does baseline look like today?

Format as a proper IEP goal:
```
Goal: [Student name] will [specific observable behaviour] in [condition/context] with [accuracy/frequency] by [date].
Baseline: [Current performance level]
Progress measure: [How progress will be tracked — e.g., teacher observation 3x/week]
```

### Update progress on a goal
Ask:
1. Which goal?
2. How is the student doing? (teacher's observation)
3. Rate progress: Not yet started / Beginning / Making progress / Nearly met / Met

Update `iep/goals-[name].md` with dated progress note.

### Mark a goal as met
Congratulate the teacher. Log completion date. Ask if they want to set a next-level goal.

### Generate progress report
Summarise all current goals, status, and progress notes in a clean format suitable for sharing with parents or professionals.

## Output file: `iep/goals-[name].md`

```markdown
# IEP Goals — [Student Full Name]
*Programme: Pendidikan Khas | Class: [X] | Teacher: [Name]*
*Last updated: [YYYY-MM-DD]*

---

## Active Goals

### Goal 1: [Area]
**Goal:** [Student name] will [behaviour] in [context] with [criteria] by [date].
**Baseline:** [Description + date]
**Progress:**
- [YYYY-MM-DD]: [Note]
- [YYYY-MM-DD]: [Note]
**Status:** In progress / Met / Not yet started
**Review date:** [YYYY-MM-DD]

---
[Repeat for each goal]

## Completed Goals
[Goals that have been met, with completion date]

---
*Annual IEP review date: [YYYY-MM-DD]*
*Review team: Teacher, [Parent name], [SLT if applicable], [OT if applicable]*
```

## Notes for Claude
- Use Bahasa Malaysia terminology where appropriate in goal descriptions (Pendidikan Khas, etc.)
- Goals must be SMART: Specific, Measurable, Achievable, Relevant, Time-bound
- If the teacher describes a vague goal ("I want him to communicate better"), help them make it specific: "By [date], [Name] will use PECS Phase 4 sentence strip to request preferred item with 80% accuracy across 3 consecutive sessions."
- Never set goals that require verbal response from a non-verbal student
- Always cross-reference the student's communication profile and learning profile when drafting new goals
