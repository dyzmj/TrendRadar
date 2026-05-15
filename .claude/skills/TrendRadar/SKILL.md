```markdown
# TrendRadar Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the TrendRadar Python codebase. You'll learn how to structure files, write imports and exports, follow commit message conventions, and implement and run tests. The repository uses a clean, Pythonic style with camelCase file naming, relative imports, and named exports, and follows conventional commit messages.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `trendAnalysis.py`, `dataLoader.py`

### Import Style
- Use **relative imports** within the codebase.
  - Example:
    ```python
    from .dataLoader import loadData
    ```

### Export Style
- Use **named exports** (define functions, classes, or variables explicitly for import).
  - Example:
    ```python
    def analyzeTrends(data):
        # analysis logic
        return result
    ```

### Commit Messages
- Follow **conventional commit** style.
- Use the `feat` prefix for new features.
- Keep commit messages concise (average 62 characters).
  - Example:
    ```
    feat: add trend analysis for social media data
    ```

## Workflows

### Adding a New Feature
**Trigger:** When you want to introduce new functionality.
**Command:** `/add-feature`

1. Create a new camelCase Python file if needed (e.g., `newFeature.py`).
2. Implement your feature using relative imports and named exports.
3. Write or update tests in a corresponding `*.test.*` file.
4. Commit your changes using the `feat` prefix:
    ```
    feat: short description of the new feature
    ```
5. Push your changes and open a pull request.

### Writing and Running Tests
**Trigger:** When you add or update code and need to verify correctness.
**Command:** `/run-tests`

1. Create or update test files matching the `*.test.*` pattern (e.g., `trendAnalysis.test.py`).
2. Write test functions for your code.
3. Run tests using your preferred Python test runner (e.g., `pytest`, `unittest`).
4. Review test output and fix any issues.

### Importing Modules
**Trigger:** When you need to use code from another module in the repository.
**Command:** `/import-module`

1. Use relative imports in your Python files.
    ```python
    from .moduleName import functionName
    ```

## Testing Patterns

- Test files are named with the `*.test.*` pattern (e.g., `dataLoader.test.py`).
- The specific testing framework is not defined; use standard Python test frameworks such as `unittest` or `pytest`.
- Place test functions in these files and ensure they cover the main logic of the corresponding modules.

  Example:
  ```python
  # trendAnalysis.test.py
  from .trendAnalysis import analyzeTrends

  def test_analyzeTrends_basic():
      data = [...]
      result = analyzeTrends(data)
      assert result == expected
  ```

## Commands
| Command        | Purpose                                      |
|----------------|----------------------------------------------|
| /add-feature   | Start the workflow for adding a new feature  |
| /run-tests     | Run all tests in the codebase                |
| /import-module | Guidance for importing modules               |
```
