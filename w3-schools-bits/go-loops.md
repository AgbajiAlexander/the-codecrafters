# Go `for` Loops

In Go, the `for` loop is the **only loop** available and is used to repeat a block of code multiple times. Each repetition is called an **iteration**.

---

## 1. Basic `for` Loop

**Syntax:**

```go
for init; condition; post {
    // code to execute
}
```

* **init** – initializes the loop counter
* **condition** – loop runs as long as this is `true`
* **post** – executed at the end of each iteration (usually increments the counter)

**Example: Print numbers 0 to 4**

```go
package main
import "fmt"

func main() {
    for i := 0; i < 5; i++ {
        fmt.Println(i)
    }
}
```

**Output:**

```
0
1
2
3
4
```

---

## 2. Custom Step

You can change the increment using `+=` or `-=`:

**Example: Count by tens**

```go
package main
import "fmt"

func main() {
    for i := 0; i <= 100; i += 10 {
        fmt.Println(i)
    }
}
```

**Output:**

```
0
10
20
30
...
100
```

---

## 3. `continue` and `break`

* **`continue`** skips the current iteration and moves to the next.
* **`break`** stops the loop completely.

**Skip 3 using `continue`:**

```go
for i := 0; i < 5; i++ {
    if i == 3 {
        continue
    }
    fmt.Println(i)
}
```

**Output:**

```
0
1
2
4
```

**Stop at 3 using `break`:**

```go
for i := 0; i < 5; i++ {
    if i == 3 {
        break
    }
    fmt.Println(i)
}
```

**Output:**

```
0
1
2
```

---

## 4. Nested Loops

You can place a loop inside another loop:

```go
adj := [2]string{"big", "tasty"}
fruits := [3]string{"apple", "orange", "banana"}

for i := 0; i < len(adj); i++ {
    for j := 0; j < len(fruits); j++ {
        fmt.Println(adj[i], fruits[j])
    }
}
```

**Output:**

```
big apple
big orange
big banana
tasty apple
tasty orange
tasty banana
```

---

## 5. Using `range`

The `range` keyword simplifies iteration over **arrays, slices, or maps**. It returns both **index** and **value**.

**Example: Iterate array with index and value**

```go
fruits := [3]string{"apple", "orange", "banana"}

for idx, val := range fruits {
    fmt.Printf("%v\t%v\n", idx, val)
}
```

**Output:**

```
0    apple
1    orange
2    banana
```

* Use `_` to ignore index or value:

```go
// Only values
for _, val := range fruits {
    fmt.Println(val)
}

// Only indexes
for idx, _ := range fruits {
    fmt.Println(idx)
}
```

---

✅ **Tips:**

* You can omit all three parts of a `for` loop and use it like a `while` loop:

```go
i := 0
for i < 5 {
    fmt.Println(i)
    i++
}
```

---

