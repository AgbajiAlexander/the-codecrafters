# Go Constants

## What are Constants?

Constants are values that cannot be changed once they are defined. They are declared using the `const` keyword and are read-only throughout the program.

---

## Declaring Constants

### Basic Syntax:

```go
const NAME type = value
```

The value must be assigned at the time of declaration.

### Example:

```go id="u4k6r9"
const PI = 3.14
```

---

## Constant Rules

* Must be assigned a value when declared
* Cannot be changed later in the program
* Follow the same naming rules as variables
* Often written in **UPPERCASE** for easy identification
* Can be declared inside or outside functions

---

## Types of Constants

### 1. Typed Constants

These have a specific type defined:

```go id="7q7b2m"
const A int = 1
```

---

### 2. Untyped Constants

These do not have a fixed type. Go decides the type based on the value:

```go id="pq1n8o"
const A = 1
```

---

## Immutability (Cannot Change Value)

Once declared, constants cannot be modified:

```go id="t3zzv9"
const A = 1
A = 2 // Error: cannot assign to A
```

---

## Multiple Constants Declaration

You can group constants together for better readability:

```go id="g3l5du"
const (
  A int = 1
  B = 3.14
  C = "Hi!"
)
```

---

## Summary

Constants are used when you have values that should remain fixed throughout your program. They improve code safety and readability by preventing accidental changes. Go supports both typed and untyped constants, making them flexible and easy to use.
