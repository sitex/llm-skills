# llm-skills

Portable, auditable skills for Codex and other Agent Skills-compatible hosts.

## Skills

### `$reflect`

`$reflect` reviews observable evidence from completed or paused work and proposes a small set of reusable instructions. It writes only the rules the user explicitly approves, placing project-specific learnings in the applicable `AGENTS.md` and cross-project learnings in `~/.codex/AGENTS.md`.

The skill intentionally does not expose hidden reasoning, modify source code, commit changes, synchronize notes, use hooks, call external services, or maintain its own persistent state.

## Install

### Codex skill installer

Invoke `$skill-installer` in Codex and ask it to install:

```text
https://github.com/sitex/llm-skills/tree/main/skills/reflect
```

### Manual installation

Clone the repository and link the skill into the user skill directory:

```bash
git clone https://github.com/sitex/llm-skills.git
mkdir -p ~/.agents/skills
ln -s "$(pwd)/llm-skills/skills/reflect" ~/.agents/skills/reflect
```

Codex supports symlinked skill folders. Restart Codex if the skill does not appear immediately.

## Use

Explicit invocation:

```text
$reflect
```

You can also ask Codex to reflect on the current session and propose reusable learnings. The skill first presents candidates with evidence and destinations. It edits instruction files only in a later turn after explicit approval.

## Development

Run the repository verification gate:

```bash
./scripts/verify
```

The gate checks skill structure, unfinished placeholders, metadata, local-path leaks, and whitespace. When the Codex `skill-creator` validator is installed, the gate runs it as an additional check.

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution requirements.

## License

[MIT](LICENSE)
