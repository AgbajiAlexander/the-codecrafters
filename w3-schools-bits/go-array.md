# Go Arrays

## Overview

Arrays in Go allow you to store **multiple values of the same type** in a single variable. This is useful for grouping related data without declaring separate variables.

Arrays in Go have a **fixed length**, which can either be defined explicitly or inferred by the compiler.

---

## Declaring Arrays

### Using the `var` keyword

```go id="yq7lkm"
var arr1 = [3]int{1, 2, 3}      // length explicitly defined
var arr2 = [...]int{4, 5, 6, 7} // length inferred
```

### Using `:=` shorthand

```go id="d3c4tb"
arr1 := [3]int{1, 2, 3}       // length explicitly defined
arr2 := [...]int{4, 5, 6, 7}  // length inferred
```

> **Note:** The length of the array determines how many elements it can store. Once defined, the length cannot be changed.

---

## Array Examples

### Example 1: Arrays with Defined Lengths

```go id="r6b7yw"
var arr1 = [3]int{1, 2, 3}
arr2 := [5]int{4, 5, 6, 7, 8}

fmt.Println(arr1)
fmt.Println(arr2)
```

**Output:**

```id="t4h5jq"
[1 2 3]
[4 5 6 7 8]
```

### Example 2: Arrays with Inferred Lengths

```go id="p9x8zl"
var arr1 = [...]int{1, 2, 3}
arr2 := [...]int{4, 5, 6, 7, 8}

fmt.Println(arr1)
fmt.Println(arr2)
```

**Output:**

```id="k3m7dn"
[1 2 3]
[4 5 6 7 8]
```

### Example 3: Array of Strings

```go id="m2v9qt"
var cars = [4]string{"Volvo", "BMW", "Ford", "Mazda"}
fmt.Print(cars)
```

**Output:**

```id="u8n6gh"
[Volvo BMW Ford Mazda]
```

---

## Summary

* Arrays store multiple values of the **same type** in one variable.
* Length is **fixed** and can be defined explicitly or inferred.
* Arrays can hold any data type: integers, floats, booleans, strings, etc.
* Access elements using index positions starting at `0`.
