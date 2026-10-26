# 16-Bit ALU Design Using Logisim

## Overview

This project implements a 16-bit Arithmetic Logic Unit (ALU) using Logisim. The ALU performs arithmetic and bitwise logical operations on two 16-bit inputs, A and B.

The project is built using individual circuits connected together through a multiplexer to select the required operation.

## Features

- **16-bit Adder:** Performs addition using full-adder circuits.
- **16-bit Subtractor:** Performs subtraction using the two's-complement method.
- **Bitwise AND:** Performs AND operation on corresponding bits.
- **Bitwise OR:** Performs OR operation on corresponding bits.
- **Bitwise XOR:** Performs XOR operation on corresponding bits.
- **Bitwise NOT:** Inverts the bits of the input.
- **Incrementer:** Increments the input value by 1.
- **Comparator:** Compares two inputs and generates Equal, Less Than, and Greater Than flags.
- **Multiplexer:** Selects the output of the required operation.
- **Overflow Detection:** Detects unsigned arithmetic overflow during addition and underflow during subtraction.
- **Reset:** Resets the outputs to zero.

## Operations

| Operation | Description |
|---|---|
| Addition | Calculates A + B |
| Subtraction | Calculates A − B |
| AND | Bitwise AND of A and B |
| OR | Bitwise OR of A and B |
| XOR | Bitwise XOR of A and B |
| NOT | Inverts the input bits |
| Increment | Calculates A + 1 |
| Comparison | Checks whether A = B, A < B, or A > B |

## Inputs and Outputs

### Inputs
- `A`: 16-bit input
- `B`: 16-bit input
- `Select`: Operation selection input
- `Reset`: Reset control input

### Outputs
- `Result`: 16-bit operation result
- `Overflow`: Unsigned arithmetic overflow/underflow flag
- `Equal`: Indicates whether A equals B
- `Less Than`: Indicates whether A is less than B
- `Greater Than`: Indicates whether A is greater than B

## Implementation

The ALU is designed using individual circuits for each operation. These circuits are connected through a multiplexer, which selects the result according to the selection input.

Subtraction is implemented using two's complement:

`A − B = A + NOT(B) + 1`

The comparator uses the subtraction result and borrow information to perform unsigned comparisons. The overflow circuit uses the final carry-out for addition and borrow for subtraction.

The adder and subtractor can support both signed and unsigned arithmetic, while the comparator and overflow logic in this implementation are designed for unsigned interpretation.

## Tools Used

- Logisim / Logisim Evolution
- Digital logic design
- Combinational circuits
- Full adders, logic gates, splitters, and multiplexers

## How to Run

1. Download or clone this repository.
2. Install Logisim or Logisim Evolution.
3. Open the `.circ` circuit file.
4. Open the main ALU circuit.
5. Set the input values A and B.
6. Select the desired operation using the Select input.
7. Observe the result and status flags.
8. Use Reset to clear the outputs.

## Learning Outcomes

- Understanding 16-bit arithmetic circuits.
- Designing adders and subtractors using logic gates.
- Implementing two's-complement subtraction.
- Building comparators and overflow-detection circuits.
- Connecting multiple subcircuits using multiplexers.
- Understanding modular digital system design.

## Author

Created as a digital logic design project using Logisim.
