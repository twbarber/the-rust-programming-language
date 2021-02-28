# The Rust Programming Language - Workbook

## Overview

This repository serves to host any artifacts created while working through [The Rust Programming Language](https://doc.rust-lang.org/book/).

## Glossary

| Term                    | Definition                                                                                                                                |
| :---------------------- | :---------------------------------------------------------------------------------------------------------------------------------------- |
| **associated function** | An associated function is implemented on a type rather than on a particular instance of a type. Some languages call this a static method. |
| **cargo**               | Rust's build system and package manager                                                                                                   |
| **crate**               | Collection of rust source code files                                                                                                      |
| **rustc**               | Rust's Compiler                                                                                                                           |
| **rustup**              | Rust's toolchian installer                                                                                                                |

## Commands

| Command       | Purpose                  | Notes                                                                  |
| :------------ | :----------------------- | :--------------------------------------------------------------------- |
| `cargo build` | Compile, with executable | Produce executable, but does not run.                                  |
| `cargo check` | Compile, no executable   | Faster than `cargo build`. No executable produced.                     |
| `cargo fmt`   | Format code              | `rustfmt <file>` for individual files, `cargo fmt` applies to project. |

| `cargo new <project>` | Build Porject                     | Creates `/src`, `Cargo.toml`, and intializes git in new directory. |
| `cargo run`           | Compile, with executable, and run | Full build and execution of project.                               |
| `cargo update`        | Update dependencies               | Update to latest that match SemVer in Cargo.toml.                  |


## Notes

- **prelude**: Part of standard library automatically imported into every Rust program
- In Rust, variables are immutable by default
  - `let foo = 5;` // immutable
  - `let mut bar = 5;` // mutable
- A reference gives you a way to let multiple parts of your code access one piece of data without needing to copy that data into memory multiple times. References are a complex feature, and one of Rust’s major advantages is how safe and easy it is to use references.
- For `Result`, the variants are `Ok` or `Err`. The `Ok` variant indicates the operation was successful, and inside `Ok` is the successfully generated value. The `Err` variant means the operation failed, and `Err` contains information about how or why the operation failed.
- Cargo fetches the latest versions of everything from the registry, which is a copy of data from Crates.io.
- Cargo figures out all the versions of the dependencies that fit the criteria and then writes them to the Cargo.lock file. When you build your project in the future, Cargo will see that the Cargo.lock file exists and use the versions specified there rather than doing all the work of figuring out versions again.
- _Shadowing_ is often used in situations in which you want to convert a value from one type to another type. 
- Switching from an `expect` call to a `match` expression is how you generally move from crashing on an error to handling the error. Remember that parse returns a `Result` type and `Result` is an enum that has the variants `Ok` or `Err`.
-  The underscore, `_`, is a catchall value (`Err(_)`).