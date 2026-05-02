---
type: Software Engineering
Status: Active
Date: 2026-05-02
_icon: code
---
# **Software Fundamentals Matter More Than Ever**

## Overview

This document turns Matt Pocock's talk, **"Software Fundamentals Matter More Than Ever,"** into a practical blueprint for AI-assisted software development, then extends it with cross-referenced principles from Claude Code and Gemini CLI documentation. The central thesis is that AI coding tools amplify the value of software fundamentals: when code quality, shared language, modular boundaries, and feedback loops are strong, AI becomes a force multiplier; when they are weak, AI accelerates software entropy. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

The video argues against a pure “specs-to-code” workflow in which developers repeatedly regenerate code from a specification while ignoring the evolving codebase, because each cycle can worsen structure and make future changes harder. In contrast, the recommended path is iterative and architecture-aware: establish shared understanding, create ubiquitous language, develop in small steps with strong feedback loops, and shape the codebase around deep modules with simple interfaces. [softengbook](https://softengbook.org/articles/deep-modules)

## Core thesis

Matt Pocock frames AI as simultaneously overhyped and powerful, with results determined less by the model and more by the development process around it. He reports that developers who succeed with AI agents are not the ones who delegate everything or refuse delegation entirely, but the ones who return to established engineering ideas such as ubiquitous language, vertical slices, TDD, and deep modules. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

This matters because bad code has become more expensive, not cheaper. A hard-to-change codebase blocks teams from realizing the full upside of AI, while a well-structured codebase gives AI clearer constraints, safer modification points, and faster validation signals. [softengbook](https://softengbook.org/articles/deep-modules)

## Full transcript

### Transcript source

The transcript below is derived from the YouTube page content for the talk published on April 23, 2026, with a runtime of 18 minutes and 26 seconds. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

### Transcript

- **00:07** Hello everyone. Having a good conference so far? Are you having a good conference so far? Good. Wonderful. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **00:22** A comforting message is offered for developers who fear their skill set may no longer matter: software fundamentals matter more now than ever. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **00:44** While creating a course called *Claude Code for Real Engineers*, the speaker found AI coding curriculum difficult because the landscape changes constantly. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **01:05** The “specs-to-code” movement is described as writing a specification, generating code with AI, changing the spec when problems appear, and regenerating without really looking at the code. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **01:45** Repeating that cycle produced progressively worse code, ending in “garbage,” which challenged the idea that code can manage itself. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **02:30** To define what makes code bad, the talk references John Ousterhout’s idea of complexity: anything in a software system’s structure that makes it hard to understand and modify. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **03:06** The *Pragmatic Programmer* concept of software entropy is introduced to explain why systems degrade when each change is made locally without protecting the design of the whole. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **03:44** The slogan “code is cheap” is rejected; instead, bad code is described as more expensive than ever because it limits how much benefit AI can provide. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **04:25** The first failure mode is that the AI did not do what the developer wanted, which is explained as a requirements and shared-understanding problem rather than just a model problem. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **05:15** Frederick P. Brooks’s idea of a “design concept” is used to explain that human and AI often do not yet share the same invisible theory of the thing being built. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **05:48** A skill called “grill me” is introduced: the AI interviews the developer relentlessly until both sides reach a shared understanding, resolving decisions branch by branch. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **06:42** The output of that interrogation can then be turned into a PRD or directly into issues for downstream implementation workflows. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **07:18** The second failure mode is AI verbosity, where it feels like the human and model are talking across purposes. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **07:44** This is connected to the familiar gap between developers and domain experts, where inconsistent terminology leads to misunderstanding. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **08:10** Domain-Driven Design and ubiquitous language are introduced as the remedy: conversations, code, and domain language should derive from the same domain model. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)
- **08:57** A skill is described that scans the codebase, extracts terminology, and builds a markdown file containing tables of shared terms. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **09:25** Reading that language file while planning improves both AI reasoning and implementation alignment, while reducing verbosity. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **09:53** The third failure mode is that the AI builds the intended thing, but the result still does not work. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **10:02** Feedback loops are proposed as the answer: static types, browser access for frontend work, and automated tests. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **10:40** Even with feedback loops available, the model tends to do too much at once and validate too late. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **10:54** The *Pragmatic Programmer* idea of not outrunning your headlights is invoked: the rate of feedback is your speed limit. [informit](https://www.informit.com/articles/article.aspx?p=2982114\&seqNum=5)
- **11:15** TDD is recommended because it forces the LLM to take small steps: write a test, make it pass, then refactor. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **11:48** The challenge is that testing itself is hard because developers must decide unit size, mocking strategy, and which behaviors to verify. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **12:35** Good codebases are described as easier to test, which means code quality directly improves the quality of AI feedback loops. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **12:58** Ousterhout’s idea of deep modules is introduced: modules should hide substantial functionality behind simple interfaces. [softengbook](https://softengbook.org/articles/deep-modules)
- **13:35** Shallow modules are contrasted as small pieces with relatively complex interfaces and little hidden functionality. [softengbook](https://softengbook.org/articles/deep-modules)
- **14:08** AI struggles more in shallow, fragmented codebases because it must navigate too many tiny blobs and unclear dependencies. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **14:38** A codebase organized around deep modules exposes well-designed interfaces at the top while letting AI handle much of the internal implementation. [softengbook](https://softengbook.org/articles/deep-modules)
- **15:15** A skill called “improve codebase architecture” is described as a reusable process for finding related code and wrapping it into deeper modules. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **15:48** Deep-module architectures are presented as more testable because verification can happen at simple boundaries. [softengbook](https://softengbook.org/articles/deep-modules)
- **16:06** Another failure mode is mental fatigue: developers can now ship more code than before, but their brains cannot keep up with the cognitive load. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **16:35** Deep modules help both humans and AI by letting teams treat many internals as gray boxes and focus on external behavior and interfaces. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **17:00** The practical rule becomes: design the interface, delegate the implementation, especially for less critical areas. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **17:18** The architecture map of modules and interfaces should be part of planning and PRD writing, not something rediscovered later. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **17:30** Kent Beck’s idea of investing in system design every day is used to argue that teams must continually shape architecture instead of divesting from it. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **17:58** The closing message is that AI is a strong tactical programmer, but human developers must stay responsible for strategic design. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

## Detailed notes

### 1. Why software fundamentals matter more

The talk directly challenges the belief that AI makes implementation so cheap that design discipline no longer matters. In reality, AI can generate more code faster, which means poorly designed systems decay faster unless developers actively manage complexity, architecture, and testing. [informit](https://www.informit.com/articles/article.aspx?p=2982114\&seqNum=5)

The practical implication is that traditional engineering skill is not being displaced so much as re-leveraged upward. The human role shifts from typing every line to shaping system boundaries, clarifying intent, choosing verification methods, and protecting maintainability. [code.claude](https://code.claude.com/docs/en/features-overview)

### 2. Shared understanding before coding

One of the strongest ideas in the talk is that prompt failure is often design failure in disguise. If the human and the model do not share the same design concept, the model can still generate polished output, but it will likely solve the wrong problem or encode the wrong assumptions. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

The “grill me” pattern is useful because it makes the model interrogate ambiguity instead of smoothing over it. This is especially valuable in backend or systems work where constraints, edge cases, failure modes, and state transitions matter more than surface-level feature wording. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

### 3. Ubiquitous language as a prompting primitive

Martin Fowler describes ubiquitous language as a common, rigorous language between domain experts and the development team, grounded in the domain model and evolving with understanding. Matt Pocock’s application of the idea to AI coding is powerful because it treats prompts, plans, code, and discussions as one semantic system rather than separate layers. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)

A project glossary reduces ambiguity and verbosity. Instead of repeatedly explaining what “retryable failure,” “invoice settlement,” or “carrier rule” means, the team and the model can refer back to stable terms that anchor planning and implementation. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)

### 4. Feedback loops determine safe speed

The *Pragmatic Programmer* guidance that “the rate of feedback is your speed limit” aligns closely with what AI systems need in practice. Fast, reliable feedback lets the model operate in smaller loops where errors become visible earlier, reducing the chance of large speculative rewrites. [informit](https://www.informit.com/articles/article.aspx?p=2982114\&seqNum=5)

In modern AI-assisted workflows, the main feedback loops are type systems, linting, browser visibility, tests, and targeted runtime checks. Hooks in Claude Code exist specifically to automate actions around lifecycle events, such as running shell commands after changes, which can operationalize those feedback loops instead of relying on the user to remember them. [code.claude](https://code.claude.com/docs/en/hooks)

### 5. TDD as a behavior-shaping tool for models

The video presents TDD less as an ideology and more as a control surface for AI. Because the model tends to overproduce, TDD creates a disciplined structure: make one expectation explicit, implement only enough to satisfy it, then refactor while tests hold the boundary. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

This makes TDD especially compatible with agentic coding where the risk is not lack of output but excess, drift, or hidden breakage. The better the test seams and interfaces, the more effectively AI can be delegated meaningful work without creating unreadable or brittle code. [softengbook](https://softengbook.org/articles/deep-modules)

### 6. Deep modules reduce cognitive load

Ousterhout’s deep module principle holds that modules should offer simple interfaces while hiding substantial internal complexity. This reduces cognitive load because consumers of the module can operate at the level of the contract instead of wading through internal detail. [softengbook](https://softengbook.org/articles/deep-modules)

The talk extends this neatly to AI-assisted coding. A fragmented system filled with shallow modules gives the model too many entry points, too much traversal work, and too many opportunities to misunderstand dependency chains, whereas deep modules let both humans and models reason from stable interfaces. [softengbook](https://softengbook.org/articles/deep-modules)

## Cross-reference map

### Principle relationships

| Video principle                    | Older software principle                                                                                       | Claude Code feature fit                                                                                                                                 | Gemini CLI fit                                                                                                                                                                                                                              | Why it matters                                                                                               |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| Shared understanding before coding | Brooks’s design concept as summarized in the talk. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)       | Skills package reusable planning workflows; CLAUDE.md stores persistent project rules. [code.claude](https://code.claude.com/docs/en/features-overview) | Hierarchical memory via `GEMINI.md` stores persistent project context. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                                                                            | Reduces wrong-yet-confident implementations. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)           |
| Ubiquitous language                | DDD ubiquitous language. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)                | Skills can encode domain vocab and workflows; CLAUDE.md can pin conventions. [code.claude](https://code.claude.com/docs/en/features-overview)           | `/memory add` and `GEMINI.md` can preserve glossary and domain rules across sessions. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                                                             | Improves alignment and reduces prompt verbosity. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)       |
| Small steps with feedback          | “Don’t outrun your headlights.” [informit](https://www.informit.com/articles/article.aspx?p=2982114\&seqNum=5) | Hooks can trigger tests or linting automatically after edits. [code.claude](https://code.claude.com/docs/en/overview)                                   | CLI command and memory flows support explicit context and task discipline, though external automation depends on shell tooling around Gemini CLI. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html) | Keeps AI work bounded by verification speed. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)           |
| TDD-guided iteration               | Test-first change discipline from the talk. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)              | Built-in tools plus hooks help run tests in looped workflows. [code.claude](https://code.claude.com/docs/en/overview)                                   | CLI workflows can be driven from terminal test commands with persistent project memory. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                                                           | Prevents overproduction and drift. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)                     |
| Deep modules                       | Ousterhout deep modules. [softengbook](https://softengbook.org/articles/deep-modules)                          | Skills and project conventions can codify interface-first architecture habits. [code.claude](https://code.claude.com/docs/en/features-overview)         | Memory files can capture architectural maps and module boundaries. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                                                                                | Makes code easier to explore, test, and safely change. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg) |

## Claude Code blueprint

Claude Code documentation recommends starting with `CLAUDE.md` for project conventions and then adding extensions only when recurring triggers appear, such as repeated mistakes, repeated prompts, or repeated manual workflows. That advice maps closely to the talk’s philosophy because both emphasize encoding stable design knowledge and reducing ambiguity before scaling up automation. [code.claude](https://code.claude.com/docs/en/features-overview)

### High-value Claude Code capabilities

| Capability  | What it does                                                                                                                                      | Best use in this blueprint                                                                                                                                                                        |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `CLAUDE.md` | Persistent context loaded every conversation. [code.claude](https://code.claude.com/docs/en/features-overview)                                    | Put coding standards, glossary terms, architectural rules, test commands, and “always validate before commit” instructions here. [code.claude](https://code.claude.com/docs/en/features-overview) |
| Skills      | Reusable knowledge and invocable workflows, loadable on demand or automatically. [code.claude](https://code.claude.com/docs/en/features-overview) | Implement `/grill`, `/ubiquitous-language`, `/write-prd`, `/deep-module-refactor`, `/tdd-loop` workflows. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)                                   |
| Hooks       | Trigger scripts, HTTP requests, prompts, or subagents on lifecycle events. [code.claude](https://code.claude.com/docs/en/features-overview)       | Run lint, type-check, focused tests, or architecture checks after file edits or before commits. [code.claude](https://code.claude.com/docs/en/hooks)                                              |
| MCP         | Connect to external services such as databases, Slack, or browsers. [code.claude](https://code.claude.com/docs/en/features-overview)              | Pull real schemas, inspect browser state, or query production-like systems safely during planning and debugging. [code.claude](https://code.claude.com/docs/en/features-overview)                 |
| Subagents   | Isolated workers with separate context that return summaries. [code.claude](https://code.claude.com/docs/en/features-overview)                    | Use for large research tasks, repo-wide exploration, or multi-file audits so main context stays clean. [code.claude](https://code.claude.com/docs/en/features-overview)                           |
| Plugins     | Package skills, hooks, subagents, and MCP servers for reuse across repositories. [code.claude](https://code.claude.com/docs/en/features-overview) | Standardize a company-wide or personal AI coding stack once workflows stabilize. [code.claude](https://code.claude.com/docs/en/features-overview)                                                 |

### Useful Claude Code skills to create

The strongest custom skills are the ones that encode repeated thinking patterns rather than one-off commands. Based on the video and official extension model, the most useful skills are these: [code.claude](https://code.claude.com/docs/en/agent-sdk/slash-commands)

- `/grill`: Ask structured questions until requirements, constraints, entities, edge cases, success criteria, and trade-offs are resolved. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- `/ubiquitous-language`: Scan docs and code, extract domain terms, identify synonyms, and write a canonical glossary. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)
- `/slice-feature`: Convert a feature into vertical slices with one observable outcome each. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- `/tdd-loop`: Write or refine a failing test, implement the smallest passing change, and refactor under test protection. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- `/deep-module-refactor`: Find shallow-module clusters and propose interface-first consolidation into deeper modules. [softengbook](https://softengbook.org/articles/deep-modules)
- `/write-prd`: Convert shared understanding into a PRD that explicitly lists module and interface impacts. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- `/post-change-review`: Summarize touched interfaces, risks introduced, tests run, and follow-up refactors needed. [code.claude](https://code.claude.com/docs/en/hooks)

### Claude Code setup pattern

A strong setup follows the layering model in the docs: put always-on rules in `CLAUDE.md`, reusable workflows in skills, external connectivity in MCP, repeated automation in hooks, and large context-hungry work in subagents. This keeps context cost manageable and prevents the session from being overloaded with instructions that should have lived in the right extension layer. [code.claude](https://code.claude.com/docs/en/features-overview)

## Gemini CLI blueprint

Gemini CLI documentation highlights command-driven workflows and a hierarchical memory system loaded from `GEMINI.md` files. The `/memory add` and `/memory show` commands are especially useful because they let teams persist project-specific rules, definitions, and reminders across sessions instead of rewriting them in every prompt. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)

### High-value Gemini CLI practices

| Practice                   | Supporting feature                                                                                                                  | Best use in this blueprint                                                                                                                                                                                         |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Project memory file        | `GEMINI.md` hierarchical memory. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)          | Store architecture map, glossary, coding standards, module boundaries, and decision records. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                             |
| Incremental memory updates | `/memory add`. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                            | Add new domain terms, testing rules, recurring bug patterns, or clarified assumptions as they emerge. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                    |
| Memory inspection          | `/memory show`. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                           | Audit whether the model is seeing the right project context before asking for changes. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                                   |
| Memory refresh             | `/memory refresh` as described in Gemini CLI guidance. [addyosmani](https://addyosmani.com/blog/gemini-cli/)                        | Reload manually edited project knowledge when collaborating or changing files outside the CLI. [addyosmani](https://addyosmani.com/blog/gemini-cli/)                                                               |
| Shell-centered workflows   | Terminal-first usage pattern in CLI docs. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html) | Pair Gemini with local test scripts, linters, formatter checks, and architecture grep tools for explicit feedback loops. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html) |

### Useful Gemini CLI skills and conventions

Gemini CLI does not expose the same extension vocabulary as Claude Code in the fetched sources, but its memory system can still support many of the same operating principles. The most useful habits are to treat `GEMINI.md` as an architecture-and-language contract and to maintain task starter templates in repo scripts or shell aliases. [addyosmani](https://addyosmani.com/blog/gemini-cli/)

Useful patterns include:

- A `GEMINI.md` section for domain glossary and forbidden synonyms. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)
- A `GEMINI.md` section for module map, with each deep module’s interface and responsibility. [addyosmani](https://addyosmani.com/blog/gemini-cli/)
- A shell alias or script that asks Gemini to propose only one test-backed change at a time, enforcing the video’s small-step discipline. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)
- A repeatable review checklist stored in memory: touched files, boundary changes, tests added, mocks introduced, and risk areas. [addyosmani](https://addyosmani.com/blog/gemini-cli/)

## Recommended editor extensions

The talk’s process depends on fast feedback, readable errors, and architecture visibility. A practical editor stack should therefore privilege extensions that shorten the distance between code changes and useful signals. [github](https://github.com/theBadT/vscode-error-lens)

### Useful extensions

| Extension or tool type             | Why it helps                                                                                                                                                                                                                                   |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Error Lens                         | Displays diagnostics inline, making errors and warnings more prominent and speeding the feedback loop. [github](https://github.com/theBadT/vscode-error-lens)                                                                                  |
| GitLens                            | Improves code history and blame visibility, which helps trace architectural drift and understand why boundaries evolved. [thesoftwarescout](https://thesoftwarescout.com/best-vs-code-extensions-2026-20-must-have-tools-for-every-developer/) |
| ESLint / language-specific linters | Enforces style and catches issues early, which gives AI faster correction signals. [code.claude](https://code.claude.com/docs/en/hooks)                                                                                                        |
| Test explorer extensions           | Make focused test execution easier, reinforcing TDD and small-step iteration. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)                                                                                                            |
| Browser/devtools integrations      | Essential for frontend AI workflows where the model must inspect real UI state. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)                                                                                                          |

## Blueprint workflow

A complete AI coding workflow built from the talk and the tool docs looks like this: [code.claude](https://code.claude.com/docs/en/features-overview)

1. **Initialize project context.** Create `CLAUDE.md` or `GEMINI.md` with coding conventions, architectural constraints, validation commands, glossary seed terms, and module boundaries. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)
2. **Interrogate the feature.** Run a “grill me” style planning loop until the design concept is shared and ambiguity is reduced. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
3. **Build ubiquitous language.** Update the glossary and normalize terminology before implementation starts. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)
4. **Slice the work.** Break the feature into vertical slices with a single observable outcome and a defined verification method. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
5. **Code in TDD loops.** Use a failing test, smallest passing change, and refactor cycle so the model never outruns feedback. [informit](https://www.informit.com/articles/article.aspx?p=2982114\&seqNum=5)
6. **Refactor toward deep modules.** Regularly consolidate related behavior behind simple interfaces and treat implementation as delegated detail where risk permits. [softengbook](https://softengbook.org/articles/deep-modules)
7. **Automate guardrails.** Use hooks, scripts, and inline diagnostics so checks happen by default, not by memory. [github](https://github.com/theBadT/vscode-error-lens)
8. **Review architecture daily.** PRDs, code reviews, and memory files should all explicitly track interface changes and module evolution. [addyosmani](https://addyosmani.com/blog/gemini-cli/)

## Example implementation

A backend pricing engine offers a good example. Start by defining exact terms such as `Quote`, `Surcharge`, `CarrierRule`, `EligibleShipment`, and `RetryableFailure` in the glossary so both the human and the model use the same domain language. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)

Next, create a deep module such as `PricingService` with a small public interface and hide rule evaluation, ranking, and exception handling inside it. Ask the model to add one behavior at a time through TDD, such as “returns the lowest valid quote for an eligible shipment,” and run tests automatically through hooks or shell scripts after each change. [code.claude](https://code.claude.com/docs/en/hooks)

## Practical templates

### Suggested `CLAUDE.md` sections

- Project goals and non-goals. [code.claude](https://code.claude.com/docs/en/features-overview)
- Canonical glossary and banned synonyms. [code.claude](https://code.claude.com/docs/en/features-overview)
- Module map with interface contracts. [code.claude](https://code.claude.com/docs/en/features-overview)
- Required validation commands, such as type-check, unit test, integration test, and lint. [code.claude](https://code.claude.com/docs/en/hooks)
- Design rules, such as “prefer deep modules,” “do not add new abstractions without need,” and “touch interfaces deliberately.” [code.claude](https://code.claude.com/docs/en/features-overview)

### Suggested `GEMINI.md` sections

- Domain glossary. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)
- Architecture map. [addyosmani](https://addyosmani.com/blog/gemini-cli/)
- Feature slicing pattern. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)
- Testing policy and mocking rules. [addyosmani](https://addyosmani.com/blog/gemini-cli/)
- Post-change review checklist. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)

### Suggested custom prompts or skill starters

- “Interview relentlessly until all constraints, failure cases, and success criteria are explicit; do not propose implementation until ambiguity is low.” [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- “Extract domain terms from code and docs, identify collisions or synonyms, and propose one canonical glossary.” [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)
- “Propose the smallest failing test for the next vertical slice; implement only enough to pass.” [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- “Find shallow-module clusters and propose a deeper interface-first consolidation.” [softengbook](https://softengbook.org/articles/deep-modules)

## Closing view

The strongest reading of the talk is not that AI changes nothing, but that it changes the leverage points. Typing code matters less than before, while architecture, naming, validation, and interface design matter more because they determine whether AI output compounds quality or compounds entropy. [informit](https://www.informit.com/articles/article.aspx?p=2982114\&seqNum=5)

Claude Code and Gemini CLI are most effective when treated as programmable environments for these old principles rather than as magic code generators. Teams that encode shared language, feedback loops, and modular design into their AI workflows are likely to outperform teams that merely ask for more code faster. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)

## Overview

This document turns Matt Pocock's talk, **"Software Fundamentals Matter More Than Ever,"** into a practical blueprint for AI-assisted software development, then extends it with cross-referenced principles from Claude Code and Gemini CLI documentation. The central thesis is that AI coding tools amplify the value of software fundamentals: when code quality, shared language, modular boundaries, and feedback loops are strong, AI becomes a force multiplier; when they are weak, AI accelerates software entropy. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

The video argues against a pure “specs-to-code” workflow in which developers repeatedly regenerate code from a specification while ignoring the evolving codebase, because each cycle can worsen structure and make future changes harder. In contrast, the recommended path is iterative and architecture-aware: establish shared understanding, create ubiquitous language, develop in small steps with strong feedback loops, and shape the codebase around deep modules with simple interfaces. [softengbook](https://softengbook.org/articles/deep-modules)

## Core thesis

Matt Pocock frames AI as simultaneously overhyped and powerful, with results determined less by the model and more by the development process around it. He reports that developers who succeed with AI agents are not the ones who delegate everything or refuse delegation entirely, but the ones who return to established engineering ideas such as ubiquitous language, vertical slices, TDD, and deep modules. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

This matters because bad code has become more expensive, not cheaper. A hard-to-change codebase blocks teams from realizing the full upside of AI, while a well-structured codebase gives AI clearer constraints, safer modification points, and faster validation signals. [softengbook](https://softengbook.org/articles/deep-modules)

## Full transcript

### Transcript source

The transcript below is derived from the YouTube page content for the talk published on April 23, 2026, with a runtime of 18 minutes and 26 seconds. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

### Transcript

- **00:07** Hello everyone. Having a good conference so far? Are you having a good conference so far? Good. Wonderful. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **00:22** A comforting message is offered for developers who fear their skill set may no longer matter: software fundamentals matter more now than ever. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **00:44** While creating a course called *Claude Code for Real Engineers*, the speaker found AI coding curriculum difficult because the landscape changes constantly. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **01:05** The “specs-to-code” movement is described as writing a specification, generating code with AI, changing the spec when problems appear, and regenerating without really looking at the code. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **01:45** Repeating that cycle produced progressively worse code, ending in “garbage,” which challenged the idea that code can manage itself. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **02:30** To define what makes code bad, the talk references John Ousterhout’s idea of complexity: anything in a software system’s structure that makes it hard to understand and modify. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **03:06** The *Pragmatic Programmer* concept of software entropy is introduced to explain why systems degrade when each change is made locally without protecting the design of the whole. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **03:44** The slogan “code is cheap” is rejected; instead, bad code is described as more expensive than ever because it limits how much benefit AI can provide. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **04:25** The first failure mode is that the AI did not do what the developer wanted, which is explained as a requirements and shared-understanding problem rather than just a model problem. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **05:15** Frederick P. Brooks’s idea of a “design concept” is used to explain that human and AI often do not yet share the same invisible theory of the thing being built. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **05:48** A skill called “grill me” is introduced: the AI interviews the developer relentlessly until both sides reach a shared understanding, resolving decisions branch by branch. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **06:42** The output of that interrogation can then be turned into a PRD or directly into issues for downstream implementation workflows. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **07:18** The second failure mode is AI verbosity, where it feels like the human and model are talking across purposes. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **07:44** This is connected to the familiar gap between developers and domain experts, where inconsistent terminology leads to misunderstanding. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **08:10** Domain-Driven Design and ubiquitous language are introduced as the remedy: conversations, code, and domain language should derive from the same domain model. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)
- **08:57** A skill is described that scans the codebase, extracts terminology, and builds a markdown file containing tables of shared terms. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **09:25** Reading that language file while planning improves both AI reasoning and implementation alignment, while reducing verbosity. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **09:53** The third failure mode is that the AI builds the intended thing, but the result still does not work. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **10:02** Feedback loops are proposed as the answer: static types, browser access for frontend work, and automated tests. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **10:40** Even with feedback loops available, the model tends to do too much at once and validate too late. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **10:54** The *Pragmatic Programmer* idea of not outrunning your headlights is invoked: the rate of feedback is your speed limit. [informit](https://www.informit.com/articles/article.aspx?p=2982114\&seqNum=5)
- **11:15** TDD is recommended because it forces the LLM to take small steps: write a test, make it pass, then refactor. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **11:48** The challenge is that testing itself is hard because developers must decide unit size, mocking strategy, and which behaviors to verify. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **12:35** Good codebases are described as easier to test, which means code quality directly improves the quality of AI feedback loops. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **12:58** Ousterhout’s idea of deep modules is introduced: modules should hide substantial functionality behind simple interfaces. [softengbook](https://softengbook.org/articles/deep-modules)
- **13:35** Shallow modules are contrasted as small pieces with relatively complex interfaces and little hidden functionality. [softengbook](https://softengbook.org/articles/deep-modules)
- **14:08** AI struggles more in shallow, fragmented codebases because it must navigate too many tiny blobs and unclear dependencies. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **14:38** A codebase organized around deep modules exposes well-designed interfaces at the top while letting AI handle much of the internal implementation. [softengbook](https://softengbook.org/articles/deep-modules)
- **15:15** A skill called “improve codebase architecture” is described as a reusable process for finding related code and wrapping it into deeper modules. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **15:48** Deep-module architectures are presented as more testable because verification can happen at simple boundaries. [softengbook](https://softengbook.org/articles/deep-modules)
- **16:06** Another failure mode is mental fatigue: developers can now ship more code than before, but their brains cannot keep up with the cognitive load. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **16:35** Deep modules help both humans and AI by letting teams treat many internals as gray boxes and focus on external behavior and interfaces. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **17:00** The practical rule becomes: design the interface, delegate the implementation, especially for less critical areas. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **17:18** The architecture map of modules and interfaces should be part of planning and PRD writing, not something rediscovered later. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **17:30** Kent Beck’s idea of investing in system design every day is used to argue that teams must continually shape architecture instead of divesting from it. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- **17:58** The closing message is that AI is a strong tactical programmer, but human developers must stay responsible for strategic design. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

## Detailed notes

### 1. Why software fundamentals matter more

The talk directly challenges the belief that AI makes implementation so cheap that design discipline no longer matters. In reality, AI can generate more code faster, which means poorly designed systems decay faster unless developers actively manage complexity, architecture, and testing. [informit](https://www.informit.com/articles/article.aspx?p=2982114\&seqNum=5)

The practical implication is that traditional engineering skill is not being displaced so much as re-leveraged upward. The human role shifts from typing every line to shaping system boundaries, clarifying intent, choosing verification methods, and protecting maintainability. [code.claude](https://code.claude.com/docs/en/features-overview)

### 2. Shared understanding before coding

One of the strongest ideas in the talk is that prompt failure is often design failure in disguise. If the human and the model do not share the same design concept, the model can still generate polished output, but it will likely solve the wrong problem or encode the wrong assumptions. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

The “grill me” pattern is useful because it makes the model interrogate ambiguity instead of smoothing over it. This is especially valuable in backend or systems work where constraints, edge cases, failure modes, and state transitions matter more than surface-level feature wording. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

### 3. Ubiquitous language as a prompting primitive

Martin Fowler describes ubiquitous language as a common, rigorous language between domain experts and the development team, grounded in the domain model and evolving with understanding. Matt Pocock’s application of the idea to AI coding is powerful because it treats prompts, plans, code, and discussions as one semantic system rather than separate layers. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)

A project glossary reduces ambiguity and verbosity. Instead of repeatedly explaining what “retryable failure,” “invoice settlement,” or “carrier rule” means, the team and the model can refer back to stable terms that anchor planning and implementation. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)

### 4. Feedback loops determine safe speed

The *Pragmatic Programmer* guidance that “the rate of feedback is your speed limit” aligns closely with what AI systems need in practice. Fast, reliable feedback lets the model operate in smaller loops where errors become visible earlier, reducing the chance of large speculative rewrites. [informit](https://www.informit.com/articles/article.aspx?p=2982114\&seqNum=5)

In modern AI-assisted workflows, the main feedback loops are type systems, linting, browser visibility, tests, and targeted runtime checks. Hooks in Claude Code exist specifically to automate actions around lifecycle events, such as running shell commands after changes, which can operationalize those feedback loops instead of relying on the user to remember them. [code.claude](https://code.claude.com/docs/en/hooks)

### 5. TDD as a behavior-shaping tool for models

The video presents TDD less as an ideology and more as a control surface for AI. Because the model tends to overproduce, TDD creates a disciplined structure: make one expectation explicit, implement only enough to satisfy it, then refactor while tests hold the boundary. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)

This makes TDD especially compatible with agentic coding where the risk is not lack of output but excess, drift, or hidden breakage. The better the test seams and interfaces, the more effectively AI can be delegated meaningful work without creating unreadable or brittle code. [softengbook](https://softengbook.org/articles/deep-modules)

### 6. Deep modules reduce cognitive load

Ousterhout’s deep module principle holds that modules should offer simple interfaces while hiding substantial internal complexity. This reduces cognitive load because consumers of the module can operate at the level of the contract instead of wading through internal detail. [softengbook](https://softengbook.org/articles/deep-modules)

The talk extends this neatly to AI-assisted coding. A fragmented system filled with shallow modules gives the model too many entry points, too much traversal work, and too many opportunities to misunderstand dependency chains, whereas deep modules let both humans and models reason from stable interfaces. [softengbook](https://softengbook.org/articles/deep-modules)

## Cross-reference map

### Principle relationships

| Video principle                    | Older software principle                                                                                       | Claude Code feature fit                                                                                                                                 | Gemini CLI fit                                                                                                                                                                                                                              | Why it matters                                                                                               |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| Shared understanding before coding | Brooks’s design concept as summarized in the talk. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)       | Skills package reusable planning workflows; CLAUDE.md stores persistent project rules. [code.claude](https://code.claude.com/docs/en/features-overview) | Hierarchical memory via `GEMINI.md` stores persistent project context. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                                                                            | Reduces wrong-yet-confident implementations. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)           |
| Ubiquitous language                | DDD ubiquitous language. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)                | Skills can encode domain vocab and workflows; CLAUDE.md can pin conventions. [code.claude](https://code.claude.com/docs/en/features-overview)           | `/memory add` and `GEMINI.md` can preserve glossary and domain rules across sessions. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                                                             | Improves alignment and reduces prompt verbosity. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)       |
| Small steps with feedback          | “Don’t outrun your headlights.” [informit](https://www.informit.com/articles/article.aspx?p=2982114\&seqNum=5) | Hooks can trigger tests or linting automatically after edits. [code.claude](https://code.claude.com/docs/en/overview)                                   | CLI command and memory flows support explicit context and task discipline, though external automation depends on shell tooling around Gemini CLI. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html) | Keeps AI work bounded by verification speed. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)           |
| TDD-guided iteration               | Test-first change discipline from the talk. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)              | Built-in tools plus hooks help run tests in looped workflows. [code.claude](https://code.claude.com/docs/en/overview)                                   | CLI workflows can be driven from terminal test commands with persistent project memory. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                                                           | Prevents overproduction and drift. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)                     |
| Deep modules                       | Ousterhout deep modules. [softengbook](https://softengbook.org/articles/deep-modules)                          | Skills and project conventions can codify interface-first architecture habits. [code.claude](https://code.claude.com/docs/en/features-overview)         | Memory files can capture architectural maps and module boundaries. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                                                                                | Makes code easier to explore, test, and safely change. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg) |

## Claude Code blueprint

Claude Code documentation recommends starting with `CLAUDE.md` for project conventions and then adding extensions only when recurring triggers appear, such as repeated mistakes, repeated prompts, or repeated manual workflows. That advice maps closely to the talk’s philosophy because both emphasize encoding stable design knowledge and reducing ambiguity before scaling up automation. [code.claude](https://code.claude.com/docs/en/features-overview)

### High-value Claude Code capabilities

| Capability  | What it does                                                                                                                                      | Best use in this blueprint                                                                                                                                                                        |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `CLAUDE.md` | Persistent context loaded every conversation. [code.claude](https://code.claude.com/docs/en/features-overview)                                    | Put coding standards, glossary terms, architectural rules, test commands, and “always validate before commit” instructions here. [code.claude](https://code.claude.com/docs/en/features-overview) |
| Skills      | Reusable knowledge and invocable workflows, loadable on demand or automatically. [code.claude](https://code.claude.com/docs/en/features-overview) | Implement `/grill`, `/ubiquitous-language`, `/write-prd`, `/deep-module-refactor`, `/tdd-loop` workflows. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)                                   |
| Hooks       | Trigger scripts, HTTP requests, prompts, or subagents on lifecycle events. [code.claude](https://code.claude.com/docs/en/features-overview)       | Run lint, type-check, focused tests, or architecture checks after file edits or before commits. [code.claude](https://code.claude.com/docs/en/hooks)                                              |
| MCP         | Connect to external services such as databases, Slack, or browsers. [code.claude](https://code.claude.com/docs/en/features-overview)              | Pull real schemas, inspect browser state, or query production-like systems safely during planning and debugging. [code.claude](https://code.claude.com/docs/en/features-overview)                 |
| Subagents   | Isolated workers with separate context that return summaries. [code.claude](https://code.claude.com/docs/en/features-overview)                    | Use for large research tasks, repo-wide exploration, or multi-file audits so main context stays clean. [code.claude](https://code.claude.com/docs/en/features-overview)                           |
| Plugins     | Package skills, hooks, subagents, and MCP servers for reuse across repositories. [code.claude](https://code.claude.com/docs/en/features-overview) | Standardize a company-wide or personal AI coding stack once workflows stabilize. [code.claude](https://code.claude.com/docs/en/features-overview)                                                 |

### Useful Claude Code skills to create

The strongest custom skills are the ones that encode repeated thinking patterns rather than one-off commands. Based on the video and official extension model, the most useful skills are these: [code.claude](https://code.claude.com/docs/en/agent-sdk/slash-commands)

- `/grill`: Ask structured questions until requirements, constraints, entities, edge cases, success criteria, and trade-offs are resolved. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- `/ubiquitous-language`: Scan docs and code, extract domain terms, identify synonyms, and write a canonical glossary. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)
- `/slice-feature`: Convert a feature into vertical slices with one observable outcome each. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- `/tdd-loop`: Write or refine a failing test, implement the smallest passing change, and refactor under test protection. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- `/deep-module-refactor`: Find shallow-module clusters and propose interface-first consolidation into deeper modules. [softengbook](https://softengbook.org/articles/deep-modules)
- `/write-prd`: Convert shared understanding into a PRD that explicitly lists module and interface impacts. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- `/post-change-review`: Summarize touched interfaces, risks introduced, tests run, and follow-up refactors needed. [code.claude](https://code.claude.com/docs/en/hooks)

### Claude Code setup pattern

A strong setup follows the layering model in the docs: put always-on rules in `CLAUDE.md`, reusable workflows in skills, external connectivity in MCP, repeated automation in hooks, and large context-hungry work in subagents. This keeps context cost manageable and prevents the session from being overloaded with instructions that should have lived in the right extension layer. [code.claude](https://code.claude.com/docs/en/features-overview)

## Gemini CLI blueprint

Gemini CLI documentation highlights command-driven workflows and a hierarchical memory system loaded from `GEMINI.md` files. The `/memory add` and `/memory show` commands are especially useful because they let teams persist project-specific rules, definitions, and reminders across sessions instead of rewriting them in every prompt. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)

### High-value Gemini CLI practices

| Practice                   | Supporting feature                                                                                                                  | Best use in this blueprint                                                                                                                                                                                         |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Project memory file        | `GEMINI.md` hierarchical memory. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)          | Store architecture map, glossary, coding standards, module boundaries, and decision records. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                             |
| Incremental memory updates | `/memory add`. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                            | Add new domain terms, testing rules, recurring bug patterns, or clarified assumptions as they emerge. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                    |
| Memory inspection          | `/memory show`. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                           | Audit whether the model is seeing the right project context before asking for changes. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)                                   |
| Memory refresh             | `/memory refresh` as described in Gemini CLI guidance. [addyosmani](https://addyosmani.com/blog/gemini-cli/)                        | Reload manually edited project knowledge when collaborating or changing files outside the CLI. [addyosmani](https://addyosmani.com/blog/gemini-cli/)                                                               |
| Shell-centered workflows   | Terminal-first usage pattern in CLI docs. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html) | Pair Gemini with local test scripts, linters, formatter checks, and architecture grep tools for explicit feedback loops. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html) |

### Useful Gemini CLI skills and conventions

Gemini CLI does not expose the same extension vocabulary as Claude Code in the fetched sources, but its memory system can still support many of the same operating principles. The most useful habits are to treat `GEMINI.md` as an architecture-and-language contract and to maintain task starter templates in repo scripts or shell aliases. [addyosmani](https://addyosmani.com/blog/gemini-cli/)

Useful patterns include:

- A `GEMINI.md` section for domain glossary and forbidden synonyms. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)
- A `GEMINI.md` section for module map, with each deep module’s interface and responsibility. [addyosmani](https://addyosmani.com/blog/gemini-cli/)
- A shell alias or script that asks Gemini to propose only one test-backed change at a time, enforcing the video’s small-step discipline. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)
- A repeatable review checklist stored in memory: touched files, boundary changes, tests added, mocks introduced, and risk areas. [addyosmani](https://addyosmani.com/blog/gemini-cli/)

## Recommended editor extensions

The talk’s process depends on fast feedback, readable errors, and architecture visibility. A practical editor stack should therefore privilege extensions that shorten the distance between code changes and useful signals. [github](https://github.com/theBadT/vscode-error-lens)

### Useful extensions

| Extension or tool type             | Why it helps                                                                                                                                                                                                                                   |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Error Lens                         | Displays diagnostics inline, making errors and warnings more prominent and speeding the feedback loop. [github](https://github.com/theBadT/vscode-error-lens)                                                                                  |
| GitLens                            | Improves code history and blame visibility, which helps trace architectural drift and understand why boundaries evolved. [thesoftwarescout](https://thesoftwarescout.com/best-vs-code-extensions-2026-20-must-have-tools-for-every-developer/) |
| ESLint / language-specific linters | Enforces style and catches issues early, which gives AI faster correction signals. [code.claude](https://code.claude.com/docs/en/hooks)                                                                                                        |
| Test explorer extensions           | Make focused test execution easier, reinforcing TDD and small-step iteration. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)                                                                                                            |
| Browser/devtools integrations      | Essential for frontend AI workflows where the model must inspect real UI state. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)                                                                                                          |

## Blueprint workflow

A complete AI coding workflow built from the talk and the tool docs looks like this: [code.claude](https://code.claude.com/docs/en/features-overview)

1. **Initialize project context.** Create `CLAUDE.md` or `GEMINI.md` with coding conventions, architectural constraints, validation commands, glossary seed terms, and module boundaries. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)
2. **Interrogate the feature.** Run a “grill me” style planning loop until the design concept is shared and ambiguity is reduced. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
3. **Build ubiquitous language.** Update the glossary and normalize terminology before implementation starts. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)
4. **Slice the work.** Break the feature into vertical slices with a single observable outcome and a defined verification method. [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
5. **Code in TDD loops.** Use a failing test, smallest passing change, and refactor cycle so the model never outruns feedback. [informit](https://www.informit.com/articles/article.aspx?p=2982114\&seqNum=5)
6. **Refactor toward deep modules.** Regularly consolidate related behavior behind simple interfaces and treat implementation as delegated detail where risk permits. [softengbook](https://softengbook.org/articles/deep-modules)
7. **Automate guardrails.** Use hooks, scripts, and inline diagnostics so checks happen by default, not by memory. [github](https://github.com/theBadT/vscode-error-lens)
8. **Review architecture daily.** PRDs, code reviews, and memory files should all explicitly track interface changes and module evolution. [addyosmani](https://addyosmani.com/blog/gemini-cli/)

## Example implementation

A backend pricing engine offers a good example. Start by defining exact terms such as `Quote`, `Surcharge`, `CarrierRule`, `EligibleShipment`, and `RetryableFailure` in the glossary so both the human and the model use the same domain language. [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)

Next, create a deep module such as `PricingService` with a small public interface and hide rule evaluation, ranking, and exception handling inside it. Ask the model to add one behavior at a time through TDD, such as “returns the lowest valid quote for an eligible shipment,” and run tests automatically through hooks or shell scripts after each change. [code.claude](https://code.claude.com/docs/en/hooks)

## Practical templates

### Suggested `CLAUDE.md` sections

- Project goals and non-goals. [code.claude](https://code.claude.com/docs/en/features-overview)
- Canonical glossary and banned synonyms. [code.claude](https://code.claude.com/docs/en/features-overview)
- Module map with interface contracts. [code.claude](https://code.claude.com/docs/en/features-overview)
- Required validation commands, such as type-check, unit test, integration test, and lint. [code.claude](https://code.claude.com/docs/en/hooks)
- Design rules, such as “prefer deep modules,” “do not add new abstractions without need,” and “touch interfaces deliberately.” [code.claude](https://code.claude.com/docs/en/features-overview)

### Suggested `GEMINI.md` sections

- Domain glossary. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)
- Architecture map. [addyosmani](https://addyosmani.com/blog/gemini-cli/)
- Feature slicing pattern. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)
- Testing policy and mocking rules. [addyosmani](https://addyosmani.com/blog/gemini-cli/)
- Post-change review checklist. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)

### Suggested custom prompts or skill starters

- “Interview relentlessly until all constraints, failure cases, and success criteria are explicit; do not propose implementation until ambiguity is low.” [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- “Extract domain terms from code and docs, identify collisions or synonyms, and propose one canonical glossary.” [martinfowler](https://martinfowler.com/bliki/UbiquitousLanguage.html)
- “Propose the smallest failing test for the next vertical slice; implement only enough to pass.” [youtube](http://www.youtube.com/watch?v=v4F1gFy-hqg)
- “Find shallow-module clusters and propose a deeper interface-first consolidation.” [softengbook](https://softengbook.org/articles/deep-modules)

## Closing view

The strongest reading of the talk is not that AI changes nothing, but that it changes the leverage points. Typing code matters less than before, while architecture, naming, validation, and interface design matter more because they determine whether AI output compounds quality or compounds entropy. [informit](https://www.informit.com/articles/article.aspx?p=2982114\&seqNum=5)

Claude Code and Gemini CLI are most effective when treated as programmable environments for these old principles rather than as magic code generators. Teams that encode shared language, feedback loops, and modular design into their AI workflows are likely to outperform teams that merely ask for more code faster. [google-gemini.github](https://google-gemini.github.io/gemini-cli/docs/cli/commands.html)
