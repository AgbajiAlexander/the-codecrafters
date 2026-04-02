# Go Slices

## Overview

Slices are **dynamic, flexible versions of arrays** in Go.
Like arrays, slices store **multiple values of the same type**, but unlike arrays, their **length can grow or shrink** as needed.

---

## Creating a Slice

### 1. Using `[]datatype{values}`

```go id="slice1"
myslice := []int{}           // empty slice, length 0, capacity 0
myslice2 := []int{1, 2, 3}   // slice with 3 elements, length 3, capacity 3
```

You can check **length** and **capacity** with `len()` and `cap()`:

```go id="slice2"
fmt.Println(len(myslice2)) // 3
fmt.Println(cap(myslice2)) // 3
```

---

### 2. Creating a Slice from an Array

Slices can be made by slicing an array using `[start:end]`:

```go id="slice3"
arr := [6]int{10, 11, 12, 13, 14, 15}
myslice := arr[2:4]  // includes index 2, up to but not including index 4

fmt.Printf("myslice = %v\n", myslice)
fmt.Printf("length = %d\n", len(myslice))
fmt.Printf("capacity = %d\n", cap(myslice))
```

**Output:**

```id="slice4"
myslice = [12 13]
length = 2
capacity = 4
```

> **Note:** Capacity is the number of elements from the starting index to the end of the array.

---

### 3. Using the `make()` Function

Slices can also be created with `make()`:

```go id="slice5"
myslice1 := make([]int, 5, 10) // length 5, capacity 10
myslice2 := make([]int, 5)     // length 5, capacity defaults to 5

fmt.Printf("myslice1 = %v, len=%d, cap=%d\n", myslice1, len(myslice1), cap(myslice1))
fmt.Printf("myslice2 = %v, len=%d, cap=%d\n", myslice2, len(myslice2), cap(myslice2))
```

**Output:**

```id="slice6"
myslice1 = [0 0 0 0 0], len=5, cap=10
myslice2 = [0 0 0 0 0], len=5, cap=5
```

---

## Summary

* **Slices are flexible arrays**; their length can change at runtime.
* **Length** (`len`) = number of elements currently in the slice.
* **Capacity** (`cap`) = maximum size slice can grow without reallocation.
* Can be created directly, from arrays, or using `make()`.
* Provide more flexibility than arrays while retaining type safety.
