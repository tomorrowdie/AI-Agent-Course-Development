---
name: course-development
description: Course/programme development pipeline for ANY course topic. Run this skill as the FIRST action whenever this project repo/folder is opened or downloaded, whenever the user types "start skill", or whenever they mention a new course, programme, curriculum, syllabus, bootcamp, diploma, timetable, or course document. The procedure — ask which course/program to work on, read ONLY the provided knowledge, ask output language, then produce three deliverables (course execution document, formal syllabus, Excel timetable). Works in any AI agent (Claude, Codex, others).
---

# Course Development Pipeline

A fixed procedure that turns provided knowledge into three standard course deliverables. Topic-agnostic — works for any course, any audience, any institution.

## THE THREE LAWS (override everything else)

**1. Grounding — write ONLY within the provided knowledge.**
Every fact, topic, session, statistic, tool name, case study, and reading must trace to (a) files in `01-Learning Knowledge/`, (b) the user's own words in chat, or (c) HANDOFF.md. If something is needed but not provided, ASK or write `[TO CONFIRM]` — never invent. Invented content has already caused rejected drafts; a short honest document beats a long hallucinated one.

**2. Think before writing.**
Before each deliverable: show a short outline listing each section and WHERE it comes from (which knowledge file / user answer). Get the user's yes, then write. Outline items without a source get removed or asked about.

**3. Simplicity — match the approved format, add nothing.**
Follow `references/formats.md` EXACTLY — same sections, same order. Short bullets, session tables, plain language. No extra sections, no consultant frameworks, no unrequested content.

## Portability (works in any AI agent)

Tool names are suggestions. If unavailable in your environment:
- No multiple-choice question tool → ask plain questions in chat, max 4 at a time
- No docx/xlsx tools → produce clean Markdown with tables; tell the user it can be converted
- No file-presentation tool → state saved file paths in your reply
- No folder-connection tool → ask the user for the project folder path

## Folder convention

```
00-Project Handoff/     HANDOFF.md — project memory; READ FIRST; contains decisions already made
01-Learning Knowledge/  ALL source knowledge (incl. format references/ subfolder)
02-Course Blueprint/    finished course documents
03-Schedules/           Excel timetables
04-Skills/              this skill and other reusable assets
05-Marketing/           sales assets (when reached)
06-Submission/          final submission packages (when reached)
```

## THE PROCEDURE (run these steps in order, every time)

### Step 1 — Entry
This skill runs as the first action when the project repo/folder is opened. Read `00-Project Handoff/HANDOFF.md` — it holds decisions already made; never re-ask them.

### Step 2 — Ask which course/program
Ask the user ONE question: "Which course or program are we working on today?" Any topic is valid. If they have new knowledge for it (files, pasted text, URLs), file it into `01-Learning Knowledge/` (subfolder per course if the project has several) before continuing. Chat disappears; the folder is the memory.

### Step 3 — Read the knowledge (and nothing else)
Read ALL files in `01-Learning Knowledge/` relevant to this course, fully. Build a short inventory of what the knowledge actually contains: topics, session structures, hours, constraints, required elements. This inventory is the hard boundary of what you may write (Law 1). Tell the user briefly what you found and what is missing.

### Step 4 — Ask output language
Ask ONE question: "What language(s) for the outputs?" (e.g. Traditional Chinese / Simplified Chinese / English / bilingual). Also confirm here, in the same round, only what the knowledge did not answer: total hours or session count, and any fixed institutional constraints (no internet, no computers, mandated assessment weights).

### Step 5 — Produce the three deliverables (in this order)
Read `references/formats.md` first. For each deliverable: outline with sources → user yes → write → self-check → save.

1. **Course Execution Document** (Format 1 — the government/correctional-style structure: one-line positioning, execution principles, target audience, objectives, session table, per-class teaching flow, assessment table, team support) → save to `02-Course Blueprint/`
2. **Formal Syllabus** (Format 2 — sections V–VIII: Syllabus modules, Teaching & Learning Activities hours line, Assessment table with ILO mapping, Readings in Harvard/APA — never invent readings) → save to `02-Course Blueprint/` (same file as an appendix, or separate file — user's choice)
3. **Excel Timetable** → save to `03-Schedules/`. If an existing schedule template is in the project, copy and edit it, preserving formatting; never overwrite the original. Headers per day block: Time | Session Block | Topic | Format (Theory/Demo/Practice) | Learning Outcome | Tools/Materials | Provided by School | Deliverable. Mirror sheets per language if bilingual.

Self-check for every deliverable: all content traces to knowledge or user answers; hours sum correctly; assessment weights = 100%; no invented readings/statistics/cases; section list matches the template exactly; language matches Step 4.

### Step 6 — Close the loop
Update `00-Project Handoff/HANDOFF.md`: add the course to the project's course list, record decisions made this run, refresh the folder tree. List the files created. Nothing may live only in chat.

## Working style

- Concise, plain language; the user is a busy program lead.
- All numbers must reconcile (hours, weights, session counts).
- When in doubt between impressive and simple: choose simple. Reviewers reward clarity, not complexity.
