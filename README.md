# 🦀 Rust Learning Journey

[![Rust CI](https://github.com/0x-sxmeer/rust-learning/actions/workflows/rust.yml/badge.svg)](https://github.com/0x-sxmeer/rust-learning/actions/workflows/rust.yml)

> My structured path from **Python developer** to **professional Rust developer**.
>
> Following [**The Rust Programming Language**](https://doc.rust-lang.org/book/) (2024 Edition) by Steve Klabnik, Carol Nichols, and Chris Krycho, with contributions from the Rust Community.
>
> 📖 [Read the book online](https://doc.rust-lang.org/book/) · 🎓 [Interactive version (Brown Univ.)](https://rust-book.cs.brown.edu) · 📕 [No Starch Press (print)](https://nostarch.com/rust-programming-language-3rd-edition)

---

## 📂 Repository Structure

This repo is a **Cargo workspace**. Each sub-folder is a standalone binary crate with focused exercises mapped 1:1 to the book's sections. Folders are named after chapters so you can read the book and code side-by-side.

```
rust-learning/
├── Cargo.toml                              # Workspace root (65 members)
├── README.md
├── .gitignore
├── .github/workflows/rust.yml              # CI: check + test + clippy + fmt
│
├── ch02-guessing-game/                     # Chapter 2  — First project
│
├── ch03-common-concepts/                   # Chapter 3  — Common Programming Concepts
│   ├── variables-and-mutability/           #   §3.1 let, mut, const, shadowing
│   ├── data-types/                         #   §3.2 Scalar & compound types
│   ├── functions/                          #   §3.3 fn, parameters, return values
│   └── control-flow/                       #   §3.5 if/else, loop, while, for
│
├── ch04-ownership/                         # Chapter 4  — Understanding Ownership ⭐
│   ├── what-is-ownership/                  #   §4.1 Stack vs heap, move, clone, Copy
│   ├── references-and-borrowing/           #   §4.2 &T, &mut T, borrowing rules
│   └── the-slice-type/                     #   §4.3 &str, &[T], string slices
│
├── ch05-structs/                           # Chapter 5  — Using Structs
│   ├── defining-structs/                   #   §5.1 Struct syntax, field init, update
│   ├── example-program/                    #   §5.2 Rectangle area calculator
│   └── methods/                            #   §5.3 impl blocks, &self, Self
│
├── ch06-enums/                             # Chapter 6  — Enums and Pattern Matching
│   ├── defining-enums/                     #   §6.1 enum, Option<T>, payload variants
│   ├── match-control-flow/                 #   §6.2 match arms, exhaustive matching
│   └── if-let/                             #   §6.3 if let, let...else shorthand
│
├── ch07-packages-crates-modules/           # Chapter 7  — Packages, Crates, and Modules
│   ├── packages-and-crates/                #   §7.1 Binary vs library crates
│   ├── modules-and-scope/                  #   §7.2 mod, pub, privacy rules
│   ├── paths/                              #   §7.3 Absolute & relative paths
│   ├── use-keyword/                        #   §7.4 use, as, re-exporting
│   └── separating-modules/                 #   §7.5 Splitting into files
│
├── ch08-collections/                       # Chapter 8  — Common Collections
│   ├── vectors/                            #   §8.1 Vec<T>, indexing, iterating
│   ├── strings/                            #   §8.2 String vs &str, UTF-8
│   └── hashmaps/                           #   §8.3 HashMap<K,V>, entry API
│
├── ch09-error-handling/                    # Chapter 9  — Error Handling
│   ├── panic/                              #   §9.1 panic!, unwinding, abort
│   ├── result/                             #   §9.2 Result<T,E>, ?, map_err
│   └── when-to-panic/                      #   §9.3 Guidelines: panic vs Result
│
├── ch10-generics-traits-lifetimes/         # Chapter 10 — Generic Types, Traits, Lifetimes
│   ├── generics/                           #   §10.1 Generic functions, structs, enums
│   ├── traits/                             #   §10.2 Defining, implementing, bounds
│   └── lifetimes/                          #   §10.3 'a annotations, elision rules
│
├── ch11-testing/                           # Chapter 11 — Writing Automated Tests
│   ├── writing-tests/                      #   §11.1 #[test], assert!, assert_eq!
│   ├── running-tests/                      #   §11.2 Filtering, --ignored, threads
│   └── test-organization/                  #   §11.3 Unit vs integration tests
│
├── ch12-minigrep/                          # Chapter 12 — I/O Project (single crate)
│                                           #   CLI grep clone: args, file I/O, TDD
│
├── ch13-closures-iterators/                # Chapter 13 — Iterators and Closures
│   ├── closures/                           #   §13.1 |x| x+1, Fn/FnMut/FnOnce
│   ├── iterators/                          #   §13.2 .iter(), .map(), .collect()
│   ├── improving-minigrep/                 #   §13.3 Refactoring ch12 with iterators
│   └── performance/                        #   §13.4 Loops vs iterators benchmarks
│
├── ch14-cargo-cratesio/                    # Chapter 14 — More about Cargo
│   └── workspaces/                         #   §14.3 Workspace configuration
│
├── ch15-smart-pointers/                    # Chapter 15 — Smart Pointers
│   ├── box-heap/                           #   §15.1 Box<T>, recursive types
│   ├── deref-trait/                        #   §15.2 Deref coercion, * operator
│   ├── drop-trait/                         #   §15.3 Drop, std::mem::drop
│   ├── rc-reference-counting/              #   §15.4 Rc<T>, Rc::clone
│   ├── refcell-interior-mutability/        #   §15.5 RefCell<T>, borrow()
│   └── reference-cycles/                   #   §15.6 Weak<T>, memory leaks
│
├── ch16-concurrency/                       # Chapter 16 — Fearless Concurrency
│   ├── threads/                            #   §16.1 thread::spawn, JoinHandle
│   ├── message-passing/                    #   §16.2 mpsc channels, tx/rx
│   ├── shared-state/                       #   §16.3 Mutex<T>, Arc<T>
│   └── send-sync/                          #   §16.4 Send & Sync traits
│
├── ch17-async/                             # Chapter 17 — Async Programming (2024 ed.)
│   ├── futures-and-syntax/                 #   §17.1 async fn, .await, Future
│   ├── concurrency-with-async/             #   §17.2 join!, select!, spawning
│   ├── working-with-futures/               #   §17.3 Pin, multiple futures
│   ├── streams/                            #   §17.4 Stream, async iteration
│   ├── async-traits/                       #   §17.5 Traits for async
│   └── futures-tasks-threads/              #   §17.6 Futures vs tasks vs threads
│
├── ch18-oop/                               # Chapter 18 — OOP Features of Rust
│   ├── characteristics-of-oo/              #   §18.1 Encapsulation, pub/private
│   ├── trait-objects/                       #   §18.2 dyn Trait, dynamic dispatch
│   └── state-pattern/                      #   §18.3 State pattern, typestate
│
├── ch19-patterns/                          # Chapter 19 — Patterns and Matching
│   ├── all-the-places/                     #   §19.1 Where patterns can be used
│   ├── refutability/                       #   §19.2 Irrefutable vs refutable
│   └── pattern-syntax/                     #   §19.3 Destructuring, guards, @
│
├── ch20-advanced/                          # Chapter 20 — Advanced Features
│   ├── unsafe-rust/                        #   §20.1 unsafe blocks, raw ptrs, FFI
│   ├── advanced-traits/                    #   §20.2 Associated types, defaults
│   ├── advanced-types/                     #   §20.3 Newtype, type aliases, !
│   ├── advanced-functions/                 #   §20.4 fn pointers, closures
│   └── macros/                             #   §20.5 macro_rules!, proc macros
│
├── ch21-web-server/                        # Chapter 21 — Final Project (single crate)
│                                           #   Multithreaded web server
│
└── notes/                                  # Personal learning notes
    ├── ownership-cheatsheet.md
    ├── python-vs-rust.md
    └── aha-moments.md
```

> **Note**: §3.4 (Comments) is covered inline in every exercise rather than having its own folder — comments are best learned by writing them alongside real code.

---

## 📊 Progress Tracker

### Part I — Getting Started (Ch 1–2)

| # | Chapter | Folder | Exercises | Status |
|---|---------|--------|-----------|--------|
| 1 | [Getting Started](https://doc.rust-lang.org/book/ch01-00-getting-started.html) | — | Installation, Hello World, Hello Cargo | ✅ Done |
| 2 | [Programming a Guessing Game](https://doc.rust-lang.org/book/ch02-00-guessing-game-tutorial.html) | `ch02-guessing-game/` | 1 project | 📅 Planned |

### Part II — Fundamentals (Ch 3–6)

| # | Chapter | Folder | Exercises | Status |
|---|---------|--------|-----------|--------|
| 3 | [Common Programming Concepts](https://doc.rust-lang.org/book/ch03-00-common-programming-concepts.html) | `ch03-common-concepts/` | 4 exercises | 🔄 In Progress |
| 4 | [Understanding Ownership](https://doc.rust-lang.org/book/ch04-00-understanding-ownership.html) | `ch04-ownership/` | 3 exercises | 📅 Planned |
| 5 | [Using Structs](https://doc.rust-lang.org/book/ch05-00-structs.html) | `ch05-structs/` | 3 exercises | 📅 Planned |
| 6 | [Enums and Pattern Matching](https://doc.rust-lang.org/book/ch06-00-enums.html) | `ch06-enums/` | 3 exercises | 📅 Planned |

### Part III — Thinking in Rust (Ch 7–9)

| # | Chapter | Folder | Exercises | Status |
|---|---------|--------|-----------|--------|
| 7 | [Packages, Crates, and Modules](https://doc.rust-lang.org/book/ch07-00-managing-growing-projects-with-packages-crates-and-modules.html) | `ch07-packages-crates-modules/` | 5 exercises | 📅 Planned |
| 8 | [Common Collections](https://doc.rust-lang.org/book/ch08-00-common-collections.html) | `ch08-collections/` | 3 exercises | 📅 Planned |
| 9 | [Error Handling](https://doc.rust-lang.org/book/ch09-00-error-handling.html) | `ch09-error-handling/` | 3 exercises | 📅 Planned |

### Part IV — Generics, Testing & Projects (Ch 10–12)

| # | Chapter | Folder | Exercises | Status |
|---|---------|--------|-----------|--------|
| 10 | [Generic Types, Traits, and Lifetimes](https://doc.rust-lang.org/book/ch10-00-generics.html) | `ch10-generics-traits-lifetimes/` | 3 exercises | 📅 Planned |
| 11 | [Writing Automated Tests](https://doc.rust-lang.org/book/ch11-00-testing.html) | `ch11-testing/` | 3 exercises | 📅 Planned |
| 12 | [I/O Project: minigrep](https://doc.rust-lang.org/book/ch12-00-an-io-project.html) | `ch12-minigrep/` | 1 project | 📅 Planned |

### Part V — Functional & Cargo (Ch 13–14)

| # | Chapter | Folder | Exercises | Status |
|---|---------|--------|-----------|--------|
| 13 | [Iterators and Closures](https://doc.rust-lang.org/book/ch13-00-functional-features.html) | `ch13-closures-iterators/` | 4 exercises | 📅 Planned |
| 14 | [More About Cargo](https://doc.rust-lang.org/book/ch14-00-more-about-cargo.html) | `ch14-cargo-cratesio/` | 1 exercise | 📅 Planned |

### Part VI — Advanced Concepts (Ch 15–20)

| # | Chapter | Folder | Exercises | Status |
|---|---------|--------|-----------|--------|
| 15 | [Smart Pointers](https://doc.rust-lang.org/book/ch15-00-smart-pointers.html) | `ch15-smart-pointers/` | 6 exercises | 📅 Planned |
| 16 | [Fearless Concurrency](https://doc.rust-lang.org/book/ch16-00-concurrency.html) | `ch16-concurrency/` | 4 exercises | 📅 Planned |
| 17 | [Async, Await, Futures, Streams](https://doc.rust-lang.org/book/ch17-00-async-await.html) | `ch17-async/` | 6 exercises | 📅 Planned |
| 18 | [OOP Features of Rust](https://doc.rust-lang.org/book/ch18-00-oop.html) | `ch18-oop/` | 3 exercises | 📅 Planned |
| 19 | [Patterns and Matching](https://doc.rust-lang.org/book/ch19-00-patterns.html) | `ch19-patterns/` | 3 exercises | 📅 Planned |
| 20 | [Advanced Features](https://doc.rust-lang.org/book/ch20-00-advanced-features.html) | `ch20-advanced/` | 5 exercises | 📅 Planned |

### Final Project (Ch 21)

| # | Chapter | Folder | Type | Status |
|---|---------|--------|------|--------|
| 21 | [Multithreaded Web Server](https://doc.rust-lang.org/book/ch21-00-final-project-a-web-server.html) | `ch21-web-server/` | Capstone project | 📅 Planned |

**Total: 21 chapters · 65 exercise crates · 3 projects (guessing game, minigrep, web server)**

---

## 📝 Exercise Breakdown by Chapter

<details>
<summary><strong>Ch 2 — Programming a Guessing Game</strong></summary>

Single project combining: `use std::io`, `rand` crate, `loop`, `match`, type parsing with `.parse()`.

```bash
cargo run -p guessing-game
```
</details>

<details>
<summary><strong>Ch 3 — Common Programming Concepts</strong> (4 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `variables-and-mutability` | [§3.1](https://doc.rust-lang.org/book/ch03-01-variables-and-mutability.html) | `let`, `mut`, `const`, shadowing, type re-binding |
| `data-types` | [§3.2](https://doc.rust-lang.org/book/ch03-02-data-types.html) | `i32`/`u64`/`f64`, `bool`, `char`, tuples `(i32, f64)`, arrays `[i32; 5]`, integer overflow |
| `functions` | [§3.3](https://doc.rust-lang.org/book/ch03-03-how-functions-work.html) | Function parameters, return values, expressions vs statements, `-> Type` |
| `control-flow` | [§3.5](https://doc.rust-lang.org/book/ch03-05-control-flow.html) | `if`/`else`, `if` in `let`, `loop`, `while`, `for`, loop labels `'label`, `break` with value |

> 📝 §3.4 (Comments) is practiced inline across all exercises — `//`, `///`, `//!`

</details>

<details>
<summary><strong>Ch 4 — Understanding Ownership</strong> (3 exercises) ⭐ Most Important Chapter</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `what-is-ownership` | [§4.1](https://doc.rust-lang.org/book/ch04-01-what-is-ownership.html) | Stack vs heap, ownership rules, variable scope, `String` type, `move`, `clone`, `Copy` trait |
| `references-and-borrowing` | [§4.2](https://doc.rust-lang.org/book/ch04-02-references-and-borrowing.html) | `&T` (shared ref), `&mut T` (mutable ref), "one mutable XOR many shared" rule, dangling references |
| `the-slice-type` | [§4.3](https://doc.rust-lang.org/book/ch04-03-slices.html) | `&str` string slices, `&[i32]` array slices, range syntax `[0..5]`, `[..]`, why slices prevent bugs |

> 💡 **Python dev note**: This chapter has no Python equivalent. Python uses garbage collection — Rust uses ownership. Spend extra time here. Re-read this chapter at least twice.

</details>

<details>
<summary><strong>Ch 5 — Using Structs to Structure Related Data</strong> (3 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `defining-structs` | [§5.1](https://doc.rust-lang.org/book/ch05-01-defining-structs.html) | Named fields, tuple structs, unit structs, field init shorthand, struct update syntax `..` |
| `example-program` | [§5.2](https://doc.rust-lang.org/book/ch05-02-example-structs.html) | `Rectangle` area calculator, `#[derive(Debug)]`, `dbg!` macro, `{:?}` / `{:#?}` formatting |
| `methods` | [§5.3](https://doc.rust-lang.org/book/ch05-03-method-syntax.html) | `impl` blocks, `&self`, `&mut self`, `Self`, associated functions (like Python `@classmethod`) |

> 💡 **Python dev note**: `struct` + `impl` = Python's `class`. Methods with `&self` = Python's `self`. Associated functions without `self` = Python's `@staticmethod`.

</details>

<details>
<summary><strong>Ch 6 — Enums and Pattern Matching</strong> (3 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `defining-enums` | [§6.1](https://doc.rust-lang.org/book/ch06-01-defining-an-enum.html) | `enum` with data payloads, `Option<T>` (`Some`/`None`), why Rust has no null |
| `match-control-flow` | [§6.2](https://doc.rust-lang.org/book/ch06-02-match.html) | `match` arms, exhaustive matching, `_` catch-all, binding values in patterns |
| `if-let` | [§6.3](https://doc.rust-lang.org/book/ch06-03-if-let.html) | `if let Some(x) = ...`, `let...else` (new in 2024 ed.), concise control flow |

</details>

<details>
<summary><strong>Ch 7 — Managing Growing Projects with Packages, Crates, and Modules</strong> (5 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `packages-and-crates` | [§7.1](https://doc.rust-lang.org/book/ch07-01-packages-and-crates.html) | Crate root (`src/main.rs` vs `src/lib.rs`), binary vs library crates, package rules |
| `modules-and-scope` | [§7.2](https://doc.rust-lang.org/book/ch07-02-defining-modules-to-control-scope-and-privacy.html) | `mod`, module tree, privacy boundary, `pub`, `pub(crate)` |
| `paths` | [§7.3](https://doc.rust-lang.org/book/ch07-03-paths-for-referring-to-an-item-in-the-module-tree.html) | `crate::`, `self::`, `super::`, absolute vs relative paths |
| `use-keyword` | [§7.4](https://doc.rust-lang.org/book/ch07-04-bringing-paths-into-scope-with-the-use-keyword.html) | `use`, `as` aliases, `pub use` re-exporting, nested paths `use std::{io, cmp}` |
| `separating-modules` | [§7.5](https://doc.rust-lang.org/book/ch07-05-separating-modules-into-different-files.html) | Multi-file modules, `mod.rs` convention vs `filename.rs` |

</details>

<details>
<summary><strong>Ch 8 — Common Collections</strong> (3 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `vectors` | [§8.1](https://doc.rust-lang.org/book/ch08-01-vectors.html) | `Vec<T>`, `vec![]` macro, `.push()`, indexing vs `.get()`, iterating, enum trick for mixed types |
| `strings` | [§8.2](https://doc.rust-lang.org/book/ch08-02-strings.html) | `String` vs `&str`, UTF-8 encoding, concatenation with `+` and `format!`, why you can't index strings |
| `hashmaps` | [§8.3](https://doc.rust-lang.org/book/ch08-03-hash-maps.html) | `HashMap<K,V>`, `.insert()`, `.entry().or_insert()`, ownership of keys/values, `use std::collections::HashMap` |

</details>

<details>
<summary><strong>Ch 9 — Error Handling</strong> (3 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `panic` | [§9.1](https://doc.rust-lang.org/book/ch09-01-unrecoverable-errors-with-panic.html) | `panic!` macro, `RUST_BACKTRACE=1`, unwinding vs aborting |
| `result` | [§9.2](https://doc.rust-lang.org/book/ch09-02-recoverable-errors-with-result.html) | `Result<T,E>`, `match` on Result, `unwrap()`, `expect()`, `?` operator, error propagation |
| `when-to-panic` | [§9.3](https://doc.rust-lang.org/book/ch09-03-to-panic-or-not-to-panic.html) | Guidelines for panic vs Result, custom types for validation, prototyping vs production |

> 💡 **Python dev note**: `Result<T,E>` + `?` = Python's `try`/`except` but enforced at compile time. You can't forget to handle errors.

</details>

<details>
<summary><strong>Ch 10 — Generic Types, Traits, and Lifetimes</strong> (3 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `generics` | [§10.1](https://doc.rust-lang.org/book/ch10-01-syntax.html) | `fn largest<T>`, generic structs/enums, monomorphization (zero-cost abstraction!) |
| `traits` | [§10.2](https://doc.rust-lang.org/book/ch10-02-traits.html) | `trait Summary`, `impl Trait for Type`, default implementations, trait bounds `T: Display + Clone`, `where` clauses |
| `lifetimes` | [§10.3](https://doc.rust-lang.org/book/ch10-03-lifetime-syntax.html) | `'a` annotations, lifetime elision rules, `'static`, lifetimes in struct definitions |

</details>

<details>
<summary><strong>Ch 11 — Writing Automated Tests</strong> (3 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `writing-tests` | [§11.1](https://doc.rust-lang.org/book/ch11-01-writing-tests.html) | `#[test]`, `assert!`, `assert_eq!`, `assert_ne!`, custom failure messages, `#[should_panic(expected = "...")]`, `Result<T, E>` in tests |
| `running-tests` | [§11.2](https://doc.rust-lang.org/book/ch11-02-running-tests.html) | `--test-threads=1`, `--show-output`, filtering by name, `#[ignore]`, `--ignored` |
| `test-organization` | [§11.3](https://doc.rust-lang.org/book/ch11-03-test-organization.html) | Unit tests in `#[cfg(test)]` mod, integration tests in `tests/` dir, testing private functions |

> 💡 **Python dev note**: `cargo test` = `pytest`. No separate test runner needed. Tests live next to your code in the same file.

</details>

<details>
<summary><strong>Ch 12 — I/O Project: Building a Command Line Program</strong> (single project)</summary>

A complete CLI program that searches for a string in a file — like a simplified `grep`. This is where it all comes together.

Sections covered:
- §12.1 — Accepting command line arguments (`std::env::args`)
- §12.2 — Reading a file (`std::fs::read_to_string`)
- §12.3 — Refactoring to improve modularity and error handling
- §12.4 — Developing library's functionality with TDD
- §12.5 — Working with environment variables (`std::env::var`)
- §12.6 — Writing error messages to `stderr` instead of `stdout`

```bash
cargo run -p minigrep -- searchstring poem.txt
IGNORE_CASE=1 cargo run -p minigrep -- to poem.txt
```
</details>

<details>
<summary><strong>Ch 13 — Functional Language Features: Iterators and Closures</strong> (4 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `closures` | [§13.1](https://doc.rust-lang.org/book/ch13-01-closures.html) | `\|x\| x + 1`, capturing environment, `Fn` / `FnMut` / `FnOnce` traits, move closures |
| `iterators` | [§13.2](https://doc.rust-lang.org/book/ch13-02-iterators.html) | `Iterator` trait, `.iter()`, `.map()`, `.filter()`, `.collect()`, `.sum()`, consuming vs borrowing |
| `improving-minigrep` | [§13.3](https://doc.rust-lang.org/book/ch13-03-improving-our-io-project.html) | Refactoring Ch 12's minigrep using closures and iterators for cleaner code |
| `performance` | [§13.4](https://doc.rust-lang.org/book/ch13-04-performance.html) | Zero-cost abstractions: iterators vs loops benchmarks, compiler optimizations |

</details>

<details>
<summary><strong>Ch 14 — More about Cargo and Crates.io</strong> (1 exercise)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `workspaces` | [§14.3](https://doc.rust-lang.org/book/ch14-03-cargo-workspaces.html) | Workspace configuration, shared `Cargo.lock`, inter-crate dependencies |

Other sections (§14.1 Release Profiles, §14.2 Publishing to Crates.io, §14.4 `cargo install`, §14.5 Custom Commands) are conceptual — notes in the exercise's comments.

</details>

<details>
<summary><strong>Ch 15 — Smart Pointers</strong> (6 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `box-heap` | [§15.1](https://doc.rust-lang.org/book/ch15-01-box.html) | `Box<T>` for heap allocation, recursive types (cons list) |
| `deref-trait` | [§15.2](https://doc.rust-lang.org/book/ch15-02-deref.html) | `Deref` trait, deref coercion, `*` operator, custom smart pointers |
| `drop-trait` | [§15.3](https://doc.rust-lang.org/book/ch15-03-drop.html) | `Drop` trait, `std::mem::drop`, cleanup logic |
| `rc-reference-counting` | [§15.4](https://doc.rust-lang.org/book/ch15-04-rc.html) | `Rc<T>`, `Rc::clone`, `Rc::strong_count`, shared ownership |
| `refcell-interior-mutability` | [§15.5](https://doc.rust-lang.org/book/ch15-05-interior-mutability.html) | `RefCell<T>`, `borrow()`, `borrow_mut()`, interior mutability pattern, `Rc<RefCell<T>>` combo |
| `reference-cycles` | [§15.6](https://doc.rust-lang.org/book/ch15-06-reference-cycles.html) | `Weak<T>`, preventing memory leaks, tree data structures |

</details>

<details>
<summary><strong>Ch 16 — Fearless Concurrency</strong> (4 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `threads` | [§16.1](https://doc.rust-lang.org/book/ch16-01-threads.html) | `thread::spawn`, `JoinHandle`, `move` closures for thread ownership |
| `message-passing` | [§16.2](https://doc.rust-lang.org/book/ch16-02-message-passing.html) | `mpsc::channel`, `tx.send()`, `rx.recv()`, multiple producers |
| `shared-state` | [§16.3](https://doc.rust-lang.org/book/ch16-03-shared-state.html) | `Mutex<T>`, `.lock()`, `Arc<T>` (atomic reference counting), `Arc<Mutex<T>>` pattern |
| `send-sync` | [§16.4](https://doc.rust-lang.org/book/ch16-04-extensible-concurrency-sync-and-send.html) | `Send` and `Sync` marker traits, extensible concurrency |

</details>

<details>
<summary><strong>Ch 17 — Async, Await, Futures, and Streams</strong> (6 exercises) 🆕 New in 2024 Edition</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `futures-and-syntax` | [§17.1](https://doc.rust-lang.org/book/ch17-01-futures-and-syntax.html) | `async fn`, `.await`, `Future` trait, async runtimes |
| `concurrency-with-async` | [§17.2](https://doc.rust-lang.org/book/ch17-02-concurrency-with-async.html) | `join!`, `select!`, task spawning, async concurrency patterns |
| `working-with-futures` | [§17.3](https://doc.rust-lang.org/book/ch17-03-more-futures.html) | Working with any number of futures, `Pin`, composition |
| `streams` | [§17.4](https://doc.rust-lang.org/book/ch17-04-streams.html) | `Stream` trait, async iteration, processing sequences |
| `async-traits` | [§17.5](https://doc.rust-lang.org/book/ch17-05-traits-for-async.html) | Traits for async: `Future`, `IntoFuture`, async in trait definitions |
| `futures-tasks-threads` | [§17.6](https://doc.rust-lang.org/book/ch17-06-futures-tasks-threads.html) | When to use futures vs tasks vs threads, runtime architecture |

> ⚠️ **Edition note**: This chapter is **not** in the No Starch Press 2nd edition paperback. It was added in the 2024 online edition.

</details>

<details>
<summary><strong>Ch 18 — Object-Oriented Programming Features of Rust</strong> (3 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `characteristics-of-oo` | [§18.1](https://doc.rust-lang.org/book/ch18-01-what-is-oo.html) | Encapsulation with `pub`/private, objects as structs + impl |
| `trait-objects` | [§18.2](https://doc.rust-lang.org/book/ch18-02-trait-objects.html) | `dyn Trait`, `Box<dyn Draw>`, dynamic dispatch vs static dispatch, object safety |
| `state-pattern` | [§18.3](https://doc.rust-lang.org/book/ch18-03-oo-design-patterns.html) | Traditional state pattern, encoding states as types (typestate pattern) |

> 💡 **Python dev note**: Rust doesn't have inheritance. Instead of `class Dog(Animal)`, use traits: `impl Animal for Dog`. Composition over inheritance.

</details>

<details>
<summary><strong>Ch 19 — Patterns and Matching</strong> (3 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `all-the-places` | [§19.1](https://doc.rust-lang.org/book/ch19-01-all-the-places-for-patterns.html) | `match`, `if let`, `while let`, `for`, `let`, function parameters — all pattern positions |
| `refutability` | [§19.2](https://doc.rust-lang.org/book/ch19-02-refutability.html) | Irrefutable patterns (always match) vs refutable patterns (might fail) |
| `pattern-syntax` | [§19.3](https://doc.rust-lang.org/book/ch19-03-pattern-syntax.html) | Destructuring structs/enums/tuples, `..` for rest, match guards, `@` bindings, `\|` in patterns |

</details>

<details>
<summary><strong>Ch 20 — Advanced Features</strong> (5 exercises)</summary>

| Exercise | Section | Concepts Practiced |
|----------|---------|-------------------|
| `unsafe-rust` | [§20.1](https://doc.rust-lang.org/book/ch20-01-unsafe-rust.html) | `unsafe` blocks, dereferencing raw pointers, calling unsafe functions, FFI with `extern "C"` |
| `advanced-traits` | [§20.2](https://doc.rust-lang.org/book/ch20-02-advanced-traits.html) | Associated types vs generics, default type parameters, operator overloading, fully qualified syntax |
| `advanced-types` | [§20.3](https://doc.rust-lang.org/book/ch20-03-advanced-types.html) | Newtype pattern, type aliases, never type `!`, dynamically sized types |
| `advanced-functions` | [§20.4](https://doc.rust-lang.org/book/ch20-04-advanced-functions-and-closures.html) | Function pointers `fn(i32) -> i32`, returning closures `Box<dyn Fn()>` |
| `macros` | [§20.5](https://doc.rust-lang.org/book/ch20-05-macros.html) | `macro_rules!` declarative macros, procedural macros, custom `derive`, attribute-like macros |

</details>

<details>
<summary><strong>Ch 21 — Final Project: Building a Multithreaded Web Server</strong> (single project)</summary>

The capstone project — building a web server from scratch using everything learned:

- §21.1 — Building a single-threaded web server (TCP listener, HTTP parsing)
- §21.2 — Turning it into a multithreaded server (thread pool)
- §21.3 — Graceful shutdown and cleanup

```bash
cargo run -p web-server
# Then open http://127.0.0.1:7878 in your browser
```
</details>

---

## 🚀 How to Use This Repo

```bash
# Clone
git clone https://github.com/0x-sxmeer/rust-learning.git
cd rust-learning

# Run any exercise by package name
cargo run -p variables-and-mutability
cargo run -p guessing-game
cargo run -p minigrep -- searchstring poem.txt

# Run ALL tests across the entire workspace
cargo test --workspace

# Lint everything (fail on warnings)
cargo clippy --workspace -- -D warnings

# Auto-format everything
cargo fmt --all

# Check if everything compiles (faster than build)
cargo check --workspace
```

### Commit Message Convention

```
feat(ch04): add ownership basics — move semantics and scope
fix(ch03):  correct type mismatch in data-types exercise
docs:       update README progress for Chapter 5
refactor:   extract helper function in minigrep
test(ch11): add integration tests for search functionality
style:      cargo fmt --all
```

---

## 🐍 Python → Rust Quick Reference

| Concept | Python | Rust |
|---------|--------|------|
| **Package manager** | `pip` | `cargo` |
| **Project config** | `pyproject.toml` | `Cargo.toml` |
| **Locked deps** | `requirements.txt` / `uv.lock` | `Cargo.lock` |
| **Virtual env** | `venv` / `virtualenv` | Not needed — Cargo isolates automatically |
| **Run code** | `python main.py` | `cargo run` |
| **Add dependency** | `pip install requests` | `cargo add reqwest` |
| **Tests** | `pytest` | `cargo test` (built-in!) |
| **Formatter** | `black` / `ruff format` | `cargo fmt` |
| **Linter** | `pylint` / `ruff check` | `cargo clippy` |
| **Type checker** | `mypy` | The compiler itself |
| **Package registry** | PyPI | [crates.io](https://crates.io) |
| **REPL** | `python` | Not built-in (try [evcxr](https://github.com/evcxr/evcxr)) |
| **Classes** | `class Foo:` | `struct Foo` + `impl Foo` |
| **Inheritance** | `class B(A):` | Traits — `impl A for B` (composition > inheritance) |
| **Exceptions** | `try`/`except` | `Result<T,E>` + `?` operator (compile-time enforced!) |
| **Null** | `None` | `Option<T>` — `Some(v)` / `None` (no null pointer crashes) |
| **Memory** | Garbage collector | Ownership + borrowing (zero-cost, no GC pause!) |
| **Concurrency** | `threading` / `asyncio` | `std::thread` / `async`/`.await` |
| **Docstrings** | `"""..."""` | `///` doc comments (Markdown!) |
| **List comprehension** | `[x*2 for x in list]` | `list.iter().map(\|x\| x*2).collect()` |

---

## 📚 Resources

| Resource | Type | Link |
|----------|------|------|
| **The Rust Programming Language** | 📖 Official Book | [doc.rust-lang.org/book](https://doc.rust-lang.org/book/) |
| **Interactive Rust Book** | 🎓 With Quizzes | [rust-book.cs.brown.edu](https://rust-book.cs.brown.edu) |
| **Rust by Example** | 💻 Code-First | [doc.rust-lang.org/rust-by-example](https://doc.rust-lang.org/rust-by-example/) |
| **Rustlings** | 🏋️ Small Exercises | [github.com/rust-lang/rustlings](https://github.com/rust-lang/rustlings) |
| **Rust Playground** | 🧪 Try Online | [play.rust-lang.org](https://play.rust-lang.org/) |
| **Standard Library Docs** | 📘 API Reference | [doc.rust-lang.org/std](https://doc.rust-lang.org/std/) |
| **Crates.io** | 📦 Package Registry | [crates.io](https://crates.io) |
| **This Week in Rust** | 📰 Newsletter | [this-week-in-rust.org](https://this-week-in-rust.org/) |
| **Rust Cheat Sheet** | 📋 Quick Reference | [cheats.rs](https://cheats.rs/) |
| **Blessed.rs** | ⭐ Curated Crates | [blessed.rs](https://blessed.rs/) |

---

## ⚙️ CI/CD

Every push to `main` automatically runs [GitHub Actions](.github/workflows/rust.yml):

| Step | Command | What It Checks |
|------|---------|----------------|
| ✅ Compile | `cargo check --workspace` | Does every crate compile? |
| ✅ Test | `cargo test --workspace` | Do all tests pass? |
| ✅ Lint | `cargo clippy --workspace -- -D warnings` | Is the code idiomatic? |
| ✅ Format | `cargo fmt --all -- --check` | Is formatting consistent? |

---

## 📄 Book Edition Note

This repo follows the **2024 Edition** of The Rust Programming Language:

| Feature | No Starch Press 2nd Ed. | Online 2024 Edition (this repo) |
|---------|------------------------|--------------------------------|
| Chapters | 20 chapters | **21 chapters** |
| Async coverage | ❌ Not included | ✅ Chapter 17 (6 sections) |
| `let...else` | ❌ Not covered | ✅ Covered in §6.3 |
| Rust edition | `edition = "2021"` | `edition = "2024"` |
| Chapter numbering (17+) | OOP=17, Patterns=18, Advanced=19, Server=20 | OOP=18, Patterns=19, Advanced=20, Server=21 |

**If you have the paperback**: Chapters 1–16 map directly. For chapters 17+, use the [free online version](https://doc.rust-lang.org/book/) as your primary reference.

---

<p align="center">
  <sub>Started: September 2026 · Rust Edition 2024 · Built with 🦀 and determination</sub>
  <br>
  <sub>By <a href="https://github.com/0x-sxmeer">@0x-sxmeer</a> — Python dev becoming a Rustacean</sub>
</p>
