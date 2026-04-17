# AI Framework

A lightweight, project-agnostic framework for working effectively with AI models during development. Built from real-world experience across 30+ sessions with v0, Claude, and other AI coding assistants.

## Philosophy

Most AI frameworks focus on what the AI should know. This one focuses on what the AI should remember, how it should behave, and how collaboration between human and AI should actually work.

The framework is inspired in part by [Andrej Karpathy's coding guidelines](https://github.com/forrestchang/andrej-karpathy-skills) and refined through practical use across multiple real projects.

## Core Files

| File | Purpose |
|---|---|
| [`MEMORY.md`](MEMORY.md) | Session memory — the most important file. Carries forward lessons, decisions, and project state across sessions. Also contains the session init sequence and execution rules. |
| [`AGENTS.md`](AGENTS.md) | Project conventions, file structure, coding standards, and tooling instructions for AI agents. |
| [`SOUL.md`](SOUL.md) | Collaboration values, design principles, and behavioral guidelines. Defines how the AI thinks and makes decisions, not just what it does. |
| [`HUMAN.md`](HUMAN.md) | Context about the human collaborator — working style, preferences, background. Prevents repetitive questions and aligns the AI with how you actually work. |
| [`TEAM.md`](TEAM.md) | Roles and responsibilities when multiple AI agents or collaborators are involved. |

## How It Works

### Session Init

The AI reads `MEMORY.md` first — always. Because `MEMORY.md` is self-serving (it contains what the AI needs to be effective), it gets read reliably. The session init sequence and behavioral rules are embedded there rather than in a separate loader file.

1. Read [`MEMORY.md`](MEMORY.md) completely
2. Read [`AGENTS.md`](AGENTS.md) — project conventions and coding standards
3. Read [`SOUL.md`](SOUL.md) — collaboration values and design principles
4. Read [`HUMAN.md`](HUMAN.md) — human collaborator context
5. Read [`TEAM.md`](TEAM.md) — roles and responsibilities

### Execution Rules

Embedded in `MEMORY.md` so they are read every session without relying on the AI to follow a separate instruction file:

1. **Ask, don't guess** — surface confusion before writing a single line
2. **Minimum code** — write the least code that correctly solves the problem. If 200 lines could be 50, the 200-line version is wrong
3. **Surgical changes** — every changed line must trace directly to the user's request. Mention unrelated issues, never fix them silently
4. **Define done first** — state the verifiable success criterion before implementing any non-trivial task

### Memory Continuity

`MEMORY.md` is updated at the end of each session with what was built, what went wrong, and what to carry forward. This solves the biggest practical problem with AI-assisted development: the AI forgetting everything between sessions.

Each session entry includes:
- What was done
- Key decisions and their rationale
- Mistakes made and lessons learned
- Open items carried forward

## Usage

### New Project

1. Copy all framework files into your project root
2. Replace `<name>` placeholder in `MEMORY.md` with your project name
3. Fill in `HUMAN.md` with your working style and preferences
4. Update `AGENTS.md` with project-specific conventions
5. Start your first session — the AI will read the framework and operate within it

### Existing Project

1. Copy the framework files into your project root
2. Add a Session 1 entry to `MEMORY.md` summarizing the current project state
3. From the next session onward, the AI has the context it needs

## Template Placeholders

| Placeholder | File | Replace With |
|---|---|---|
| `<name>` | `MEMORY.md` | Your project name |
| `<human_name>` | `HUMAN.md` | Your name |
| `<project_description>` | `AGENTS.md` | Short project description |

## What Makes This Different

- **Memory-first design** — `MEMORY.md` is the entry point because it is the file the AI is most motivated to read
- **Behavioral rules embedded where they are read** — not in a separate file that gets skipped
- **Human context as a first-class concern** — `HUMAN.md` prevents the AI from treating every session as a blank slate relationship
- **Refined through real sessions** — not theoretical. Every design decision came from observing what actually worked and what did not across 30+ sessions

## Credits

- Execution rules inspired by [Andrej Karpathy's coding guidelines](https://github.com/forrestchang/andrej-karpathy-skills)
- Framework developed collaboratively between [Jiab77](https://github.com/Jiab77) and [v0 by Vercel](https://v0.dev) across the [Athena](https://github.com/Jiab77/athena) and [Virgil](https://github.com/Jiab77/virgil) projects.
