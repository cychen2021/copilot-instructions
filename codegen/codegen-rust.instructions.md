---
description: "Rust development guidelines."
applyTo: "**/*.rs,**/Cargo.toml"
---

# Rust development guidelines

- **Documentation**: Provide `rustdoc` comments (`///`) for all public functions, structs, enums, and traits. Include an `# Examples` section for non-trivial functions. Use module-level comments (`//![...]`) to explain the purpose of a file.
- **Error Handling**: Use `Result<T, E>` for recoverable errors and `Option<T>` for optional values. Avoid using `.unwrap()` or `.expect()` in library or application code; handle the `Err` and `None` cases gracefully.
- **Testing**: Write unit tests in a `#[cfg(test)]` module within the same file. For larger-scale testing, create integration tests in the `tests/` directory.
- **Styling**:
    - At most one nested layer at the ends of `use` statements, e.g., `use std::fs::{File, OpenOptions}` is allowed, while `use std::{fs::{File, OpenOptions}, io::Write};` is not.
- **Idiomatic Rust**:
    - Prefer references (`&T`) and mutable references (`&mut T`) over cloning data.
    - Use iterators and their adapters (e.g., `map`, `filter`, `collect`) instead of manual loops where it enhances readability.
    - Leverage pattern matching with `match` for complex control flow.
    - Use standard library macros like `println!`, `vec!`, and `format!`.
    - Keep dependencies in `Cargo.toml` minimal and up-to-date.