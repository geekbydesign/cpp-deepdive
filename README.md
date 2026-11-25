# C++ Deep Dive

A comprehensive guide to understanding C++ internals, memory management, STL implementation, compiler mechanisms, runtime behaviour, concurrency and advanced C++ concepts.

This repository focuses on understanding **how C++ works internally**, rather than just learning how to use its language features and standard library.

The objective is to develop a deep understanding of C++ by studying its internal mechanisms, implementing simplified versions of important standard library components and preparing for advanced C++ technical interviews.

---

## Objectives

- Understand how C++ language features work internally.
- Understand memory allocation, object lifetime and memory management.
- Explore the internal implementation of STL containers and algorithms.
- Understand smart pointers, reference counting and ownership management.
- Understand virtual functions, VTables and object memory layout.
- Explore copy semantics, move semantics and perfect forwarding.
- Understand templates, type erasure and compile-time mechanisms.
- Explore mutexes, atomics, synchronization and memory ordering.
- Understand compiler, linker, ABI and runtime mechanisms.
- Implement simplified versions of important C++ standard library components.
- Develop the ability to explain C++ internals during technical interviews.

---

## Learning Roadmap

The repository is organized into **18 levels**, covering C++ internals from fundamental memory concepts to advanced runtime mechanisms and interview-oriented implementation exercises.

### Level 1 — C++ Object Model and Memory Layout

- How C++ Objects Are Stored in Memory
- Stack vs Heap Internals
- Object Lifetime and Storage Duration
- Alignment, Padding and Memory Layout
- Object Construction and Destruction Internals
- Placement New and Manual Object Construction

### Level 2 — Pointers and Memory Management

- How Pointers Work Internally
- Pointer Arithmetic and Address Calculation
- How `new` and `delete` Work
- `malloc` vs `new` Internals
- Memory Allocation and Deallocation
- Memory Fragmentation
- Custom Memory Allocators
- Memory Pools and Object Pools

### Level 3 — Smart Pointer Internals

- How `unique_ptr` Works Internally
- How `shared_ptr` Works Internally
- Shared Pointer Control Block
- Reference Counting Mechanism
- How `weak_ptr` Works Internally
- Circular References and Memory Leaks
- Custom Deleters
- `make_unique` vs `make_shared`
- Implementing Custom Smart Pointers

### Level 4 — STL Container Internals

- How `std::vector` Works Internally
- Vector Size vs Capacity
- Vector Reallocation and Growth Strategy
- How `std::string` Works Internally
- Small String Optimization (SSO)
- How `std::deque` Works Internally
- How `std::list` Works Internally
- How `std::array` Works Internally
- How `std::forward_list` Works Internally

### Level 5 — Associative Container Internals

- How `std::map` Works Internally
- Red-Black Tree Implementation
- How `std::set` Works Internally
- How `std::multimap` and `std::multiset` Work
- How `std::unordered_map` Works Internally
- Hash Tables and Collision Resolution
- Hashing, Buckets and Load Factor
- Rehashing and Iterator Invalidation
- How `std::unordered_set` Works Internally

### Level 6 — STL Algorithms and Iterators

- How Iterators Work Internally
- Iterator Categories and Their Implementation
- Iterator Invalidation
- How `std::sort` Works Internally
- Introsort: Quick Sort, Heap Sort and Insertion Sort
- How `std::stable_sort` Works
- How `std::find`, `std::lower_bound` and `std::upper_bound` Work
- How `std::priority_queue` Works Internally
- Heap Implementation

### Level 7 — C++ Class and Object Internals

- How Virtual Functions Work
- VTable and VPtr Internals
- Virtual Function Dispatch
- Virtual Destructors Internals
- Multiple Inheritance and Object Layout
- Virtual Inheritance and Virtual Base Classes
- RTTI and `dynamic_cast` Internals
- Object Slicing
- CRTP and Static Polymorphism

### Level 8 — Copy, Move and Resource Management Internals

- Copy Constructor Internals
- Move Constructor Internals
- Move Assignment Internals
- `std::move` and `std::forward` Internals
- Perfect Forwarding
- Reference Collapsing
- Copy Elision and RVO
- Return Value Optimization
- Rule of Three, Five and Zero Internals

### Level 9 — Template and Compile-Time Internals

- How Templates Are Instantiated
- Template Specialization Internals
- Function Template Overload Resolution
- SFINAE
- Type Traits Internals
- `constexpr` and Compile-Time Evaluation
- Variadic Templates and Parameter Packs
- Fold Expressions
- Concepts: C++20 Overview

### Level 10 — Callable Objects and Type Erasure

- How Lambda Expressions Are Implemented
- Lambda Capture Internals
- How `std::function` Works
- Type Erasure
- Small Buffer Optimization in `std::function`
- How `std::bind` Works
- `std::invoke` Internals
- How `std::optional` Works
- How `std::variant` Works
- How `std::any` Works

### Level 11 — Exception Handling Internals

- How Exceptions Work Internally
- Stack Unwinding
- Exception Object Creation and Destruction
- Exception Handling Runtime
- Zero-Cost Exception Handling
- RAII and Exception Safety Guarantees
- `noexcept` Internals

### Level 12 — Multithreading and Synchronization Internals

- How `std::thread` Works Internally
- Thread Creation at OS Level
- How `std::mutex` Works Internally
- Mutex vs Recursive Mutex
- Spinlocks vs Mutexes
- How `std::lock_guard` Works
- How `std::unique_lock` Works
- How `std::scoped_lock` Works
- How `std::condition_variable` Works
- How `std::call_once` Works
- Deadlock Prevention Internals

