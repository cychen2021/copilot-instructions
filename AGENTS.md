# GitHub Copilot Instruction Agents

This repository contains reusable instruction sets for GitHub Copilot. Each instruction set defines specific guidelines and best practices for different development contexts.

## Available Instruction Sets

### Code Generation (`codegen/`)

#### General Coding Guidelines
- **File**: `codegen/codegen-general.instructions.md`
- **Description**: General coding guidelines and best practices
- **Applies to**: All files (`**`)
- **Key features**:
  - Modular design principles
  - Comment preservation
  - Database naming conventions (CamelCase)
  - Python dependency management with `uv`

#### Python Development
- **File**: `codegen/codegen-python.instructions.md`
- **Description**: Python-specific development guidelines
- **Applies to**: `**/*.py`, `**/pyproject.toml`
- **Key features**:
  - Strict typing and PEP 257 docstrings
  - Modern Python features (up to 3.12)
  - Google-style docstrings
  - Testing with pytest
  - Best practices for string formatting, file operations, and None checks

#### Rust Development
- **File**: `codegen/codegen-rust.instructions.md`
- **Description**: Rust-specific development guidelines
- **Applies to**: `**/*.rs`, `**/Cargo.toml`
- **Key features**:
  - Comprehensive rustdoc documentation
  - Proper error handling with Result and Option types
  - Unit and integration testing patterns
  - Idiomatic Rust coding practices
  - Dependency management guidelines

#### Shell Usage
- **File**: `codegen/shell.instructions.md`
- **Description**: Shell usage tips and platform-specific guidelines
- **Applies to**: All files (`**`)
- **Key features**:
  - Platform-specific shell recommendations (Nushell for Windows, default terminal for macOS/Linux)
  - Command execution best practices

### Commit Messages (`commit/`)

#### Commit Message Guidelines
- **File**: `commit/commit-general.instructions.md`
- **Description**: Comprehensive commit message formatting guidelines
- **Key features**:
  - Concise headlines (less than 10 words)
  - Proper capitalization and punctuation
  - Structured body with bullet points
  - Code and file reference formatting
  - Guidelines for describing changes (moves, renames, etc.)

### Prompts (`prompts/`)

#### Agent Instruction Generation
- **File**: `prompts/generate-agent-instructions.prompt.md`
- **Description**: Template for generating new instruction sets
- **Status**: TODO (placeholder)

## Usage

These instruction files are designed to be used with GitHub Copilot to provide context-specific guidance during development. Each file includes YAML frontmatter specifying:

- `description`: Brief description of the instruction set
- `applyTo`: File patterns where the instructions should be applied

## File Format

All instruction files follow this structure:

```markdown
---
description: "Brief description"
applyTo: "file_pattern"
---

# Title

- Instruction points...
```

## Contributing

When adding new instruction sets:

1. Follow the established file naming convention: `category-specific.instructions.md`
2. Include proper YAML frontmatter with description and applyTo fields
3. Use clear, actionable instruction points
4. Update this AGENTS.md file to document the new instruction set