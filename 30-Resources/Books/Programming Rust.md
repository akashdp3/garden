---
tags:
  - rust
  - programming
  - technical-book
---

# Programming Rust

## Book Info

**Medium:** Book
**Status:** Reading

## Related Zettelkasten Notes

- [[Type inference improves code readability]]
- [[Ownership eliminates garbage collection overhead]]

---

## Chapter 3: Fundamental Types

`Rust`programming language is designed around types. Unlike dynamically typed languages like `javascript` & `python`, Rust requires developer to specify types for each variable in each step. But it becomes less tedius because of 2 features

- **Type Inference:** Rust infers / figures out type for any variable most of time by checking types of the surrounding (for example, function arguments, return types, assignment values). But when rust compiler determines it cannot infer the type correctly, it forces the developer to specify type explicitly.
​
​For example, suppose this is sample rust program to create a vector

    ```rust
    fn build_vector() -> Vec<i32> {
      let mut v::Vec<i32> = Vec::<i32>::new();
      v.push(10i32);
      v.push(20i32);
    
      v
    }
    ```



    The above program is cluttered and most importantly, readability takes a hit because of repetitive type declaration. ​The same program can be written as:

    ```rust
    fn build_vector() -> Vec<i32> {
      let mut v = Vec::new();
      v.push(10);
      v.push(20);
    
      v
    }
    ```

    Rust infers types for variable `v` based on return type of function `build_vector`.

- **Generic Functions:** In `Python` & `Javascript`, a function argument takes value of any type. The mentioned function can operate on any value of any type. This flexibility makes things easier for programmers to reuse the same function with different types. But this makes error detection difficult.
​
​Let's consider the following program which take a vector as argument and returns the first element of the vecto​r.

    ```rust
    fn first_element(list: &Vec<u16>) -> u16 {
      list[0]
    }
    
    fn main() {
      let list = vec![1, 2, 3];
    
      assert!(1 == first_element(&list));
    }
    ```



    Since rust requires type for function arguments & return types, the above code only runs for vector of `u16` type. This program is going to panic when it is passed with value of different type. Rust solves it with `generic types`. The above program can look something like this with generic types​:

    ```rust
    fn first_element<T: Clone>(list: &Vec<T>) -> T {
      list[0].clone()
    }
    
    fn main() {
      let list1 = vec![1, 2, 3];
      let list2 = vec!["a", "b"];
    
      assert!(1 == first_element(&list1));
      assert!("a" == first_element(&list2));
    }
    ```



### Numeric Types

| Size (bits)  | Unsighed Integer | Signed Integer | Floating Point |
| :----------- | :--------------- | :------------- | :------------- |
| 8            | u8               | i8             |                |
| 16           | u16              | i16            |                |
| 32           | u32              | i32            | f32            |
| 64           | u64              | i64            | f64            |
| 128          | u128             | i128           |                |
| Machine word | usize            | isize          |                |

**Points to remember**

- `usize` & `isize` are dependent on the machine configuration. For 32-bit configuration, these size is going to be of 32 bit long where as for 64-bit configuration machines, these size is going to be 64 bit long.

- Rust does not convert between types unless specified otherwise. If a function expects `f64` as argument and we are passing `f32` , then compiler is going to throw an error. We need to explicitly convert the value before calling the method i.e. `floating_point_method(32 as f64)`.



### The bool type

- Just like other programming language, `bool` has two values i.e. `true` & `false`. Any comparison expression is going to produce a bool value.

- Just like number types, rust does not do automatic type conversion between other types and bool type. For example, in `javascript` , empty string, number 0 etc evaluate to `false`. But rust expects a expression in `if` block instead of a value. 

- Although a bool types needs a single bit to represent iin memory, rust uses an entire byte (8 bit) for a bool value, so that you can create a point to it.
​

```rust
assert_eq!(false, 0); // INVALID
assert_eq!(false as i32, 0); // VALID

assert_eq!(0, false); // INVALID
assert_eq!(0 as bool, false); // INVALID since rust does not allow to type cast from numbers to bool. We need use actual expression
assert_eq!(0 == 1, false); // VALID
```


### Characters, Strings & String Literals

`Rust` have 3 different types for character/strings.

- `char`: This represents a single character in rust. The compiler stores the value as it is in memory as 4 byte value.
- `String`: This type represents a owned string stored in heap. The compiler stores it in UTF-8 format in memory i.e. as compared to `char`, this value is encoded and stored in UTF-8 format.
- `&str`: This type represents a reference value to a `String`. Rust just points to a memory address for this type, it does not store anything in heap.
​
```rust
let a = 'a'; // a is of char type when value is wrapped in single quote (ex. 'x')
let b = "hello"; // b is of &str type. Values declared with double quote is treated as &str
let c = String::from("hello"); // c is of String type. It is explicitly declared with String or to_string() method.
```

### Tuples

A `tuple` is a sequence of elements, separated by comma and surrounded by parentheses.

```rust
let x: (&str, &str) = ("Name", "Akash")
```

### Array

```rust
let sample_array = [1,2,3]; // declaring array directly;
let sample_array2 = [true; 1000] // declaring a default value with a fixed length
```



## Chapter 4: Ownership and Moves

Many programming language use garbage collector to manage memory. Basically languages like `java`, `python` & `javascript` runs a program called garbage collector which periodically (not exactly. different programming language implements differently) checks if any variable is not reachable anymore and if it finds any, it frees up the memory. It takes control of memory management with some performance overhead. On scale, it becomes a problem as you can see spikes in system's performance whenever `garbage collection` runs. On the other hand, there are programming languages like `C`, `C++` which gives control of memory allocation & deallocation to developer. While it gives control to developer, it also pass the risk to humans to not to make a mistake like a `dangling pointers`.

Rust solves this problem by introducing a new concept called `ownership`. It eliminates the need for a `garbage collector` while introducing a steeper learning curve.

Memory management has two important characteristics:
- Memory needs to be freed promptly.
- Rust guarantees **no undefined behaviour.** So no pointer to a freed memory should exist.



