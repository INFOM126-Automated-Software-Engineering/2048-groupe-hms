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

A simple CI pipeline has been set up to run on every pull request and push to the `main` branch. In addition, a manual trigger has been added to allow on-demand execution of the pipeline.

The pipeline includes the following steps:
1. A linting step to ensure code quality and adherence to coding standards.
   1. Checkout the code from the repository. This step uses the `actions/checkout@v3` action to clone the repository.
   2. Set up Maven environment using `actions/setup-java@v3` action with Java 11 and activate the cache for Maven dependencies.
   3. Lint the code using Maven Formatter plugin to ensure code style consistency.
2. A build step to compile the code
   1. Checkout the code from the repository.
   2. Set up Maven environment using `actions/setup-java@v3` action with Java 11 and activate the cache for Maven dependencies.
   3. Build the project using Maven to ensure that the code compiles successfully. This step uses the `mvn package -DskipTests` command to compile the code without running tests.
3. A test step to run unit tests and ensure code functionality.
    1. Checkout the code from the repository.
    2. Set up Maven environment using `actions/setup-java@v3` action with Java 11 and activate the cache for Maven dependencies.
    3. Run unit tests using Maven to verify that the code behaves as expected. This step uses the `mvn test` command to execute the tests.

Future improvements:
- Avoid to run the pipeline if only documentation files are changed.
- Integrate code coverage report generation
- Integrate code scanning with CodeQL
- Integrate SonarCloud analysis
- Integrate deployment step to a staging environment (via GitHub Pages or docker container deployment - if time permits)

### 3. Dependabot Integration

### 4. Contribution Guidelines

Some files have already been created to guide contributors, but are still to be completed:
- pull_request_template.md
- the folder for the issue templates (in `.github/ISSUE_TEMPLATE`)