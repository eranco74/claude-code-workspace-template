# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Context

<!-- What language(s), frameworks, and tools does this project use? -->
<!-- Example: Primary languages: Go, TypeScript. Primary tools: kubectl, docker, npm. -->

## Project Overview

<!-- What does this project do? What problem does it solve? -->
<!-- Example: A REST API for managing widget inventories, built with Express and PostgreSQL. -->

### Repository Structure

<!-- Describe the high-level directory layout -->
<!-- Example:
- **src/**: Application source code
- **tests/**: Test suites
- **docs/**: Documentation
- **scripts/**: Build and deployment scripts
-->

## Development Commands

<!-- List the commands Claude should know about -->
<!-- Example:
```bash
# Build
npm run build

# Run tests
npm test

# Run a single test file
npm test -- --grep "widget creation"

# Lint
npm run lint

# Start development server
npm run dev
```
-->

## Architecture Patterns

<!-- Describe key patterns and conventions in your codebase -->
<!-- Example:
### API Design
- RESTful endpoints under /api/v1/
- Request validation with Zod schemas
- Error responses follow RFC 7807 (Problem Details)

### Database
- Migrations in src/db/migrations/
- Repository pattern for data access
- All queries use parameterized statements
-->

## Common Pitfalls

<!-- What mistakes should Claude avoid? -->
<!-- Example:
- Always run migrations before testing: `npm run db:migrate`
- The `config/` directory is generated -- don't edit it directly
- Tests require a running PostgreSQL instance (see docker-compose.yml)
-->

## Git & PR Workflow

<!-- How should Claude handle git operations? -->
<!-- Example:
- Commit messages use Conventional Commits format (feat:, fix:, chore:)
- PRs target the `main` branch
- Always run `npm test` before committing
-->

## GSD Workflow Integration

This project uses the GSD (Get Stuff Done) workflow system:

- **Planning**: `.planning/PROJECT.md` tracks project state, milestones, and requirements
- **Phases**: `.planning/phases/<phase-number>-<name>/` contains phase plans and summaries
- **Verification**: Each phase has a VERIFICATION.md documenting completion
- **State**: `.planning/STATE.md` tracks performance metrics and trends

When working on this project:
- Check `.planning/PROJECT.md` for current milestone and requirements
- Use `/gsd:progress` to check project status
- Use `/gsd:plan-phase` when planning new work
- Use `/gsd:execute-phase` to implement planned phases
