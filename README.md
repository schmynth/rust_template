# Rust template repo

This is my template repo for Rust projects. It also serves as my personal knowledge base for Rust, the language.

# cargo

cargo is the package manager and build system for rust.  

`cargo new project_name` initializes a new rust project named "project name".
It makes a new directory with the same name. It contains a `src/` directory containing the source files and a Cargo.toml file for project meta data and dependencies.  

`cargo build` is the build command, however, using `cargo run` is more convenient.  

`cargo check` checks the project for errors without building or running it.  

To build the project for release: `cargo build --release`. This builds the project with optimizations.








