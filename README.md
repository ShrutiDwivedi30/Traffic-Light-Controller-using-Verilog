# 4-Way Traffic Light Controller in Verilog

A digital **Traffic Light Controller** designed for a 4-way intersection (North, South, East, West) using **Verilog HDL** and simulated in **Xilinx Vivado**. The system relies on a Finite State Machine (FSM) to safely cycle through green, yellow, and red light combinations.

## 🚀 Features
- **4-Way Intersection Management:** Controls independent signal outputs for `north_light`, `south_light`, `east_light`, and `west_light`.
- **FSM-Based Controller:** Implemented as a Moore machine with 8 sequential states cycling through Green 🟢 → Yellow 🟡 → Red 🔴.
- **Custom Hardware Timers:** 
  - **Green light** remains active for **16 clock cycles** (`count == 4'b1111`).
  - **Yellow light** transition remains active for **4 clock cycles** (`count == 4'b0011`).
- **Asynchronous Reset:** Activating `reset` instantly overrides the system and defaults the North direction to Green while keeping South, East, and West safely on Red.

## 🚥 Signal State Encoding
The outputs are 3-bit registers where the binary values map to specific light conditions:
- `3'b001` = **Green** 🟢
- `3'b010` = **Yellow** 🟡
- `3'b100` = **Red** 🔴

## 📁 Repository Structure
- `src/`
  - `Traffic_sys.v` (Main FSM Design module)

## 🛠️ Tools Used
- **Language:** Verilog HDL
- **Software Suite:** Xilinx / AMD Vivado Design Suite
- **Simulation:** Vivado Behavioral Simulator
