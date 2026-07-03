---
name: course-development
description: End-to-end course/programme development pipeline. Use whenever the user types "start skill" or similar, or has a new course concept, training idea, or education product to develop — including mentions of "new course", "programme", "curriculum", "bootcamp", "diploma", "funding submission", "course blueprint", "training schedule", or competitor course materials/landing pages to analyze. Also trigger to turn research into a sellable course or prepare a government funding bid. Runs the full pipeline — collect and file the user's knowledge into the project folder, analyze competitors, interview the program lead, produce a programme blueprint (Word), build a delivery schedule (Excel), update the project handoff — with every input and output filed into numbered stage folders so the structure stays clean.
---

# Course Development Pipeline

Turn a raw course concept plus research materials into a sellable, fundable programme: competitor analysis → structured interview → programme blueprint (.docx) → delivery schedule (.xlsx) → updated handoff.

Run the phases in order. Each phase produces a file the next phase depends on. Do not skip the interview — the blueprint's most expensive mistakes (wrong audience, wrong credit structure, wrong differentiator) all come from guessing what only the program lead knows.

## Folder convention

Work inside the user's project folder using numbered stage folders. Create any that don't exist:

```
00-Project Handoff/     HANDOFF.md — project memory & entry point for any AI session
01-Learning Knowledge/  research inputs: competitor pages, transcripts, notes, summaries
02-Course Blueprint/    programme blueprint .docx (one per course concept)
03-Schedules/           delivery schedule .xlsx files
04-Skills/              reusable AI skills & automation assets for the project
05-Marketing/           landing page copy, masterclass scripts, funnel assets (when reached)
06-Submission/          funding/accreditation documents (when reached)
```

New materials always get filed by stage number. If a HANDOFF.md exists in `00-Project Handoff/`, read it FIRST — it contains decisions already made; do not re-ask them.

## Phase 0 — Start & knowledge intake

This phase runs whenever the skill is invoked — especially on a bare trigger like "start skill" where the user hasn't provided anything yet. The goal: by the end of Phase 0, all raw knowledge is saved inside `01-Learning Knowledge/` so nothing lives only in the chat.

1. **Locate the project folder.** If a project folder with the numbered structure is already connected, use it. If not, ask the user to connect one (request_cowork_directory) or confirm where to create the structure. Create any missing numbered folders.
2. **Read the handoff.** If `00-Project Handoff/HANDOFF.md` exists, read it before asking the user anything.
3. **Collect the knowledge.** Ask the user (AskUserQuestion or plain question) how they want to provide input for this course concept — they can do any mix of:
   - **Upload files** (competitor pages saved as text, transcripts, notes, PDFs, screenshots)
   - **Type or paste** the concept, ideas, or research directly into chat
   - **Give URLs** to competitor courses or reference material
4. **File everything into `01-Learning Knowledge/`** before proceeding:
   - Copy uploaded files in, keeping meaningful names
   - Save typed/pasted content as dated text files, e.g. `2026-07-03 course concept - <topic>.txt`
   - Save fetched URL content as `<site> landing page.txt`
   - If this is a new course concept inside an existing project, group its inputs in a subfolder: `01-Learning Knowledge/<concept-name>/`
5. **Confirm the record.** Briefly list what was filed, then proceed to Phase 1.

Why this matters: chat content disappears; the folder is the project's memory. Every future session (including the partner's) depends on the knowledge being in `01`, not in a conversation transcript.

## Phase 1 — Research (before any interviewing or writing)

Gather every fact before touching deliverables:

1. Read ALL files in `01-Learning Knowledge/` (and any files the user uploads or points to).
2. Fetch any URLs the user gives (competitor landing pages, reference courses). If a page is client-rendered and returns only meta tags, open it in the browser tools to get full text.
3. For each competitor course found, extract a teardown:
   - **Promise & positioning** — the transformation being sold (often identity change, e.g. "operator → commander"), not the feature list
   - **Audience segments** and the pain narrative used
   - **Curriculum skeleton** — modules/skills progression
   - **Use cases shown** — with any before/after time or ROI numbers
   - **Authority stack** — instructor credentials, testimonials, proof numbers
   - **Price/funnel model** — webinar, lead magnet, urgency mechanics
   - **Weaknesses** — the openings: no credential? no assessment? no data? no QA? demo-led with no practice?
