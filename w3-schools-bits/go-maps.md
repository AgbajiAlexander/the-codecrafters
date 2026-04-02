# Go Maps

## Overview

A **map** in Go is an **unordered collection of key:value pairs**. Maps are **changeable**, **do not allow duplicate keys**, and their **length** can be found using `len()`. The default value of a map is `nil`.

Maps reference an underlying **hash table**, so changes in one map variable can affect another if they reference the same map.

---

## Creating Maps

### Using `var` or `:=`

```go id="1b2zqx"
var a = map[string]string{"brand":"Ford","model":"Mustang","year":"1964"}
b := map[string]int{"Oslo":1,"Bergen":2,"Trondheim":3,"Stavanger":4}
```

### Using `make()`

```go id="1g3klv"
a := make(map[string]string)
a["brand"] = "Ford"
a["model"] = "Mustang"
a["year"] = "1964"

b := make(map[string]int)
b["Oslo"] = 1
b["Bergen"] = 2
```

### Creating an Empty Map

```go id="1j4fpo"
var a map[string]string        // nil map
a = make(map[string]string)    // empty, safe to write
```

> Writing to a nil map causes a runtime panic.

---

## Key & Value Types

### Allowed Key Types

* Booleans
* Numbers
* Strings
* Arrays
* Pointers
* Structs
* Interfaces (with equality support)

> Invalid key types: slices, maps, functions

### Allowed Value Types

* Any type

---

## Accessing Map Elements

```go id="2k6tvc"
val := a["brand"]
fmt.Println(val) // Output: Ford
```

---

## Adding and Updating Elements

```go id="2m7hcv"
a["year"] = "1970"   // update
a["color"] = "red"   // add
```

---

## Removing Elements

```go id="2n8bwc"
delete(a, "year")
```

---

## Checking Key Existence

```go id="2p9lmc"
val, ok := a["brand"]  // ok is true if key exists
_, exists := a["model"] // only check existence
```

---

## Maps are References

Changes in one variable affect another if both reference the same map:

```go id="2r1dgc"
b := a
b["year"] = "1970"
fmt.Println(a["year"]) // Output: 1970
```

---

## Iterating Over Maps

```go id="2s2hmc"
for k, v := range a {
    fmt.Printf("%v : %v, ", k, v)
}
```

> Maps are unordered. To iterate in a specific order, use a separate slice to define the order:

```go id="2t3kpc"
order := []string{"one", "two", "three", "four"}
for _, key := range order {
    fmt.Printf("%v : %v, ", key, a[key])
}
```

---
