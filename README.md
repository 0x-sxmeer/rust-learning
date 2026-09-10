# 🦀 Rust Learning Journey

Following **"The Rust Programming Language"** by Steve Klabnik and Carol Nichols.
Book: https://doc.rust-lang.org/book/

## 📂 Structure (Mapped to Book Chapters)

| Folder | Book Chapter | Topics | Status |
|--------|-------------|--------|--------|
| `ch02-guessing-game/` | Ch 2 | First project — I/O, random, match | 📅 Planned |
| `ch03-common-concepts/` | Ch 3 | Variables, data types, functions, control flow | 🔄 In Progress |
| `ch04-ownership/` | Ch 4 | Ownership, borrowing, slices, lifetimes | 📅 Planned |
| `ch05-structs/` | Ch 5 | Defining structs, methods, associated functions | 📅 Planned |
| `ch06-enums/` | Ch 6 | Enums, Option, match, if let | 📅 Planned |
| `ch07-modules/` | Ch 7 | mod, pub, use, crate structure | 📅 Planned |
| `ch08-collections/` | Ch 8 | Vec, String, HashMap | 📅 Planned |
| `ch09-error-handling/` | Ch 9 | panic!, Result, ? operator | 📅 Planned |
| `ch10-generics-traits/` | Ch 10 | Generics, traits, lifetimes | 📅 Planned |
| `ch11-testing/` | Ch 11 | Unit tests, integration tests | 📅 Planned |
| `ch12-io-project/` | Ch 12 | Building a CLI program (minigrep) | 📅 Planned |
| `projects/` | Beyond the book | Real-world practice projects | 📅 Planned |

## 📝 Exercises per Chapter

### Ch 3 — Common Programming Concepts
- [x] `variables-and-mutability` — let, mut, const, shadowing
- [ ] `data-types` — integers, floats, bools, chars, tuples, arrays
- [ ] `functions` — parameters, return values, expressions vs statements
- [ ] `control-flow` — if/else, loops, while, for

### Ch 4 — Understanding Ownership
- [ ] `ownership-basics` — move semantics, scope, String type
- [ ] `references-and-borrowing` — &T, &mut T, rules of references
- [ ] `slices` — string slices, array slices

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/0x-sxmeer/rust-learning.git
cd rust-learning

# Run a specific exercise
cargo run -p variables-and-mutability
cargo run -p data-types

# Run all tests
cargo test

# Lint and format
cargo clippy --workspace
cargo fmt --all
```

## 📚 Resources

- [The Rust Programming Language (The Book)](https://doc.rust-lang.org/book/)
- [Rust by Example](https://doc.rust-lang.org/rust-by-example/)
- [Rustlings](https://github.com/rust-lang/rustlings)

## 🐍 Background

Python developer transitioning to Rust — documenting the journey chapter by chapter.
