# GitHub Copilot Instructions for copilot-instructions Repository

This repository contains reusable instruction sets and prompts for GitHub Copilot. When working in this repository, follow these guidelines:

## Repository Structure

- `codegen/` - Contains instruction files for different programming languages and general coding guidelines
- `commit/` - Contains instruction files for commit message formatting
- `prompts/` - Contains prompt templates for generating new instruction sets
- `AGENTS.md` - Documentation of all available instruction sets

## File Naming Conventions

- Instruction files: `category-specific.instructions.md`
- Prompt files: `name.prompt.md`
- Use lowercase with hyphens for multi-word names

## Instruction File Format

All instruction files must include YAML frontmatter:

```yaml
---
description: "Brief description of the instruction set"
applyTo: "file_pattern_where_instructions_apply"
---
```

## Content Guidelines

- Use clear, actionable bullet points
- Focus on specific, measurable guidelines
- Include examples where helpful
- Maintain consistency with existing instruction sets
- Keep instructions concise but comprehensive

## Documentation Updates

When adding or modifying instruction sets:

1. Update `AGENTS.md` to reflect changes
2. Follow the established documentation format
3. Include all relevant metadata (file patterns, descriptions, key features)
4. Test instructions for clarity and completeness

## Language-Specific Guidelines

- For Python: Follow PEP standards and modern Python practices
- For Rust: Emphasize safety, documentation, and idiomatic patterns
- For shell: Consider cross-platform compatibility
- For general coding: Focus on maintainability and best practices