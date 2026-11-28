# Stage 10 — AI Security Engineering, Threat Modeling & Adversarial Testing

This package establishes reusable security standards for AI-enabled applications, RAG systems, agents, model integrations, tools, and delivery pipelines. It supplements Stages 1–9 and does not replace existing security, governance, QA, or operations requirements.

## Workflow
1. Extract this package into the repository root.
2. Review the files and existing repository conventions.
3. Integrate `AGENTS_STAGE_10_ADDENDUM.md` into the existing root `AGENTS.md`; never replace it.
4. Preserve Stages 1–9 and project-specific requirements.
5. Run `ai/prompts/ai-security/06-integrate-and-audit-stage-10.md` in Antigravity.
6. Review the independent read-only audit before staging or committing.

## Package inventory
33 files: 2 root files, 14 documentation files, 7 templates, 4 checklists, and 6 prompts.

## Scope
Threat modeling, attack-surface inventory, prompt injection, agent/tool security, authentication, data protection, secrets, sandboxing, supply-chain security, adversarial testing, findings, incident response, and release gates.

## Limitation
Documentation does not itself secure an application, perform penetration testing, or establish legal compliance. Validate controls in the actual target system and record evidence against the exact commit, environment, and scope.
