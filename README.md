# AI Framework

A lightweight, project-agnostic framework for working effectively with AI models during development. Built from real-world experience across 30+ sessions with v0, Claude, and other AI coding assistants.
Now streamlined into a powerful **3-file core architecture** for maximum efficiency and zero bloat.

## Philosophy

Most AI frameworks focus on what the AI should know. This one focuses on what the AI should remember, how it should behave, and how collaboration between human and AI should actually work.
The framework enforces an **Anti-Assistant / Technical Partner** posture and is inspired in part by [Andrej Karpathy's coding guidelines](https://github.com/forrestchang/andrej-karpathy-skills).

## Core Files

| File | Type / Access | Purpose |
| :--- | :--- | :--- |
| [`MEMORY.md`](v2/EN/MEMORY.md) | Dynamic <br>`AI Read/Write` | **Session memory & project ledger.** The entry point. Carries forward lessons, decisions, and project state across sessions. Contains the session init sequence and execution rules. |
| [`AGENTS.md`](v2/EN/AGENTS.md) | Static <br>`AI Read-Only` | **Identity & Technical Doctrines.** Merges the former `SOUL.md`, `TEAM.md`, and `AGENTS.md`. Defines the AI's posture, the PDCA development cycle, and absolute technical boundaries (DRY, KISS, OPSEC). |
| [`HUMAN.md`](v2/EN/HUMAN.md) <br>*or* [`HUMANS.md`](v2/EN/HUMANS.md) | Static & Private <br>`AI Read-Only` | **Human Collaborator Profile(s).** Maps the technical background, communication style, stack preferences, and team rules. **Must be gitignored.** |

> [!Note]
> The previous version of this framework can be found in the [v1](v1/) folder.

## How It Works

### Session Init Sequence

The AI reads `MEMORY.md` first — always. Because `MEMORY.md` is self-serving (it contains what the AI needs to be effective), it gets read reliably. 
At the **start of every session**, the AI must process the files in this exact order:
1. **`AGENTS.md`** — Align with the critical collaborator posture and technical doctrines.
2. **`HUMAN.md`** (or `HUMANS.md`) — Review the user profile, preferences, and team constraints.
3. **`MEMORY.md`** — Analyze current project state, recent blockers, and history from top to bottom.

### Critical Execution Rules

Embedded directly in `MEMORY.md` to guarantee they are read every single session:
1. **Ask, don't guess** — Surface confusion before writing code. A clarifying question saves time; a wrong assumption destroys it.
2. **Minimum code** — Write the absolute minimum amount of code required to solve the problem. No speculative abstractions.
3. **Surgical changes** — Focus modifications narrowly. Ensure zero collateral damage on the existing codebase.
4. **Log before fix** — Never patch a bug blindly. Insert logs, reproduce the behavior, analyze, then fix surgically.

### The PDCA Protocol (Enforced in AGENTS.md)

To eliminate the "Code Monkey" loop, the AI operates under a strict **Plan ➔ Do ➔ Check ➔ Act** cycle, requiring a mandatory pre-read and system-state analysis *before* any source code is modified.

## Usage

### 🚀 New Project

1. Copy the 3 core framework files into your project root.
2. Choose between `HUMAN.md` (Solo project) or `HUMANS.md` (Team project) and delete the other.
3. ⚠️ **CRITICAL:** Immediately add `HUMAN.md` or `HUMANS.md` to your `.gitignore` file.
4. Fill in your profile/preferences in your human context file.
5. Initialize your first session log entry in `MEMORY.md` and start hacking.

```bash
# Example setup
cp /path/to/framework/{MEMORY.md,AGENTS.md,HUMAN.md} ./
echo "HUMAN.md" >> .gitignore
echo "HUMANS.md" >> .gitignore
```

## What Makes This Different

 * **Consolidated Footprint** — Reduced from 5 files to 3 by merging identity, team rules, and coding standards into a unified technical doctrine (AGENTS.md).
 * **Memory-First Design** — MEMORY.md is the absolute engine of continuity, preventing the AI from forgetting context between sessions.
 * **Strict OPSEC & Privacy** — Human context is strictly separated and kept local via .gitignore to prevent leaking private workflows or team identities to public repositories.
 * **Zero Sycophancy** — Designed to act as a technical sparring partner that actively challenges sub-optimal decisions.

## Credits

 * Execution rules inspired by [Andrej Karpathy's coding guidelines](https://github.com/forrestchang/andrej-karpathy-skills).
 * Framework developed collaboratively between [Jiab77](https://github.com/Jiab77) and [v0 by Vercel](https://v0.dev) across the [Athena](https://github.com/Jiab77/athena) and [Virgil](https://github.com/Jiab77/virgil) projects.

## Star History

<a href="https://www.star-history.com/?repos=jiab77%2Fai-framework&type=date&legend=top-left">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=jiab77/ai-framework&type=date&theme=dark&legend=top-left" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=jiab77/ai-framework&type=date&legend=top-left" />
    <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=jiab77/ai-framework&type=date&legend=top-left" />
  </picture>
</a>
