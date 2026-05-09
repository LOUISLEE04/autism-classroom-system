# /morning — Daily Class Briefing

Run at the start of each school day.

## Steps

1. Read `memory/class-roster.md`
2. Read `memory/teacher-profile.md` (support staff present today)
3. Read the last 3 entries in `logs/daily-notes.md` (yesterday's observations)
4. Read the last 3 entries in `logs/incidents.md` (any recent incidents that need follow-up)

## Output

Present a clean morning briefing:

```
📋 MORNING BRIEFING — [Day, Date]

CLASS TODAY: [X students present / full class]

⚡ ACTIVE FLAGS:
- [Name]: [flag — e.g., "Had meltdown yesterday — monitor today"]
- [Name]: [flag — e.g., "Parent notified of medication change"]
- (if no flags: "No active flags — clean slate")

COMMUNICATION CHECK:
- Non-verbal (PECS/AAC): [S01, S02, ...]
- Minimally verbal: [S03, ...]
- Verbal: [S05, ...]

FOLLOW-UP NEEDED:
- [Any outstanding parent messages, IEP notes, incident reports to complete]

SUPPORT STAFF TODAY:
- [Names and roles present]
```

5. Ask: **"Any changes or alerts before we start today?"**
   - Teacher can add flags for the day (e.g., "Izzat didn't sleep well", "S03 has a new aide today")
   - Update the "Alerts Today" section of `memory/class-roster.md` with anything flagged

6. Ask: **"What's today's theme or main activity? I can help you adapt it for the class."**
   - If teacher provides one → run a quick `/plan [topic]` preview
   - If not → offer 2–3 simple, low-prep activity suggestions appropriate for the class range

## Notes for Claude
- Keep the briefing clear and scannable — the teacher is busy
- Flag anything from yesterday's notes that needs a follow-up today
- If any student hasn't had their profile updated in over 30 days, note it briefly (don't nag)
