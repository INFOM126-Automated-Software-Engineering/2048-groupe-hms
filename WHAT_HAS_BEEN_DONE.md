# What has been done in this project?

This document highlights the key features and implementations completed in te 2048-groupe-hms project. It serves as a summary of the work accomplished to enhance the project with CI/CD practices and DevOps principles.

## Key Implementations

### 1. Branch protection and PR requirements

- The `main` branch is protected to ensure that all changes go through a pull request (PR) process.
- PRs must pass all checks before they can be merged, ensuring code quality and stability.

This changes have been done by configuring a ruleset in the repository settings. The ruleset, named "Protect main branch", enforces the following:
- No Bypass
- All branches are targeted
- Require PR before merging, with required reviews set to 1 (as there is only 4 contributors in total)
- Require status checks to pass -> specific checks to add later
- Block force pushes
- Require code scanning results with CodeQL
- Automatically request Copilot code review
- Manage static analysis tools in Copilot code review with ESLint 

### 2. CI Pipeline on PRs

Idée pour pipeline : ne pas la déclencer lors de modifications de ce fichier. (ou autre markdown)

### 3. Dependabot Integration

### 4. Contribution Guidelines