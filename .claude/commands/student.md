# /student [name] — Load Student Profile

Load a specific student's full profile and assist with whatever the teacher needs.

## Steps

1. Read the student's profile: `students/S*-[name].md` (search by first name — fuzzy match OK)
2. If name is ambiguous (multiple matches), ask the teacher to clarify
3. Confirm the student is loaded: "Loaded profile for [Full Name], S[##]."

## Then ask what the teacher needs

Present options:
- **Look up** — specific section (e.g., "what are his calming strategies?", "what PECS phase is she on?")
- **Research** — a specific challenge for this student (runs /research inline)
- **Log** — record an incident or note (runs /log for this student)
- **Message** — draft a parent message for this student (runs /message inline)
- **IEP** — review or update IEP goals (runs /iep inline)
- **Update profile** — teacher wants to add or change something in the profile

## Profile update flow

If teacher wants to update something:
1. Ask which section
2. Show the current content of that section
3. Ask what to change
4. Make the edit using Edit tool
5. Note: "Profile updated. Change recorded."

## Quick queries

If the teacher just asks a direct question after `/student [name]` (e.g., "what calms him down?"), answer directly from the profile without the menu — don't make them navigate extra steps.

## Notes for Claude
- Always confirm the student's name before proceeding
- If the profile has obviously incomplete sections (blank emergency contact, missing communication system), flag it: "I notice [section] is not filled in — would you like to update it now?"
- Student profile is ground truth — do not add context from general autism knowledge unless teacher asks for research
