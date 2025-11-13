---
description: "General coding guidelines."
applyTo: "**"
---

# Best coding practices

- **Modular Design:** Emphasize clear separation of concerns.
- **Preserve Comments:** Existing comments in code must be retained.
- Tables and columns in databases should use CamelCase, including those one-word names.
- Remember to refer to the library/package/tool documentation provided by the Context7 MCP if necessary and available. Note that I frequently use the following private libraries/packages without docs on the Context7 server, for which you should reference their source code or the private indices on DeepWiki:
  - `phdkit`: Reference the source code or DeepWiki.
- **Python Dependency Management:** (VERY IMPORTANT!) Utilize `uv` and virtual environments.
  - All code and scripts must be executed via `uv run <main_command> <subcommand>`, since `python -m <main_command_module> <subcommand>` is expected to produce a module import error.
  - This is because we will always define a `main_command = <main_command_module>:<main_function>` entry point in the `[project.scripts]` section of `pyproject.toml`. For example, in this project, we have:
    ```toml
    [project.scripts]
    print-fuzzing-book = "print_fuzzing_book.main:main"
    ```
  - Besides, `uv run python -m <main_command_module> <subcommand>` will likely cause problems too. Instead, you should directly run `uv run <main_command_module> <subcommand>`. Similarly, use `uv run pytest` to run `pytest` unit tests. DON'T USE `python -m cmd` or `python -m src/cmd` to run the module!
- **Don't reinvent the wheel:** Use third-party libraries if any suitable before implementing complex functionality from scratch.
- **Maintain `.gitignore`:** Ensure unnecessary files are excluded from version control.
- Always use English in code comments, unless specified otherwise.
