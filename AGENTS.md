# AGENTS.md — Chat agent instructions (workspace-level)

Purpose
-------
This file gives concise, actionable guidance to AI coding agents working in this repository. Keep it minimal: link to project docs rather than embedding them.

Workspace state
---------------
The workspace currently contains no project files (no README, build scripts, or source code). If this is unexpected, pull or restore the project contents before running typical agent workflows.

Quick agent checklist
--------------------
- Look for common project entry points: `README.md`, `package.json`, `pyproject.toml`, `Dockerfile`, `Makefile`.
- If none exist, ask the user whether to scaffold a project or to import existing sources.
- Prefer `git` to inspect history: run `git status` and `git log --oneline -n 20` to learn recent activity.

How to handle the user argument: "sacc"
--------------------------------------
- Treat `sacc` as a focal area or component name. Search the workspace for folders or files containing the token `sacc` (case-insensitive) and prioritize those when answering or making changes.
- If `sacc` is ambiguous, ask the user whether it refers to a subsystem, package, script, or third-party integration.

Agent behavior conventions
-------------------------
- Link, don't embed: when documentation exists in the repo, reference it with a workspace-relative link instead of copying content.
- Be minimal and actionable: include only what's necessary for an agent to start working. Defer to the user for missing context.
- Ask short clarifying questions before making large or irreversible changes.

Next steps for maintainers
-------------------------
- Add a short `README.md` with build/test commands and architecture notes.
- If `sacc` is a key component, add a dedicated `docs/SACC.md` describing its purpose, entry points, and commands.

Contact
-------
If you want the agent to behave differently (different test commands, lint rules, or CI), update this file and include links to the relevant scripts or docs.
