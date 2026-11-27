# CLAUDE.md

These rules apply to all my projects.

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
- If a paid option is much better, you can suggest it. Say clearly that it costs money. Do not add a paid service without my approval.

## Third-party libraries

Check each new dependency before you add it. Tell me what you found.

- Check for known vulnerabilities (`pnpm audit`, GitHub advisories, OSV). Run `pnpm audit` after you add or update dependencies.
- Check that it is maintained and has a clear license. Check the package name for typosquatting.
- Check postinstall scripts. Do not run unknown install scripts.
- Prefer well-known libraries. Do not add one for a task that is easy to write.
- Ask me before you install a package with an unfixed high or critical vulnerability.

## Safety

- Never read, print, or commit `.env*` files or secrets. Keep a `.env.example` with names only. Tell me if a secret appears in code or logs.
- Ask first before you delete files, run `rm -rf`, force push, run `git reset --hard`, run `prisma migrate reset` or `db push --force`, or run SQL that drops or deletes data. Never run these against a production database.

## Working style

- Plan first for non-trivial work: more than 2 files, or a new dependency. Propose an approach and wait for my approval before editing.
- Ask only when a choice is costly to undo or changes behavior. For a small, reversible choice, pick one and say so in one line.
- Keep explanations brief. Explain reasoning when it matters, skip recaps of what you just did.
- Do not edit any CLAUDE.md file unless I clearly ask for the change. If I ask a question or state a wish, answer it and offer a draft. Edit only after I say yes.

## Writing

- Use ASD-STE100 Simplified Technical English for everything written for me: explanations, code comments, commit messages, issues, and tickets.
- Short sentences, active voice, one idea per sentence, simple common words, no idioms.
- Never show me a bare code or ID. When you mention a requirement, task, option, question, or ticket by ID (for example FR-020), add a short label in the same place (for example "FR-020 (address lookup)"). Do this even if the ID appeared earlier in the conversation.
- Make each question stand on its own. I should not need to scroll up to understand it.
- When you start a subagent, tell it to write in plain short sentences, to label every ID, and to make each question stand on its own.

## Code style

- Readability for humans comes first. Code doesn't need to be optimal or use the newest language features.
- Match the existing conventions of the repo over your own preferences.
- Comments only for the non-obvious why.
- Keep diffs small. No drive-by refactors or unrelated cleanups.

## Testing

- Run relevant tests after changes, and write tests for new logic.
- Test what matters. Don't add tests just to raise coverage, since they become a maintenance liability.
- If a test fails, fix the cause. Do not skip, delete, or weaken the test.
- When you finish, say what you ran and what you did not run. Do not say "done" if checks did not pass.

## Git

- Never commit unless I ask.
- Commit, push, open a pull request, and merge are separate steps. Do each one only when I ask. A clear combined request (for example "commit and push") covers the steps it names. Never force push or merge without a separate yes.
- Branch before making changes. Don't work directly on main.
- Use Conventional Commits (`feat:`, `fix:`, `chore:`, etc.) when I do ask for a commit.
- Make atomic commits. One logical change per commit. Each commit builds and passes tests on its own.
- Commit messages tell why, not only how. Use a clear subject line. Add a short body only when the why is not obvious.
