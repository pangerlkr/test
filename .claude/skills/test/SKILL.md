```markdown
# test Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `test` TypeScript repository. It covers file organization, import/export styles, commit message habits, and testing patterns. The guide is designed to help contributors quickly align with the project's established practices.

## Coding Conventions

### File Naming
- **PascalCase** is used for file names.
  - **Example:**  
    ```
    MyComponent.ts
    UserService.ts
    ```

### Import Style
- **Relative imports** are preferred.
  - **Example:**  
    ```typescript
    import { UserService } from './UserService';
    import { MyComponent } from '../components/MyComponent';
    ```

### Export Style
- **Named exports** are used instead of default exports.
  - **Example:**  
    ```typescript
    // In UserService.ts
    export function getUser() { ... }
    export const USER_ROLE = 'admin';

    // Importing
    import { getUser, USER_ROLE } from './UserService';
    ```

### Commit Patterns
- **Freeform commit messages** with no strict prefixes.
- **Average commit message length:** 47 characters.

  - **Example:**  
    ```
    Fix bug in user authentication flow
    Add logging to payment processing
    ```

## Workflows

### Adding a New Module
**Trigger:** When you need to add a new feature or module  
**Command:** `/add-module`

1. Create a new file using PascalCase (e.g., `NewFeature.ts`).
2. Use named exports for all functions, classes, or constants.
3. Import dependencies using relative paths.
4. Write corresponding tests in a file named `NewFeature.test.ts`.
5. Commit changes with a clear, concise message.

### Writing Tests
**Trigger:** When you need to add or update tests  
**Command:** `/write-test`

1. Create or update a test file matching `*.test.*` (e.g., `UserService.test.ts`).
2. Follow the same import/export conventions as production code.
3. Use the project's preferred (unknown) testing framework.
4. Run tests to ensure they pass before committing.

### Refactoring Code
**Trigger:** When improving or reorganizing existing code  
**Command:** `/refactor`

1. Rename files using PascalCase if needed.
2. Update all relative imports to match new file names/locations.
3. Ensure all exports remain named.
4. Update or add tests as necessary.
5. Commit with a descriptive message about the refactor.

## Testing Patterns

- **Test files** use the pattern `*.test.*` (e.g., `UserService.test.ts`).
- The specific testing framework is not detected; follow existing test file patterns.
- Tests should use the same import/export conventions as the main codebase.

  - **Example:**  
    ```typescript
    import { getUser } from './UserService';

    describe('getUser', () => {
      it('should return a user object', () => {
        // test implementation
      });
    });
    ```

## Commands
| Command      | Purpose                                 |
|--------------|-----------------------------------------|
| /add-module  | Guide for adding a new module/feature   |
| /write-test  | Steps for writing or updating tests      |
| /refactor    | Instructions for refactoring code        |
```