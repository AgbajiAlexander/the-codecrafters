# Go Comments

## What are Comments?

Comments are parts of the code that are ignored during execution. They are mainly used to explain what the code does, improve readability, or temporarily disable code during testing.

---

## Types of Comments in Go

Go supports two types of comments:

* Single-line comments
* Multi-line comments

---

## Single-line Comments

Single-line comments start with `//`.
Anything written after `//` on the same line will not be executed.

### Example:

```go
// This is a comment
package main

import "fmt"

func main() {
  // This prints a message
  fmt.Println("Hello World!")
}
```

You can also place comments at the end of a line:

```go
fmt.Println("Hello World!") // This is a comment
```

---

## Multi-line Comments

Multi-line comments start with `/*` and end with `*/`.
Everything between them is ignored by the compiler.

### Example:

```go
package main

import "fmt"

func main() {
  /* This code prints
     Hello World to the screen */
  fmt.Println("Hello World!")
}
```

---

## When to Use Each

* Use `//` for short, quick explanations
* Use `/* */` for longer descriptions or detailed notes

---

## Summary

Comments are essential for writing clear and maintainable Go code. They help explain logic, make code easier to understand, and allow developers to test changes without deleting code.
