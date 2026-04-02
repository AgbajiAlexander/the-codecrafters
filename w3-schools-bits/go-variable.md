# Go Variables

## What are Variables?

Variables are used to store data values in a program. Each variable has a type that determines what kind of data it can hold, such as numbers, text, or true/false values.

---

## Common Variable Types

* **int** → whole numbers (e.g., 10, -5)
* **float32** → decimal numbers (e.g., 3.14)
* **string** → text (e.g., "Hello")
* **bool** → true or false

---

## Declaring Variables

### 1. Using `var`

You can declare a variable by specifying its name, type, and value:

```go
var name string = "John"
```

You can also let Go figure out the type:

```go
var name = "John"
```

---

### 2. Using `:=`

This is a shorter way to declare variables, where Go automatically determines the type:

```go
age := 25
```

⚠️ Note: You must assign a value when using `:=`.

---

## Declaring Variables with Values

```go
var student1 string = "John"
var student2 = "Jane"
x := 2
```

Go automatically infers the type for `student2` and `x`.

---

## Multiple Variable Declaration

### Same Type:

```go
var a, b, c int = 1, 2, 3
```

### Different Types:

```go
var a, b = 6, "Hello"
c, d := 7, "World"
```

---

## Variable Declaration in a Block

You can group variables for better readability:

```go
var (
  a int
  b int = 1
  c string = "hello"
)
```

---

## Variable Naming Rules

* Must start with a letter or underscore `_`
* Cannot start with a number
* Can contain letters, numbers, and underscores
* Case-sensitive (`age`, `Age`, `AGE` are different)
* Cannot contain spaces
* Cannot use Go keywords

---

## Naming Styles

To improve readability, use:

* **Camel Case** → `myVariableName`
* **Pascal Case** → `MyVariableName`
* **Snake Case** → `my_variable_name`

---

## Summary

Variables are essential for storing and managing data in Go. You can declare them using `var` or `:=`, and Go makes things easier by automatically determining types when possible. Clear naming and proper structure make your code easier to read and maintain.
