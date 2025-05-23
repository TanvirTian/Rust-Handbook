# Constants
in Rust, constants are values that are bound to a name and are not allowed to change. They are evaluated at compile time and must have a type annotation.
Constants can be declared in any scope, including the global scope, which makes them useful for values that many parts of the code need to know about.

## Declaring Constants

Use the `const` keyword, followed by the name in `SCREAMING_SNAKE_CASE`, a type, and a value:
```rust
const MAX_POINTS: u32 = 100_000;
```
### Rules for Constants

-   You must specify the type.
    
-   The value must be a constant expression, not the result of a function that runs at runtime.
    
-   Constants are valid for the entire lifetime of a program.
    
-   Naming convention is UPPERCASE with underscores.

 ## const vs let
| Feature         | `const`          | `let`                |
| --------------- | ---------------- | -------------------- |
| Mutability      | Always immutable | Mutable with `mut`   |
| Type annotation | Required         | Inferred or optional |
| Evaluated at    | Compile time     | Runtime              |
| Scope           | Global or local  | Mostly used locally  |

**Example**:
```rust
const SECONDS_IN_MINUTE: u32 = 60;

fn main() {
    println!("One minute has {} seconds.", SECONDS_IN_MINUTE);
}
```

## const vs static

Both `const` and `static` define values that live for the entire duration of the program, but:

-   `const` is inlined wherever it's used.
    
-   `static` has a **fixed memory location** and can be mutable (with `unsafe`).

```rust
static APP_NAME: &str = "RustyApp";
```


