# HANDOFF — AI Course Programme Development (HKU Business Department)

> **Purpose of this file:** Context handoff for any Claude / Fable session continuing this project.
> Read this fully before doing any work. It contains all decisions already made — do not re-ask these questions.

---

## 1. Who you're working with

- **John** (johnchin@pandaocean.com) — Program Lead AND instructor at a Hong Kong university college (business department).
- His partner may also work on this project via their own AI session — keep outputs consistent with this file.

## 2. The project

Design and develop a **120-credit, QF Level 5 diploma programme** teaching business people to build and command AI agent teams. It will be **submitted to a government funding scheme** (free for students) and carries **undergraduate module diploma credit** at the college.

## 3. Decisions already made (DO NOT re-ask)

| Item | Decision |
|---|---|
| Credits / hours | 120 QF credits = 1,200 notional learning hours (10 hrs/credit) |
| Structure | 8 modules × 15 credits; 45 contact hrs each (360 total), 105 self-study each |
| Pedagogy | Every module = **Theory (12h) → Demo (12h) → Practice (21h)** — this is the programme's signature |
| QF level | Level 5 (degree-linked) |
| Delivery | Hybrid: theory online (recorded + Q&A), demos live online, practice in-person labs |
| Duration | 18 months part-time recommended (2 modules/term × 3 terms... see blueprint §3.3); 12-month accelerated variant |
| Audience | Undergrads + working professionals + SME owners + faculty (internal capability cohort first) |
| Tools budget | Paid Claude/ChatGPT seats, Claude Code, no-code platforms (n8n self-hosted preferred) |
| Instructor | John himself |
| Positioning | Differentiate from private competitor (see §5) — university credential + government-funded (free) + **proprietary data** |

## 4. The unfair advantage: PROPRIETARY DATA

The school has **proprietary Amazon/e-commerce sales data and tools/database access** that no private course can replicate. Modules 5–6 and the capstone are built on it. Every marketing message and funding-bid argument should lead with: *accredited + free + real marketplace data*.

## 5. Competitor analysis (already done)

**Steven Tse — Remarkable Marketing — https://getaiagents.co/** ("打造你的 AI Agent 團隊")
- Sells Claude Code agent-building to non-coders (bosses, freelancers, agencies, creators). Cantonese market.
- His 7-module arc: Mindset → Workflow decomposition → Agent roles → Integration → SOP → Context management → Remote control.
- His marketing: identity transformation ("operator → commander"), ROI math (3–5 hrs/day saved, HK$360k/yr), FOMO ("divide within 12 months"), 9 concrete use cases with before/after times.
- **His weaknesses = our openings:** no credential, paid, demo-led with no assessment, no data, no governance/ethics, no QA.
- **What we adopt from him:** concrete use cases with time savings, identity narrative, deployable output every module, his 7-skill skeleton (becomes our M1–M4).
- Source files in this folder: `ai with steven.txt` (his full landing page text), `chatgpt summary.txt` (funnel breakdown).

## 6. The 8-module curriculum (locked structure — content can be developed)

| # | Module | Term | Core |
|---|---|---|---|
| M1 | AI Foundations & the Agentic Business Paradigm | 1 | Chat vs agent; AI Opportunity Audit |
| M2 | Prompt Engineering & AI Workflow Design | 1 | Task decomposition; reusable SOPs |
| M3 | Building AI Agent Teams with Claude Code | 2 | Sub-agents, context files, MCP, remote access |
| M4 | No-Code Automation & Systems Integration | 2 | n8n/Make/Zapier; AI-in-the-loop pipelines |
| M5 | E-Commerce Data Analytics with Proprietary Marketplace Data | 3 | **THE MOAT** — real Amazon data, buyer intent, market entry |
| M6 | AI-Driven Marketing & Content Operations | 3 | Content intelligence, ads (ROAS/CPA/CTR), landing pages |
| M7 | AI Governance, Ethics & Responsible Deployment | 3–4 | PDPO, IP, hallucination risk, org policy |
| M8 | Capstone: Applied AI Agent System | 3–4 | Real deployment with **measured before/after ROI** |

Full specs (theory/demo/practice content + assessments per module): see `AI_Course_Programme_Blueprint.docx` §4.

## 7. How the agents are technically built (John's knowledge gap — now answered)

Steven's stack is entirely public tools — no secret tech:
1. **Claude Code** — terminal AI agent; reads/writes files, runs commands, multi-step autonomy; plain-language, no coding.
2. **Context files** (CLAUDE.md per project folder) = "employee handbook" the agent reads on start.
3. **Sub-agents** = specialist roles (research/copy/review) orchestrated by a lead agent.
4. **MCP connectors** = the agent's "hands" (web, YouTube transcripts, Sheets, ad accounts, databases).
5. **n8n / Make / Zapier** = scheduled recurring automations calling AI at smart steps.
6. **Remote access** = Claude Code on an always-on machine, controlled from phone.

All 9 of Steven's showcase use cases are combinations of the above. **Instructor bootcamp = rebuild all 9 before launch.**

