# 📦 `mutable variable` — Mutability in Rust

as i mentioned, variables are **immutable** by default. This means that once a value is assigned to a variable, it cannot be changed. However, sometimes you may need to modify a variable's value during execution. In such cases, you can declare the variable as **mutable** by using the `mut` keyword.

## Declaring Mutable Variables

To declare a **mutable variable** in Rust, simply add `mut` before the variable name.

### Example: Mutable Variables

```rust
fn main() {
    let mut x = 5; // mutable variable
    println!("x is: {}", x); // Output: x is: 5
    x = 10; // changing the value of x
    println!("Now, x is: {}", x); // Output: Now, x is: 10
}
```
🔎 **Line-by-line breakdown**:

-   `let mut x = 5;` — This declares a **mutable** variable `x` and assigns it the value `5`.
    
-   `x = 10;` — This changes the value of `x` from `5` to `10`.


### Why Use Mutability?

-   **Memory Safety**: By default, Rust prevents accidental changes to variables, which helps avoid bugs and ensures that the program’s state is predictable.
    
-   **Explicit Intent**: Declaring variables as `mut` makes it clear in the code that the variable is intended to be modified. This improves code readability and reduces confusion.

**Example: without Mutability**
```rust
fn main() {
    let x = 5; // immutable variable
    println!("x is: {}", x); // Output: x is: 5
    // x = 10; // This would cause an error: cannot assign twice to immutable variable
}
```

💡 **Key points to remember**:

-   In Rust, variables are immutable by default.
    
-   Use the `mut` keyword to make a variable mutable if you plan to change its value after initial assignment.

-   You cannot change the value of an immutable variable.
