# Coding Guidelines

This document summarizes the project's coding style and quality principles. Use these guidelines for all new and updated code.

## Core principles

- Keep code simple, readable, and maintainable.
- Follow DRY (Don't Repeat Yourself): avoid duplicated logic by extracting reusable functions, utilities, or components.
- Prefer small, focused functions and modules with a single clear responsibility.
- Optimize for clarity first; only optimize for performance when there is a measured need.
- Keep behavior predictable and avoid hidden side effects.
- Leave the codebase better than you found it (small refactors are encouraged).

## Formatting best practices

- Use consistent formatting across the codebase.
- Keep line length reasonable for readability.
- Use meaningful indentation and spacing to improve scanability.
- Use clear, descriptive names for variables, functions, classes, and files.
- Keep functions short and avoid deep nesting where possible.
- Remove unused code, dead comments, and stale TODOs.
- Prefer explicitness over clever one-liners.

## Import best practices

- Group imports by type and keep ordering consistent.
- Prefer absolute or project-consistent paths over fragile relative chains.
- Import only what you use.
- Remove unused imports promptly.
- Avoid circular dependencies between modules.
- Keep module boundaries clear: shared utilities should live in shared locations.
- Prefer named exports when they improve discoverability and refactoring safety.

## Lint usage

- Linting is required and should pass before opening or merging changes.
- Use ESLint as the source of truth for style and common code-quality rules.
- Do not ignore lint rules unless there is a strong justification.
- If a lint rule must be disabled, scope the disable to the smallest possible block and document why.
- Run lint checks locally during development, not only in CI.
- Treat new warnings as issues to fix, not noise to postpone.

## General quality best practices

- Write code that is easy to test.
- Handle errors explicitly and provide useful error messages.
- Validate inputs at system boundaries (API handlers, forms, and external integrations).
- Prefer immutable patterns when practical to reduce accidental state bugs.
- Keep business logic out of UI rendering code when possible.
- Document non-obvious decisions with brief, high-value comments.
- Ensure new features include appropriate tests and do not regress existing behavior.

## Pull request expectations

- Keep pull requests focused and reasonably small.
- Include a clear summary of what changed and why.
- Ensure lint and tests pass before requesting review.
- Address review feedback with maintainability and long-term code health in mind.
