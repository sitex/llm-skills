# Contributing

Contributions should keep every skill portable, narrowly scoped, and easy to audit.

## Requirements

- Put each distributable skill in `skills/<skill-name>/`.
- Include a valid `SKILL.md` with a discriminating `name` and `description`.
- Add scripts, references, assets, or tool dependencies only when the workflow needs them.
- Do not add secrets, private paths, hidden global state, telemetry, automatic network access, or shell hooks.
- Preserve explicit user approval boundaries for external or destructive actions.
- Document installation or behavior changes in `README.md` when they affect users.

## Verification

Run:

```bash
./scripts/verify
```

Describe the behavioral scenario used to test instruction changes in the pull request.
