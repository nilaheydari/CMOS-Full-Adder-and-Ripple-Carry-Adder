# CMOS Full Adder and Ripple Carry Adder

CMOS transistor-level design and T-Spice simulation of a 1-bit Full Adder and a 4-bit Ripple Carry Adder.

## Project Overview
This project includes:
- Design and functional simulation of a 1-bit CMOS Full Adder.
- Propagation delay, rise/fall time, and average power measurements.
- Design and functional simulation of a 4-bit Ripple Carry Adder.
- Critical-path timing and power analysis of the 4-bit adder.

## Tools and Specifications
- Simulator: T-Spice
- Supply voltage: 1.8 V
- CMOS technology model: mosistsmc180.lib
- Output load: 10 fF

## Project Structure
- `1-bit-Full-Adder/`: Functional simulation and measurement files.
- `4-bit-Ripple-Carry-Adder/`: Functional simulation and critical-path measurement files.

## How to Run
1. Obtain the required CMOS technology model library.
2. Update the `.include` path in each circuit file.
3. Open the desired `.cir` file in T-Spice.
4. Run the transient simulation and inspect the outputs.

## Note
The technology model library is required separately. Measurement values should be obtained from the simulation results.
