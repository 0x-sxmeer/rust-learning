# 🔑 Ownership Cheatsheet

## The Three Rules
1. Each value has exactly **one owner**
2. When the owner goes out of scope, the value is **dropped**
3. There can be **either** one `&mut T` **or** any number of `&T` — never both

## Quick Reference
```
let s = String::from("hello");  // s owns the String
let s2 = s;                     // s2 now owns it, s is INVALID
let s3 = s2.clone();            // Deep copy, both valid
```

*Fill in as you learn Chapter 4!*
