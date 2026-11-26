# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## About me

I work mostly on web frontends and backend APIs. Defaults unless a project says otherwise:

- TypeScript for frontend and backend.
- Python for scripting.
- pnpm as the package manager.
- Tailwind for styling.

## Working style

- Plan first. For anything non-trivial, propose an approach and wait for my go-ahead before editing.
- Check in often. If a decision could reasonably go two ways, ask instead of picking.
- Keep explanations brief. Explain reasoning when it matters, skip recaps of what you just did.

## Writing

- Use ASD-STE100 Simplified Technical English for everything written for me: explanations, code comments, commit messages, issues, and tickets.
- Short sentences, active voice, one idea per sentence, simple common words, no idioms.

## Code style

- Readability for humans comes first. Code doesn't need to be optimal or use the newest language features.
- Match the existing conventions of the repo over your own preferences.
- Comments only for the non-obvious why.
- Keep diffs small. No drive-by refactors or unrelated cleanups.

## Testing

- Run relevant tests after changes, and write tests for new logic.
- Test what matters. Don't add tests just to raise coverage, since they become a maintenance liability.

## Git

- Never commit unless I ask.
- Branch before making changes. Don't work directly on main.
- Use Conventional Commits (`feat:`, `fix:`, `chore:`, etc.) when I do ask for a commit.
