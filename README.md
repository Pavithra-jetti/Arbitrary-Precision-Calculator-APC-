# Arbitrary Precision Calculator in C

## Overview

This project is an **Arbitrary Precision Calculator (APC) developed in C**. It performs addition, subtraction, multiplication, and division on integers of unlimited size — beyond the range of standard C data types — by representing each number as a **doubly linked list** of digits.

The project demonstrates the practical use of **dynamic memory allocation, doubly linked lists, pointer-to-pointer manipulation, and modular multi-file compilation using a Makefile** in C.

## Features

* Addition, subtraction, multiplication, and division of arbitrarily large integers
* Supports signed operands (leading `+` or `-`)
* Digit-by-digit arithmetic using doubly linked lists without standard integer overflow limits
* Input validation for operand format and supported operators
* Correct sign handling for different combinations of positive and negative operands
* Dynamic memory management with proper cleanup
* Modular design — each operation (`add`, `sub`, `mul`, `div`) is implemented in a separate file
* Build automation using `makefile`

## Technologies Used

* **Programming Language:** C
* **Compiler:** GCC
* **Platform:** Linux / Windows
* **Concepts:** Doubly Linked Lists, Dynamic Memory Allocation, Pointers, Modular Programming
* **Libraries:** `stdio.h`, `stdlib.h`, `string.h`, `ctype.h`
* **Build Tool:** `make`

## Project Structure

```text
Arbitrary-Precision-Calculator-in-C/
│
├── main.c
├── apc.h
├── dll.c
├── add.c
├── add.h
├── sub.c
├── sub.h
├── mul.c
├── mul.h
├── div.c
├── div.h
├── makefile
├── README.md
└── .gitignore
```

### File Description

| File         | Description                                                                                 |
| ------------ | ------------------------------------------------------------------------------------------- |
| `main.c`     | Program entry point; validates arguments and operands and dispatches the selected operation |
| `apc.h`      | Doubly linked list (`dlist`) structure and shared function declarations                     |
| `dll.c`      | Doubly linked list helper functions such as insert, print, free, and sign extraction        |
| `add.c`      | Addition logic and handling of mixed-sign operands                                          |
| `add.h`      | Function declarations for addition                                                          |
| `sub.c`      | Subtraction logic for linked-list represented numbers                                       |
| `sub.h`      | Function declarations for subtraction                                                       |
| `mul.c`      | Multiplication logic for linked-list represented numbers                                    |
| `mul.h`      | Function declarations for multiplication                                                    |
| `div.c`      | Division logic for linked-list represented numbers                                          |
| `div.h`      | Function declarations for division                                                          |
| `makefile`   | Build rules to compile all modules and create the executable                                |
| `README.md`  | Project documentation                                                                       |
| `.gitignore` | Specifies generated files that should not be uploaded to GitHub                             |

## How to Run

### 1. Clone the Repository

Open **Command Prompt / Terminal** and run:

```bash
git clone <your-github-repository-link>
```

### 2. Open the Project Directory

```bash
cd Arbitrary-Precision-Calculator-in-C
```

### 3. Compile the Program

Using the makefile:

```bash
make
```

Or manually:

```bash
gcc main.c add.c sub.c mul.c div.c dll.c -o APC.out
```

### 4. Run the Program

```bash
./APC.out <Operand1> <Operator> <Operand2>
```

**Example:**

```bash
./APC.out 12345 + 67890
```

Supported operators:

```text
+   -   x   /
```

## Run

The calculator takes exactly three command-line arguments:

```text
./APC.out <Operand1> <Operator> <Operand2>
```

Each operand can optionally start with `+` or `-`.

**Example:**

```bash
./APC.out 999999999999999999999 + 888888888888888888888
```

The result is calculated using linked-list based arithmetic and displayed on the console.

To clean up build artifacts:

```bash
make clean
```

## Learning Outcomes

* Gained practical understanding of arbitrary-precision arithmetic algorithms
* Learned to represent and manipulate large numbers using doubly linked lists
* Practiced dynamic memory allocation and pointer-to-pointer techniques
* Improved understanding of sign handling and arithmetic edge cases
* Learned to structure a multi-file C project using separate `.c` and `.h` modules
* Practiced build automation using `make` and a `makefile`
* Improved debugging and problem-solving skills

## Author

**Pavithra Jetti**
