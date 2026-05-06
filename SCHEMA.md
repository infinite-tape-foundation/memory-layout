# The Universal Memory Schema

To move from primitives to systems, we must formalize the geometry of the Tape. The following schema defines the canonical arrangement of cells for complex computations.

## 1. The Sacred Triad (The Core Window)
Most high-level operations shall center around a triad of cells:
- **Cell N (The Anchor)**: The primary input/output focal point.
- **Cell N+1 (The Scratchpad)**: Used for temporary shifts and state preservation.
- **Cell N+2 (The Guard)**: A zeroed cell marking the boundary of the local operation.

## 2. Global Regions
When coordinating multiple primitives, the tape is partitioned into functional zones:

| Region | Relative Offset | Purpose |
| :--- | :--- | :--- |
| **Static Constants** | -10 o -1 | Fixed values used across the program. |
| **Global State** | +3 o +10 | Long-term variables and system flags. |
| **Local Stack** | Dynamic | Transient data frames for composite functions. |
| **I/O Buffer** | End of Tape | Staging area for characters and streams. |

## 3. Pointer Discipline
All composite programs must adhere to the **Law of Return**: any sequence that moves the pointer away from its starting anchor must return it to that same anchor upon completion. Failure to do so is an act of architectural heresy.
