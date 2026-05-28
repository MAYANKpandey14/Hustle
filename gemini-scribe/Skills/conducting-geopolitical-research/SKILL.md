---
name: conducting-geopolitical-research
description: Use when conducting geopolitical research, analyzing defense policies, mapping energy supply chains, or structuring scenario briefs in this vault.
---

# Conducting Geopolitical Research & Scenario Analysis

## Overview
This skill defines the methodology for executing high-fidelity geopolitical research, supply chain mapping, and scenario analysis. It ensures data is gathered dynamically and formatted to the vault's rigorous standards.

## When to Use
- **Trigger**: Researching regional security, maritime logistics, or military procurement policies.
- **Symptom**: Need to analyze strategic shifts (e.g., U.S. diplomatic pivots, OPEC+ re-routing) rather than surface-level facts.
- **When NOT to use**: Do not use for personal development, sales scripts, or philosophical studies.

## Core Pattern

### 1. Document Frontmatter Requirements
Every geopolitical research document MUST start with this exact YAML metadata block. Never omit this:
```yaml
---
type: Geopolitics-Research  # Or Geopolitics-Analysis
status: Active              # Active, Expanded, or Archive
tags: [geopolitics, india, ...]
related_to: ["[[related-note-1]]", "[[related-note-2]]"]
Date: YYYY-MM-DD
---
```

### 2. Systematic Research Steps
1. **Initial Web Search**: Execute targeted queries to capture current events, official statements, and chokepoint data.
2. **Deep-Dive Verification**: Drill down into military stock depletion rates, trade agreements, and bilateral policy briefs.
3. **Structured Mapping**: Divide the report into logical sections: Executive Summary, Current Landscape, Scenario Projections (Best/Worst/Most-Likely), Strategic Impacts on India, and References.

## Common Mistakes

| Mistake | Prevention |
|--------|------------|
| **Omit YAML Frontmatter** | **CRITICAL**: Always prefix the file with the YAML block containing `type`, `status`, `tags`, and `Date`. |
| **Outdated/Assumed Data** | Always verify recent dates (such as late 2026 events) using web search rather than relying on static training data. |
| **No WikiLinks** | Connect tactical platform issues (e.g., Tejas engines) to broad strategic goals (e.g., naval dominance) using `[[WikiLinks]]`. |
| **No Scenario Cases** | Scenario mapping must specify three distinct projections: Best-Case, Worst-Case, and Most-Likely Case. |
