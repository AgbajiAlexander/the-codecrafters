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


# Go Slices: Access, Modify, Append, and Copy

## Access Slice Elements

Use **indexes** to access elements. Indexes start at `0`.

```go
package main
import "fmt"

func main() {
    prices := []int{10, 20, 30}
    fmt.Println(prices[0]) // first element
    fmt.Println(prices[2]) // third element
}
```

**Output:**

```
10
30
```

---

## Change Slice Elements

Assign a new value to a specific index to modify it:

```go
package main
import "fmt"

func main() {
    prices := []int{10, 20, 30}
    prices[2] = 50
    fmt.Println(prices)
}
```

**Output:**

```
[10 20 50]
```

---

## Append Elements to a Slice

Use `append()` to add elements at the end:

```go
package main
import "fmt"

func main() {
    myslice := []int{1, 2, 3, 4, 5, 6}
    myslice = append(myslice, 20, 21)
    fmt.Println(myslice)
}
```

**Output:**

```
[1 2 3 4 5 6 20 21]
```

---

## Append One Slice to Another

Use `...` to append all elements from one slice to another:

```go
package main
import "fmt"

func main() {
    s1 := []int{1, 2, 3}
    s2 := []int{4, 5, 6}
    s3 := append(s1, s2...)
    fmt.Println(s3)
}
```

**Output:**

```
[1 2 3 4 5 6]
```

---

## Change the Length of a Slice

You can **reslice** or **append** to modify a slice’s length:

```go
package main
import "fmt"

func main() {
    arr := [6]int{9, 10, 11, 12, 13, 14}
    s := arr[1:5]       // slice of array
    fmt.Println(s, len(s), cap(s)) // [10 11 12 13] 4 5

    s = arr[1:3]        // reslice
    fmt.Println(s, len(s), cap(s)) // [10 11] 2 5

    s = append(s, 20, 21, 22, 23) // append to increase length
    fmt.Println(s, len(s), cap(s)) // [10 11 20 21 22 23] 6 10
}
```

---

## Copy Slices (Memory Efficiency)

`copy(dest, src)` copies elements from `src` to `dest`. Useful to create a smaller slice from a large array:

```go
package main
import "fmt"

func main() {
    numbers := []int{1,2,3,4,5,6,7,8,9,10,11,12,13,14,15}
    needed := numbers[:5]               // select first 5 elements
    numbersCopy := make([]int, len(needed))
    copy(numbersCopy, needed)

    fmt.Println(numbersCopy)
    fmt.Println(len(numbersCopy), cap(numbersCopy))
}
```

**Output:**

```
[1 2 3 4 5]
5 5
```

---

### ✅ Key Points

* Slice elements are **accessed and changed** via indexes.
* Use `append()` to **grow slices**.
* Use `append(slice1, slice2...)` to **merge slices**.
* Use `copy()` to **create a new slice with its own underlying array** for memory efficiency.
* Slices have **length** (`len()`) and **capacity** (`cap()`), which can change with reslicing and appending.
