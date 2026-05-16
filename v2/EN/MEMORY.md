# MEMORY.md - Session Memory & Project Ledger

> **Status:** Dynamic and persistent. This is the AI's primary tool to preserve context, lock down architectural decisions, and prevent repeating mistakes across sessions.

---

## 🚀 Initialization Sequence (Execute at the START of EVERY session)

Before processing any request or writing code, the AI must read the three context files in this exact order:
1. **`AGENTS.md`**: Align with the critical collaborator posture and technical doctrines.
2. **`HUMAN.md`**: Review the user's profile, preferences, and OPSEC constraints.
3. **`MEMORY.md`**: Analyze current project state, recent blockers, and history (read from top to bottom).

---

## 🛠️ Critical Execution Rules (Karpathy Style)

1. **Ask, don't guess** – Surface confusion before writing code. A clarifying question saves time; a wrong assumption destroys it.
2. **Minimum code** – Prefer 50 well-thought-out lines over 200 complex ones. Unwritten code has no bugs and requires no maintenance.
3. **Surgical changes** – Focus modifications narrowly. Ensure zero collateral damage on the existing codebase.
4. **Log before fix** – Never patch a bug blindly. Insert logs, reproduce the behavior, analyze, then fix surgically.

---

## 📌 Architectural Reminders & Project Constraints
*(To be continuously updated and enriched by the AI during development)*

* **Auth/Session Management:** Before adding any abstraction layer (proxy, middleware), validate full compatibility with the existing session design.
* **Dead Code Mitigation:** Before declaring a function or component as "dead code", *grep* all consumers across the entire repository first.
* **Diff Verification:** Mentally process the full final *diff* to ensure no hidden dependencies were broken during cleanup.

---

## 👤 User Context (Decision-Making Guidelines)

* **Quality > Speed:** Never sacrifice security, readability, or cleanliness to rush a feature.
* **Systems Thinking:** Focus on the big picture, interconnections, and architecture rather than isolated components.
* **Strict OPSEC:** Zero blind trust toward third-party services. Keep private data encapsulated and protected.
* **Honest Partnership:** High value placed on direct feedback, constructive criticism, and logical debate.

---

## 📅 Session Log (Reverse Chronological Order)

### [YYYY-MM-DD] - Session Name / Main Objective
* **What was accomplished:**
  - Item 1
  - Item 2
* **Blockers Encountered & Solutions:**
  - *Error:* Description of the issue.
  - *Solution / Lesson:* How it was fixed and what to remember for the future.
* **Current State & Next Steps:**
  - Current health/status of the project.
  - Remaining items to tackle during the next session.

---
*(Duplicate the template block above for every new session)*
