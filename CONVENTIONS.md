# Coding Conventions

<!-- Aider reads this file before every session via .aider.conf.yml -->

## General
- Follow existing code style — match the surrounding code
- Prefer explicit variable names over short ones
- No magic numbers — use named constants
- Delete dead code instead of commenting it out

## TypeScript / JavaScript
- `const` over `let`, never `var`
- Async/await over `.then()` chains
- No `any` types without a comment explaining why

## Testing
- Every bug fix needs a test that would have caught it
- Test behavior, not implementation details
- Unit tests next to source: `foo.ts` → `foo.test.ts`

## Git
- Commit messages: imperative mood, one sentence
- One logical change per commit
