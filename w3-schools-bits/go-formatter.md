# Go Formatting Verbs

## Overview

Formatting verbs are special placeholders used with the `Printf()` function to control how values are displayed. They allow you to format output in a more precise and readable way.

---

## General Formatting Verbs

These verbs work with most data types:

* **`%v`** → Prints the value in its default format
* **`%#v`** → Prints the value in Go syntax format
* **`%T`** → Prints the data type
* **`%%`** → Prints a percent sign

### Example:

```go id="y4j9e3"
var i = 15.5
var txt = "Hello World!"

fmt.Printf("%v\n", i)
fmt.Printf("%#v\n", i)
fmt.Printf("%v%%\n", i)
fmt.Printf("%T\n", i)

fmt.Printf("%v\n", txt)
fmt.Printf("%#v\n", txt)
fmt.Printf("%T\n", txt)
```

---

## Integer Formatting Verbs

These are used specifically for integers:

* **`%b`** → Binary (base 2)
* **`%d`** → Decimal (base 10)
* **`%+d`** → Decimal with sign
* **`%o`** → Octal (base 8)
* **`%O`** → Octal with `0o` prefix
* **`%x`** → Hexadecimal (lowercase)
* **`%X`** → Hexadecimal (uppercase)
* **`%#x`** → Hexadecimal with `0x` prefix

---

## Width and Padding

You can control spacing and alignment:

* **`%4d`** → Right-aligned, width of 4
* **`%-4d`** → Left-aligned, width of 4
* **`%04d`** → Pads with zeros

### Example:

```go id="pjq9x2"
var i = 15

fmt.Printf("%b\n", i)
fmt.Printf("%d\n", i)
fmt.Printf("%+d\n", i)
fmt.Printf("%o\n", i)
fmt.Printf("%O\n", i)
fmt.Printf("%x\n", i)
fmt.Printf("%X\n", i)
fmt.Printf("%#x\n", i)
fmt.Printf("%4d\n", i)
fmt.Printf("%-4d\n", i)
fmt.Printf("%04d\n", i)
```

---

## Summary

Formatting verbs in Go give you full control over how data is displayed. Whether you want to show types, change number bases, or align output, `Printf()` with formatting verbs makes it possible.
