---
name: everything-claude-code-conventions
description: Development conventions and patterns for everything-claude-code. JavaScript project with conventional commits.
---

# Everything Claude Code Conventions

> Generated from [Gusty1/everything-claude-code](https://github.com/Gusty1/everything-claude-code) on 2026-03-22

## Overview

This skill teaches Claude the development patterns and conventions used in everything-claude-code.

## Tech Stack

- **Primary Language**: JavaScript
- **Architecture**: hybrid module organization
- **Test Location**: separate

## When to Use This Skill

Activate this skill when:
- Making changes to this repository
- Adding new features following established patterns
- Writing tests that match project conventions
- Creating commits with proper message format

## Commit Conventions

Follow these commit message conventions based on 200 analyzed commits.

### Commit Style: Conventional Commits

### Prefixes Used

- `fix`
- `feat`
- `docs`

### Message Guidelines

- Average message length: ~55 characters
- Keep first line concise and descriptive
- Use imperative mood ("Add feature" not "Added feature")


*Commit message example*

```text
docs: restore zenith.chat and @DRodriguezFX in Background (own project)
```

*Commit message example*

```text
security: remove supply chain risks, external promotions, and unauthorized credits
```

*Commit message example*

```text
fix(zh-CN): update image path
```

*Commit message example*

```text
feat(agents): add flutter-reviewer agent and skill (#716)
```

*Commit message example*

```text
chore(deps-dev): bump flatted (#675)
```

*Commit message example*

```text
Merge pull request #736 from pvgomes/docs/add-brazilian-portuguese-translation
```

*Commit message example*

```text
Update docs/pt-BR/commands/eval.md
```

*Commit message example*

```text
Update docs/pt-BR/commands/plan.md
```

## Architecture

### Project Structure: Single Package

This project uses **hybrid** module organization.

### Configuration Files

- `.github/workflows/ci.yml`
- `.github/workflows/maintenance.yml`
- `.github/workflows/monthly-metrics.yml`
- `.github/workflows/release.yml`
- `.github/workflows/reusable-release.yml`
- `.github/workflows/reusable-test.yml`
- `.github/workflows/reusable-validate.yml`
- `.opencode/package.json`
- `.opencode/tsconfig.json`
- `.prettierrc`
- `eslint.config.js`
- `package.json`

### Guidelines

- This project uses a hybrid organization
- Follow existing patterns when adding new code

## Code Style

### Language: JavaScript

### Naming Conventions

| Element | Convention |
|---------|------------|
| Files | camelCase |
| Functions | camelCase |
| Classes | PascalCase |
| Constants | SCREAMING_SNAKE_CASE |

### Import Style: Relative Imports

### Export Style: Mixed Style


*Preferred import style*

```typescript
// Use relative imports
import { Button } from '../components/Button'
import { useAuth } from './hooks/useAuth'
```

## Testing

### Test Framework

No specific test framework detected — use the repository's existing test patterns.

### File Pattern: `*.test.js`

### Test Types

- **Unit tests**: Test individual functions and components in isolation
- **Integration tests**: Test interactions between multiple components/services

### Coverage

This project has coverage reporting configured. Aim for 80%+ coverage.


## Error Handling

### Error Handling Style: Try-Catch Blocks


*Standard error handling pattern*

```typescript
try {
  const result = await riskyOperation()
  return result
} catch (error) {
  console.error('Operation failed:', error)
  throw new Error('User-friendly message')
}
```

## Common Workflows

These workflows were detected from analyzing commit patterns.

### Database Migration

Database schema changes with migration files

**Frequency**: ~2 times per month

**Steps**:
1. Create migration file
2. Update schema definitions
3. Generate/update types

**Files typically involved**:
- `migrations/*`

**Example commit sequence**:
```
Add Kiro IDE support (.kiro/) (#548)
Revert "Add Kiro IDE support (.kiro/) (#548)"
fix: resolve ESLint errors and add npx command support in hook tests
```

### Feature Development

Standard feature implementation workflow

**Frequency**: ~14 times per month

**Steps**:
1. Add feature implementation
2. Add tests for feature
3. Update documentation

**Files typically involved**:
- `**/*.test.*`
- `**/api/**`

**Example commit sequence**:
```
fix: strip ANSI escape codes from session persistence hooks (#642) (#684)
feat: agent compression, inspection logic, governance hooks (#491, #485, #482) (#688)
fix: auto-detect ECC root from plugin cache when CLAUDE_PLUGIN_ROOT is unset (#547) (#691)
```

### Add New Language Translation

Adds a new language translation for documentation, including agents, commands, rules, examples, and core docs.

**Frequency**: ~1 times per month

**Steps**:
1. Create new language directory under docs/ (e.g., docs/pt-BR/ or docs/zh-CN/).
2. Add translated versions of core docs (README.md, CONTRIBUTING.md, TERMINOLOGY.md, etc.).
3. Add translated agents documentation (docs/<lang>/agents/*.md).
4. Add translated commands documentation (docs/<lang>/commands/*.md).
5. Add translated rules documentation (docs/<lang>/rules/**/*.md).
6. Add translated examples (docs/<lang>/examples/*.md).
7. Add translated skills documentation if applicable (docs/<lang>/skills/*/SKILL.md).
8. Update main README.md to link to the new language.

**Files typically involved**:
- `docs/<lang>/README.md`
- `docs/<lang>/CONTRIBUTING.md`
- `docs/<lang>/TERMINOLOGY.md`
- `docs/<lang>/agents/*.md`
- `docs/<lang>/commands/*.md`
- `docs/<lang>/rules/**/*.md`
- `docs/<lang>/examples/*.md`
- `docs/<lang>/skills/*/SKILL.md`
- `README.md`

**Example commit sequence**:
```
Create new language directory under docs/ (e.g., docs/pt-BR/ or docs/zh-CN/).
Add translated versions of core docs (README.md, CONTRIBUTING.md, TERMINOLOGY.md, etc.).
Add translated agents documentation (docs/<lang>/agents/*.md).
Add translated commands documentation (docs/<lang>/commands/*.md).
Add translated rules documentation (docs/<lang>/rules/**/*.md).
Add translated examples (docs/<lang>/examples/*.md).
Add translated skills documentation if applicable (docs/<lang>/skills/*/SKILL.md).
Update main README.md to link to the new language.
```

### Add New Skill Or Agent

Adds a new agent or skill to the project, including documentation and catalog updates.

**Frequency**: ~2 times per month

**Steps**:
1. Create new skill directory under skills/ (skills/<skill-name>/SKILL.md).
2. If agent, add agent documentation under agents/ (agents/<agent-name>.md).
3. Update AGENTS.md and/or README.md to increment agent/skill counts and add references.
4. If needed, add command documentation (commands/<command-name>.md).
5. If needed, add scripts or tests related to the new skill/agent.

**Files typically involved**:
- `skills/<skill-name>/SKILL.md`
- `agents/<agent-name>.md`
- `AGENTS.md`
- `README.md`
- `commands/<command-name>.md`

**Example commit sequence**:
```
Create new skill directory under skills/ (skills/<skill-name>/SKILL.md).
If agent, add agent documentation under agents/ (agents/<agent-name>.md).
Update AGENTS.md and/or README.md to increment agent/skill counts and add references.
If needed, add command documentation (commands/<command-name>.md).
If needed, add scripts or tests related to the new skill/agent.
```

### Update Or Sync Language Docs

Keeps translated documentation up to date with upstream changes or fixes specific translation files.

**Frequency**: ~3 times per month

**Steps**:
1. Edit one or more files under docs/<lang>/ to update content, fix errors, or sync with upstream.
2. If syncing, update a large batch of files in docs/<lang>/ (agents, commands, rules, skills, etc.).
3. If fixing, update a single or a few files in docs/<lang>/.

**Files typically involved**:
- `docs/<lang>/**/*.md`

**Example commit sequence**:
```
Edit one or more files under docs/<lang>/ to update content, fix errors, or sync with upstream.
If syncing, update a large batch of files in docs/<lang>/ (agents, commands, rules, skills, etc.).
If fixing, update a single or a few files in docs/<lang>/.
```

### Add Or Update Security Guides

Publishes or updates security-related documentation and assets, including images and README references.

**Frequency**: ~1 times per month

**Steps**:
1. Add or update the-security-guide.md or SECURITY.md.
2. Add or update images under assets/images/security/.
3. Update README.md to reference new/updated security guides.
4. Remove or update references to deprecated guides or credits.

**Files typically involved**:
- `the-security-guide.md`
- `SECURITY.md`
- `assets/images/security/*.png`
- `assets/images/security/*.jpeg`
- `README.md`

**Example commit sequence**:
```
Add or update the-security-guide.md or SECURITY.md.
Add or update images under assets/images/security/.
Update README.md to reference new/updated security guides.
Remove or update references to deprecated guides or credits.
```

### Fix Or Update Tests For Ci Or Platform

Fixes or updates test files to resolve CI failures, platform-specific issues, or improve test coverage.

**Frequency**: ~3 times per month

**Steps**:
1. Edit test files under tests/ (e.g., hooks, integration, lib, ci).
2. Update or add platform guards (e.g., skip on Windows).
3. Fix or update test assertions and metadata.
4. Sometimes update related scripts or documentation.

**Files typically involved**:
- `tests/**/*.test.js`
- `tests/**/*.test.ts`
- `tests/**/*.js`
- `tests/**/*.ts`

**Example commit sequence**:
```
Edit test files under tests/ (e.g., hooks, integration, lib, ci).
Update or add platform guards (e.g., skip on Windows).
Fix or update test assertions and metadata.
Sometimes update related scripts or documentation.
```


## Best Practices

Based on analysis of the codebase, follow these practices:

### Do

- Use conventional commit format (feat:, fix:, etc.)
- Follow *.test.js naming pattern
- Use camelCase for file names
- Prefer mixed exports

### Don't

- Don't write vague commit messages
- Don't skip tests for new features
- Don't deviate from established patterns without discussion

---

*This skill was auto-generated by [ECC Tools](https://ecc.tools). Review and customize as needed for your team.*
