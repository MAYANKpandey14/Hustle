---
name: resuming-sessions
description: Use when resuming an active research, study, or notes compilation session from past logs and state documents.
---

# Resuming Sessions

## Overview
This skill outlines the process for resuming study and research sessions. It ensures that the incoming agent synchronizes with the actual workspace state, rather than relying solely on session logs.

## When to Use
- **Trigger**: Starting a new session or handing over tasks to subagents under the `[Scribe: Resume Session]` trigger command.
- **Symptom**: Need to know exactly what notes were written, what files were edited, and what preferences are set.
- **When NOT to use**: Do not use when starting a completely unrelated codebase task from scratch.

## Core Pattern

### 1. Workspace State Sync
1. **Agent-Sessions Audit**: Locate the last log file in `gemini-scribe/Agent-Sessions/` to parse the history of instructions.
2. **Workspace Delta Scan**: **REQUIRED ACTION**: You MUST explicitly call directory listing tools (such as `list_dir`) on all primary directories (`GeoPolitics & Def/`, `Sales Resources/`, `Self Mastery/`, `Productivity/`) to inspect the actual list of files. Do NOT assume or guess.
3. **Preferences Alignment**: Read `gemini-scribe/AGENTS.md` to load the active topics and user preferences.
4. **Draft Summary**: Present the user with a summary of the true workspace state, detailing the delta changes, and suggest 3-4 structured options for continuation.

## Common Mistakes

| Mistake | Prevention |
|--------|------------|
| **Trusting logs or memory only** | **CRITICAL**: Never assume the last session log represents the current state. Always call directory-listing or file-search tools to identify any untracked or newly created notes in the workspace. |
| **Ignoring AGENTS.md** | Always read `AGENTS.md` to ensure your proposed next tasks align with Mayank's preferred data-driven, cause-and-effect research style. |
