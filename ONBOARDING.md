# Onboarding Guide — Autism Classroom Support System
### Setup guide for teachers | Pendidikan Khas

Welcome. This guide will get your classroom AI assistant running in about 30–60 minutes, depending on how many students you add today. You don't need to complete everything at once — the system works as soon as your first student profile is in.

---

## What You Need Before Starting

- [ ] **Claude Code installed** on your device (the teacher's laptop or school device)
- [ ] **This folder** downloaded/cloned to your computer
- [ ] **20–30 minutes** for initial setup
- [ ] **Your students' basic info** ready (you don't need everything — see below for what's essential)

---

## Step 1: Open This Folder in Claude Code

1. Open Claude Code
2. Click **Open Folder** (or from the terminal: `claude "/path/to/autism-classroom-system"`)
3. Claude will load and read the `CLAUDE.md` instructions automatically

You'll know it's working when Claude responds with awareness of the classroom context.

---

## Step 2: Fill In Your Teacher Profile

Open `memory/teacher-profile.md` in any text editor (or ask Claude to help you fill it in).

**Essential fields to fill in now:**
- Your name and school
- Classroom location
- Admin contacts (Principal, Senior Assistant)
- Your support staff (aides) and their names
- Any classroom equipment available (AAC devices, sensory tools, etc.)

Everything else can be filled in later.

---

## Step 3: Add Your Students

This is the most important step. Run this command in Claude:

```
/add-student
```

Claude will guide you through a series of questions for one student at a time. Focus on **safety-critical information first:**
- Communication method (PECS phase / AAC / verbal)
- Known triggers
- De-escalation strategies that work
- Emergency contact
- Any medical alerts

**You don't need everything today.** The system will flag what's missing and remind you to complete it.

Repeat `/add-student` for each of your 10 students. You can do them over multiple sessions.

---

## Step 4: Review Your Class Roster

After adding students, check `memory/class-roster.md`.

Make sure:
- [ ] All 10 students are listed
- [ ] Communication levels are correct
- [ ] Emergency contacts are in place
- [ ] Medical alerts are captured for any student who has them

---

## Step 5: Test the System

Try these commands to make sure everything is working:

```
/morning
```
→ Should show you a class briefing with your students' names

```
/student [any student's name]
```
→ Should load their profile and ask what you need

```
/emergency [a student's name]
```
→ Should show their emergency protocol immediately

---

## Step 6: Daily Use

Once set up, your typical daily flow:

| When | What to do |
|------|-----------|
| Morning (before students arrive) | `/morning` — get the day's briefing |
| During class | `/student [name]` — quick lookup for any student |
| During/after an incident | `/log` — document what happened |
| When planning activity | `/plan [topic]` — get differentiated activity ideas |
| End of day | Quick `/log` for any notable observations |
| When writing to parent | `/message [name]` — draft the WhatsApp/message |

---

## What You Can Ask (Beyond Slash Commands)

You don't have to use slash commands for everything. You can just talk to Claude naturally:

> *"Izzat is covering his ears and I think he's about to have a meltdown, what do I do?"*

> *"I want to teach colours today — what activity works for my non-verbal students?"*

> *"Hazwan's mum wants to know why he's been coming home stressed. Help me write a WhatsApp message."*

> *"My substitute is coming on Thursday — can you prepare a handoff pack?"*

Claude will always check the relevant student profile before responding.

---

## Privacy — Important

This system stores student information on **your device only**. Please:

- Keep your device password-protected
- Do not paste student profiles into other AI tools, emails, or cloud storage
- When a student leaves your class: archive their profile (don't delete — records may be needed)
- This system operates in line with Malaysia's **Personal Data Protection Act 2010 (PDPA)**

---

## Getting Help

If something doesn't work or you're not sure how to do something, just ask Claude directly:

> *"How do I add a new goal for [student]?"*
> *"Show me all the commands I can use"*
> *"How do I update [student's] sensory profile?"*

Claude will guide you through it.

---

## Quick Command Reference Card

*Print this and keep it at your desk.*

```
/morning              Daily briefing — run before class starts
/student [name]       Load a student's profile
/emergency [name]     ⚠️ Emergency protocol — immediate response
/log                  Record an incident, observation, or milestone
/plan [topic]         Plan a differentiated class activity
/research [name] [?]  Evidence-based research for a specific student
/iep [name]           Track or update IEP goals
/message [name]       Draft a parent/guardian message
/sub                  Generate substitute teacher handoff pack
/add-student          Add a new student to the system
```

---

*System built on Claude Code (Anthropic)*
*Designed for Pendidikan Khas classrooms in Malaysia*
*Open-source — adapt freely for your classroom*
