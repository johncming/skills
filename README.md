# Agent Skills

A collection of agent skills that extend capabilities across planning, development, and tooling.

## Output Location

Most planning skills output to `john_plans/` directory:

```
john_plans/
├── prd-<feature>.md      # Product requirements documents
├── issue-<bug>.md        # Bug/issue triage reports
├── refactor-<desc>.md    # Refactor plans
├── slice-<feature>.md    # Vertical slice work items
└── plan-<feature>.md     # Implementation plans
```

Each file has frontmatter with `type`, `status`, `blocked_by`, and `created` fields. When done, delete the file (git preserves history).

## Planning & Design

These skills help you think through problems before writing code.

- **write-a-prd** — Create a PRD through an interactive interview, codebase exploration, and module design. Saved to `john_plans/prd-*.md`.
- **prd-to-issues** — Break a PRD into independently-grabbable work items using vertical slices. Saved to `john_plans/slice-*.md`.
- **prd-to-plan** — Turn a PRD into a multi-phase implementation plan. Saved to `john_plans/plan-*.md`.
- **grill-me** — Get relentlessly interviewed about a plan or design until every branch of the decision tree is resolved.

## Development

These skills help you write, refactor, and fix code.

- **tdd** — Test-driven development with a red-green-refactor loop. Builds features or fixes bugs one vertical slice at a time.
- **triage-issue** — Investigate a bug by exploring the codebase, identify the root cause, and save a TDD-based fix plan to `john_plans/issue-*.md`.
- **request-refactor-plan** — Create a detailed refactor plan with tiny commits. Saved to `john_plans/refactor-*.md`.
- **improve-codebase-architecture** — Explore a codebase for architectural improvement opportunities, focusing on deepening shallow modules and improving testability.

## Tooling & Setup

- **setup-pre-commit** — Set up Husky pre-commit hooks with lint-staged, Prettier, type checking, and tests.
- **git-guardrails-claude-code** — Set up Claude Code hooks to block dangerous git commands (push, reset --hard, clean, etc.) before they execute.

## Other

- **ubiquitous-language** — Extract a DDD-style ubiquitous language glossary from the conversation. Saved to `UBIQUITOUS_LANGUAGE.md`.
- **obsidian-vault** — Search, create, and manage notes in the Obsidian vault.
- **edit-article** — Edit and improve articles by restructuring sections, improving clarity, and tightening prose.
- **design-an-interface** — Generate multiple radically different interface designs for a module using parallel sub-agents.
- **scaffold-exercises** — Create exercise directory structures with sections, problems, solutions, and explainers.
- **migrate-to-shoehorn** — Migrate test files from `as` type assertions to @total-typescript/shoehorn.
- **write-a-skill** — Create new skills with proper structure, progressive disclosure, and bundled resources.
