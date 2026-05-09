# /add-student — Add a New Student

Interactive wizard to create a new student profile. Takes about 10–15 minutes to complete.

## Before starting

1. Read `memory/class-roster.md` — check existing student numbers (S01–S10, etc.) to assign the next number
2. Tell the teacher: "I'll guide you through the essential information first. You can fill in the detailed sections later — the important thing is to get the safety-critical info in now."

## Phase 1: Safety-Critical (MUST complete before saving any profile)

Ask these questions one at a time using the AskUserQuestion tool:

1. **What is the student's full name? And what do they prefer to be called?**
2. **How old are they?**
3. **How does this student communicate?**
   - Non-verbal (PECS/AAC/signs)
   - Minimally verbal (some words/phrases)
   - Verbal (with support)
   - If PECS: which phase?
   - If AAC: which device/app?
4. **What are the top 2–3 things that can trigger a meltdown or distress?**
5. **When they're upset, what are the first signs you notice?** (early warning signals)
6. **What helps calm them down?** (top 2–3 strategies that actually work)
7. **What makes it WORSE?** (what to absolutely avoid during distress)
8. **Is there any elopement risk?** (do they run/try to leave?)
9. **Any self-injurious behaviour?** (hitting head, biting self, etc.)
10. **Any medical alerts?** (seizures, allergies, medications — anything the school must know)
11. **Primary emergency contact: name, relationship, phone number?**
12. **ASD level if known?** (1, 2, 3 — or "not formally assessed")

## Phase 2: Learning & Sensory (Important — ask now or later)

Ask: "Do you want to fill in the learning and sensory information now, or come back to it?"
- If now: continue with questions below
- If later: save Phase 1 info and remind teacher to complete the profile within the first week

13. **What calms their sensory system?** (weighted blanket, music, rocking, etc.)
14. **What sensory inputs cause distress?** (sounds, lights, textures, etc.)
15. **What are their strongest motivators?** (iPad, stickers, specific toys, food, praise)
16. **What's their current academic/communication level?** (pre-literacy, Year 1 level, etc.)
17. **Preferred seating position in the classroom?**

## Phase 3: Create the profile file

1. Determine the next student number: check how many files exist in `students/` (S01, S02... pick next)
2. Copy the template structure from `students/_template.md`
3. Fill in all Phase 1 and Phase 2 answers
4. Leave all blank/unknown sections as `[Not yet documented — update when available]`
5. Save as `students/S[##]-[firstname].md`
6. Add to `memory/class-roster.md`: new row with name, age, communication level, key alert, emergency contact

## After creating

Tell the teacher:
- "Profile created for [Name] as S[##]."
- "The following sections still need completing: [list any blanks]"
- "You can update these anytime by saying '/student [name]' and choosing 'Update profile'."
- "I'd recommend completing the sensory profile, full learning profile, and support services section within the first week — these help a lot for daily planning."

## Notes for Claude
- Never save a profile without at minimum: name, communication method, 1 trigger, 1 de-escalation strategy, and 1 emergency contact. These 5 are non-negotiable.
- If the teacher is mid-session and hasn't finished, save a partial profile with clear [INCOMPLETE] markers — don't wait to save nothing
- Do NOT create generic placeholder content — only document what the teacher actually tells you
- If teacher doesn't know something (e.g., ASD level), that's fine: document as "Unknown — recommend formal assessment referral"
