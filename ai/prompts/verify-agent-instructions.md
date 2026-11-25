# Prompt: Verify AI agent instruction loading

Act as a developer-environment and repository configuration auditor. Do not modify files.

1. Identify the active tool and exact surface (IDE, CLI, desktop or cloud).
2. Inspect instruction files relevant to that surface.
3. Explain which files are supported and which may be ignored.
4. Summarize applicable instructions without exposing secrets.
5. Identify conflicts, duplication and stale instructions.
6. Inspect permissions/sandbox settings without changing them.
7. Identify risky permissions, broad filesystem access or network access.
8. State what cannot be verified.

Return active files with evidence, ignored files, conflicts, permission findings, risk-ranked recommendations and verification steps.

Do not claim an instruction is active unless documented discovery or tool status establishes it. Do not edit until approved.
