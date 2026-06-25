# ai-agent-base

> Workshop 1: your first AI agent, with a memory.

The seed of the whole approach. A single, general-purpose AI agent that
remembers, because its memory and context live in plain Markdown files,
versioned in git. That is what turns a forgetful chatbot into an assistant
accurate enough to trust with real work. One agent, persistent memory.

## What is in here
- `CLAUDE.md`: the startup routine the agent reads on every session.
- `MEMORY.md`: what the agent has learned about you, updated in place as it goes.
- `context/VOICE.md`: how you want it to write and talk to you.

## How to start
1. Fork or clone this repo.
2. Open it in Claude Code.
3. Say **"Hi"** to kick off. On the first run that triggers a quick setup (the
   welcome wizard); after that it reads your memory and voice and gets to work,
   and updates `MEMORY.md` whenever you correct it so it remembers next time.

## The progression
`ai-agent-base` (one agent) ->
[`ai-team-base`](https://github.com/gbergeret/ai-team-base) (a team with a
router) ->
[`ai-teams-base`](https://github.com/gbergeret/ai-teams-base) (an organisation of
teams). This is step 1.
