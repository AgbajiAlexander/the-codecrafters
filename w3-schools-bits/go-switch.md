# Go `switch` Statement

The `switch` statement in Go lets you **select one of many code blocks to execute** based on a value. Unlike some languages, **Go automatically breaks after the matched case**, so you don’t need a `break` statement.

---

## 1. Single-Case `switch`

**Syntax:**

```go
switch expression {
case x:
    // code block if expression == x
case y:
    // code block if expression == y
default:
    // code block if no case matches
}
```

**How it works:**

1. Evaluate the expression once.
2. Compare it with each `case` value.
3. Execute the code block of the first matching case.
4. If no case matches, execute the `default` block (optional).

**Example:**

```go
package main
import "fmt"

func main() {
    day := 4

    switch day {
    case 1:
        fmt.Println("Monday")
    case 2:
        fmt.Println("Tuesday")
    case 3:
        fmt.Println("Wednesday")
    case 4:
        fmt.Println("Thursday")
    case 5:
        fmt.Println("Friday")
    case 6:
        fmt.Println("Saturday")
    case 7:
        fmt.Println("Sunday")
    default:
        fmt.Println("Invalid day")
    }
}
```

**Output:**

```
Thursday
```

---

## 2. Multi-Case `switch`

Go allows **multiple values in a single case** using commas.

**Syntax:**

```go
switch expression {
case x, y:
    // executes if expression == x or expression == y
case v, w:
    // executes if expression == v or expression == w
default:
    // executes if no case matches
}
```

**Example:**

```go
package main
import "fmt"

func main() {
    day := 5

    switch day {
    case 1, 3, 5:
        fmt.Println("Odd weekday")
    case 2, 4:
        fmt.Println("Even weekday")
    case 6, 7:
        fmt.Println("Weekend")
    default:
        fmt.Println("Invalid day number")
    }
}
```

**Output:**

```
Odd weekday
```

---

✅ **Key Points About Go `switch`:**

* No `break` needed; only the first matching case executes.
* `default` is optional.
* Cases can have **multiple values**.
* You can use `switch` with **expressions**, **variables**, or even **types**.

---

If you want, I can also show **switch with conditions** (like `switch true`) which makes `switch` behave like multiple `if-else if` statements—a very common Go pattern.

Do you want me to show that?
