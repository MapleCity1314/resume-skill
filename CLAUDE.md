# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repository Is

A modular Claude AI Skills Suite for resume optimization. It contains no compiled code — only SKILL.md prompt definitions and reference documentation.

## Skill Architecture

**Hub-and-spoke model:**
- `resume-editor/SKILL.md` — main entry hub; routes users to specialized skills after diagnosis
- `resume-experience/SKILL.md` — work/internship experience rewriting (STAR method)
- `resume-project/SKILL.md` — project/case experience optimization
- `resume-skills/SKILL.md` — technical and core skills module
- `resume-summary/SKILL.md` — self-evaluation / personal statement rewriting

**Specialist support skills:**
- `resume-jd-match/SKILL.md` — JD parsing, keyword extraction, gap analysis, rewrite routing
- `resume-interview-bridge/SKILL.md` — interview question prediction + STAR prep + self-trap alerts
- `resume-file-export/SKILL.md` — Markdown/HTML export with Typora/pandoc/VSCode methods
- `resume-ats/SKILL.md` — ATS format audit and keyword density check (foreign company use only)
- `resume-cover-letter/SKILL.md` — BOSS/Maimai/LinkedIn outreach messages (China-focused)

**Reference knowledge base** (under `resume-editor/references/`):
- `star-method.md` — STAR framework with 20+ industry examples
- `field-guides.md` — role-specific tech stacks and metrics (Frontend, Backend, AI, Ops, etc.)
- `common-mistakes.md` — 50+ categorized resume errors with fixes

## Hard Constraints (Do Not Modify)

The following bottom-layer logic must remain intact across all skills:
- **Six Iron Rules** (六条铁律) in `resume-editor/SKILL.md`
- **STAR formula** and sentence structures in `resume-experience/SKILL.md` and `references/star-method.md`
- **5-dimension scoring system** (5 维评分) in `resume-editor/SKILL.md`
- **Forbidden word lists** (禁用词) in each skill
- **Golden structure** (黄金结构) in `resume-project/SKILL.md`

When adding content: append-only to existing files. When building new skills: follow existing formatting conventions.

## Priority Levels

- **P0** (must): resume-editor, resume-jd-match, resume-experience, resume-skills (core fixes)
- **P1** (important): resume-project, resume-summary, resume-interview-bridge, resume-file-export, career-stage-weights
- **P2** (optional): resume-ats, resume-cover-letter, ats-guide (foreign company scenarios only)

## Skill File Format

Each SKILL.md follows this structure:
```
---
name: [skill-name]
description: [trigger phrases + use cases]
---
[Role definition in Chinese]
[Numbered workflow steps]
[Output format templates]
[Industry-specific examples with before/after pairs]
```

## Key Content Conventions

- **Primary language**: Simplified Chinese for all user-facing content; English acceptable in technical terms
- **Experience format**: STAR (Situation-Task-Action-Result) is the canonical structure for all work/project descriptions
- **Quality progression**: Each skill shows weak → medium → strong examples — maintain this pattern when adding examples
- **Industry segmentation**: Guidance must cover both tech roles (Frontend, Backend, AI, Full-stack) and non-tech roles (Operations, Marketing, Product, Design, Finance, HR)
- **Prohibited words**: Each skill maintains a "禁用词" (banned phrase) list — do not remove these or add phrases that are vague/unverifiable
- **Quantification rule**: Every bullet point should end with or include a measurable outcome; scale (headcount/budget/users) is acceptable when exact numbers are unavailable

## Resume Scoring Dimensions (used in resume-editor)

| Dimension | Weight |
|-----------|--------|
| Content Relevance | 30% |
| Quantification | 25% |
| Structure Clarity | 20% |
| Expression Professionalism | 15% |
| Visual Formatting | 10% |

Do not alter these weights without reviewing the full diagnostic workflow in `resume-editor/SKILL.md`.

## Editing Guidelines

- When adding new industry examples, place them in the appropriate section under the existing role list — do not create new top-level sections
- Reference files (`star-method.md`, `field-guides.md`, `common-mistakes.md`) are sourced by `resume-editor` — keep cross-references consistent
- The six "Iron Laws" in `resume-editor/SKILL.md` are load-bearing rules cited throughout all skills; changes there ripple to all modules
