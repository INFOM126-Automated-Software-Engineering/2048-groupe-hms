
# Pull Request Template - Project 2048 

This document describes the rules and best practices to follow when contributing to the 2048 project via Pull Requests.
All contributions must go through a Pull Request in order to ensure code quality and project stability.

---

## General rules for contributing to the project 

- **Do not push directly to `main`**. All changes or contributions must go through a Pull Request.

- **Each feature must be developed in a dedicated branch**.
    - `ci/check_path_ignore`
    - `dependabot/maven/org.pitest-pitest-maven-1.22.0`

- ** One Pull Request per objective

- ** Respect the existing code style** and ensure that Maven accepts it.

- Use **Draft Pull Requests** if the work is not complete but you want to launch CI or request early feedback.

- A Pull Request must be reviewed and approved before being merged.


---

## Submit a Pull Request

1. Create a branch from `main`.
2. Implement the desired feature or fix.
3. Ensure that:
   - the project compiles correctly and passes the tests
   - the code is formatted correctly
4. Write a well-explained Pull Request
5. Wait for review and apply the requested changes.


---

## Rules for code review

- Pull requests must be approved by **at least one reviewer**.
- Comments must be taken into account, responded to, or justified.
- In case of Git conflict: **resolve by merging**
- Avoid rebasing your changes. If you are asked to make changes during the review process, make them as a new commit.
- If you are asked to make changes during the review process, make them as a new commit.


---

## Conditions for merging a Pull Request:

A Pull Request can only be merged if:

- It has at least **one approval** from a reviewer
- All CI checks are successful
- All conflicts are resolved
- The Pull Request description is clear  

---

Please respect these rules to ensure the quality of the 2048 project and facilitate collaboration between group members.