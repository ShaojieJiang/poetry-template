# Poetry Template

A modern Python project template with Poetry package management, pre-commit hooks for code quality, and documentation support via MkDocs.

## Features

- 📦 Poetry for dependency management
- 🔍 Pre-commit hooks for code quality
- 📚 Documentation setup with MkDocs Material theme
- 🛠️ Makefile for common development tasks
- ✨ Code quality tools:
  - Black-compatible formatting (via Ruff)
  - Import sorting (via Ruff)
  - Type checking with mypy
  - Comprehensive linting with Ruff
- 📊 Testing setup with pytest and coverage reporting

## Installation

```bash
# Install dependencies
poetry install

# Set up pre-commit hooks
pre-commit install
```

## Development

This template includes several tools to ensure code quality and maintainability:

- **Poetry**: Modern dependency management for Python 3.12+
- **Pre-commit hooks**: Automated code quality checks
- **MkDocs**: Documentation generation with Material theme and Python API docs support
- **Ruff**: All-in-one Python linter and formatter with:
  - Code style enforcement (PEP 8)
  - Import sorting
  - Complexity checking (McCabe)
  - Docstring validation (Google style)
  - And many more checks
- **mypy**: Static type checking with strict settings

### Code Quality Tools

The template comes with pre-configured linting and formatting tools that run automatically on commit:

- **Ruff Format**: Formats your code consistently (Black-compatible)
- **Ruff Lint**: Comprehensive linting with multiple rule sets enabled:
  - Code style (pycodestyle)
  - Bugs and complexity (pyflakes, flake8-bugbear)
  - Naming conventions (PEP 8)
  - Import organization
  - And more
- **mypy**: Strict type checking with `disallow_untyped_defs=true`

To manually run the tools:
```bash
# Check code quality (ruff, mypy, and format check)
make lint

# Format code
make format

# Run tests with coverage report
make test

# Serve documentation locally
make doc
```

You can also run individual tools directly with Poetry:
```bash
# Format and lint code
poetry run ruff check .
poetry run ruff format .

# Type checking
poetry run mypy .

# Run tests with coverage
poetry run pytest --cov --cov-report term-missing tests/
```

## Usage

1. Clone this template
2. Update the project details in `pyproject.toml`
3. Start developing with the included tools

For more detailed information, check the documentation.
