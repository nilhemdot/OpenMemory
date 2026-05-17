```markdown
# OpenMemory Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the OpenMemory TypeScript codebase. You'll learn how to structure files, write imports/exports, follow commit message standards, and manage testing. These patterns ensure consistency and maintainability in projects without a specific framework.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example: `user-profile.ts`, `memory-store.test.ts`

### Import Style
- Use **relative imports** for referencing other modules.
  - Example:
    ```typescript
    import { fetchData } from './utils';
    ```

### Export Style
- Use **named exports** instead of default exports.
  - Example:
    ```typescript
    // In memory-store.ts
    export function saveMemory(data: Memory) { ... }
    export const MEMORY_LIMIT = 1000;
    ```

### Commit Messages
- Follow **conventional commit** format.
- Use `chore` as the prefix for routine changes.
- Keep commit messages concise (average 77 characters).
  - Example:
    ```
    chore: update dependencies and fix minor lint issues
    ```

## Workflows

### Code Update
**Trigger:** When making any code changes or improvements  
**Command:** `/code-update`

1. Make changes in TypeScript files using kebab-case naming.
2. Use relative imports and named exports.
3. Write a commit message using the conventional format with the `chore` prefix.
4. Push your changes to the repository.

### Testing
**Trigger:** When adding or updating features, or fixing bugs  
**Command:** `/run-tests`

1. Create or update test files matching the `*.test.*` pattern.
2. Write tests in TypeScript.
3. Run the tests using your preferred test runner (framework not specified).
4. Ensure all tests pass before committing.

## Testing Patterns

- Test files are named using the `*.test.*` pattern (e.g., `memory-store.test.ts`).
- Tests are written in TypeScript.
- Testing framework is not specified; use your team's preferred runner.
- Place tests alongside or near the code they test for clarity.

  Example:
  ```typescript
  // memory-store.test.ts
  import { saveMemory } from './memory-store';

  describe('saveMemory', () => {
    it('should save data correctly', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command        | Purpose                                      |
|----------------|----------------------------------------------|
| /code-update   | Apply code changes following conventions     |
| /run-tests     | Run all tests matching the `*.test.*` pattern|
```
