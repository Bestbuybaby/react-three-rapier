```markdown
# react-three-rapier Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `react-three-rapier` TypeScript codebase. You'll learn about file naming, import/export styles, commit message conventions, and how to work with and write tests in this repository. This guide is designed to help contributors quickly align with the project's established practices.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `physicsEngine.ts`, `useRigidBody.ts`

### Import Style
- Use **relative imports** for modules within the repository.
  - Example:
    ```typescript
    import { useRigidBody } from './useRigidBody';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In useRigidBody.ts
    export function useRigidBody() { ... }
    ```

### Commit Messages
- Follow the **Conventional Commits** specification.
- Use prefixes like `chore` for maintenance or non-feature changes.
  - Example:
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Code Contribution
**Trigger:** When adding new features or fixing bugs  
**Command:** `/contribute`

1. Create a new branch from `main`.
2. Write your code following the coding conventions.
3. Add or update tests as needed.
4. Commit changes using a conventional commit message.
5. Push your branch and open a pull request.

### Dependency Maintenance
**Trigger:** When updating dependencies or performing maintenance  
**Command:** `/update-deps`

1. Update the necessary dependency in `package.json`.
2. Run `npm install` or `yarn install` to update lock files.
3. Commit the changes with a message like:
    ```
    chore: update [dependency] to vX.Y.Z
    ```
4. Push and create a pull request.

### Testing
**Trigger:** Before submitting a pull request or after making code changes  
**Command:** `/test`

1. Identify or create test files matching the `*.test.*` pattern.
2. Run the test suite using the project's test runner (framework unknown; try `npm test` or `yarn test`).
3. Ensure all tests pass before pushing changes.

## Testing Patterns

- Test files use the `*.test.*` naming convention, e.g., `physicsEngine.test.ts`.
- The specific testing framework is **unknown**, but standard TypeScript test runners like Jest or Vitest may be used.
- Place tests alongside the modules they test or in a dedicated `__tests__` directory.
- Example test file:
    ```typescript
    // physicsEngine.test.ts
    import { physicsEngine } from './physicsEngine';

    describe('physicsEngine', () => {
      it('should initialize correctly', () => {
        expect(physicsEngine.init()).toBeTruthy();
      });
    });
    ```

## Commands

| Command        | Purpose                                  |
|----------------|------------------------------------------|
| /contribute    | Start a new feature or bugfix workflow   |
| /update-deps   | Update dependencies and perform maintenance |
| /test          | Run the test suite                       |
```