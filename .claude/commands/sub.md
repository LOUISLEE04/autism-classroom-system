# /sub — Substitute Teacher Handoff Pack

Generate a clear, printable handoff document for a substitute teacher.

## Purpose

A substitute walks in knowing nothing about your students. This pack gives them the minimum critical information to keep every student safe and the day running.

## Steps

1. Read all student profiles: `students/S*.md` (all except `_template.md`)
2. Read `memory/teacher-profile.md` (classroom info, support staff, admin contacts, school protocol)
3. Read `memory/class-roster.md` (communication levels, alerts)

## Output format

Print-friendly. Maximum 1 page per section.

---

```
SUBSTITUTE TEACHER HANDOFF PACK
[Classroom / Teacher Name]
[Date generated]
⚠️ CONFIDENTIAL — For school use only. Do not photograph or share.

═══════════════════════════════════════
CLASSROOM BASICS
═══════════════════════════════════════
Room: [X] | Programme: [PPKI/Pendidikan Khas]
Your aide today: [Name, phone]
If you need help: [Admin name, extension]
Quiet room / calm space: [Location]

DAILY SCHEDULE (posted on classroom board):
Follow the visual schedule on the board — do NOT change the order.
Use visual timer for each activity — students rely on this.

KEY RULES:
- Never remove a student from their visual schedule without showing them "change" card
- Always give 2-minute warning before transitions (hold up timer)
- Calm corner = back-left. Any student can use it — do not prevent this.

═══════════════════════════════════════
STUDENT PROFILES (one per student)
═══════════════════════════════════════

[For EACH student — repeat this block:]

───────────────────────────────────────
[NAME] | Age [X] | [Photo reference: photos/[name]-photo.jpg]
COMMUNICATION: [Non-verbal PECS Ph.3 / Minimally verbal / Verbal — brief]
TOP TRIGGERS: [1. X   2. Y   3. Z]
IF DISTRESSED:
  1. [Step 1]
  2. [Step 2]
  3. [Step 3]
DON'T: [What makes it worse — 1–2 points]
ELOPEMENT: [YES — [brief protocol] / No]
EMERGENCY CONTACT: [Parent name] — [Phone]
MEDICAL: [Any alert — or "None"]
───────────────────────────────────────
[Next student...]

═══════════════════════════════════════
EMERGENCY CONTACTS
═══════════════════════════════════════
Admin / Principal: [Name] — [Phone/Extension]
School guard / Security: [Phone]
999 (ambulance/police): When? Seizure, serious injury, elopement off school grounds
DO NOT call police for meltdowns — call parent first, then admin.

Parent emergency contacts: (see each student's section above)
```

## After generating

Ask: "Would you like to save this as a file (sub-pack-[date].md) or just read it here?"
- If save: Write to `logs/sub-pack-[YYYY-MM-DD].md`
- Mention: "You can print this from the file — each section is designed to fit on one printed page."

## Notes for Claude
- Keep each student section to a maximum of half a page — subs are overwhelmed, not reading a novel
- ONLY include what is documented — no generic advice added
- The tone should be clear and direct, not clinical — a sub needs to act on this quickly
- Include the photo reference so the sub can match faces to names (photos stored locally in photos/ folder)
- Mark clearly: CONFIDENTIAL. For school use only.
