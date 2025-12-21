
Type inference allows the compiler to deduce types automatically, reducing visual clutter while maintaining type safety.

## Key Insight

In statically-typed languages like Rust, explicit type annotations can make code verbose and harder to read. Type inference solves this by letting the compiler figure out types from context (function signatures, assignments, operations).

## Example

Instead of:
```rust
let mut v: Vec<i32> = Vec::<i32>::new();
v.push(10i32);
```

Type inference allows:
```rust
let mut v = Vec::new();
v.push(10);
```

The compiler infers `Vec<i32>` from the return type and push operations.

## Related Concepts

- [[Generic functions enable code reuse]]
- [[Static typing catches errors early]]
- Trade-off: Less explicit but more maintainable

## Source

Extracted from [[30-Resources/Books/Programming Rust]]

---

*Tags: #programming #rust #type-systems*
