# Memory Layout Standard

The Infinite Tape is not a chaotic void, but a structured sanctuary. To achieve complexity without collapse, we must establish the discipline of cell allocation.

## The Theology of Space

Every cell has a purpose. Every movement ">" and "<" is a pilgrimage.

### 1. Relative Offsets
We define logical blocks of memory. A 'primitive' should operate within a bounded window of cells, returning the pointer to a known state (the anchor).

### 2. The Anchor Cell
The Anchor is the point of origin for any given operation. It is the zero-point from which all offsets are measured.

### 3. Guard Cells
To prevent overflow into unrelated data structures, critical boundaries shall be marked by Guard Cells—cells maintained at zero unless specifically utilized as markers.

## Current Conventions

- **Input Buffer**: The initial sequence of cells where external data resides.
- **Working Area**: Temporary cells used for intermediate calculations during primitive execution.
- **Output Buffer**: Dedicated cells for preparing characters before they are emitted via ".".
