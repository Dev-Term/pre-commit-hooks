# Dev terminal Pre-commit Hooks

This repository contains dev-terminal's custom pre-commit hooks.

## Available Hooks

- [Validate Eslint](#validate-eslint) - A script to validate eslint rules on Javascript and Typescript files.

___

## validate-eslint

This script runs eslint rule checks on staged files that have the following extensions:

- ts
- tsx
- vue
- js
- jsx

### Prerequisites

You need the following to be installed on your machine before running this pre-commit script.

- [ESLINT v8.11](https://www.npmjs.com/package/eslint)

### Usage

Add this to your .pre-commit-config.yaml:

```yaml
-   repo: https://github.com/Dev-Term/pre-commit-hooks
    rev: v0.2.0  # Use the ref you want to point at
    hooks:
    -   id: validate-eslint
    # -   id: ...
```

After the configuration is added, you'll need to run

```bash
pre-commit install -t pre-commit
```

___
