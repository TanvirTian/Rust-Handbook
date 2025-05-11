📦 `variable` — Rust Variables
---
In Rust, **variables** are used to store data for later use in your program. They are declared using the `let` keyword.

By default, **Rust variables are immutable** — meaning once a value is assigned, it cannot be changed. If you want to change the value of a variable later, you must explicitly make it **mutable** by adding `mut` before the variable name.
```rust
fn main() {
    let x = 5;//immutable variable
    println!("x is: {}", x);
}
```
🔎 Line-by-line breakdown:

.`let` creates a new variable.

.`x` is the variable name.

.`5` is the integer value assigned. 

.`println!` is a macro that prints text to the console.

💡 If you're not sure what a macro is, don’t worry! For now, just remember that `println!` is used to display text in the console.

You might be wondering about the `{}` inside the string:  
This is a placeholder. It gets replaced by the value of `x` when printed.
So the line:
```rust
println!("x is: {}", x);
```
will output:
```rust
x is: 5
```

