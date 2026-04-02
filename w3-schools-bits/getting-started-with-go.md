# Go Getting Started

## Getting Started with Go

To begin using Go, you need two main tools:

* A **text editor or IDE** to write your code (e.g., VS Code)
* A **Go compiler** to convert your code into an executable program

---

## Installing Go

Go can be downloaded from the official website. After installation, you can verify it worked by running:

```bash
go version
```

This command shows the installed version of Go, confirming everything is set up correctly.

---

## Choosing an IDE

An IDE (Integrated Development Environment) helps you write, run, and debug code efficiently.

Popular options include:

* Visual Studio Code (VS Code)
* Vim
* Eclipse
* Notepad

VS Code is a great choice for beginners because it is simple and powerful.

---

## Setting Up VS Code for Go

To configure VS Code for Go development:

1. Open VS Code
2. Go to Extensions (Ctrl + Shift + X)
3. Search for **Go** and install the official extension
4. Open Command Palette (Ctrl + Shift + P)
5. Run: **Go: Install/Update Tools**
6. Install all recommended tools

Now your environment is ready.

---

## Creating Your First Go Program

### Step 1: Initialize a Go Module

Run this command in the terminal:

```bash
go mod init example.com/hello
```

This sets up your project structure (you’ll understand it better later).

---

### Step 2: Write Your First Code

Create a file named `helloworld.go` and add:

```go
package main

import "fmt"

func main() {
  fmt.Println("Hello World!")
}
```

---

### Step 3: Run the Program

In the terminal, run:

```bash
go run helloworld.go
```

Output:

```
Hello World!
```

---

## Summary

Getting started with Go involves installing the language, setting up an IDE like VS Code, and writing your first simple program. Once your environment is ready, you can quickly build and run Go applications.
