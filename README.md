# Rust template repo

This is my template repo for Rust projects. It also serves as my personal knowledge base for Rust, the language.

Most info is taken from [this tutorial](https://doc.rust-lang.org/book/ch02-00-guessing-game-tutorial.html).  

# basic syntax

## comments

Single line comments are introduced by `//`.  


# cargo

cargo is the package manager and build system for rust.  

`cargo new project_name` initializes a new rust project named "project name".
It makes a new directory with the same name. It contains a `src/` directory containing the source files and a Cargo.toml file for project meta data and dependencies.  

`cargo build` is the build command, however, using `cargo run` is more convenient.  

`cargo check` checks the project for errors without building or running it.  

To build the project for release: `cargo build --release`. This builds the project with optimizations.  

## crates

If you want to include Rust libraries called "crates", you can do so in the `Cargo.toml` file. For random numbers:  

```
[dependencies]
rand = "0.8.5"
```  

This will add `rand` with version > 0.8.5 and < 0.9.x.  


# basic I/O

To print to stdout: `println!("The variable has the value {variable}");`  
This prints a line to stdout with the value of `variable` at the placeholder initiated with the curly braces.  

If some item is not in the [prelude](https://doc.rust-lang.org/std/prelude/index.html), it has to be included with `use`.  

To read input:  

```
use std::io;

let mut guess = String::new();

io::stdin()
    .read_line(&mut guess)
    .expect("Failed to read line");
```  

Here, `expect()` is exception handling.  

# variables

To create a variable, the keyword `let` is used.  

Variables are immutable by default. That means if you create a variable like this:  
`let apples = 5;`  
apples is a variable with the value of 5, that can not be changed. If you want the variable to be mutable, it has to be created as such:  
`let mut apples = 5;`  



