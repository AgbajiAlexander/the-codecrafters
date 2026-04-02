# Go Output Functions

## Overview

Go provides built-in functions to display output to the console. The three main output functions are:

* `Print()`
* `Println()`
* `Printf()`

---

## The `Print()` Function

`Print()` outputs values using their default format and **does not automatically add spaces or new lines**.

### Example:

```go
var i, j string = "Hello", "World"
fmt.Print(i)
fmt.Print(j)
```

**Output:**

```
HelloWorld
```

---

## Adding New Lines

To move output to a new line, you can use `\n`:

```go
fmt.Print(i, "\n")
fmt.Print(j, "\n")
```

**Output:**

```
Hello
World
```

---

## Printing Multiple Values

You can print multiple values in one statement:

```go
fmt.Print(i, "\n", j)
```

---

## Adding Spaces

To add a space between values, include `" "`:

```go
fmt.Print(i, " ", j)
```

**Output:**

```
Hello World
```

---

## Behavior with Non-String Values

When printing non-string values, `Print()` automatically adds a space:

```go
var i, j = 10, 20
fmt.Print(i, j)
```

**Output:**

```
10 20
```

---

## Summary

The `Print()` function is useful for simple output. It gives you control over formatting, but you must manually add spaces or new lines when needed. For more automatic formatting, `Println()` and `Printf()` are often preferred.