4. Save a short competitor-teardown summary into `01-Learning Knowledge/` if one doesn't already exist.

The teardown does double duty: weaknesses become the new course's differentiators, and strengths become marketing patterns to adopt (concrete use cases, time-saved numbers, identity narrative).

## Product matrix — tracks & levels

The business runs a portfolio of courses, not one course. Every new course concept must be placed in the matrix before designing, because level determines depth, template, and price point, and each level's job is to sell the next (masterclass → L1 → L2 → L3):

**Tracks:** AI Agent · E-commerce · Hybrid (AI × E-commerce — the flagship, uses proprietary data)

**Levels — defined by outcome, not hours:**
- **L1 Foundation** (~6–15 contact hrs): can use AI tools on guided tasks. Deliberately shallow — leaves room for L2 upsell. No prerequisites.
- **L2 Practitioner** (~30–60 contact hrs): can independently build a strategy/portfolio/deliverable. Portfolio project required.
- **L3 Professional** (credit-bearing, e.g. 120-credit QF L5): can build complete systems; earns the credential; funding-submission grade.

File naming: `<TRACK>-L<level>_<Name>` — e.g. `ECOM-L1_AI_Ecommerce_Starter_Blueprint.docx`, `AI-L1_Agent_Bootcamp_Schedule.xlsx`. Keep one portfolio-matrix table in HANDOFF.md showing which cells are built and which are gaps — update it whenever a course is added.

## Phase 2 — Interview the program lead

Use the AskUserQuestion tool in 2–3 short rounds (not one giant round). Cover, in roughly this order:

**Round 1 — context:** track and level in the product matrix (AI / E-commerce / Hybrid × L1/L2/L3) — check HANDOFF's portfolio matrix for gaps and adjacent courses first; primary audience(s); the user's role and mandate; the transformation students should achieve; relationship to competitors found in Phase 1 (template / rival / partner).

**Round 2 — structure:** format and duration (short course vs credit-bearing programme); accreditation/funding requirements (credits, QF/EQF level, contact-hour rules); domain focus vs general; tools/budget realistically available to students.

**Round 3 — sharpen:** the unfair advantage (proprietary data, industry access, credential, funding = free for students); delivery mode (in-person / online / hybrid); the user's biggest gap right now.

Rules of thumb:
- If a HANDOFF.md already answered a question, don't re-ask it.
- If the user answers vaguely ("advise me"), make the professional recommendation and state it in the blueprint rather than stalling.
- The single most valuable question is the unfair advantage — a course without one is a commodity; push politely until something concrete surfaces.

## Phase 3 — Programme blueprint (.docx)

Read the docx skill's SKILL.md before building. Output to `02-Course Blueprint/<TRACK>-L<level>_<Course_Name>_Blueprint.docx`.

Pick the template by level:

**Short-course template (L1 / L2, non-credit):** lighter document — course positioning & rationale; total hours and module table (modules × hours); learning outcomes; per-module detail with THEORY / DEMO / PRACTICE / Student Output rows; final project or portfolio; tools required; upsell path (which matrix cell this course feeds into). Bilingual (EN + Chinese) if the audience is HK/mainland. An L1 course must stay tool-operation level — if module outcomes read like independent strategy-building, that's L2 content; push it up or cut it.

**Credit-bearing template (L3, funding-grade):** the full structure below, with reconciled credit math.

### Credit & hours math (must reconcile — verify before delivering)

For credit-bearing programmes use the local qualification framework convention (HKQF: 1 credit = 10 notional learning hours). Typical defensible structure:
- Total NLH = credits × 10
- Contact hours ≈ 30% of NLH (standard for funded sub-degree provision)
- Equal-credit modules (e.g. 120 credits = 8 × 15) keep timetabling and funding submissions clean
- Every module's contact hours split **Theory → Demo → Practice** (roughly 25% / 25% / 50%, practice-heavy) — declare this split explicitly; it is the pedagogy signature funding assessors and marketing can both use

For short courses/bootcamps: total contact hours per day (~6h with lunch), map each block to the same Theory/Demo/Practice pattern.

### Required blueprint sections (credit-bearing / L3)

