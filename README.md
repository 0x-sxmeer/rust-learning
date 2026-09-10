# 🦀 Rust Learning Journey

My structured path from Python developer to professional Rust developer.

Following [**The Rust Programming Language**](https://doc.rust-lang.org/book/) by Steve Klabnik, Carol Nichols, and Chris Krycho, with contributions from the Rust Community.

## 📂 Repository Structure

Organized chapter-by-chapter to mirror the book. Each sub-folder is a standalone Cargo binary with focused examples.

### Getting Started

| Folder | Chapter | Topic | Status |
|--------|---------|-------|--------|
| `ch02-guessing-game/` | [Ch 2](https://doc.rust-lang.org/book/ch02-00-guessing-game-tutorial.html) | Programming a Guessing Game | 📅 Planned |

### Fundamentals

| Folder | Chapter | Topic | Status |
|--------|---------|-------|--------|
| `ch03-common-concepts/` | [Ch 3](https://doc.rust-lang.org/book/ch03-00-common-programming-concepts.html) | Variables, data types, functions, control flow | 🔄 In Progress |
| `ch04-ownership/` | [Ch 4](https://doc.rust-lang.org/book/ch04-00-understanding-ownership.html) | Ownership, borrowing, slices | 📅 Planned |
| `ch05-structs/` | [Ch 5](https://doc.rust-lang.org/book/ch05-00-structs.html) | Structs, methods, associated functions | 📅 Planned |
| `ch06-enums/` | [Ch 6](https://doc.rust-lang.org/book/ch06-00-enums.html) | Enums, `Option`, `match`, `if let` | 📅 Planned |

### Project Organization & Collections

| Folder | Chapter | Topic | Status |
|--------|---------|-------|--------|
| `ch07-packages-crates-modules/` | [Ch 7](https://doc.rust-lang.org/book/ch07-00-managing-growing-projects-with-packages-crates-and-modules.html) | Packages, crates, modules, `use`, `pub` | 📅 Planned |
| `ch08-collections/` | [Ch 8](https://doc.rust-lang.org/book/ch08-00-common-collections.html) | `Vec`, `String`, `HashMap` | 📅 Planned |
| `ch09-error-handling/` | [Ch 9](https://doc.rust-lang.org/book/ch09-00-error-handling.html) | `panic!`, `Result`, `?` operator | 📅 Planned |

### Generics, Traits & Testing

| Folder | Chapter | Topic | Status |
|--------|---------|-------|--------|
| `ch10-generics-traits-lifetimes/` | [Ch 10](https://doc.rust-lang.org/book/ch10-00-generics.html) | Generics, traits, lifetimes | 📅 Planned |
| `ch11-testing/` | [Ch 11](https://doc.rust-lang.org/book/ch11-00-testing.html) | Writing and organizing tests | 📅 Planned |

### Applied Projects

| Folder | Chapter | Topic | Status |
|--------|---------|-------|--------|
| `ch12-minigrep/` | [Ch 12](https://doc.rust-lang.org/book/ch12-00-an-io-project.html) | I/O project — building a CLI program | 📅 Planned |

### Functional Features & Cargo Deep Dive

| Folder | Chapter | Topic | Status |
|--------|---------|-------|--------|
| `ch13-closures-iterators/` | [Ch 13](https://doc.rust-lang.org/book/ch13-00-functional-features.html) | Closures, iterators, improving minigrep | 📅 Planned |
| `ch14-cargo-cratesio/` | [Ch 14](https://doc.rust-lang.org/book/ch14-00-more-about-cargo.html) | Release profiles, workspaces, `cargo install` | 📅 Planned |

### Advanced Concepts

| Folder | Chapter | Topic | Status |
|--------|---------|-------|--------|
| `ch15-smart-pointers/` | [Ch 15](https://doc.rust-lang.org/book/ch15-00-smart-pointers.html) | `Box<T>`, `Rc<T>`, `RefCell<T>`, `Deref`, `Drop` | 📅 Planned |
| `ch16-concurrency/` | [Ch 16](https://doc.rust-lang.org/book/ch16-00-concurrency.html) | Threads, channels, `Arc<Mutex<T>>` | 📅 Planned |
| `ch17-async/` | [Ch 17](https://doc.rust-lang.org/book/ch17-00-async-await.html) | Async, await, futures, streams | 📅 Planned |
| `ch18-oop/` | [Ch 18](https://doc.rust-lang.org/book/ch18-00-oop.html) | OOP features, trait objects, state pattern | 📅 Planned |
| `ch19-patterns/` | [Ch 19](https://doc.rust-lang.org/book/ch19-00-patterns.html) | Pattern matching deep dive | 📅 Planned |
| `ch20-advanced/` | [Ch 20](https://doc.rust-lang.org/book/ch20-00-advanced-features.html) | Unsafe, advanced traits/types, macros | 📅 Planned |

### Final Project

| Folder | Chapter | Topic | Status |
|--------|---------|-------|--------|
| `ch21-web-server/` | [Ch 21](https://doc.rust-lang.org/book/ch21-00-final-project-a-web-server.html) | Multithreaded web server | 📅 Planned |

### Exercises per Chapter

<details>
<summary><strong>Ch 3 — Common Programming Concepts</strong> (click to expand)</summary>

| Exercise | Section | What I Practiced |
|----------|---------|-----------------|
| `variables-and-mutability` | [3.1](https://doc.rust-lang.org/book/ch03-01-variables-and-mutability.html) | `let`, `mut`, `const`, shadowing |
| `data-types` | [3.2](https://doc.rust-lang.org/book/ch03-02-data-types.html) | Integers, floats, bools, chars, tuples, arrays |
| `functions` | [3.3](https://doc.rust-lang.org/book/ch03-03-how-functions-work.html) | Parameters, return values, expressions vs statements |
| `control-flow` | [3.5](https://doc.rust-lang.org/book/ch03-05-control-flow.html) | `if`/`else`, `loop`, `while`, `for` |

</details>

<details>
<summary><strong>Ch 4 — Understanding Ownership</strong> (click to expand)</summary>

| Exercise | Section | What I Practiced |
|----------|---------|-----------------|
| `ownership-basics` | [4.1](https://doc.rust-lang.org/book/ch04-01-what-is-ownership.html) | Move semantics, scope, `String` type |
| `references-and-borrowing` | [4.2](https://doc.rust-lang.org/book/ch04-02-references-and-borrowing.html) | `&T`, `&mut T`, rules of references |
| `slices` | [4.3](https://doc.rust-lang.org/book/ch04-03-slices.html) | String slices (`&str`), array slices |

</details>

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/0x-sxmeer/rust-learning.git
cd rust-learning

# Run a specific exercise
cargo run -p variables-and-mutability

# Run all tests
cargo test --workspace

# Lint all code
cargo clippy --workspace

# Format all code
cargo fmt --all
```

## 🛠️ Adding a New Exercise

```bash
# Create a new exercise (e.g., for Chapter 3 — Functions)
cargo new ch03-common-concepts/functions

# The exercise is auto-added to the workspace
# Write your code, then commit:
git add .
git commit -m "feat(ch03): add functions — parameters and return values"
git push
```

## 📚 Resources

| Resource | Link |
|----------|------|
| **The Rust Book** | [doc.rust-lang.org/book](https://doc.rust-lang.org/book/) |
| **Rust by Example** | [doc.rust-lang.org/rust-by-example](https://doc.rust-lang.org/rust-by-example/) |
| **Rustlings** | [github.com/rust-lang/rustlings](https://github.com/rust-lang/rustlings) |
| **Rust Playground** | [play.rust-lang.org](https://play.rust-lang.org/) |
| **Interactive Book (Brown Univ.)** | [rust-book.cs.brown.edu](https://rust-book.cs.brown.edu) |

## 🐍 Coming from Python

I'm a Python developer transitioning to Rust. Documenting the differences, "aha moments," and mental model shifts along the way.

| Python | Rust Equivalent |
|--------|----------------|
| `pip install` | `cargo add` or edit `Cargo.toml` |
| `venv` | Not needed — Cargo isolates per-project |
| `pytest` | `cargo test` (built-in) |
| `black` / `ruff format` | `cargo fmt` |
| `pylint` / `ruff check` | `cargo clippy` |
| `mypy` | The compiler itself |
| PyPI | [crates.io](https://crates.io) |

## ⚙️ CI/CD

Every push runs [GitHub Actions](.github/workflows/rust.yml):
- ✅ `cargo check` — compilation
- ✅ `cargo test` — tests
- ✅ `cargo clippy` — linting
- ✅ `cargo fmt --check` — formatting

---

<sub>Started: September 2026 · Rust Edition 2024 · Built with 🦀 and determination</sub>
