# Go Functions

## Overview

A **function** in Go is a block of code designed to perform a specific task. Functions are **not executed automatically**; they run only when called. Functions can be reused multiple times and can accept input parameters and return values.

---

## Declaring a Function

Use the `func` keyword, followed by the function name, parentheses, and curly braces:

```go
func FunctionName() {
    // code to execute
}
```

**Example:**

```go
func myMessage() {
    fmt.Println("I just got executed!")
}
```

---

## Calling a Function

Call a function by its name followed by parentheses:

```go
myMessage()
```

Functions can be called multiple times:

```go
myMessage()
myMessage()
myMessage()
```

---

## Naming Rules

* Must start with a **letter**
* Can contain letters, numbers, and underscores (`A-z`, `0-9`, `_`)
* Case-sensitive
* No spaces
* Use descriptive names reflecting the function’s purpose

---

## Function Parameters and Arguments

Functions can accept **parameters** to receive input:

```go
func familyName(fname string) {
    fmt.Println("Hello", fname, "Refsnes")
}

func main() {
    familyName("Liam")  // "Liam" is the argument
}
```

Multiple parameters:

```go
func familyName(fname string, age int) {
    fmt.Println("Hello", age, "year old", fname, "Refsnes")
}

familyName("Liam", 3)
```

> ⚠️ Argument order and count must match the parameters.

---

## Function Return Values

To return a value, specify its type and use `return`:

```go
func add(x int, y int) int {
    return x + y
}

total := add(1, 2)
fmt.Println(total)  // Output: 3
```

### Named Return Values

```go
func add(x int, y int) (result int) {
    result = x + y
    return  // naked return
}
```

---

## Multiple Return Values

Functions can return multiple values:

```go
func myFunction(x int, y string) (result int, txt string) {
    result = x + x
    txt = y + " World!"
    return
}

a, b := myFunction(5, "Hello")
fmt.Println(a, b)  // Output: 10 Hello World!
```

Use `_` to ignore unwanted return values:

```go
_, b := myFunction(5, "Hello")
fmt.Println(b)  // Output: Hello World!
```

---

## Recursive Functions

A recursive function calls itself until a stop condition is met.

**Example 1: Counting**

```go
func testcount(x int) int {
    if x == 11 {
        return 0
    }
    fmt.Println(x)
    return testcount(x + 1)
}
testcount(1)
```

**Example 2: Factorial**

```go
func factorial(x float64) (y float64) {
    if x > 0 {
        y = x * factorial(x-1)
    } else {
        y = 1
    }
    return
}
fmt.Println(factorial(4))  // Output: 24
```

> Be careful with recursion to avoid infinite loops or excessive memory use.

---
