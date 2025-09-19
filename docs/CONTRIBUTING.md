# Contributing to PhamHongDuc Backend

Thank you for your interest in contributing to our NestJS backend project! This document provides guidelines for contributing to the project, with a special focus on writing clear and meaningful commit messages.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Commit Message Guidelines](#commit-message-guidelines)
- [Development Workflow](#development-workflow)
- [Testing](#testing)
- [Pull Request Process](#pull-request-process)

## Code of Conduct

This project and everyone participating in it is governed by our Code of Conduct. By participating, you are expected to uphold this code.

## Getting Started

1. Fork the repository
2. Clone your fork: `git clone https://github.com/your-username/phamhongduc_be.git`
3. Install dependencies: `pnpm install`
4. Set up your environment variables (see `.env.example`)
5. Run database migrations: `npx prisma migrate dev`
6. Start the development server: `pnpm run start:dev`

## Commit Message Guidelines

We follow the **Conventional Commits** specification to maintain clear and consistent commit messages. This helps with:

- Automatic changelog generation
- Semantic versioning
- Better code review process
- Easier debugging and issue tracking

### Commit Message Format

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Commit Types

| Type       | Description                           | Example                                      |
| ---------- | ------------------------------------- | -------------------------------------------- |
| `feat`     | A new feature                         | `feat: add user authentication endpoint`     |
| `fix`      | A bug fix                             | `fix: resolve database connection timeout`   |
| `docs`     | Documentation changes                 | `docs: update API documentation`             |
| `style`    | Code style changes (formatting, etc.) | `style: format code with prettier`           |
| `refactor` | Code refactoring                      | `refactor: extract user service logic`       |
| `test`     | Adding or updating tests              | `test: add unit tests for user controller`   |
| `chore`    | Maintenance tasks                     | `chore: update dependencies`                 |
| `perf`     | Performance improvements              | `perf: optimize database queries`            |
| `ci`       | CI/CD changes                         | `ci: add GitHub Actions workflow`            |
| `build`    | Build system changes                  | `build: update webpack configuration`        |
| `revert`   | Reverting previous commits            | `revert: revert user authentication changes` |

### Commit Message Rules

1. **Capitalization**: Use lowercase for the type and description
2. **Punctuation**: No period at the end of the description
3. **Length**: Keep the subject line under 50 characters
4. **Mood**: Use imperative mood ("add", "fix", "update", not "added", "fixed", "updated")
5. **Scope**: Optional scope in parentheses (e.g., `feat(auth): add JWT validation`)

### Good vs Bad Examples

#### ✅ Good Commit Messages

```
feat: add user registration endpoint
fix(auth): resolve JWT token validation issue
docs: update API documentation with new endpoints
refactor: extract database connection logic
test: add integration tests for user service
chore: update dependencies to latest versions
```

#### ❌ Bad Commit Messages

```
fixed bug
updated stuff
oops
I think I fixed it this time?
empty commit messages
```

### Writing Better Commit Messages

Think like a journalist! Ask yourself:

1. **What** did I change?
2. **Why** was this change needed?
3. **How** does this change work?

#### Example Transformation

Instead of:

```
git commit -m 'Add margin'
```

Use:

```
git commit -m 'style: add margin to nav items to prevent logo overlap'
```

### Commit Body

For complex changes, use the commit body to provide additional context:

```
feat: add user authentication system

- Implement JWT token generation and validation
- Add login and registration endpoints
- Include password hashing with bcrypt
- Add user role-based access control

Closes #123
```

### Breaking Changes

Use `BREAKING CHANGE:` in the commit body to indicate breaking changes:

```
feat: change user API response format

BREAKING CHANGE: User API now returns user object instead of user ID
```

## Development Workflow

1. **Create a feature branch**: `git checkout -b feature/your-feature-name`
2. **Make your changes**: Follow the coding standards
3. **Write tests**: Ensure your code is properly tested
4. **Commit your changes**: Use conventional commit format
5. **Push your branch**: `git push origin feature/your-feature-name`
6. **Create a Pull Request**: Follow the PR template

## Testing

Before submitting your changes, ensure:

- [ ] All tests pass: `pnpm run test`
- [ ] E2E tests pass: `pnpm run test:e2e`
- [ ] Code coverage is maintained: `pnpm run test:cov`
- [ ] Linting passes: `pnpm run lint`
- [ ] Code is formatted: `pnpm run format`

## Pull Request Process

1. **Title**: Use conventional commit format (e.g., "feat: add user authentication")
2. **Description**: Clearly describe what the PR does and why
3. **Related Issues**: Link any related issues using keywords (e.g., "Closes #123")
4. **Screenshots**: Include screenshots for UI changes
5. **Testing**: Describe how you tested your changes

### PR Template

```markdown
## Description

Brief description of what this PR does.

## Type of Change

- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update

## Testing

- [ ] Unit tests pass
- [ ] E2E tests pass
- [ ] Manual testing completed

## Checklist

- [ ] My code follows the style guidelines of this project
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes

## Related Issues

Closes #123
```

## Questions?

If you have questions about contributing, please:

1. Check the existing issues and discussions
2. Create a new issue with the "question" label
3. Reach out to the maintainers

Thank you for contributing to our project! 🚀
