# Prism Compiler

A simple compiler written in C++ that compiles a small custom programming language into x86-64 NASM assembly on Linux.

## Features

- Integer literals
- Variables (`let`)
- Variable reassignment
- Arithmetic operators (`+`, `-`, `*`, `/`, `%`)
- Operator precedence parsing
- Nested scopes
- `if`, `elif`, and `else` statements
- Single-line (`//`) and multi-line (`/* */`) comments
- Parser error messages with line numbers
- Generates x86-64 NASM assembly

## Building

### Requirements

- Linux
- C++20 compatible compiler
- CMake
- NASM
- GNU Linker (`ld`)

### Build

```bash
git clone https://github.com/harsha-praveen/Prism.git
cd Prism

cmake -S . -B build
cmake --build build
```

The executable will be generated in the `build/` directory.

## Usage

Compile a Prism source file:

```bash
cd build
./prism ../test.pr
```

The compiler automatically:

- Generates `out.asm`
- Assembles it with NASM
- Links it using `ld`
- Produces an executable named `out`

Run the generated executable:

```bash
../out
```

Check the program's exit code:

```bash
echo $?
```