# Go Operators Overview

In Go, **operators** are symbols used to perform operations on values or variables. They are grouped into **arithmetic, assignment, comparison, logical, and bitwise operators**.

---

## 1. Arithmetic Operators

Used for mathematical calculations.

| Operator | Name           | Example | Description              |
| -------- | -------------- | ------- | ------------------------ |
| `+`      | Addition       | `x + y` | Adds two values          |
| `-`      | Subtraction    | `x - y` | Subtracts y from x       |
| `*`      | Multiplication | `x * y` | Multiplies x and y       |
| `/`      | Division       | `x / y` | Divides x by y           |
| `%`      | Modulus        | `x % y` | Remainder after division |
| `++`     | Increment      | `x++`   | Increases x by 1         |
| `--`     | Decrement      | `x--`   | Decreases x by 1         |

**Example:**

```go
package main
import "fmt"

func main() {
    a := 15 + 25
    fmt.Println(a) // 40
}
```

---

## 2. Assignment Operators

Used to assign or modify values of variables.

| Operator | Example   | Same As      |      |        |    |
| -------- | --------- | ------------ | ---- | ------ | -- |
| `=`      | `x = 5`   | `x = 5`      |      |        |    |
| `+=`     | `x += 3`  | `x = x + 3`  |      |        |    |
| `-=`     | `x -= 3`  | `x = x - 3`  |      |        |    |
| `*=`     | `x *= 3`  | `x = x * 3`  |      |        |    |
| `/=`     | `x /= 3`  | `x = x / 3`  |      |        |    |
| `%=`     | `x %= 3`  | `x = x % 3`  |      |        |    |
| `&=`     | `x &= 3`  | `x = x & 3`  |      |        |    |
| `        | =`        | `x           | = 3` | `x = x | 3` |
| `^=`     | `x ^= 3`  | `x = x ^ 3`  |      |        |    |
| `>>=`    | `x >>= 3` | `x = x >> 3` |      |        |    |
| `<<=`    | `x <<= 3` | `x = x << 3` |      |        |    |

**Example:**

```go
x := 10
x += 5
fmt.Println(x) // 15
```

---

## 3. Comparison Operators

Used to compare two values. Returns a **boolean** (`true` or `false`).

| Operator | Example  | Description              |
| -------- | -------- | ------------------------ |
| `==`     | `x == y` | Equal to                 |
| `!=`     | `x != y` | Not equal to             |
| `>`      | `x > y`  | Greater than             |
| `<`      | `x < y`  | Less than                |
| `>=`     | `x >= y` | Greater than or equal to |
| `<=`     | `x <= y` | Less than or equal to    |

**Example:**

```go
x, y := 5, 3
fmt.Println(x > y) // true
```

---

## 4. Logical Operators

Used to combine or reverse **boolean expressions**.

| Operator | Name        | Example              |            |        |   |        |
| -------- | ----------- | -------------------- | ---------- | ------ | - | ------ |
| `&&`     | Logical AND | `x < 5 && x < 10`    |            |        |   |        |
| `        |             | `                    | Logical OR | `x < 5 |   | x < 4` |
| `!`      | Logical NOT | `!(x < 5 && x < 10)` |            |        |   |        |

**Example:**

```go
x := 4
fmt.Println(x < 5 && x < 10) // true
fmt.Println(!(x < 5 && x < 10)) // false
```

---

## 5. Bitwise Operators

Operate on **binary representations** of numbers.

| Operator | Name        | Example  | Description                                |    |                                        |
| -------- | ----------- | -------- | ------------------------------------------ | -- | -------------------------------------- |
| `&`      | AND         | `x & y`  | Sets bit to 1 if both bits are 1           |    |                                        |
| `        | `           | OR       | `x                                         | y` | Sets bit to 1 if at least one bit is 1 |
| `^`      | XOR         | `x ^ y`  | Sets bit to 1 if only one of the bits is 1 |    |                                        |
| `<<`     | Left shift  | `x << 2` | Shifts bits left, filling with zeros       |    |                                        |
| `>>`     | Right shift | `x >> 2` | Shifts bits right, sign-extended           |    |                                        |

**Example:**

```go
x := 5  // 0101 in binary
y := 3  // 0011 in binary
fmt.Println(x & y)  // 1 (0001)
fmt.Println(x | y)  // 7 (0111)
fmt.Println(x ^ y)  // 6 (0110)
```

---

