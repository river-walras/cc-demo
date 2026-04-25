---
paths:
  - summaries
---

# Writing Phase Rules (Agent)

Receives extracted content from Phase 1. Writes all output files using Obsidian wikilinks.

**Link format**: `[[id|Title]]` for summaries, `[[filename]]` for tables/synthesis.

---

## Summary Files (raw/summaries/)

### Front Matter (Required)
```yaml
---
source: [Author/Handle]
title: [Original title or first 15 words]
date: [YYYY-MM-DD]
url: [Direct link]
category: [Metric|Best Practice|Tool/Feature|Concept|Case Study|Opinion/Critique|Tutorial|Trend]
---
```

### Content Structure
```markdown
## Core Claim
[1-2 sentence thesis]

## Key Points
- Point with supporting data
- Point with example
- Point with metric/number

## Critical Details
- Numbers, percentages, measurements
- Specific tools or frameworks
- Timeline or sequence

## Notes (optional)
- Connections to other posts
- Questions or argument gaps
```

### Quality
- 80-150 words (excluding metadata)
- Preserve exact data; quote key claims
- File naming: `001.md`, `002.md`, ... in `raw/summaries/`

---

## raw/index.md

### Required Sections
1. **By Category** — grouped summaries
2. **By Date** — chronological
3. **By Source** — grouped by author
4. **Statistics** — totals, date range, category counts

### Format Example
```markdown
# Reading Summaries Index

## By Category

### Metric (3 posts)
- [[001|Post Title]] — 1 line description

## By Date
- 2026-03-15 [[001|Post Title]]

## By Source
### Author Name (2 posts)
- [[001|Post Title]]

## Statistics
- Total: X summaries
- Date range: YYYY-MM-DD to YYYY-MM-DD
- Categories: Metric (3), Best Practice (2)
```

---

## summaries/index.md

```markdown
# Content Index

## Phase 1: Raw Summaries
| # | Title | Category | Source |
|---|-------|----------|--------|
| [[001]] | Title | Category | Author |

## Core Themes
- Theme 1: [Definition] — Posts: [[001]], [[003]]
- Theme 2: [Definition] — Posts: [[002]], [[005]]

## Quick Stats
- Total posts: X
- Themes: X
- Conflicts: X
- Timeline: YYYY-MM-DD to YYYY-MM-DD
```

---

## Tables (summaries/tables/)

### comparison.md — Core Arguments

| Source | Main Claim | Evidence | Applies To | Confidence |
|--------|-----------|----------|-----------|-----------|
| [[001\|Author (001)]] | "exact quote" | data/numbers | scope | High/Medium/Low |

- 5 columns exactly; max 20 rows; no interpretation

---

### timeline.md — Chronological Evolution

| Date | Author | Claim | Change | Status |
|------|--------|-------|--------|--------|
| 2026-01-15 | [[001\|Author]] | Claim | Initial | Refined |

- Chronological order; mark shifts in **bold**; flag contradictions with ⚡

---

### categories.md — Thematic Matrix

| Post | Title | Theme1 | Theme2 | Theme3 |
|------|-------|--------|--------|--------|
| [[001]] | Title | ✓ | ◐ | ✗ |

- ✓ Primary · ◐ Secondary · ✗ Not addressed
- 6-10 theme columns; include 1-line definition per column

---

### contradictions.md — Opposing Viewpoints

```markdown
## Contradiction 1: [Title]

| Claim | Post | Author | Date | Severity |
|-------|------|--------|------|----------|
| Claim A | [[001]] | Author | Date | Major |
| Claim B | [[005]] | Author | Date | Major |

### Analysis
- Nature: Fact-based vs Interpretation-based
- Resolution: [one correct / both valid / needs data]
- Context: [time gap, scope difference]
```

- Only genuine contradictions; exact quotes; min 3 identified

---

## summaries/synthesis.md

```markdown
# Synthesis: [Topic]

## Overview
[2-3 paragraph executive summary]

## Key Findings
- Finding 1 ([[001]], [[003]])
- Finding 2 ([[002]], [[005]])

## Detailed Analysis

### [Theme Name]
[Integrated narrative, 3-4 paragraphs]
**Sources**: [[001]], [[003]]

## Contradictions & Tensions
### [Title]
[[001]] claims... | [[005]] claims...
**Analysis**: [how to understand this tension]

## Trends & Patterns
- **Pattern 1**: evidence from [[001]], [[002]], [[003]]

## Gaps & Open Questions
- What's missing, unresolved, or needs more data

## Conclusion
[Synthesis-level insight]
```

- 800-1500 words; cover 60%+ of summaries; every claim linked

---

## Quality Thresholds

| | Minimum | High |
|--|---------|------|
| Tables | 60% posts, 2+ data columns | All posts, full cross-refs |
| Synthesis | 800w, 3 themes, 1 contradiction | 1000w+, 3+ patterns, gaps noted |
| Index | All summaries listed, stats | 3+ views, clickable links |
