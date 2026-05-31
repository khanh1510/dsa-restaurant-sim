# Restaurant Simulation

A C++ console application simulating restaurant customer operations using custom-implemented tree and hash table data structures, built as a Data Structures and Algorithms course project at HCMUT.

## Tech Stack

- **Language:** C++11
- **Compiler:** g++ (MinGW-W64) 11.2.0
- **Data Structures:** Custom tree, custom hash table, doubly-linked list

## Features

- Custom tree and hash table implementations without standard library containers
- Doubly-linked customer list with name and energy attributes
- Command-based interface for customer management operations
- Two-restaurant simulation (Gojo and Sukuna themed)
- Manual memory allocation and deallocation

## Project Structure

```
├── main.cpp         # Entry point (read-only)
├── main.h           # Restaurant abstract class & customer struct
├── Restaurant.cpp   # Data structure implementation
├── test.txt         # Test input cases
└── test2.txt        # Additional test cases
```

## Data Structure Design

**Customer node:**
```cpp
class customer {
    string name;
    int energy;
    customer* prev;
    customer* next;
};
```

**Restaurant interface (abstract):**

| Method | Description |
|--------|-------------|
| `RED(name, energy)` | Add customer |
| `BLUE(num)` | Remove customer by position |
| `PURPLE()` | Traverse and process list |
| `REVERSAL()` | Reverse customer order |
| `UNLIMITED_VOID()` | Clear all customers |
| `DOMAIN_EXPANSION()` | Hash table expansion |
| `LIGHT(num)` | Tree-based lookup |

## Getting Started

### Build

```bash
g++ -o main.exe main.cpp Restaurant.cpp
```

### Run

```bash
./main.exe < test.txt
```

### Notes

- Only `Restaurant.cpp` should be modified
- Only `#include "main.h"` is allowed — no additional headers
- All memory must be explicitly freed