### Level 13 — Atomic Operations and Memory Model

- CPU Atomic Instructions
- How `std::atomic` Works Internally
- Compare-and-Swap (CAS)
- Test-and-Set Operations
- Atomic vs Mutex
- Memory Ordering
- Relaxed, Acquire and Release Semantics
- Sequential Consistency
- Cache Coherence
- False Sharing
- Lock-Free vs Wait-Free Algorithms
- ABA Problem

### Level 14 — Asynchronous Programming Internals

- How `std::promise` Works
- How `std::future` Works
- Shared State Internals
- How `std::async` Works
- Packaged Tasks
- Futures and Thread Synchronization
- C++20 Coroutines Internals
- Coroutine State Machine
- Coroutine Promise Objects

### Level 15 — Compiler, Linker and ABI Internals

- C++ Compilation Pipeline
- Preprocessor Internals
- Compiler Frontend and Backend
- Object Files and Symbol Tables
- Name Mangling and Demangling
- Linking and Symbol Resolution
- Static vs Dynamic Linking
- Inline Functions and ODR
- ABI and Calling Conventions
- Stack Frames and Function Calls

### Level 16 — Advanced Runtime and Performance Internals

- CPU Cache Hierarchy
- Cache Lines and Cache Locality
- Branch Prediction
- Instruction-Level Optimization
- SIMD and Vectorization
- Memory Alignment and Performance
- Heap Allocation Overhead
- Benchmarking C++ Code
- Profiling and Performance Analysis
- Compiler Optimizations and Assembly Analysis

### Level 17 — Build Your Own C++ (BYOC)

This level focuses on implementing simplified versions of important C++ standard library components.

The objective is to understand their internal architecture and develop the ability to implement them independently.

#### Smart Pointers

- MyUniquePtr
- MySharedPtr
- MyWeakPtr
- Custom Control Block
- Reference Counting Mechanism

#### STL Containers

- MyVector
- MyString
- MyUnorderedMap
- MyMap using Red-Black Tree
- MyPriorityQueue

#### Callable Objects and Utilities

- MyFunction using Type Erasure
- MyOptional
- MyVariant

#### Memory Management

- MyAllocator
- Custom Memory Pool
- Object Pool

#### Concurrency

- MyLockGuard
- MyUniqueLock
- MyBlockingQueue
- MyThreadPool
- MyThreadSafeCounter
- MyLockFreeStack

Each implementation will include:

- Problem Statement
- Internal Architecture
- Design and Implementation
- Complete C++ Source Code
- Test Cases
- Edge Cases
- Time and Space Complexity
- Comparison with Standard Library
- Interview Questions

**Note:** These are educational implementations, not production replacements for the standard library. OS-dependent synchronization and hardware-level atomic behaviour will be studied using appropriate platform primitives.

### Level 18 — C++ Internals Interview Preparation

- Memory Management Interview Questions
- Smart Pointer Implementation Questions
- STL Internals Interview Questions
- Object Model and VTable Questions
- Copy and Move Semantics Questions
- Multithreading Internals Questions
- Atomic and Memory Model Questions
- Compiler and Runtime Questions
- Output-Based Internals Questions
- Scenario-Based Questions
- Quick Revision Notes

---

## Recommended Learning Approach

Every topic should be studied using the following approach:

1. **Concept:** Understand the purpose and problem being solved.
2. **Internal Architecture:** Understand how the feature works internally.
3. **Memory Layout:** Visualize memory representation wherever applicable.
4. **Execution Flow:** Understand what happens step by step.
5. **Source Code Exploration:** Examine relevant standard library implementation details.
6. **Practical Implementation:** Build a simplified implementation where applicable.
7. **Performance Analysis:** Understand complexity, overhead and trade-offs.
8. **Interview Preparation:** Practice basic, intermediate and advanced questions.

---

## Implementation Standards

- Primary language standard: **C++17**.
- C++20 features will be covered in dedicated advanced chapters.
- Use modern C++ coding practices.
- Include complete, compilable examples.
- Prefer simple implementations before introducing advanced optimizations.
- Include memory diagrams and execution flow diagrams.
- Explain platform-dependent implementation differences.
- Compare GCC/libstdc++, LLVM/libc++ and MSVC STL wherever relevant.
- Include appropriate unit tests for custom implementations.
- Never skip important concepts just to reduce the number of chapters.

---

## Development Environment

Recommended tools:

- **Compiler:** GCC / Clang / MSVC
- **Language Standard:** C++17
- **IDE:** Visual Studio Code / Visual Studio
- **Debugger:** GDB / LLDB / Visual Studio Debugger
- **Build System:** CMake
- **Memory Analysis:** AddressSanitizer, UndefinedBehaviorSanitizer and Valgrind
- **Performance Analysis:** Google Benchmark and platform profilers
- **Assembly Exploration:** Compiler Explorer

---

## Learning Goal

By completing this repository, the goal is to be able to:

- Explain how important C++ language features work internally.
- Explain how major STL components are implemented.
- Understand memory allocation, ownership and object lifetime.
- Implement simplified versions of smart pointers and STL components independently.
- Explain synchronization mechanisms and atomic operations at a deeper level.
- Understand compiler-generated code and runtime behaviour.
- Analyze performance issues and identify their underlying causes.
- Confidently handle advanced C++ internals and implementation-oriented interview questions.

---

## Repository Philosophy

**Don't just learn how to use C++. Understand how C++ works.**

Understand the internals. Explore the implementation. Write the code yourself. Analyze the trade-offs. Be ready to explain it in an interview.
