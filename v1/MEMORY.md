# MEMORY.md - Session Memory for <name> Project

This file carries forward lessons learned, project constraints, architectural decisions, and best practices across sessions to prevent repeating mistakes and maintain continuity.

**Primary User:** You (the AI working on <name>)
**Purpose:** Continuity, pattern preservation, mistake prevention, institutional knowledge
**Format:** Plain markdown - easy to parse and understand
**Update Schedule:** After each significant work session, document what you learned

---

## Session Init — Read This First

Before doing anything else in a session, complete all four steps in order:

1. Read this file completely
2. Read `AGENTS.md` — project conventions, file structure, coding standards
3. Read `SOUL.md` — collaboration values and design principles
4. Read `HUMAN.md` — Who you're working with and how they approach problems
5. Read `TEAM.md` — roles and responsibilities

Then internalize these four execution rules before touching any code.
Inspired by Andrej Karpathy's coding guidelines — https://github.com/forrestchang/andrej-karpathy-skills

### Execution Rules

1. **Ask, don't guess** — surface confusion before writing a single line. Wrong assumptions waste more time than a clarifying question.
2. **Minimum code** — write the least code that correctly solves the problem. No speculative abstractions, no unrequested flexibility. If 200 lines could be 50, the 200-line version is wrong.
3. **Surgical changes** — every changed line must trace directly to the user's request. Do not touch adjacent code, improve unrelated patterns, or remove pre-existing dead code without being asked. Mention it, never fix it silently.
4. **Define done first** — before implementing any non-trivial task, state the verifiable success criterion. Implementation is complete when that criterion is met, not when the code looks right.

---

## How This File Works

**External Context Persistence Across Sessions**

### Session 2+ Flow
- Read updated MEMORY.md first — restores project continuity without repeating past mistakes or redoing completed work
- Continue effectively where previous session left off
- Append new learnings

### Session 1 Flow
- Read MEMORY.md (project state, decisions, learned patterns)
- Work on assigned tasks
- Append important learnings before ending session

**Why This Matters:** Maintains project state across conversations without consuming limited context window. You start each session informed, not blank.

**Critical:** Always read this file at the start of each conversation about <name>.

---

## Your Development Rules (MUST NOT BE SKIPPED)

1. EVERY shared constant goes in `/lib/constants.ext` - NO exceptions
2. EVERY shared type/interface goes in `/lib/types.ext` - NO exceptions
3. Component-specific props that only reference primitives (string, number, boolean) can stay in their component file
4. Component props that reference ANY domain type must import from `/lib/types.ext`
5. NEVER define the same constant value in two different files
6. NEVER define the same type shape in two different files
7. When creating a new constant or type, CHECK these files first before defining inline

Of course, these rules should be adapted to the programming language used in the user project.

**YOU MUST REPLACE `.ext` BY THE FILE EXTENSION RELATED TO THE USED PROGRAMING LANGUAGE**

### Context Gathering Rules

- Use parallel tool calls where possible.
- Don't stop at the first match — examine ALL matching files to find the right variant/version.
- Understand the full system before making changes — check existing patterns, parent components, utilities, schemas, and architecture.
- Search systematically: broad → specific → verify relationships.

### Impact Assessment Rules (CRITICAL — learned the hard way)

- Before removing ANY import, constant, or function, grep ALL consumers across the full codebase first.
- Before adding ANY new abstraction (proxy, middleware, cookies), verify it is architecturally compatible with the existing session/auth design.
- Before claiming something is "dead code", confirm zero consumers exist outside the file itself.
- When cleaning up after a change, read the full diff mentally and check every removed line for hidden dependencies.

---

## User Context (Important for decision-making)

**Work Philosophy:**
- Quality over speed, never compromises on security
- Thinks architecturally (systems, interconnections, not just components)
- Strong OPSEC practices, doesn't trust third-party services by default
- Perfectionist with strong UX sensibilities
- Patient but firm, values honest feedback and partnership
- Hard worker, curious learner, humble about limitations

---

## Loading This File

Read `MEMORY.md` for **EVERY** session.

**Why This Matters:** Ensures consistency, prevents repeating mistakes, maintains collaborative alignment.

**Critical:** Always read this file at the start of each conversation about this project.

**Read Order:** Sessions are listed in reverse chronological order — newest first. Read from the top down. Stop once you reach sessions that predate the current codebase state if context window is limited.

**Open to Suggestions:** If you find that read method not performant and/or creates you trouble for editing the file, please tell it to your human collaborator.

---