1. **Executive Summary** — programme in one page: size, structure, duration, delivery, differentiators
2. **Positioning & Competitive Differentiation** — competitor teardown table (them vs us), what we deliberately adopt from them, one-line positioning statement
3. **Programme Architecture** — credit/hour framework table, Theory–Demo–Practice split, duration options (recommend one), programme map (terms × modules × theme)
4. **Module Specifications** — per module: credits, NLH, contact hours, Theory content, Demo content, Practice content, Assessment (deployable artefact + one controlled component)
5. **Technical Delivery Guide** — how the thing being taught actually works, so the instructor can deliver it (close the instructor's own knowledge gaps explicitly)
6. **Tooling, Infrastructure & Budget Lines** — table mapped to funding lines; position owned assets as in-kind contribution
7. **Assessment & QA Framework** — assessment philosophy, AI-use policy if relevant, outcome-level alignment to the qualification framework, external input
8. **Go-to-Market for Enrolment** — lead magnet (free masterclass live-building one use case), message hierarchy, proof engine, audience segments
9. **Risks & Mitigations** — table
10. **Immediate Next Steps** — numbered, concrete, assignable

Write for a funding-submission audience: measured claims, framework terminology, no hype. Verify all credit/hour totals reconcile before delivering.

## Phase 4 — Delivery schedule (.xlsx)

Read the xlsx skill's SKILL.md before building. Output to `03-Schedules/`. If the user has an existing template, edit a copy and preserve its formatting; never overwrite the original.

### Standard schedule headers (per day block)

| Column | Header |
|---|---|
| A | Time |
| B | Session Block |
| C | Topic / Use Case |
| D | Format (Theory / Demo / Practice) |
| E | Learning Outcome |
| F | Tools Used |
| G | Dataset / Materials |
| H | Provided by School |
| I | Deliverable |
| J | Real-World Application |

- If the audience is bilingual, mirror the sheet in the second language (e.g. English + Chinese sheets) with identical structure.
- Include a "Things Need Before Classes" checklist sheet: accounts created/tested, hardware ready, dataset access granted, platform instances running, materials pack, pre-course survey sent.
- Every session block should end in a Deliverable — students leave each block with something built. Blocks without deliverables are lecture filler; challenge them.
- Sanity-check the hours: blocks per day must sum to the day's contact hours; total must match the blueprint's contact-hour commitment for whatever slice of the programme this schedule covers.

## Phase 5 — Handoff & sell

1. Create or update `00-Project Handoff/HANDOFF.md` with: who's involved, the project in one paragraph, a **Decisions already made (DO NOT re-ask)** table, the unfair advantage, competitor summary, curriculum table, the product portfolio matrix, folder structure, open next steps, and working rules (tone per audience, credit math invariants).
2. Update the folder-structure section whenever files move.
3. If the user is ready to sell: draft the lead-magnet masterclass outline and landing copy into `05-Marketing/`, borrowing the competitor's proven mechanics (concrete use cases with before/after numbers, identity transformation narrative, honest scarcity) while leading with the differentiators (credential, funding/free, proprietary assets).

## Export & clean structure rule

Every output must land in its stage folder — never leave deliverables in the chat, a scratchpad, or the folder root:

| Output | Destination |
|---|---|
| Filed knowledge, competitor teardowns | `01-Learning Knowledge/` |
| Programme blueprint .docx | `02-Course Blueprint/` |
| Schedule .xlsx | `03-Schedules/` |
| Skills / automation assets | `04-Skills/` |
| Marketing copy, masterclass scripts | `05-Marketing/` (create when reached) |
| Funding/accreditation documents | `06-Submission/` (create when reached) |

If multiple course concepts share one project, prefix files with the concept name so folders stay sortable. At the end of a run, list the final folder tree so the user sees the structure is clean, and update HANDOFF.md's folder section to match.

## Working style

- Concise and direct; the user is a busy program lead, not a developer.
- Present every deliverable file when done (present_files), with a two-sentence summary — not an essay.
- Flag scope mismatches immediately (e.g. a 2-day schedule cannot deliver a 120-credit programme — name it as the pilot/bootcamp version and proceed).
- All numbers must reconcile: credits × 10 = NLH; module hours × modules = totals; schedule hours = blueprint commitment.
