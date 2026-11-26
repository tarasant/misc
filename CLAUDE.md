# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## About me

I work mostly on web frontends and backend APIs.

## Preferred stack

These are defaults. A project can override them. Do not pin versions here.

- React with Next.js (App Router).
- TypeScript for frontend and backend. Python for scripting.
- pnpm as the package manager.
- Tailwind CSS with shadcn/ui.
- PostgreSQL with Prisma. Neon for hosted databases.
- Zod for validation. React Hook Form for forms.
- Self-hosted auth library (for example Better Auth) over a hosted auth service.
- Vitest for unit tests. Playwright for end-to-end tests.
- Vercel for hosting.
- Docker (Compose) is an option for local services such as Postgres. It is not required. Run the app itself directly with `pnpm dev`.

## Cost

My projects are hobby projects. Use free services and third parties when possible.

- Only suggest services that are verified and trusted. Check that the free tier exists and is still current.
- If a paid option is much better, you can suggest it. Always say clearly that it costs money.
- Do not add a paid service without my approval.

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
- Make atomic commits. One logical change per commit. Each commit builds and passes tests on its own.
- Commit messages tell the story of why, not only how. The diff shows how. The message explains the reason for the change, the problem it solves, and any choice that was not obvious. Keep messages short: a clear subject line, and a few lines of body only when the why is not obvious from the subject.
