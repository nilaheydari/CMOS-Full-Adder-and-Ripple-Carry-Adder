# CMOS Full Adder Design and Simulation

![SPICE](https://img.shields.io/badge/Language-SPICE-2E8B57)
![CMOS](https://img.shields.io/badge/Technology-CMOS-blue)
![180nm](https://img.shields.io/badge/Process-180nm-orange)
  

## 1. 1-Bit Full Adder

The 1-bit Full Adder is implemented using transistor-level CMOS logic gates and simulated in Tanner T-Spice. It takes three binary inputs (A, B, and Cin) and generates two outputs: Sum and Carry-out (Cout).

### Performance Metrics
| Metric | Sum | $C_{out}$ |
|:---|---:|---:|
| $T_r$ (Rise Time) | 133.2871 ps | 117.5888 ps |
| $T_f$ (Fall Time) | 97.9716 ps | 92.5223 ps |
| $T_{plh}$ (Low-to-High Delay) | 216.4226 ps | 204.2583 ps |
| $T_{phl}$ (High-to-Low Delay) | 196.8354 ps | 216.7416 ps |
| $T_p$ (Avg. Prop. Delay) | 206.6290 ps | 210.4999 ps |

**Average Power Consumption:** $P_{avg}=7.0422\,\mu W$

### Output Waveforms

![1-Bit Full Adder Waveforms](1bit-waveforms.png)

**Figure 1.** Simulated waveforms for A = 1, B = 0, and varying Cin.

## 2. 4-Bit Ripple Carry Adder

The 4-bit Ripple Carry Adder consists of four cascaded 1-bit CMOS Full Adders. The carry-out of each stage is connected to the carry-in of the next stage.

### Performance Metrics
| Metric | $S_3$ (Sum 3) | $C_{out}$ (Carry) |
|:---|---:|---:|
| $T_r$ (Rise Time) | 133.6552 ps | 117.2394 ps |
| $T_f$ (Fall Time) | 96.8724 ps | 92.6011 ps |
| $T_{plh}$ (Low-to-High Delay) | 862.1975 ps | 827.0337 ps |
| $T_{phl}$ (High-to-Low Delay) | 821.0529 ps | 861.0426 ps |
| $T_p$ (Avg. Prop. Delay) | 841.6252 ps | 844.0381 ps |

**Average Power Consumption:** $P_{avg}=28.1715\,\mu W$

### Critical Path Analysis

The carry propagation path was evaluated with $A=1111$, $B=0000$, and a pulsed $C_{in}$.

**Critical Path:**

$C_{in} \rightarrow C_1 \rightarrow C_2 \rightarrow C_3 \rightarrow C_{out}$

**Average Propagation Delays:**

- **$C_{in} \rightarrow C_{out}$:** $T_p = 844.0381\,ps$
- **$C_{in} \rightarrow S_3$:** $T_p = 841.6252\,ps$

## 3. Requirements and Usage

### Requirements

| Requirement | Description |
|:---|:---|
| Software | Tanner T-Spice |
| Technology | 180 nm CMOS |
| Model Library | `mosistsmc180.lib` |
| Supply Voltage | 1.8 V |


### How to Run

**Step 1:** Clone or download the repository.

**Step 2:** Open the desired `.cir` file in Tanner T-Spice.

**Step 3:** Ensure that the `.include` statement correctly references the provided `mosistsmc180.lib` file.

**Step 4:** Run the transient simulation.

**Step 5:** View the output waveforms and measurement results.



