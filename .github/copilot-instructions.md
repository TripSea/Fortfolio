<!--
  Auto-generated starter for repo-level AI coding instructions.
  This file was created because no existing agent instruction files were found.
  Please review and edit to add concrete project details (build/test commands,
  important directories, and any nonstandard conventions) so AI agents can be
  immediately productive.
-->

# Copilot / AI agent instructions — Fortfolio

Purpose
-------
Provide concise, repository-specific guidance that helps an AI coding agent be immediately productive when working on this project.

NOTE: At the time this file was created there were no repository-sourced agent files (for example `.github/copilot-instructions.md`, `AGENT.md`, or `README.md`). This document is a focused template and a checklist for the human maintainer to fill in project-specific facts.

Quick facts you should add here (replace placeholders)
----------------------------------------------------
- Primary language(s): <e.g. TypeScript, Python, Go>
- Build command: `e.g. npm run build` or `./gradlew build`
- Test command(s): `e.g. npm test` or `pytest -q`
- Start/dev command: `e.g. npm run dev` or `uvicorn app:app --reload`
- Key directories: `src/`, `packages/`, `services/`, `web/` (update to match repo)
- CI: path to workflow file(s) (e.g. `.github/workflows/ci.yml`)

What AI agents should do first (discoverable steps)
-------------------------------------------------
1. Look for a language manifest at the repo root: `package.json`, `pyproject.toml`, `Pipfile`, `requirements.txt`, `go.mod`, `Cargo.toml`. Use that to infer the language and build tools.
2. Check for common entry points: `src/`, `app/`, `cmd/`, `main.py`, `index.tsx`, `Dockerfile`, `docker-compose.yml` to learn runtime structure and services.
3. Scan `.github/workflows/` to discover CI commands and test matrices — copy exact commands from workflows when available.
4. Search for `README.md` or `docs/` for architecture notes and runbook steps.

Project-specific patterns (add examples below)
---------------------------------------------
- Monorepo layout: If present, list package-manager (pnpm/workspaces, yarn workspaces, lerna). Example: `packages/*` contains reusable components; `apps/*` contains deployable services.
- API servers: e.g. `services/api/` uses FastAPI and uvicorn; tests run with `pytest -q` and coverage with `coverage run -m pytest`.
- Frontend: e.g. `web/` is a Vite/React app; start with `pnpm dev` and build with `pnpm build`.

Conventions and coding patterns to follow
----------------------------------------
- Import style: prefer absolute imports from `@/` or relative? (fill in)
- Linting and formatting: e.g. `prettier`, `eslint`, `black` — include exact commands and config file locations.
- Testing: where tests live (e.g. `tests/`, `__tests__/`) and how to run a single test file.

Integration and external dependencies
------------------------------------
- List external services and how to spin them up locally (Postgres, Redis, S3, Auth). Provide docker-compose file path if used.
- Any API keys or secrets are stored in: (env files, secret manager). Agents must not attempt to access secrets.

Examples from the repo (replace with actual matches)
---------------------------------------------------
- If this repo had a `package.json`, show the `scripts.build` and `scripts.test` entries here.
- If there's a `services/api/main.py`, show how the app is launched locally.

When editing code
-----------------
- Keep changes minimal and focused. Respect existing coding style and tests.
- If adding a dependency, prefer small, well-known packages and update the lockfile/manifest.

What I couldn't discover automatically
-------------------------------------
- Concrete build/test/start commands and primary language — please fill these in.

How you can help the AI agent
-----------------------------
1. Replace placeholders above with concrete commands and paths.
2. Add one-paragraph architecture summary describing major components (web, api, db, background workers) and how they communicate.
3. Add examples for 2–3 typical tasks (run tests, add feature, fix CI) showing exact commands.

Feedback
--------
If anything here is unclear or you want the file to be more prescriptive, tell me which commands and top-level directories to include and I will update the file.

-- End of starter template --
