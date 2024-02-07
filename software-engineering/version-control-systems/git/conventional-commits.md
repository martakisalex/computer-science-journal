# Conventional Commits

<img src="https://miro.medium.com/max/3386/1*1xZsQg8bbz6C5p8bUOWhwQ.png" height="100">

## Overview

Conventional Commits provide a set of rules for creating an explicit commit history, making it easier to manage versions and release notes. The structure categorizes changes to highlight new features, bug fixes, and other modifications.

## Types of Conventional Commits

### API Relevant Changes
- **`feat`**: Introduces a new feature or removes an existing feature. These changes might affect the API or the user interface.
- **`fix`**: Addresses a bug in the application, leading to a more stable version.

### Codebase Refactoring
- **`refactor`**: Involves code changes that neither fix a bug nor add a feature but improve the existing codebase. The API behavior remains unchanged.
  - **`perf`**: A subset of refactor commits aimed at enhancing performance without altering functionality.

### Code Appearance
- **`style`**: Pertains to cosmetic changes that do not influence the program's logic (e.g., formatting, missing semi-colons).

### Testing
- **`test`**: Includes modifications related to adding new tests or correcting existing ones, contributing to a more robust codebase.

### Documentation
- **`docs`**: Encompasses changes exclusively to the documentation, improving clarity or accuracy.

### Build and Operations
- **`build`**: Affects the build system or external dependencies, such as the toolchain, CI/CD pipeline, or project versioning.
- **`ops`**: Impacts operational aspects like infrastructure, deployment processes, backup, or recovery mechanisms.

### Miscellaneous
- **`chore`**: Covers other types of changes that don't fit into the above categories, such as updates to the `.gitignore` file.

## Commit Message Structure

A conventional commit message should succinctly describe the changes made, following this format:

```
<type>(<scope>): <subject>
<body>
<footer>
```

- **Type**: One of the predefined types listed above.
- **Scope** (Optional): A scope provides additional context, such as the part of the codebase affected.
- **Subject**: A brief description of the change.
- **Body** (Optional): A more detailed explanation of the changes.
- **Footer** (Optional): Additional metadata, such as related issue IDs or breaking changes.

## Example Commit

```
feat(auth): implement OAuth2 authentication flow

Introduce OAuth2 authentication flow to improve security and user experience. This includes handling tokens and session management.

Closes #142, Ref #45
```
## Resources
- [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/)
- [Conventional Commit Messages](https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13)
