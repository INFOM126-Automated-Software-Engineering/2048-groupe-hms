# Contributing to 2048 Game Project

Thank you for your interest in contributing to the 2048 game project! This document provides guidelines and best practices to ensure smooth collaboration and maintain code quality.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Branching Strategy](#branching-strategy)
- [Pull Request Process](#pull-request-process)
- [Code Quality Standards](#code-quality-standards)
- [Testing Requirements](#testing-requirements)
- [Security Guidelines](#security-guidelines)

## Code of Conduct

- Be respectful and constructive in all communications
- Welcome newcomers and help them get started
- Focus on what is best for the project and the community

## Getting Started

### Prerequisites

- Java Development Kit (JDK) 11 or higher
- Maven 3.6+
- Git

### Setting Up Your Development Environment

1. **Fork the repository** (if you're an external contributor)

2. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/2048-groupe-hms.git
   cd 2048-groupe-hms
   ```

3. **Build the project:**
   ```bash
   mvn clean package
   ```

4. **Run tests to ensure everything works:**
   ```bash
   mvn test
   ```

## Development Workflow

### General Rules

- **Never push directly to `main`** - All changes must go through a Pull Request
- **Create a new branch for each feature or fix** - Keep your work organized and isolated
- **One Pull Request per objective** - Don't mix multiple unrelated changes
- **Keep commits atomic** - Each commit should represent one logical change
- **Write meaningful commit messages** - Clearly describe what and why

### Branch Naming Conventions

Use descriptive branch names that follow these patterns:

- **Features:** `feature/description-of-feature`
- **Bug fixes:** `fix/description-of-bug`
- **Documentation:** `docs/description-of-change`
- **CI/CD:** `ci/description-of-change`
- **Dependencies:** `dependabot/package-name-version`

**Examples:**
- `feature/add-undo-functionality`
- `fix/tile-merge-animation`
- `docs/update-readme`
- `ci/add-code-coverage`

## Branching Strategy

1. **Create a branch from `main`:**
   ```bash
   git checkout main
   git pull origin main
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes and commit:**
   ```bash
   git add .
   git commit -m "Add meaningful commit message"
   ```

3. **Push your branch:**
   ```bash
   git push origin feature/your-feature-name
   ```

4. **Create a Pull Request** on GitHub

## Pull Request Process

### Before Submitting a Pull Request

Ensure your code meets these requirements:

- Code compiles successfully: `mvn package`
- All tests pass: `mvn test`
- Code follows the existing style and conventions
- No new warnings or errors introduced
- Documentation updated if needed

### Creating a Pull Request

1. **Use the Pull Request template** - It will guide you through the required information
2. **Write a clear title** - Summarize the change in one line
3. **Provide a detailed description:**
   - What changes were made
   - Why these changes are necessary
   - How to test the changes
   - Any breaking changes or dependencies

4. **Use Draft PRs** if your work is incomplete but you want:
   - Early feedback
   - To trigger CI checks
   - To share progress with the team

### Code Review Process

- **All Pull Requests require at least one approval** from a reviewer
- **Address review comments** - Respond to or justify each comment
- **Make requested changes** as new commits (avoid force-pushing during review)
- **Resolve conflicts** - Rebase your branch onto the latest main branch and resolve conflicts before merging
- **Be patient and respectful** - Reviews help improve code quality

### Merging Requirements

A Pull Request can only be merged when:

- At least **one approval** from a reviewer
- All **CI checks pass** (build, tests, security scans)
- All **merge conflicts resolved**
- **Clear description** provided
- No outstanding **unresolved comments**

## Code Quality Standards

### Code Style

- Follow existing code conventions and formatting
- Use meaningful variable and method names
- Add comments for complex logic
- Keep methods short and focused on a single responsibility
- Avoid code duplication - follow DRY (Don't Repeat Yourself)

### Documentation

- Update README.md if you add new features
- Document public APIs and complex algorithms
- Add JavaDoc comments for public classes and methods
- Keep documentation up-to-date with code changes

## Testing Requirements

### Writing Tests

- **Write tests for new features** - All new functionality should have tests
- **Update tests when modifying code** - Ensure existing tests still pass
- **Aim for good coverage** - Test both success and failure scenarios
- **Use meaningful test names** - Clearly describe what is being tested

### Running Tests

```bash
# Run all tests
mvn test

# Run with coverage report
mvn clean test jacoco:report
```

### Before Submitting

Always run `mvn test` before creating a Pull Request to ensure all tests pass.

## Security Guidelines

### Protecting Sensitive Information

- **Never commit secrets** - No passwords, API keys, or tokens
- **Review dependencies** - Keep them updated and secure

### Security Tools

- **Dependabot** - Automatically monitors and updates dependencies
- **CodeQL** - Scans for security vulnerabilities
- **Keep these tools enabled** - They protect the project

If you discover a security vulnerability, please report it privately to the maintainers.

## Issue Tracking

### Reporting Bugs

Use the [Bug Report template](.github/ISSUE_TEMPLATE/bug_report.md) to report bugs. Include:
- Clear description of the problem
- Steps to reproduce
- Expected vs actual behavior
- Environment details (OS, Java version, etc.)

### Suggesting Features

Use the [Feature Request template](.github/ISSUE_TEMPLATE/feature_request.md) to suggest new features. Explain:
- The feature you want to add
- Why it's beneficial
- How it should work
- Any alternatives considered

## Questions or Need Help?

- Check existing issues and pull requests
- Review project documentation
- Ask questions in issue comments
- Reach out to maintainers if needed

---

Thank you for contributing to the 2048 game project!
