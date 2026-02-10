# CLAUDE.md

## Project Overview

**ClaudeTest** is a Python research repository for experimentation, prototyping, and analysis. It serves as a workspace for research-oriented Python code.

## Repository Structure

```
ClaudeTest/
├── CLAUDE.md      # AI assistant guidance (this file)
└── README.md      # Project description
```

## Tech Stack

- **Language:** Python
- **Purpose:** Research — experiments, data analysis, prototyping

## Current State

The repository is in early setup. No Python code, dependencies, or tooling have been added yet.

## Development Workflow

### Git

- **Remote:** `origin` hosted on GitHub (`92dl92/ClaudeTest`)
- **Default branch:** `main`
- Commits are signed with SSH keys
- Use clear, descriptive commit messages

### Python Environment

When adding Python code, follow these conventions:

- **Dependency management:** Use `requirements.txt` for pinned dependencies (or `pyproject.toml` if packaging is needed)
- **Virtual environments:** Use `venv` or `conda` for isolation
- **Python version:** Target Python 3.10+ unless otherwise specified

### Testing

- Use `pytest` as the test framework
- Place tests in a `tests/` directory mirroring the source structure
- Run tests with: `pytest`

### Linting & Formatting

- Use `ruff` for linting and formatting (combines flake8 + isort + black functionality)
- Run with: `ruff check .` and `ruff format .`

### Recommended Project Layout

As the repository grows, prefer this structure:

```
ClaudeTest/
├── CLAUDE.md
├── README.md
├── requirements.txt
├── src/               # Source modules
│   └── __init__.py
├── notebooks/         # Jupyter notebooks for exploration
├── tests/             # Unit tests
│   └── __init__.py
├── data/              # Data files (gitignored if large)
└── scripts/           # Standalone scripts and entrypoints
```

## Code Quality Standards

### Type Annotations (Required)

All Python code **must** include complete type annotations:

- Annotate all function parameters and return types
- Annotate class attributes and instance variables
- Use `typing` module types where needed (`list[str]`, `dict[str, int]`, `Optional[T]`, `Union[A, B]`, etc.)
- Use modern annotation syntax (Python 3.10+ style: `X | None` instead of `Optional[X]`)
- For complex types, define `TypeAlias` or use `TypeVar` as appropriate

```python
# Good
def load_data(path: str, columns: list[str] | None = None) -> pd.DataFrame:
    ...

# Bad — missing annotations
def load_data(path, columns=None):
    ...
```

### Documentation (Required)

All code **must** be fully documented:

- **Module-level docstrings:** Every `.py` file must have a module docstring explaining its purpose
- **Function/method docstrings:** Every function and method must have a docstring describing:
  - What it does
  - Parameters (with types and descriptions)
  - Return value (with type and description)
  - Raises (if applicable)
- **Class docstrings:** Every class must have a docstring explaining its purpose and usage
- **Inline comments:** Add comments for non-obvious logic, algorithm steps, and research-specific decisions
- Use Google-style docstrings

```python
def normalize_features(
    data: pd.DataFrame,
    method: str = "z-score",
    columns: list[str] | None = None,
) -> pd.DataFrame:
    """Normalize numerical features in the dataset.

    Args:
        data: Input DataFrame containing the features.
        method: Normalization method. One of "z-score" or "min-max".
        columns: Specific columns to normalize. If None, all numeric
            columns are normalized.

    Returns:
        DataFrame with normalized features.

    Raises:
        ValueError: If an unsupported normalization method is specified.
    """
    ...
```

## Conventions for AI Assistants

- Read existing files before making modifications
- Keep changes minimal and focused on the requested task
- Do not introduce unnecessary dependencies or over-engineer solutions
- Prefer standard library solutions when they are sufficient
- For research code, prioritize clarity and correctness over premature optimization
- **Always include full type annotations on all code** — no exceptions
- **Always include docstrings on every module, class, and function** — no exceptions
- When adding notebooks, include markdown cells explaining the purpose and approach
- Update this CLAUDE.md file when significant structural changes are made to the repository
