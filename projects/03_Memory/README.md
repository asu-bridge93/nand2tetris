# Nand2Tetris Project 3: Memory

## Implemented Chips

### Basic Sequential Logic
- **Bit.hdl** - 1-bit register (stores a single bit using DFF)

### 16-bit Register
- **Register.hdl** - 16-bit register (stores a 16-bit value)

### RAM Modules
- **RAM8.hdl** - Memory of 8 registers (24 bytes)
- **RAM64.hdl** - Memory of 64 registers (128 bytes)
- **RAM512.hdl** - Memory of 512 registers (1KB)
- **RAM4K.hdl** - Memory of 4K registers (8KB)
- **RAM16K.hdl** - Memory of 16K registers (32KB)

### Program Counter
- **PC.hdl** - 16-bit counter with increment, load, and reset operations

## File Structure

Each chip includes the following files:

- **\*.hdl** - HDL implementation file
- **\*.tst** - Test script
- **\*.cmp** - Expected output (for comparison)
- **\*.out** - Actual test execution results

## Testing Instructions

1. Launch the Hardware Simulator
2. Load the corresponding `.tst` file
3. Run the test
4. Verify that the output (`.out`) matches the expected values (`.cmp`)

## Implementation Notes

### Sequential Logic Foundation
- **Bit**: Uses a Mux to select between current value (feedback) and new input, with DFF providing the time delay
- **Register**: Composed of 16 Bit chips, all controlled by the same load signal

### Memory Hierarchy
All RAM modules follow a consistent pattern of hierarchical composition:

- **RAM8**: Uses DMux8Way to decode addresses and 8 Register chips to store data
- **RAM64**: Uses DMux8Way with 8 RAM8 chips (address bits split: [0..2] for bank selection, [3..5] for internal addressing)
- **RAM512**: Uses DMux8Way with 8 RAM64 chips (address bits: [0..2] for bank, [3..8] for internal)
- **RAM4K**: Uses DMux8Way with 8 RAM512 chips (address bits: [0..2] for bank, [3..11] for internal)
- **RAM16K**: Uses DMux4Way with 4 RAM4K chips (address bits: [0..1] for bank, [2..13] for internal)

### Program Counter
- **PC**: Implements priority logic for three operations:
  1. Reset (highest priority): Sets output to 0
  2. Load: Sets output to input value
  3. Increment (lowest priority): Adds 1 to current value
  - Uses cascaded Mux16 gates to implement the priority hierarchy
  - Computes a combined load flag to determine when to update the internal register
  - The register maintains its value when no operation is specified