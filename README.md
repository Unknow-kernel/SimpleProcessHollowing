# Simple Process Hollowing

This project is a **simple** shellcode injector for Windows. It creates a suspended process, allocates memory in that process, writes the shellcode into the memory, and then creates a remote thread to execute the shellcode.

## Features

- Creates a target process in suspended mode.
- Allocates executable memory in the target process.
- Writes the shellcode into the allocated memory.
- Creates a remote thread in the target process to execute the shellcode.

## Compilation Instructions

- ```cmake -S . -B build```
- ```cmake --build build```

# Usage

Prepare your shellcode and save it in a file named shellcode.bin. This file should be placed in the same directory as the executable or provide the full path to the shellcode file in the code.

By default, the program will look for a file named shellcode.bin in the current directory where the executable is located. If the shellcode file is located elsewhere, update the shellcodePath variable in the main function with the correct path to your shellcode.bin file.