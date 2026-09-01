# Repository Working Agreement

## Purpose

- This repository publishes portable, open-source skills for Codex.
- Keep each skill focused, auditable, and independent of private infrastructure.
- Store distributable skills under `skills/<skill-name>/`.

## Skill Development

- Follow the Agent Skills format: every skill requires `SKILL.md` with a precise `name` and `description`.
- Prefer instructions over scripts. Add scripts, references, or assets only when they materially improve repeatability.
- Do not add hidden global state, automatic network access, telemetry, shell hooks, or broad permissions to a skill.
- Validate every changed skill with the bundled Codex `quick_validate.py` and run `./scripts/verify` before claiming completion.

## Workflow

- WF plans belong in `thoughts/shared/plans/`; durable research belongs in `thoughts/shared/research/`.
- End research reports with one concrete recommended next step.
- Do not commit `thoughts/` or run HumanLayer Thoughts sync implicitly.
- Keep GitHub issue and release notes aligned with verified, user-visible work when applicable.

## Git and Publication

- Preserve unrelated work and stage explicit paths only.
- Never commit secrets or local environment files.
- A public release requires a clean verification gate, an open-source license, installation instructions, and a reviewed public-repository diff.
