# Contributing to madupite

We're excited that you're interested in contributing to madupite! This document provides guidelines and information to help you get started.

## Project Structure

### Root Directory Overview
```
madupite/
├── docs/             # Documentation files (Sphinx)
├── examples/         # Example implementations
├── include/          # Header files for C++ implementation
├── joss/             # Journal of Open Source Software paper
├── src/              # Source code directory
└── tests/            # Unit tests
```

### Source Directory Overview
```
src/
├── madupite/                 # Python package directory
│   ├── __init__.py             # Package initialization
│   ├── __init__.pyi            # Type hints
│   └── util.py                 # Utility functions
├── madupite_matrix.cpp       # Implementation for PETSc Mat wrapper
├── madupite_vector.cpp       # Implementation for PETSc Vec wrapper
├── mdp_algorithm.cpp         # MDP class: dyn. prog. algorithm core functionality
├── mdp_matrix.cpp            # MDP-specific madupite_matrix functions
├── mdp_setup.cpp             # MDP class: initialization, options, setup
└── pymadupite.cpp            # Python bindings using nanobind
```

## Getting Started

See the [documentation](https://madupite.github.io/) for installation instructions.

## Development Guidelines

### Code Style and Formatting

Before submitting any changes: Configure your pre-commit hooks to automatically clean up and format the code.
The CI pipeline enforces these formatting rules. Pull requests will fail if code doesn't comply with:
- `.clang-format` specifications for C++
- `.flake8` configuration for Python
- Additional checks defined in `.pre-commit-config.yaml`

### Pull Request Process

1. Create a new branch from `main` for your changes
2. Make your changes with clear commit messages
3. Add/update tests as needed
4. Update documentation if introducing new features
5. Submit a pull request with:
   - Clear description of changes
   - Reference to any related issues
   - List of dependencies if added/modified

### Testing

- Write unit tests for new functionality
- Ensure all tests pass before submitting PR
- Test both Python and C++ components where applicable

### Documentation

- Update API documentation for new/modified functions
- Add examples for new features
- Update README.md if adding major features

## Bug Reports and Feature Requests

- Use GitHub Issues for bug reports and feature requests
- Include minimal reproducible example for bugs
- Clearly describe expected vs. actual behavior
- Include system information and madupite version

## License

By contributing to madupite, you agree that your contributions will be licensed under the project's MIT license.
