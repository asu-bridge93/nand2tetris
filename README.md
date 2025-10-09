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
