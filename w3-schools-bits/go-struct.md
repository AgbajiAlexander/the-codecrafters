# Go Structs

## Overview

In Go, a **struct** (short for structure) is a composite data type used to group **multiple values of different types** into a single variable. Unlike arrays, which store values of the **same type**, structs can store a collection of heterogeneous data.

Structs are commonly used to represent **records** or **objects**.

---

## Declaring a Struct

Use the `type` and `struct` keywords:

```go
type StructName struct {
    member1 datatype
    member2 datatype
    member3 datatype
}
```

**Example:**

```go
type Person struct {
    name   string
    age    int
    job    string
    salary int
}
```

> Tip: Struct members can have different data types. For example, `name` and `job` are `string`, while `age` and `salary` are `int`.

---

## Accessing Struct Members

Use the **dot operator (`.`)** to access or assign struct fields:

```go
var pers1 Person
pers1.name = "Hege"
pers1.age = 45
pers1.job = "Teacher"
pers1.salary = 6000
```

**Example Program:**

```go
package main

import "fmt"

type Person struct {
    name   string
    age    int
    job    string
    salary int
}

func main() {
    var pers1, pers2 Person

    // Pers1 details
    pers1.name = "Hege"
    pers1.age = 45
    pers1.job = "Teacher"
    pers1.salary = 6000

    // Pers2 details
    pers2.name = "Cecilie"
    pers2.age = 24
    pers2.job = "Marketing"
    pers2.salary = 4500

    // Print info
    fmt.Println("Name:", pers1.name, "Age:", pers1.age, "Job:", pers1.job, "Salary:", pers1.salary)
    fmt.Println("Name:", pers2.name, "Age:", pers2.age, "Job:", pers2.job, "Salary:", pers2.salary)
}
```

**Output:**

```
Name: Hege Age: 45 Job: Teacher Salary: 6000
Name: Cecilie Age: 24 Job: Marketing Salary: 4500
```