---
applyTo: "**/*.py"
description: "Python coding standards and practices for this project"
---

# Python Coding Standards

## Code Quality
- Follow PEP8 formatting standards
- Use type hints for all function parameters and return values
- Format code with `black` and lint with `ruff`
- Maximum file length: 500 lines (refactor if exceeded)

## Documentation
- Write Google-style docstrings for all functions:
  ```python
  def example_function(param1: str, param2: int) -> bool:
      """
      Brief description of what the function does.

      Args:
          param1: Description of parameter 1
          param2: Description of parameter 2

      Returns:
          Description of return value

      Raises:
          ValueError: When parameter validation fails
      """
  ```

## Error Handling
- Use specific exception types, avoid generic `except Exception`
- Add inline `# Reason:` comments for complex logic
- Handle edge cases explicitly

## Testing Requirements  
- Create corresponding test file in `tests/` folder for each module
- Include minimum test cases:
  - 1 test for expected behavior
  - 1 test for edge case  
  - 1 test for error condition
- Use pytest with descriptive test function names

## Dependencies
- Use `python-dotenv` for environment variables with `load_dotenv()`
- Prefer relative imports within packages
- Use `pydantic` for data validation
- Use virtual environment for all Python commands
