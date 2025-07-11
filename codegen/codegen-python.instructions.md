---
description: "Python development guidelines."
applyTo: "**/*.py,**/pyproject.toml"
---

# Python development guidelines

- **Modular Design:** Emphasize clear separation of concerns.
- **Strict Typing & Docstrings:** ALWAYS add type hints (including return types) and PEP 257 compliant docstrings to all functions and classes.
- **Dependency Management:** Utilize `uv` and virtual environments.
- **Preserve Comments:** Existing comments in code must be retained.
- **Modern Python Features:** Use modern Python features up to 3.12.
- **Doc Strings**: The doc strings should be in the format of Google style. Always leave a blank line after doc strings.
- **Miscellaneous**
    - Use `is` for identity checks and `==` for equality checks.
    - Use f-strings for string formatting.
    - Use `with` statements for file operations.
    - Use list comprehensions where appropriate.
    - Use double quotes for strings.
    - Use `_ is None` and `_ is not None` for `None` checks.
    - Tables and columns in databases should use CamelCase, including those one-word names.
    - Don't test your code right after writing it. The testing will be done manually later.