## 8. Folder structure & files

```
D:\PycharmProjects\PythonProject\033-AI-Agent-Course-Development\
├── 00-Project Handoff/        <- START HERE
│   └── HANDOFF.md                (this file)
├── 01-Learning Knowledge/     <- research & source material
│   ├── ai with steven.txt        (competitor's full landing page text, Cantonese)
│   └── chatgpt summary.txt       (structural breakdown of the competitor funnel)
├── 02-Course Blueprint/       <- programme design
│   └── AI_Course_Programme_Blueprint.docx  (master blueprint: positioning, architecture, module specs, tooling, QA, GTM, risks)
├── 03-Schedules/              <- delivery schedules
│   ├── AI_Bootcamp_Schedule_2-3Day.xlsx    (2.5-day rush bootcamp, EN+CN sheets, revised headers)
│   └── Training Course Schedule Template for 2_3 Day.xlsx  (original template, reference only)
└── 04-Skills/                 <- reusable AI skills for this project
    ├── course-development.skill            (installable — drag into Claude / Save skill button; runs the full pipeline: read research -> interview -> blueprint docx -> schedule xlsx -> update handoff)
    └── course-development-SKILL.md         (readable source of the same skill)
```

**Convention:** file new materials by stage number — research into `01`, design docs into `02`, schedules into `03`, skills into `04`; create `05-Marketing`, `06-Submission`, etc. as the project grows.

## 8b. Product portfolio matrix (tracks × levels)

The business runs a course portfolio; every course slots into this matrix. Levels are defined by outcome: L1 = use AI tools on guided tasks; L2 = independently build a strategy/portfolio; L3 = build systems + credential. Each level sells the next (masterclass → L1 → L2 → L3).

| Level | AI Agent track | E-commerce track | Hybrid track |
|---|---|---|---|
| L1 Foundation | 2.5-day bootcamp ✅ (`03-Schedules`) | **GAP — assigned to partner, build next** (~15h, tool-operation level, subset of the L2 course, deliberately shallow to leave upsell room) | Free masterclass (lead magnet, to design) |
| L2 Practitioner | *(gap, optional)* | 30h Brand Internationalization ✅ (`02-Course Blueprint/HKU_SPACE_AI_Brand_Internationalization_Blueprint.docx`) | *(gap)* |
| L3 Professional | — | — | 120-credit QF L5 diploma ✅ (`02-Course Blueprint/AI_Course_Programme_Blueprint.docx`) |

File naming for new courses: `<TRACK>-L<level>_<Name>` (e.g. `ECOM-L1_..._Blueprint.docx`). Note: the L2 Brand Internationalization doc says "零基础" — treat that as "no prerequisites", not "beginner"; by outcome it is L2. Update this matrix whenever a course is added.

## 9. Next steps (open work — pick up here)

1. **Confirm funding scheme specifics** — exact credit definition, contact-hour minimums, assessment rules; adjust 8×15 structure if required. *(John to supply scheme name/docs.)*
2. **Write full QF L5 learning outcomes** per module (submission core document) — use Level 5 descriptor verbs: analyse, design, construct, evaluate, manage.
3. **Develop detailed session plans** — per module: 12 theory sessions, demo scripts, 21 lab hours of exercises.
4. **Instructor bootcamp materials** — step-by-step rebuilds of Steven's 9 use cases in Claude Code + n8n.
5. **Scope the proprietary database for teaching** — access model, anonymisation, M5 lab dataset.
6. **Design the free public masterclass** (lead magnet) — 90 min, live-build one agent, end with funded-programme offer; collect waitlist.
7. **Assessment rubrics** per module + capstone ROI measurement template.

## 10. Working rules for the AI session

- **GROUNDING RULE (most important):** write course content ONLY from files in `01-Learning Knowledge/` and the user's own words. Never invent statistics, readings, case studies, or tool claims. If information is missing, ask or mark `[TO CONFIRM]`. Outline with sources first, get approval, then write.
- **FORMAT RULE:** course documents follow the approved formats in `01-Learning Knowledge/format references/` (government execution document + formal syllabus V–VIII). Simple bullets and session tables — no extra sections, no consultant frameworks.
- Write for a **government funding submission audience** when producing official docs: measured claims, QF terminology, no hype.
- Write for **HK adult learners** when producing course/marketing material: concrete use cases, before/after time savings, Cantonese-friendly phrasing acceptable.
- Keep the **Theory → Demo → Practice** split in anything session-level.
- Never position the programme as a clone of Steven's course; frame as *accredited, data-driven, free* superset. Consider practitioners like him as potential guest speakers.
- All credit math must reconcile to 120 credits / 1,200 NLH / 360 contact hours (for the L3 diploma; other courses have their own totals — always reconcile).
- John prefers **concise, direct** communication.
- The `course-development` skill (v4, in `04-Skills/`) is **general-purpose** — it works for ANY course topic and any AI agent (Claude, Codex, etc.). Project-specific conventions (tracks/levels matrix, naming, tone) live in THIS file, not in the skill.
