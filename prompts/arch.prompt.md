---
mode: 'agent'
description: 'Analyze the architecture of the source code of the project and compile a detailed document about it.'
---

# Architecture Analysis and Documentation

Compile a detailed document about the architecture of the status quo of the codebase of the project. The document should illustrate the overall structure as well as critical details using code snippets and mermaid charts. Later, we will adjust the codebase and evolve and extend the project according to this document.

You should complete the following tasks:

1. Analyze the codebase of the project and compile a detailed document about the current architecture. Put the document at `dev_log/${input:filename}.md`.
2. Update the contents of the outdated `AGENTS.md` accordingly.

During the analysis, you should reference the source code and the previous documentation, including the `AGENTS.md` file and the old architecture documentation files in `dev_log/`. Note that the contents of these files may be outdated, always validate them against the current source code.

Tips:

- Only include the most important details in the architecture document. Avoid overwhelming the reader with too many details. Some old documentation files didn't do a good job at this.
