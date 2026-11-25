# AI Engineering System — Stage 1

Universal foundation for AI-assisted software development.

## Included
- `AGENTS.md`: common repository-level instructions for coding agents.
- `docs/AI_ENGINEERING_STANDARD.md`: global engineering, security, quality and collaboration standards.
- `docs/AI_DEVELOPMENT_WORKFLOW.md`: controlled workflow for AI-assisted changes.
- `ai/checklists/TASK_COMPLETION_CHECKLIST.md`: evidence-based completion checklist.
- `ai/checklists/SECURITY_BASELINE_CHECKLIST.md`: baseline security review checklist.

## Installation

1. Extract this folder.
2. Copy `AGENTS.md`, `docs/`, and `ai/` into the root of an existing project.
3. If the project already has an `AGENTS.md`, merge the instructions rather than overwriting project-specific rules.
4. Commit the standards to version control.
5. Instruct your coding agent to read `AGENTS.md` and the linked standards before making changes.

## Important
This is the universal foundation only. Do not add framework-specific commands or architecture conventions here. Those belong in later stages (technology standards and project-specific instructions).

Different coding agents support different instruction-file conventions. Stage 2 will add tool-specific adapters such as Copilot instructions and Claude Code guidance while keeping this standard as the shared source of truth.

## Recommended first-use prompt

> Read the repository's `AGENTS.md` and all documents it references. Do not modify application code yet. Inspect the existing repository and report: (1) current architecture, (2) existing conventions, (3) test and quality commands discovered from project files, (4) security-sensitive areas, (5) conflicts between the repository and the AI Engineering Standard, and (6) any missing information that requires my decision. Do not invent commands or claim tests have passed unless you execute them. Wait for approval before implementation.
