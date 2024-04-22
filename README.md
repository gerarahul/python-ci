
# Python Code Quality and Security Setup

This guide provides instructions on setting up your Python repository to improve code quality and security using various tools integrated via pre-commit hooks.

## Setup Instructions

### 1. Pyproject.toml

First, create a `pyproject.toml` file in the root directory of your repository. This file will be used to configure various Python tools. You can find a reference implementation of this file in this repository.

Reference: [pyproject.toml](link-to-pyproject.toml-in-your-repo)

### 2. GitHub Actions Workflow

Create a directory `.github/workflows/` in your repository and add a CI workflow file `ci.yml`. You can copy the workflow file from this repository to set up automated checks that run on GitHub Actions.

Reference: [ci.yml](link-to-ci.yml-in-your-repo)

## Tool Descriptions

### Installed Tools

- **isort**: Automatically sorts and organizes Python imports in a consistent manner across your project.
- **black**: An uncompromising code formatter that adheres to a strict style guide to ensure code consistency.
- **flake8**: A tool that checks the style and quality of Python code to catch programming errors and potentially confusing or problematic code.
- **autoflake**: Removes unused imports and unused variables from Python code.
- **pyproject-autoflake**: A wrapper for autoflake that allows configuration via `pyproject.toml`.
- **bandit**: A tool that scans Python code for security issues.
- **pre-commit**: Manages and maintains pre-commit hooks that run tools like linters and formatters before each commit to ensure code quality and style consistency.

### Setting Up Pre-commit Hooks

Run the following command in the root path of your repository to install pre-commit hooks:

```bash
pre-commit install
```

### Running Pre-commit Hooks Without Committing

To run all configured pre-commit hooks on your repository without making a commit:

```bash
pre-commit run --all
```

This command is useful for testing or enforcing project-wide code standards even before attempting to commit changes to your version control system.

## Conclusion

Following this setup helps maintain high standards of code quality and security across your Python projects. By integrating these tools into your development process, especially with automated workflows like GitHub Actions, you ensure consistent adherence to best practices.

