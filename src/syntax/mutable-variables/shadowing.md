# Shadowing in Rust

In Rust, **shadowing** allows you to declare a new variable with the same name as a previous one. This new variable *shadows* the previous one, meaning the old variable is no longer accessible after the new one is introduced.

Shadowing is different from mutability, and it's a powerful feature for transforming data without needing mutability.



## Example

```rust
fn main() {
    let x = 5;
    let x = x + 1; // shadows the previous x
    let x = x * 2; // shadows again

    println!("The value of x is: {x}"); // Output: 12
}
```
In this example:

-   First, `x` is `5`.
    
-   Then `x + 1` becomes `6`, shadowing the original `x`.
    
-   Finally, `x * 2` becomes `12`, shadowing the second `x`.

**Shadowing vs. Mutability**
```rust
fn main() {
    let mut y = 5;
    y = y + 1; // OK because y is mutable

    let z = 5;
    let z = z + 1; // OK because this is shadowing
}
```
Key differences:

-   `mut` allows _changing_ a variable's value.
    
-   Shadowing allows _redefining_ a variable, even changing its type.

**Changing Types with Shadowing**
```rust
fn main() {
    let spaces = "   ";
    let spaces = spaces.len(); // Now spaces is a number!

    println!("Number of spaces: {spaces}"); // Output: 3
}
```

**When to Use Shadowing**

-   When transforming a variable step-by-step.
    
-   When changing the type of a variable (e.g., from `&str` to `usize`).
    
-   When you want to avoid making a variable mutable.

 
<b> Summary</b>

-   Shadowing lets you declare a new variable with the same name.
    
-   It's different from `mut` — it creates a _new binding_, not modifies the original.
    
-   You can change types with shadowing.
    
-   It's useful for cleaner, more functional-style code.
