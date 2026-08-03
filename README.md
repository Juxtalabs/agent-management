# agent-management

Internal, shared rules for Claude Code sessions. [`CLAUDE.md`](./CLAUDE.md) holds a set of working rules that make Claude act reliably and efficiently — no unasked-for changes, no wasted tokens.

## Apply it to your Claude

**Pick ONE of the two prompts below and paste it into a Claude Code session.** Both point Claude at this repo's `CLAUDE.md` and set up your **global** rules at `~/.claude/CLAUDE.md` (applies to every session on your machine).

- **Option A — Merge:** use this if you already have your own `~/.claude/CLAUDE.md` and want to keep it. Adds these rules on top of yours and removes duplicates.
- **Option B — Replace:** use this if you don't have one yet, or you just want this ruleset as-is. Overwrites your `~/.claude/CLAUDE.md` with this one (your old file is backed up first).

### Option A — Merge & dedupe into your existing CLAUDE.md

```
Fetch https://raw.githubusercontent.com/Juxtalabs/agent-management/main/CLAUDE.md and merge its rules into my global CLAUDE.md at ~/.claude/CLAUDE.md. Create the file if it doesn't exist. Keep every rule I already have — just add the ones from this file and dedupe anything that overlaps. Show me the diff before you write it.
```

### Option B — Replace my CLAUDE.md with this one

```
Fetch https://raw.githubusercontent.com/Juxtalabs/agent-management/main/CLAUDE.md and make it my global CLAUDE.md at ~/.claude/CLAUDE.md, replacing whatever is currently there. Create the file if it doesn't exist. Back up any existing file to ~/.claude/CLAUDE.md.bak first, then show me the result.
```

> Want these rules for one project only instead of everywhere? Drop `CLAUDE.md` at that repository's root instead of `~/.claude/` — a project's own rules stack on top of your global ones.
