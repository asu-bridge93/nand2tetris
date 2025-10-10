# Nand2Tetris

Building a modern computer from first principles. Starting with elementary NAND gates and culminating in a general-purpose computer system capable of running Tetris.

## Projects

### [Project 1: Boolean Logic](projects/01_BooleanLogic/README.md)
Implementation of fundamental logic gates, building from NAND to create Not, And, Or, Xor, Mux, DMux, and their variants.

**What I Learned:**
- **Logic Gate Universality**: How NAND alone can implement any Boolean function
- **Hardware Description Language (HDL)**: Declarative approach to circuit design
- **Hierarchical Design**: Building complex chips from simpler components
- **Bus Notation**: Working with multi-bit data paths (16-bit operations)
- **Multiplexing/Demultiplexing**: Data routing and selection mechanisms

**Implemented:**
- Basic gates: Not, And, Or, Xor
- 16-bit variants: Not16, And16, Or16
- Multi-way gates: Or8Way
- Multiplexers: Mux, Mux16, Mux4Way16, Mux8Way16
- Demultiplexers: DMux, DMux4Way, DMux8Way

### [Project 2: Boolean Arithmetic](projects/02_BooleanArithmetic/README.md)
Implementation of arithmetic circuits, from basic adders to a complete Arithmetic Logic Unit (ALU).

**What I Learned:**
- **Binary Addition**: Half adder and full adder circuits with carry propagation
- **Ripple-Carry Architecture**: Chaining adders for multi-bit addition
- **Two's Complement Arithmetic**: Hardware representation of negative numbers
- **ALU Design**: Using control bits to configure multiple operations in one chip
- **Status Flags**: Computing zero (zr) and negative (ng) flags for conditional logic
- **Arithmetic Tricks**: Implementing subtraction and increment using addition and bit manipulation

**Implemented:**
- Basic adders: HalfAdder, FullAdder
- 16-bit arithmetic: Add16, Inc16
- ALU: 18 operations controlled by 6 control bits (zx, nx, zy, ny, f, no)
  - Arithmetic: 0, 1, -1, x+1, y+1, x-1, y-1, x+y, x-y, y-x
  - Logical: x, y, !x, !y, -x, -y, x&y, x|y