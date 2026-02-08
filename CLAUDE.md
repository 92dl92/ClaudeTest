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

## Conventions for AI Assistants

- Read existing files before making modifications
- Keep changes minimal and focused on the requested task
- Do not introduce unnecessary dependencies or over-engineer solutions
- Prefer standard library solutions when they are sufficient
- For research code, prioritize clarity and correctness over premature optimization
- Use type hints for function signatures
- Include docstrings for non-trivial functions
- When adding notebooks, include markdown cells explaining the purpose and approach
- Update this CLAUDE.md file when significant structural changes are made to the repository
