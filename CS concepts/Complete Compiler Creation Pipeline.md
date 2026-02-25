## 1️⃣ Preprocessing (Optional but Common)

Used in languages like C/C++.

- Handles `#include`
    
- Macro expansion
    
- Conditional compilation
    

Example:  
`#define PI 3.14` → replaced before compilation

---

## 2️⃣ Lexical Analysis (Lexer / Scanner)

**Input:** Source code (text)  
**Output:** Tokens

Converts characters → meaningful symbols.

Example:

int x = 5;

Tokens:

KEYWORD(int)  
IDENTIFIER(x)  
ASSIGN(=)  
NUMBER(5)  
SEMICOLON

Purpose:

- Remove whitespace/comments
    
- Detect invalid characters
    
- Produce token stream
    

---

## 3️⃣ Syntax Analysis (Parser)

**Input:** Tokens  
**Output:** AST (Abstract Syntax Tree)

The parser:

- Checks grammar rules
    
- Validates syntax
    
- Builds tree structure
    

Example AST for `x = 5 + 3`:

      =  
     / \  
    x   +  
       / \  
      5   3

Parser types:

- Recursive descent
    
- LL
    
- LR
    
- Pratt parser (common in modern compilers)
    

---

## 4️⃣ Semantic Analysis

Very important step.

Checks:

- Type checking
    
- Variable declared?
    
- Function arguments match?
    
- Scope rules
    
- Return type correctness
    

Example error:

int x = "hello";   ❌ type mismatch

Also builds:

- Symbol table
    
- Scope tree
    

---

## 5️⃣ AST Optimization (Optional)

Some compilers optimize at AST level:

- Constant folding  
    `2 + 3` → `5`
    
- Dead code elimination
    
- Simplifications
    

---

## 6️⃣ Intermediate Representation (IR)

Now the AST is lowered into a lower-level representation.

Why IR?

- Machine-independent
    
- Easier to optimize
    
- Closer to assembly
    

There are many IRs:

- Three-address code
    
- SSA (Static Single Assignment)
    
- LLVM IR
    

Example LLVM IR:

%1 = add i32 5, 3

LLVM uses **SSA form** internally.

---

# 🔥 Where LLVM Fits

## 7️⃣ LLVM Optimizer

LLVM runs many optimization passes:

- Constant propagation
    
- Dead code elimination
    
- Loop unrolling
    
- Inlining
    
- Strength reduction
    
- Common subexpression elimination
    

Optimization levels:

- `-O0`
    
- `-O1`
    
- `-O2`
    
- `-O3`
    
- `-Os`
    

---

## 8️⃣ Backend (Code Generation)

Converts optimized IR → Machine Code.

Responsibilities:

- Instruction selection
    
- Register allocation
    
- Stack frame management
    
- Calling conventions
    
- Target architecture handling
    

Example targets:

- x86
    
- ARM
    
- RISC-V
    

---

## 9️⃣ Assembler

Machine instructions → Object file (.o)

---

## 🔟 Linker

Final step.

Combines:

- Your object files
    
- Standard libraries
    
- Runtime
    

Produces:

- Executable file
    

Example:

main.o + libc → a.out

---

# 🔁 Full Pipeline (Clean Version)

Source Code  
   ↓  
Preprocessor  
   ↓  
Lexer (Tokens)  
   ↓  
Parser  
   ↓  
AST  
   ↓  
Semantic Analysis  
   ↓  
IR Generation  
   ↓  
IR Optimization (LLVM passes)  
   ↓  
Code Generation (Backend)  
   ↓  
Assembly  
   ↓  
Object File  
   ↓  
Linker  
   ↓  
Executable

---

# 🧠 Extra Advanced Steps (Modern Compilers)

Some compilers also include:

### ✔ Control Flow Graph (CFG)

Built from IR to analyze program flow.

### ✔ Data Flow Analysis

Used for advanced optimizations.

### ✔ SSA Construction

LLVM converts IR into SSA form.

### ✔ Runtime / Standard Library Integration

---

# 🏗 If YOU Want to Build a Compiler (Practical Order)

For a student project:

1. Design grammar
    
2. Write lexer
    
3. Write parser
    
4. Build AST
    
5. Add semantic analysis
    
6. Generate LLVM IR
    
7. Use LLVM to compile to native code
    

That’s exactly how **Clang** works inside the LLVM Project.

---

# 🧩 Real-World Example

- LLVM Project = Backend infrastructure
    
- Clang = Frontend for C/C++
    
- Rust compiler uses LLVM as backend
    
- Swift also uses LLVM
    

---
