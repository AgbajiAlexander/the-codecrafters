# Go Conditional Statements

Conditional statements in Go allow you to execute code **based on whether a condition is true or false**. Go uses the usual **comparison** and **logical operators**:

* **Comparison operators:** `<`, `<=`, `>`, `>=`, `==`, `!=`
* **Logical operators:** `&&` (AND), `||` (OR), `!` (NOT)

---

## 1. `if` Statement

The `if` statement executes a block of code only if a condition is true.

**Syntax:**

```go
if condition {
    // code executes if condition is true
}
```

**Example:**

```go
package main
import "fmt"

func main() {
    x := 20
    y := 18
    if x > y {
        fmt.Println("x is greater than y")
    }
}
```

**Output:**

```
x is greater than y
```

---

## 2. `if-else` Statement

The `else` block executes if the `if` condition is false.

**Syntax:**

```go
if condition {
    // if true
} else {
    // if false
}
```

**Example:**

```go
package main
import "fmt"

func main() {
    temperature := 14
    if temperature > 15 {
        fmt.Println("It is warm out there")
    } else {
        fmt.Println("It is cold out there")
    }
}
```

**Output:**

```
It is cold out there
```

**Important:** The closing brace of `if` must be immediately followed by `else` on the same line:

```go
} else { // correct
```

---

## 3. `else if` Statement

Use `else if` to check multiple conditions in sequence.

**Syntax:**

```go
if condition1 {
    // code if condition1 is true
} else if condition2 {
    // code if condition1 is false but condition2 is true
} else {
    // code if both conditions are false
}
```

**Example:**

```go
package main
import "fmt"

func main() {
    time := 22
    if time < 10 {
        fmt.Println("Good morning.")
    } else if time < 20 {
        fmt.Println("Good day.")
    } else {
        fmt.Println("Good evening.")
    }
}
```

**Output:**

```
Good evening.
```

**Example (checking equality):**

```go
a := 14
b := 14
if a < b {
    fmt.Println("a is less than b.")
} else if a > b {
    fmt.Println("a is more than b.")
} else {
    fmt.Println("a and b are equal.")
}
```

**Output:**

```
a and b are equal.
```

**Note:** If multiple conditions are true, only the **first true condition** executes.

---

## 4. Nested `if` Statements

`if` statements can be placed inside other `if` statements.

**Syntax:**

```go
if condition1 {
    if condition2 {
        // executed if both condition1 and condition2 are true
    }
}
```

**Example:**

```go
package main
import "fmt"

func main() {
    num := 20
    if num >= 10 {
        fmt.Println("Num is more than 10.")
        if num > 15 {
            fmt.Println("Num is also more than 15.")
        }
    } else {
        fmt.Println("Num is less than 10.")
    }
}
```

**Output:**

```
Num is more than 10.
Num is also more than 15.
```

---

Conditional statements are the backbone of decision-making in Go. You can combine them with **logical operators** (`&&`, `||`, `!`) to handle complex conditions efficiently.

