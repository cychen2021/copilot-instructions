---
mode: 'agent'
description: 'Analyze the architecture of the source code of the project and compile a detailed document about it.'
---

# Architecture Analysis and Documentation

Compile a detailed document about the architecture of the current status of the project's codebase. The document should illustrate the overall structure as well as critical details using code snippets and Mermaid charts. Later, we will adjust the codebase and evolve and extend the project according to this document.

You should complete the following tasks:

1. Analyze the codebase of the project and compile a detailed document about the current architecture. Put the document at `dev_log/${input:filename}.md`.
2. Update the contents of the outdated `AGENTS.md` accordingly.

During the analysis, you should reference the source code and the previous documentation, including the `README.md`, the `AGENTS.md` file, and the old architecture documentation files in `dev_log/`. Note that the contents of these files may be outdated; always validate them against the current source code.

What to include and what not to include:

- Only include the most essential source code snippets in the document. Avoid including large chunks of code.
- Use Mermaid charts to illustrate:
    - The overall architecture of the project
    - The architecture of each major module
    - The class diagrams of critical types (structs, enums, traits, classes, etc.)
    - The state diagrams of critical entities
    - The sequence diagrams of critical interactions between entities
