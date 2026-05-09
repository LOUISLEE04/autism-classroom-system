# Autism Classroom Support System

An AI assistant for special education teachers — built on Claude Code, designed for **Pendidikan Khas** classrooms in Malaysia.

Know every student. Respond faster in a crisis. Plan better lessons. Spend less time on paperwork.

---

## What It Does

You have 10 students. Each one communicates differently, has different triggers, different calming strategies, different medical needs. Holding all of that in your head every day is exhausting.

This system gives you a structured profile for each student — and an AI that reads those profiles before answering any question you ask.

**Daily use:**
- `/morning` — start the day with a class briefing and any flags from yesterday
- `/student [name]` — pull up any student's full profile instantly
- `/emergency [name]` — surface a student's crisis protocol in under 5 seconds
- `/log` — guided incident logging (structured, consistent, shareable)
- `/plan [topic]` — get activity ideas differentiated across all communication levels
- `/research [name] [question]` — evidence-based strategies specific to your student's profile
- `/message [name]` — draft a parent WhatsApp or written note
- `/iep [name]` — track and update IEP goals
- `/sub` — generate a substitute teacher handoff pack

---

## Who This Is For

Special education teachers running a dedicated autism classroom — especially in Malaysian government or private schools under the PPKI (Program Pendidikan Khas Integrasi) framework.

Works best for classrooms with a mix of non-verbal, minimally verbal, and verbal students at different support levels.

---

## What's Inside Each Student Profile

Every student gets a detailed profile covering:

- **Communication** — PECS phase, AAC device, what they can and can't express, how they signal distress
- **Sensory profile** — what overwhelms them, what calms them, accommodations in place
- **Behavioural profile** — meltdown early warning signs, de-escalation steps that work, what makes it worse, crisis protocol
- **Learning profile** — academic level, attention span, motivators, preferred and challenging activities
- **Medical & safety** — medications, allergies, seizure history, elopement risk, self-injury
- **Parent contact** — preferred language, contact method, standing notes
- **IEP goals** — current goals, progress notes, review dates
- **Visual supports** — PECS board details, AAC vocabulary, calm corner setup

---

## Getting Started

### Prerequisites
- [Claude Code](https://claude.ai/code) installed on your device
- That's it

### Setup (30–60 minutes)

```
1. Download or clone this repo
2. Open the folder in Claude Code
3. Fill in memory/teacher-profile.md with your school and classroom details
4. Run /add-student for each of your students
5. Run /morning to test everything is working
```

Claude will guide you through every step. See [ONBOARDING.md](ONBOARDING.md) for the full walkthrough.

---

## File Structure

```
CLAUDE.md                    ← System instructions (Claude reads this automatically)
ONBOARDING.md                ← Step-by-step setup guide
memory/
  teacher-profile.md         ← Your classroom, staff, admin contacts
  class-roster.md            ← One-page overview of all students
  malaysia-resources.md      ← NASOM, PPKI, JKM, SERC, OT/SLT references
students/
  _template.md               ← Blank profile template
  S01-sample-izzat.md        ← Filled example (fictional student)
logs/
  incidents.md               ← Behaviour and incident log
  daily-notes.md             ← Quick daily observations
  parent-comms.md            ← Parent communication log
iep/
  goals-template.md          ← IEP goal tracking template
.claude/commands/            ← All slash commands
```

---

## Optional: Private Backup

You can back up your classroom data to a private GitHub repository — useful for disaster recovery or getting support from a trusted administrator.

Just tell Claude:

> *"Set up private sync"*

Claude handles everything automatically. See [ONBOARDING.md](ONBOARDING.md) for details.

---

## Privacy

All student data is stored **locally on your device**. Nothing is uploaded anywhere unless you explicitly set up the optional private sync.

This system is designed with Malaysia's **Personal Data Protection Act 2010 (PDPA)** in mind:
- Keep your device password-protected
- Do not paste student profiles into other AI tools or cloud services
- Archive (do not delete) profiles when students leave — records may be needed later

---

## Malaysian Context

Built specifically for the Malaysian special education system. References throughout to:
- PPKI (Program Pendidikan Khas Integrasi)
- NASOM, JKM, SERC, Permata
- PECS and AAC frameworks common in Malaysian classrooms
- Bahasa Malaysia terminology where relevant
- Parent messaging in BM or English

---

## Contributing

This is open-source and community-owned. Contributions welcome:
- Additional Malaysian resources (therapy centres, funded programmes, state-specific contacts)
- Bahasa Malaysia translations of the onboarding guide and templates
- Adaptations for other diagnoses (ADHD, Down Syndrome, dyslexia)
- Improvements to the student profile template based on real classroom use

---

## This Is Not a Replacement for Professionals

This tool helps you:
- Respond faster in a crisis using documented, agreed protocols
- Plan better by knowing each student's needs
- Research evidence-based strategies when you're stuck
- Spend less time on paperwork

It does not replace your OT, SLT, SERC officer, or the student's professional care team.

---

*Built on Claude Code (Anthropic) · Designed for Pendidikan Khas classrooms in Malaysia*
