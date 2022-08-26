# `roman-literals`

`roman-literals` provides an easy way to write integer literals using Roman
numerals.

# Features

* Supports all integers from I to MMMCMXCIX (1 to 3999)
* Type inference with the [`roman!`] macro
* Zero cost!

# Usage

* Type aliases like [`iXXXII`] are provided to replace primitive types like
[`i32`].

* Using the [`roman!`] macro, the type of the literal is automatically
inferred, with [`iXXXII`] being the default. The macro also supports
negative numbers; see [`roman!`] for more details.

* Constants are also provided, such as [`III_uXXXII`]. These constants are
all suffixed with their type.

# Examples

```rust
use roman_literals::*;

let forty_two: uXXXII = roman!(XLII);
assert_eq!(forty_two, 42);

let negative_3999: iXVI = roman!(-MMMCMXCIX);
assert_eq!(negative_3999, -3999);

let negative_300 = -CCC_iLXIV; // i64
assert_eq!(negative_300, -300);
```

# Why?

Why not?
