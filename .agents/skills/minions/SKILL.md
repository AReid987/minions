```markdown
# minions Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `minions` TypeScript repository. You'll learn how to structure files, write imports/exports, follow commit message standards, and organize tests. These patterns ensure consistency and maintainability across the codebase.

## Coding Conventions

### File Naming
- All files use **kebab-case**.
  - Example: `my-module.ts`, `user-service.test.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { doSomething } from './utils/do-something';
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```typescript
    // good
    export function fetchData() { ... }

    // bad
    export default function fetchData() { ... }
    ```

### Commit Messages
- Follow the **Conventional Commits** format.
- Most commits use the `chore` prefix.
  - Example:
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Code Contribution
**Trigger:** When adding or updating code in the repository  
**Command:** `/contribute`

1. Create or update files using kebab-case naming.
2. Use relative imports and named exports in all TypeScript files.
3. Write or update tests in files matching `*.test.*`.
4. Commit changes using the conventional commit format (e.g., `chore: ...`).
5. Open a pull request for review.

### Testing
**Trigger:** When verifying code changes  
**Command:** `/test`

1. Locate or create test files following the `*.test.*` naming pattern.
2. Write tests for new or modified code.
3. Run the test suite using the project's test runner (framework not specified; check project scripts).
4. Ensure all tests pass before merging changes.

## Testing Patterns

- Test files follow the `*.test.*` naming convention (e.g., `utils.test.ts`).
- The specific testing framework is not detected; refer to project documentation or scripts for details.
- Example test file structure:
  ```typescript
  import { myFunction } from './my-function';

  describe('myFunction', () => {
    it('should return true', () => {
      expect(myFunction()).toBe(true);
    });
  });
  ```

## Commands
| Command      | Purpose                                 |
|--------------|-----------------------------------------|
| /contribute  | Start the code contribution workflow    |
| /test        | Run the testing workflow                |
```
