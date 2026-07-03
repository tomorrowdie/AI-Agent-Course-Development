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
2. First message: `Read 00-Project Handoff/HANDOFF.md first, then let's continue the course development.`
3. To install the project skill: drag `04-Skills/course-development.skill` into the chat and click **Save skill**. After that, typing `start skill` runs the full course-development pipeline.

**Claude Code (terminal):**
```
cd AI-Agent-Course-Development
claude
```
Then say: `Read "00-Project Handoff/HANDOFF.md" first, then let's continue the course development.`

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
