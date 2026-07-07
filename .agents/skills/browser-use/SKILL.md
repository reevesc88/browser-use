```markdown
# browser-use Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `browser-use` TypeScript repository. It covers file organization, code style, commit practices, and testing approaches to help you contribute effectively and maintain consistency across the codebase.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example: `browser-utils.ts`, `user-session.test.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { getUserSession } from './user-session';
    ```

### Export Style
- Use **named exports** exclusively.
  - Example:
    ```typescript
    // In browser-utils.ts
    export function parseUrl(url: string): URL { ... }

    // Importing
    import { parseUrl } from './browser-utils';
    ```

### Commit Messages
- Follow the **Conventional Commits** specification.
- Use the `feat` prefix for new features.
  - Example:
    ```
    feat: add session timeout handling
    ```

## Workflows

### Adding a New Feature
**Trigger:** When implementing a new feature or module  
**Command:** `/add-feature`

1. Create a new file using kebab-case (e.g., `new-feature.ts`).
2. Use relative imports to include dependencies.
3. Export all functions or constants using named exports.
4. Write corresponding tests in a file named `new-feature.test.ts`.
5. Commit your changes using a conventional commit message with the `feat` prefix.
6. Push your branch and open a pull request.

### Writing Tests
**Trigger:** When adding or updating functionality  
**Command:** `/write-test`

1. Create a test file with the `.test.ts` suffix (e.g., `browser-utils.test.ts`).
2. Write tests for all exported functions.
3. Use the project's preferred (unknown) testing framework.
4. Run tests locally to ensure correctness.

## Testing Patterns

- Test files follow the `*.test.*` naming convention.
  - Example: `browser-utils.test.ts`
- Each test file should correspond to a source file and cover all named exports.
- The specific testing framework is not specified; refer to existing tests for structure.

## Commands
| Command        | Purpose                                      |
|----------------|----------------------------------------------|
| /add-feature   | Guide for adding a new feature or module     |
| /write-test    | Steps for writing and organizing tests       |
```
