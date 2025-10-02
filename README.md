# Java-- Compiler Project

This project consisted in developing a working compiler for **Java--**, a simplified but realistic subset of the Java programming language.  
The compiler was built step by step over three checkpoints, covering all main phases of a modern compiler:

---

## Features Implemented

### 1. **Lexical & Syntactic Analysis (CP1)**
- Implemented using **ANTLR4** to define the Java-- grammar.
- Built the **Abstract Syntax Tree (AST)**.
- Constructed the **Symbol Table** with support for classes, methods, variables, and imports.
- Ensured parsing error detection and reporting.

### 2. **Semantic Analysis & Intermediate Representation (CP2)**
- Implemented semantic checks, including:
  - Type checking of expressions and assignments.
  - Method existence and argument verification.
  - Correct use of `this`, arrays, and varargs.
- Annotated the AST with type information for later phases.
- Generated **OLLIR** (Object-Oriented Low-Level Intermediate Representation):
  - Class and method structure.
  - Assignments and arithmetic operations.
  - Method invocation.
- Began translation into **Jasmin** (assembly for the JVM).

### 3. **Code Generation & Optimizations (CP3)**
- Completed OLLIR generation for:
  - Conditionals (`if`, `if-else`).
  - Loops (`while`).
  - Arrays and varargs.
- Generated **Jasmin bytecode** with correct `.limit stack` and `.limit locals`.
- Used **low-cost instructions** (e.g., `iload_0` instead of `iload 0`, `iinc` for increments).
- Implemented optimizations:
  - **Constant propagation**.
  - **Constant folding**.
  - **Register allocation** (`-r` option).
- Produced fully functional `.class` files executable on the JVM.

---

## Tech Stack
- **ANTLR4** for parsing.
- **Java** for compiler implementation.
- **OLLIR** as intermediate representation.
- **Jasmin** for bytecode generation.


## Group Members 

- Alexandre Felgueiras de Morais (up201906049@fe.up.pt)
- Nuno Jorge da Costa Ramos (nunoramos2142@gmail.com)
- Tiago Rocha Silveira Pires (up202008790@fe.up.pt)

## Work Distribution

- Alexandre Felgueiras de Morais - 27.5 %
- Nuno Jorge da Costa Ramos - 27.5 %
- Tiago Rocha Silveira Pires - 45 %
