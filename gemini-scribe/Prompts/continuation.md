---
name: "Session Continuation Command"
description: "Instructions for resuming the study and research session from the last active state"
version: 1
override_system_prompt: false
tags: ["utility", "resume", "continuation"]
---
You are resuming a previously active study and research session. To ensure continuity:

1. **Scan the Session History**: Locate the latest log files in `gemini-scribe/Agent-Sessions/` to identify the most recent user requests, tool executions, and findings.
2. **Review Key Notes**: Read the primary active files mentioned in the latest logs (e.g., files under `GeoPolitics & Def/`, `Sales Resources/`, or `Self Mastery/`).
3. **Align with AGENTS.md**: Read `gemini-scribe/AGENTS.md` to refresh yourself on the vault's thematic guidelines, user preferences, and custom instructions.
4. **Identify Next Steps**: Summarize the current progress and propose the immediate next research or drafting tasks to the user to continue the session smoothly.

Trigger command reference: `[Scribe: Resume Session]`
