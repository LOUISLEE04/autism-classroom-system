# /log — Guided Incident & Behaviour Logging

Use after any notable incident, meltdown, behaviour worth tracking, or positive milestone.

## Steps

Ask these questions ONE AT A TIME using the AskUserQuestion tool where possible, or as a conversational flow:

1. **Which student?** (name or number)
2. **What type of log entry?**
   - Incident / meltdown
   - Positive milestone / progress
   - Quick daily observation
   - Parent communication
3. **What happened?** (brief description — teacher's own words, no interpretation needed)
4. **When did it happen?** (time, e.g., "10:30am" or "after lunch")
5. **What do you think triggered it?** (or "unknown" is fine)
6. **What strategies did you use?** (even if they didn't work)
7. **How was it resolved?** (e.g., "calmed after 12 min in calm corner" / "still unsettled at end of day")
8. **Duration?** (approximate — e.g., "about 15 minutes")
9. **Were other students affected?** (Yes / No / Briefly)
10. **Any injury?** (Student / Teacher / Other)
11. **Does a parent need to be contacted?** (Yes / No / Already done)

## Output

Format the log entry and append to the correct file:

**For incidents/meltdowns/observations → `logs/incidents.md`:**
```
---
[YYYY-MM-DD HH:MM] | Student: [Name] | Type: [Incident/Positive/Observation]
What happened: [description]
Trigger (known/suspected): [X]
Strategies used: [X]
Resolution: [X]
Duration: [X min]
Other students affected: [Yes/No]
Injury: [None / describe]
Parent notified: [Yes — [method] / No / N/A]
Logged by: [Teacher — today's date]
```

**For parent communications → `logs/parent-comms.md`:**
```
---
[YYYY-MM-DD HH:MM] | Student: [Name]
Contact: [Parent name]
Method: [WhatsApp / Call / Note]
Summary: [What was communicated]
Response: [e.g., "Parent acknowledged, will monitor at home" / "No response yet"]
Follow-up needed: [Yes/No]
```

## After logging

Ask: "Would you like me to check if this incident matches a pattern for [student name]?" 
- If yes: scan previous incidents.md entries for this student and flag patterns (same trigger, same time of day, increasing frequency)
- Note: patterns are informational only — always recommend discussing with SLT/OT/SERC for interpretation

## Notes for Claude
- Never editorialize or interpret beyond what the teacher described
- Use teacher's own words where possible
- If teacher mentions injury, remind them of school incident report obligation
- Positive milestones are just as important to log as incidents
