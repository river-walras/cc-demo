# Reading & Writing Workflows

## Phase 1: Read
Fetch content from URLs. Extract and present only — no file writes.
Rule: `.claude/rules/raw.md`

## Phase 2: Write (Agent)
Run as Agent. Takes extracted content, writes all output files.
Rule: `.claude/rules/summaries.md`

## Directory
```
raw/
├── index.md
└── summaries/  (001.md, 002.md, ...)

summaries/
├── index.md
├── synthesis.md
└── tables/
    ├── comparison.md
    ├── timeline.md
    ├── categories.md
    └── contradictions.md
```

## Workflow
