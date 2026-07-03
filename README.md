# AI Agent Course Development

Course development project for a 120-credit QF Level 5 programme (AI Business Automation & Agentic Commerce).

## Get the project on your computer

1. Install Git from https://git-scm.com (default options).
2. Open a terminal where you want the folder (e.g. Documents: right-click → Open in Terminal) and run:

```
git clone https://github.com/tomorrowdie/AI-Agent-Course-Development.git
```

This creates the `AI-Agent-Course-Development` folder with everything in it.

> **Note:** this is a private repo — you need a GitHub account and an invite from John (repo → Settings → Collaborators) before cloning works.

## Work on it with Claude

**Claude Cowork (desktop app):**
1. Start a session and connect the `AI-Agent-Course-Development` folder.
2. One-time: install the skill — drag `04-Skills/course-development.skill` into the chat and click **Save skill**.
3. Every time you open this repo, your FIRST message is: `start skill`

The procedure then runs by itself: asks which course/program to work on (any topic) → reads ONLY the knowledge in `01-Learning Knowledge` → asks your output language → produces the three deliverables — course execution document + formal syllabus (into `02-Course Blueprint`) and Excel timetable (into `03-Schedules`).

**Claude Code / other AI (terminal):**
```
cd AI-Agent-Course-Development
claude
```
First message: `Read "04-Skills/course-development-SKILL.md" and follow its procedure.` (Works in Codex or other agents too — the skill file is plain text with fallback instructions.)

## Folder guide

| Folder | Contents |
|---|---|
| `00-Project Handoff/` | **START HERE** — HANDOFF.md is the project memory: all decisions made, curriculum, next steps |
| `01-Learning Knowledge/` | Research inputs (private — empty on GitHub, ask John for the files) |
| `02-Course Blueprint/` | Programme blueprint (private — empty on GitHub, ask John for the file) |
| `03-Schedules/` | Delivery schedules (Excel, EN+CN) |
| `04-Skills/` | The installable `course-development` Claude skill |

## Saving your changes back to GitHub

After editing files:

```
git add .
git commit -m "describe what you changed"
git push
```

To get the latest changes someone else pushed:

```
git pull
```

**Rule:** always `git pull` before you start working, and `git push` when you finish — this avoids conflicts when two people edit the same files.
