# Stage 3 — Technology-Specific Engineering Standards

Stage 3 adds conditional engineering standards for common technology stacks. It is an add-on to Stages 1 and 2, not a replacement for their supporting files.

## Install
1. Commit or back up your current repository.
2. Extract this package into your existing AI Engineering System repository.
3. Replace the root `AGENTS.md` with the Stage 3 version included here.
4. Merge the `docs/technology/`, `ai/checklists/` and `ai/prompts/` folders into the matching folders.
5. Keep all Stage 1 and Stage 2 files unless a later stage explicitly replaces them.
6. Review and commit the changes.

## Included standards
Core PHP, Laravel, JavaScript/TypeScript, React, Node.js/Express, MySQL, MongoDB, HTML/CSS/Bootstrap/responsive UI, REST APIs/integrations, testing/automation, performance/scalability/production readiness.

## Required behavior
Agents must discover the actual stack from repository evidence, verify versions, select only relevant standards, follow approved project conventions, and disclose unknowns. These standards do not themselves enforce permissions or runtime behavior.

## First use
Run `ai/prompts/technology-stack-audit.md` as a read-only audit. Use `ai/prompts/technology-aware-task.md` for implementation tasks.
