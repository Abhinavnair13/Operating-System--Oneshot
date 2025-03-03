# Program vs Process vs Thread

## 1. What is a Program?
- A **program** is a set of instructions written in a programming language that
performs a specific task or set of tasks. It is typically stored in a file on disk
and represents an executable entity.
- Programs can be compiled or
interpreted, and they serve as a blueprint for the execution of tasks on a
computer system.
### Characteristics:
- A **static entity** stored on disk.
- Contains instructions but does not execute by itself.
- Requires execution to become a **process**.

### Example:
A **Microsoft Word executable file (`winword.exe`)** stored on disk is a **program**. When you double-click it, it becomes a **process**.

---

## 2. What is a Process?
- A **process** is an instance of a program in execution. When a program is
loaded into memory and executed, it becomes a process.
- It is an independent entity with its own memory space, resources, and execution
context. It has its own program counter, stack, and variables.
- Processes are
managed by the operating system, and each process runs in its own
protected memory space.
- Processes can be concurrent and communicate
with each other through inter-process communication mechanisms.
### Characteristics:
- A **dynamic entity** that runs in memory.
- Has a **unique Process ID (PID)**.
- Allocates system resources (memory, CPU time, I/O).
- Can have multiple **threads** running within it.

### Example:
When you open **Google Chrome**, it creates multiple **processes**, such as:
- A main process for the browser.
- Separate processes for each tab.
- Additional processes for plugins and extensions.

---

## 3. What is a Thread?
- A **thread** is a unit of execution within a process.
- It represents a sequence of
instructions that can be scheduled and executed independently. Threads
share the same memory space and resources within a process.
- Multiple
threads within a process can run concurrently, allowing for parallel execution
of tasks.
- Threads within the same process can communicate and share data
more easily than inter process communication. Each thread has its own program counter and stack
### Characteristics:
- A **lightweight unit of execution** within a process.
- Shares memory with other threads in the same process.
- Can run in **parallel** for better performance.
- Faster to create and switch compared to processes.

### Types of Threads:
1. **User-Level Threads** – Managed by user applications, not the OS.
2. **Kernel-Level Threads** – Managed by the OS, offering better system integration.

### Example:
When you open **Microsoft Word**:
- One **thread** handles user input (keyboard/mouse).
- Another **thread** performs spell checking.
- A separate **thread** autosaves your document in the background.

---

## Key Differences:

| Feature | Program | Process | Thread |
|---------|---------|---------|--------|
| Definition | A set of instructions | An executing instance of a program | A smaller unit within a process |
| Execution | Not running | Running in memory | Runs within a process |
| Resource Sharing | No resources | Has its own memory & resources | Shares memory with other threads in the process |
| Overhead | No overhead | High (needs more memory, CPU) | Low (lightweight) |
| Example | `chrome.exe` file | Chrome's process for a tab | Multiple threads handling rendering, user input |

---

## Real-World Analogy:
Imagine a **restaurant**:
- A **program** is like a **recipe book** (instructions stored but not running).
- A **process** is like a **chef cooking a dish using a recipe** (executing instructions).
- A **thread** is like the **chef’s hands** working on different parts of the dish (cutting, frying, plating) simultaneously.

---
