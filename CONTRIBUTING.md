# Contributing to Alembic Converger

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to the project.

## Development Setup

1. **Fork and clone the repository**
   ```bash
   git clone https://github.com/rishav00a/alembic_converger.git
   cd alembic-converger
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install development dependencies**
   ```bash
   pip install -e ".[dev]"
   ```

## Development Workflow

1. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes**
   - Write clear, readable code
   - Add docstrings (Google or NumPy style)
   - Update tests as needed

3. **Run tests**
   ```bash
   pytest
   pytest --cov=alembic_converger --cov-report=html
   ```

4. **Format and lint your code**
   ```bash
   black alembic_converger tests
   ruff check alembic_converger tests
   ```

5. **Commit your changes**
   ```bash
   git add .
   git commit -m "feat: add amazing feature"
   ```
   
   Follow [Conventional Commits](https://www.conventionalcommits.org/):
   - `feat:` - New features
   - `fix:` - Bug fixes
   - `docs:` - Documentation changes
   - `test:` - Test additions/changes
   - `refactor:` - Code refactoring
   - `chore:` - Maintenance tasks

6. **Push and create a pull request**
   ```bash
   git push origin feature/your-feature-name
   ```

## Code Style

- **Python version**: Code must support Python 3.8+
- **Formatting**: Use `black` with default settings
- **Linting**: Pass `ruff` checks
- **Line length**: 88 characters (black default)
- **Docstrings**: Google or NumPy style for all public functions/classes

## Testing Guidelines

- **Coverage**: Aim for >80% test coverage
- **Test types**:
  - Unit tests for individual functions
  - Integration tests for workflows
  - CLI tests for user interface
- **Test naming**: `test_<function>_<scenario>`
- **Fixtures**: Use pytest fixtures in `tests/conftest.py`

### Example Test

```python
def test_sort_heads_deterministically():
    """Test that heads are sorted alphabetically."""
    heads = ["zzz", "aaa", "mmm"]
    result = sort_heads_deterministically(heads)
    assert result == ["aaa", "mmm", "zzz"]
```

## Pull Request Process

1. **Ensure tests pass**: All tests must pass before merging
2. **Update documentation**: Update README.md if adding features
3. **Add changelog entry**: Describe your changes
4. **Request review**: Tag maintainers for review
5. **Address feedback**: Respond to review comments promptly

## Reporting Issues

When reporting bugs, please include:
- Python version
- Alembic version
- Steps to reproduce
- Expected vs actual behavior
- Error messages/stack traces

## Feature Requests

For feature requests:
- Explain the use case
- Describe the proposed solution
- Consider backward compatibility
- Discuss alternatives you've considered

## Code Review Checklist

- [ ] Tests added/updated and passing
- [ ] Code formatted with black
- [ ] Linting passes with ruff
- [ ] Documentation updated
- [ ] Docstrings added for public APIs
- [ ] No breaking changes (or clearly documented)
- [ ] Commit messages follow conventions

## Questions?

Feel free to:
- Open a [Discussion](https://github.com/rishav00a/alembic_converger/discussions)
- Ask in an issue
- Reach out to maintainers

Thank you for contributing! 🎉
