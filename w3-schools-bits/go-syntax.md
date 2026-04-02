# Go Syntax

## Overview

A Go program is made up of a few essential parts that define how the code is structured and executed. These include:

* Package declaration
* Imported packages
* Functions
* Statements and expressions

---

## Basic Example

```go
package main
import "fmt"

func main() {
  fmt.Println("Hello World!")
}
```

---

## Explanation

* **Package Declaration (`package main`)**
  Every Go file belongs to a package. The `main` package is special because it is where program execution starts.

* **Import Statement (`import "fmt"`)**
  This brings in external packages. The `fmt` package is used for formatting and printing output.

* **Function (`func main()`)**
  The `main` function is the entry point of the program. Any code inside it will run when the program starts.

* **Print Statement (`fmt.Println`)**
  This is used to display output to the console. In this case, it prints `"Hello World!"`.

---

## Go Statements

* A statement is an instruction that the program executes (e.g., `fmt.Println("Hello World!")`)
* In Go, statements are usually separated by:

  * A new line (automatically adds a semicolon)
  * Or explicitly using `;` (rarely needed)

---

## Important Syntax Rules

* **Whitespace matters for readability**, but not execution
* **Curly braces `{}` must follow the function declaration on the same line**

Incorrect:

```go
func main()
{
  fmt.Println("Hello World!")
}
```

Correct:

```go
func main() {
  fmt.Println("Hello World!")
}
```

---

## Key Takeaways

* Every Go program starts in the `main` package
* The `main()` function is where execution begins
* Code structure must follow strict formatting rules
* Go automatically handles semicolons at the end of lines

---

## Summary

Go syntax is simple and strict. Once you understand how packages, imports, and functions work together, writing Go programs becomes straightforward and easy to manage.
