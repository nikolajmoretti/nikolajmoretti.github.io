# CLAUDE.md — Working Rules for This Repository

This file governs how Claude Code operates in this repository. These rules apply to every session and every task unless explicitly overridden by the user in the chat.

---

## 1. Supervision Model

You are operating under **close human supervision**. Correctness, diligence, and reliability are the top priorities — not speed. When in doubt, stop and ask.

---

## 2. Task Tracking

The file **`plans/TODO.md`** is the running list of tasks for this repository.

**At the start of each session:**
- Read `plans/TODO.md` (if it exists) to understand current priorities and pick up where things left off.

**During the session:**
- Add new tasks to `TODO.md` as they are identified.

**When a task completes:**
- Move it from "Active Tasks" to "Completed Tasks" with a completion date and brief note.

---

## 3. Clarifying Questions

- **Before making any changes:** Identify all major questions — ambiguities in requirements or unclear scope. Ask them **one at a time**, waiting for an answer before moving to the next. Do not begin work until all questions are resolved.
- **During implementation:** Minor clarifications may be raised mid-task if they arise from concrete findings. Do not use this as license to proceed through significant ambiguity.

---

## 4. Scope Discipline

- Implement **only what is specified**. Do not refactor, restructure, rename, or clean up content beyond the task at hand.
- If you notice a potential improvement in files you are touching, **flag it explicitly** in your status update but **do not implement it**.

---

## 5. Stopping Conditions

Stop immediately and report to the user if any of the following occur:

- An unexpected error is encountered
- A decision point arises that was not anticipated in the task description
- You are unsure how to proceed correctly

Do **not** attempt to resolve the issue autonomously before reporting. State clearly: what happened, what you tried (if anything), and what options you see.

---

## 6. Destructive Operations — Require Explicit Approval

The following actions require explicit user confirmation **before** execution, even if they seem obviously necessary:

- Deleting any file or content
- Overwriting existing content (not just adding to it)
- Any dependency changes (adding, removing, or upgrading packages)

State clearly what you intend to do and wait for a "yes, proceed" before acting.

---

## 7. Incremental Checkpoints

Apply checkpoints only when a task has **multiple clearly distinct phases** (e.g., restructuring site navigation and separately updating content). For single-file or single-step edits, proceed without interruption.

When checkpoints apply: pause and report after each phase before proceeding to the next. Provide a status update (see §8) and wait for confirmation.

---

## 8. Status Updates — Detailed Log Format

After every action or group of actions, report in this format:

```
DONE:
- [List every file created or modified, with a one-line description of what changed]

NEXT:
- [What you intend to do next, with rationale]

FLAGS:
- [Any improvements noticed but not implemented]
- [Any assumptions made that the user should be aware of]
- [Any uncertainties or risks]
```

Be specific. Vague summaries are not acceptable.

---

## 9. Task Completion Workflow

When a task completes, perform these steps in order:

1. **Update `plans/TODO.md`** — move the task to "Completed Tasks" with completion date and one-line notes.
2. **Commit** — stage and commit all related changes together with a descriptive commit message.
3. **Push** — push to the current branch's remote.

Pushes wait for explicit user confirmation (per §6).

---

## 10. General Principles

- Prefer explicit over implicit.
- Prefer simple and correct over clever and fragile.
- If a decision is not covered by the task description or these rules, ask — do not assume.
