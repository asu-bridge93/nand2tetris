# Nand2Tetris Project 2: Boolean Arithmetic

## Implemented Chips

### Basic Adders
- **HalfAdder.hdl** - Half adder (adds two 1-bit values)
- **FullAdder.hdl** - Full adder (adds three 1-bit values with carry)

### 16-bit Arithmetic Chips
- **Add16.hdl** - 16-bit adder (adds two 16-bit two's complement values)
- **Inc16.hdl** - 16-bit incrementer (increments a 16-bit value by 1)

### Arithmetic Logic Unit
- **ALU.hdl** - ALU (Arithmetic Logic Unit)
  - Performs 18 different arithmetic and logical operations
  - Computes operations: 0, 1, -1, x, y, !x, !y, -x, -y, x+1, y+1, x-1, y-1, x+y, x-y, y-x, x&y, x|y
  - Outputs two status flags: zr (zero flag) and ng (negative flag)

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

- **HalfAdder**: Uses XOR for sum and AND for carry
- **FullAdder**: Combines two HalfAdders with an OR gate
- **Add16**: Chains one HalfAdder and fifteen FullAdders for ripple-carry addition
- **Inc16**: Uses Add16 to add 1 to the input value
- **ALU**: Uses six control bits (zx, nx, zy, ny, f, no) to configure operations
  - The ALU-basic.tst tests only the 'out' output (ignoring zr and ng flags)
  - The ALU.tst performs comprehensive testing including all output flags