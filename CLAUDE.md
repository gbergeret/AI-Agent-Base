# CLAUDE.md

The startup routine. Read this first, on every session.

## First run: the welcome wizard
On the first session, if `playbooks/000-welcome-wizard.md` exists and the name
under "About you" in `MEMORY.md` is still the placeholder, run that playbook
before anything else. It onboards you, then deletes itself, so this happens only
once.

## Load on every session
1. `MEMORY.md`: what you have learned about me and the work in flight.
2. `context/VOICE.md`: how I want you to write and talk to me.

Use both to shape every response.

## Playbooks
Playbooks in `playbooks/` are saved procedures. Some run on demand: when the
user uses a playbook's trigger word, run that playbook. The triggers are listed
in `playbooks/README.md`. Available now:
- "save" (or "save to main") -> run `playbooks/001-save-to-main.md`
- "reload" (or "rebase from main") -> run `playbooks/002-rebase-from-main.md`

## Keep memory current
When I correct you, or you learn something new, update `MEMORY.md` in place.
Replace what is outdated, do not just pile new lines on top. Memory should
always reflect the latest state.

## How we work
- If a request is ambiguous, ask before acting.
- Lead with the answer, then add the detail.
