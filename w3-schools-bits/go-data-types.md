# Go Data Types

## Overview

Data types define the kind of data a variable can store and its size in memory. Go is **statically typed**, which means a variable can only store values of its declared type.

Go has three main categories of data types:

1. **Boolean (`bool`)** – true or false
2. **Numeric** – integers, floating-point numbers, and complex numbers
3. **String (`string`)** – sequence of characters

---

## Boolean Data Type

Boolean values represent `true` or `false`. The default value is `false`.

### Example:

```go id="6w3nox"
var b1 bool = true
var b2 = true
var b3 bool
b4 := true

fmt.Println(b1) // true
fmt.Println(b2) // true
fmt.Println(b3) // false
fmt.Println(b4) // true
```

Boolean variables are mainly used in conditional statements.

---

## Integer Data Types

### Signed Integers

Can store both positive and negative numbers. Default type is `int`.

| Type  | Size               | Range                                                   |
| ----- | ------------------ | ------------------------------------------------------- |
| int   | Platform-dependent | -2³¹ to 2³¹-1 (32-bit), -2⁶³ to 2⁶³-1 (64-bit)          |
| int8  | 8 bits             | -128 to 127                                             |
| int16 | 16 bits            | -32,768 to 32,767                                       |
| int32 | 32 bits            | -2,147,483,648 to 2,147,483,647                         |
| int64 | 64 bits            | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |

### Unsigned Integers

Can store only non-negative numbers.

| Type   | Size               | Range                                                                 |
| ------ | ------------------ | --------------------------------------------------------------------- |
| uint   | Platform-dependent | 0 to 4,294,967,295 (32-bit), 0 to 18,446,744,073,709,551,615 (64-bit) |
| uint8  | 8 bits             | 0 to 255                                                              |
| uint16 | 16 bits            | 0 to 65,535                                                           |
| uint32 | 32 bits            | 0 to 4,294,967,295                                                    |
| uint64 | 64 bits            | 0 to 18,446,744,073,709,551,615                                       |

### Example:

```go id="2k0v3x"
var x int = 500
var y uint = 4500
fmt.Printf("Type: %T, value: %v\n", x, x)
fmt.Printf("Type: %T, value: %v\n", y, y)
```

---

## Float Data Types

Used to store decimal numbers. Default type is `float64`.

| Type    | Size    | Range                 |
| ------- | ------- | --------------------- |
| float32 | 32 bits | -3.4e+38 to 3.4e+38   |
| float64 | 64 bits | -1.7e+308 to 1.7e+308 |

### Example (float32):

```go id="q8s4nv"
var x float32 = 123.78
var y float32 = 3.4e+38
fmt.Printf("Type: %T, value: %v\n", x, x)
fmt.Printf("Type: %T, value: %v\n", y, y)
```

### Example (float64):

```go id="n7z1dk"
var x float64 = 1.7e+308
fmt.Printf("Type: %T, value: %v\n", x, x)
```

---

## String Data Type

Strings store sequences of characters and are enclosed in double quotes (`""`).

### Example:

```go id="m9v5bt"
var txt1 string = "Hello!"
var txt2 string
txt3 := "World 1"

fmt.Printf("Type: %T, value: %v\n", txt1, txt1)
fmt.Printf("Type: %T, value: %v\n", txt2, txt2)
fmt.Printf("Type: %T, value: %v\n", txt3, txt3)
```

**Output:**

```
Type: string, value: Hello!
Type: string, value:
Type: string, value: World 1
```

---

## Summary

Go enforces static typing for safety and clarity. Its core data types—`bool`, numeric (`int`, `float`), and `string`—allow you to handle most programming needs. Choosing the right type ensures correct storage, calculation, and performance.
