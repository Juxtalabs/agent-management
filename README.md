# agent-management

Internal, shared rules for Claude Code sessions. [`CLAUDE.md`](./CLAUDE.md) holds working rules that make Claude act reliably and efficiently, with no unasked-for changes and no wasted tokens. It also ships the [`unslop`](./skills/unslop/SKILL.md) writing skill, which strips AI tells from everything Claude writes.

You don't clone this repo. The two files just live here so Claude can fetch them by URL and install them onto your machine.

## Set it up

Paste this into a Claude Code session. It backs up your current global `~/.claude/CLAUDE.md` (if you have one), replaces it with this one, and installs the `unslop` skill that `CLAUDE.md` loads.

```
Set up my global Claude Code rules. In this session:

1. If ~/.claude/CLAUDE.md already exists, back it up to
~/.claude/CLAUDE.md.bak first.

2. Fetch this URL and save it as ~/.claude/CLAUDE.md,
replacing whatever is there now:
https://raw.githubusercontent.com/Juxtalabs/agent-management/main/CLAUDE.md

3. Fetch this URL and save it as
~/.claude/skills/unslop/SKILL.md, creating folders if needed:
https://raw.githubusercontent.com/Juxtalabs/agent-management/main/skills/unslop/SKILL.md

Then show me what you changed.
```

> Want these rules for one project only instead of everywhere? Save the `CLAUDE.md` URL above at that repository's root instead of `~/.claude/`. A project's own rules stack on top of your global ones. The `unslop` skill still installs globally at `~/.claude/skills/`.
