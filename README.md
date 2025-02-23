# 2x1 Multiplexer (MUX) Project

## Overview

This project involves designing, simulating, and analysis of a **2x1 Multiplexer (MUX)** using Cadence Virtuoso. The MUX is a fundamental combinational logic circuit that selects one of the two input signals based on a control signal. The project demonstrates schematic design, layout creation, and post-layout simulation. The design is implemented at the **transistor level using CMOS technology** to ensure a deep understanding of circuit behavior and optimization.

## Software & Tools Used

- **Cadence Virtuoso** (for schematic capture, layout, and simulation)

- **Assura** (for DRC and LVS verification)

- **Analog Design Environment (ADE)** (for waveform analysis)

## Project Workflow

### 1. Schematic Design

- Designed using **Virtuoso Schematic Editor**.
- Implements a **2x1 MUX** using **CMOS transistor-level design** with MOSFETs.
- Verified functionality through **Transient Analysis**.

### 2. Layout Design

- Created using **Virtuoso Layout Editor**.
- Optimized for area efficiency and minimal parasitics.
- Performed **Design Rule Check (DRC)** to ensure compliance.

### 3. Layout Versus Schematic (LVS) Check

- Ensured that the layout matches the schematic.
- Verified through **LVS Check** using Assura.

### 4. Parasitic Extraction & Post-Layout Simulation

- Extracted parasitics using **Assura**.
- Performed **post-layout simulation** to analyze parasitic effects on performance.

## Circuit Description

The **2x1 MUX** operates as follows:

- **Inputs:** `I0`, `I1` (data inputs), `S` (select signal)
- **Output:** `Y`
- **Truth Table:**
  | Select (S) | Output (Y) |
  | ---------- | ---------- |
  | 0          | I0         |
  | 1          | I1         |
- **Boolean Expression:**
  ```
  Y = (I0 & ~S) | (I1 & S)
  ```

## Design Implementation

### 1. CMOS Transistor-Level Design

- The circuit is designed at the **CMOS transistor level** for optimized power and performance.
- Consists of a **pull-up network (PMOS) and pull-down network (NMOS)** to implement the MUX logic.
- Simulated to ensure correct operation under various conditions.

### 2. Using Verilog

```verilog
module mux2x1 (input I0, I1, S, output Y);
    assign Y = (I0 & ~S) | (I1 & S);
endmodule
```

### 3. Using MATLAB Simulink and Cadence Software

- Blocks like **Multiplexer**, **Logical Operators**, and **Scope** can be used to model and simulate the behavior in MATLAB Simulink.
- **Cadence Virtuoso** used for schematic design, layout, and post-layout simulation.

## Technical Specifications

- **Technology Node:** 90nm
- **Supply Voltage (VDD):** 1V
- **Logic Operation:** `Y = (I0 & ~S) | (I1 & S)`

## Simulation and Testing

- Simulated the design in **Cadence Virtuoso**.
- Verified output correctness using test cases for all possible input combinations.
- If using hardware, test the circuit with an **oscilloscope or logic analyzer**.

## Results & Observations

- **Schematic Simulation:** Verified correct **MUX logic functionality**.
- **Layout Optimization:** Ensured minimal area and DRC compliance.
- **Post-Layout Simulation:** Observed deviations due to parasitic capacitance and resistance.

## Applications

- **Data selection** and **routing** in digital systems
- **ALU (Arithmetic Logic Unit)** operations
- **Communication** and **signal processing**
- **Memory addressing** and **control circuits**

## Future Enhancements

- Extend to **4x1 MUX** or **8x1 MUX** using cascading techniques.
- Implement using **FPGA** and test with real-world applications.
- Design a **low-power optimized version** for embedded systems.

## Reference Images

- **MUX Schematic Diagram**

  ![2_X_1_Mux_Schematic](https://github.com/user-attachments/assets/1243e2d6-a33c-4715-a596-75f2573ab715)

- **MUX Test**

  ![2_X_1_Mux_Test](https://github.com/user-attachments/assets/83cec5a0-8271-48c8-a838-b3a6ef8903d4)

- **MUX Test Setup**

  ![2_X_1_Mux_Test](https://github.com/user-attachments/assets/a8bbfbd8-f6d0-4626-8170-032e01068cd4)

- **MUX Test Setup**

  ![2_X_1_Mux_ADE](https://github.com/user-attachments/assets/426ad35b-88af-4503-94a8-540ec68f9c11)

- **MUX Layout**

  ![2_X_1_Mux_Layout](https://github.com/user-attachments/assets/6da0a688-e97a-470d-b6b9-b2ea63929138)



## Conclusion

This **2x1 MUX project** provides a **comprehensive approach** to understanding digital circuit design and implementation. The design is implemented at the **CMOS transistor level**, making it suitable for advanced **VLSI and low-power applications**. It is a **fundamental building block** for more complex systems and is widely used in **digital electronics** and **computing**.

---

###


*This project is intended for educational and research purposes only and should not be used directly for other purposes without permission.*

*For further inquiries or contributions, feel free to contact or contribute to the repository.*

