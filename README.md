# DSA Assignment – Stack and Circular Queue

This repository contains the solutions for the DSA assignment.

## Q1. Stack Using Array

### Operations
- PUSH(x): Inserts an element at the top.
- POP(): Removes the top element.
- PEEK(): Shows the top element without removing it.
- DISPLAY(): Displays all stack elements.

### Overflow and Underflow
- **Stack Overflow:** Occurs when PUSH is attempted while the stack is full.
- **Stack Underflow:** Occurs when POP or PEEK is attempted on an empty stack.

### Complexity
| Operation | Time Complexity | Space Complexity |
|---|---|---|
| PUSH | O(1) | O(1) |
| POP | O(1) | O(1) |
| PEEK | O(1) | O(1) |
| DISPLAY | O(n) | O(1) |

The complete stack uses O(n) space for storing n elements.

### Fixed-size stack
If the stack capacity is fixed and the user tries to insert more elements than its capacity, **Stack Overflow** occurs and the new element is not inserted.

## Q2. Circular Queue Using Array

### Operations
- ENQUEUE(x): Inserts an element at the rear.
- DEQUEUE(): Removes an element from the front.
- FRONT(): Shows the front element.
- DISPLAY(): Displays queue elements.

### Why circular queue uses memory better
In a linear queue, after deletions, empty positions at the beginning may remain unused when REAR has reached the last index. A circular queue connects the last position back to the first position, so these free positions can be reused.

### Complexity
| Operation | Time Complexity |
|---|---|
| ENQUEUE | O(1) |
| DEQUEUE | O(1) |

The queue uses **O(n) space** for a capacity of n.

### Full and empty conditions
- Empty: `front == -1`
- Full: `front == (rear + 1) % MAX`

## Files
- `stack_array.c` – Stack implementation
- `circular_queue.c` – Circular queue implementation

## How to compile and run

### Stack
```bash
gcc stack_array.c -o stack
./stack
```

### Circular Queue
```bash
gcc circular_queue.c -o circular_queue
./circular_queue
```

On Windows, after compiling with GCC:
```bash
stack.exe
circular_queue.exe
```
