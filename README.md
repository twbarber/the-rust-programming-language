# The Rust Programming Language - Workbook

## Overview

This repository serves to host any artifacts created while working through [The Rust Programming Language](https://doc.rust-lang.org/book/).

## Glossary

| Term       | Definition                              |
| :--------- | :-------------------------------------- |
| **cargo**  | Rust's build system and package manager |
| **rustc**  | Rust's Compiler                         |
| **rustup** | Rust's toolchian installer              |


## Commands

| Command               | Purpose                           | Notes                                                              |
| :-------------------- | :-------------------------------- | :----------------------------------------------------------------- |
| `cargo build`         | Compile, with executable          | Produce executable, but does not run.                              |
| `cargo check`         | Compile, no executable            | Faster than `cargo build`. No executable produced.                 |
| `cargo new <project>` | Build Porject                     | Creates `/src`, `Cargo.toml`, and intializes git in new directory. |
| `cargo run`           | Compile, with executable, and run | Full build and execution of project.                               |
