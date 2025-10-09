# Nand2Tetris Project 1: Boolean Logic

## Implemented Chips

### Basic Logic Gates
- **Not.hdl** - NOT gate (inverter)
- **And.hdl** - AND gate
- **Or.hdl** - OR gate
- **Xor.hdl** - XOR gate (exclusive OR)

### 16-bit Logic Gates
- **Not16.hdl** - 16-bit NOT gate
- **And16.hdl** - 16-bit AND gate
- **Or16.hdl** - 16-bit OR gate

### Multi-way Gates
- **Or8Way.hdl** - 8-input OR gate

### Multiplexers
- **Mux.hdl** - Basic 2-to-1 multiplexer
- **Mux16.hdl** - 16-bit 2-to-1 multiplexer
- **Mux4Way16.hdl** - 16-bit 4-to-1 multiplexer
- **Mux8Way16.hdl** - 16-bit 8-to-1 multiplexer

### Demultiplexers
- **DMux.hdl** - Basic 1-to-2 demultiplexer
- **DMux4Way.hdl** - 1-to-4 demultiplexer
- **DMux8Way.hdl** - 1-to-8 demultiplexer

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