# ai-agent-base

> Workshop 1: your first AI agent, with a memory.

The seed of the whole approach. A single, general-purpose AI agent that
remembers, because its memory and context live in plain Markdown files,
versioned in git. That is what turns a forgetful chatbot into an assistant
accurate enough to trust with real work. One agent, persistent memory.

## What is in here
- `CLAUDE.md`: the startup routine the agent reads on every session.
- `MEMORY.md`: what the agent has learned, updated in place as it goes.
- `context/`: loaded on demand via `context/INDEX.md`. `VOICE.md` (how to write)
  and `PROFILE.md` (who you are: what you do, where you live), filled in by the
  first-run setup.

## How to start
1. Fork or clone this repo.
2. Open it in Claude Code.
3. Say **"Hi"** to kick off. On the first run that triggers a quick setup (the
   welcome wizard); after that it reads your memory and context and gets to work,
   and updates `MEMORY.md` whenever you correct it so it remembers next time.

## Concepts in this repo
- **Written memory** (`MEMORY.md`) — the agent records what it learns and reads
  it back every session, so it stops forgetting.
- **Written context, loaded on demand** (`context/` + `context/INDEX.md`) — who
  you are (`PROFILE.md`) and how to write (`VOICE.md`), pulled in only when a
  task needs them rather than all at once.
- **The startup routine** (`CLAUDE.md`) — the first thing read every session; it
  says what to load and how to behave.
- **Playbooks** (`playbooks/`) — saved procedures run on a trigger word: the
  first-run welcome wizard, plus `save` and `reload`.
- **First-run onboarding** — the welcome wizard interviews you once, writes your
  answers into `PROFILE.md` / `VOICE.md`, then removes itself.
- **Git as the store** — everything is plain Markdown in git: diffable,
  revertable, and yours, with no hidden state and models you can swap freely.

## Claude Code files (and Codex equivalents)
Almost everything here is plain Markdown that any agent runner reads because the
startup file points it there, so it copies to other tools unchanged. The only
genuinely Claude Code-specific file is the startup file itself:

| This repo (Claude Code) | Codex equivalent |
|---|---|
| `CLAUDE.md` (auto-loaded startup file) | `AGENTS.md` |

`MEMORY.md`, `context/`, and `playbooks/` are not platform features, they are
conventions in plain Markdown (playbooks are just SOPs written down, not the
Claude "skills" feature). Copy them to Codex as-is and have `AGENTS.md` point at
them the same way `CLAUDE.md` does here.

## The progression
`ai-agent-base` (one agent) ->
[`ai-team-base`](https://github.com/gbergeret/ai-team-base) (a team with a
router) ->
[`ai-teams-base`](https://github.com/gbergeret/ai-teams-base) (an organisation of
teams). This is step 1.
