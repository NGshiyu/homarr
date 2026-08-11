```markdown
# homarr Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides a comprehensive guide to the development patterns used in the `homarr` TypeScript codebase. It covers coding conventions, commit patterns, testing approaches, and suggested commands for common workflows. Whether you're contributing code, reviewing pull requests, or writing tests, this document will help you align with the project's established practices.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `dashboardWidget.ts`

### Imports
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { getUser } from './userService';
    ```

### Exports
- **Mixed export style**: Both named and default exports are used.
  - Named export example:
    ```typescript
    export function fetchData() { /* ... */ }
    ```
  - Default export example:
    ```typescript
    export default App;
    ```

### Commit Messages
- Use **conventional commit** format.
- Prefix with the type, such as `fix`.
- Keep commit messages concise (average 74 characters).
  - Example:  
    ```
    fix: resolve issue with user authentication flow
    ```

## Workflows

### Code Contribution
**Trigger:** When adding new features or fixing bugs  
**Command:** `/contribute`

1. Create a new branch from `main`.
2. Implement your changes following the coding conventions.
3. Write or update tests as needed.
4. Commit changes using the conventional commit format (e.g., `fix: ...`).
5. Push your branch and open a pull request.

### Testing
**Trigger:** When verifying code functionality  
**Command:** `/test`

1. Identify or create test files matching the `*.test.*` pattern.
2. Write tests for new or updated code.
3. Run the test suite using the project's test runner (framework unknown; refer to project scripts).
4. Ensure all tests pass before submitting changes.

### Code Review
**Trigger:** When reviewing a pull request  
**Command:** `/review`

1. Check that file naming, imports, and exports follow the documented conventions.
2. Ensure commit messages use the conventional format.
3. Verify that tests are present and passing.
4. Leave feedback or approve the pull request.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern (e.g., `userService.test.ts`).
- The testing framework is not specified; check the project documentation or scripts for details.
- Place tests alongside the code or in a dedicated `tests` directory as per project structure.

**Example test file:**
```typescript
// userService.test.ts
import { getUser } from './userService';

test('should fetch user by ID', () => {
  const user = getUser(1);
  expect(user.id).toBe(1);
});
```

## Commands
| Command      | Purpose                                   |
|--------------|-------------------------------------------|
| /contribute  | Start the code contribution workflow      |
| /test        | Run or write tests for the codebase       |
| /review      | Perform a code review on a pull request   |
```