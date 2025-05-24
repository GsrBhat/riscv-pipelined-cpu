# RISC-V 5-Stage Pipelined Processor (Simulation Only)

This project implements a **RISC-V 32-bit, 5-stage pipelined processor** using **Verilog**. It is designed purely for simulation and educational purposes using **Vivado 2024.2**. No FPGA hardware is used.

## 🔧 Pipeline Stages

This processor includes the standard five stages:

1. **IF (Instruction Fetch)**
2. **ID (Instruction Decode)**
3. **EX (Execute)**
4. **MEM (Memory Access)**
5. **WB (Write Back)**

Each stage is separated by pipeline registers: `IF/ID`, `ID/EX`, `EX/MEM`, `MEM/WB`.

---

## 📂 Files Included

| File Name              | Description                                                |
| ---------------------- | ---------------------------------------------------------- |
| `top.v`                | Top-level integration of all stages and pipeline registers |
| `instruction_memory.v` | ROM module containing hardcoded instructions               |
| `data_memory.v`        | RAM module for load/store                                  |
| `register_file.v`      | 32 general purpose registers                               |
| `control_unit.v`       | Generates control signals based on opcode                  |
| `alu.v`                | Performs arithmetic and logical operations                 |
| `if_id_reg.v`          | Pipeline register between IF and ID stages                 |
| `id_ex_reg.v`          | Pipeline register between ID and EX stages                 |
| `ex_mem_reg.v`         | Pipeline register between EX and MEM stages                |
| `mem_wb_reg.v`         | Pipeline register between MEM and WB stages                |
| `tb_top.v`             | Testbench for simulation in Vivado                         |

---

## 🧪 Simulation Output

Screenshots were taken for:

* **PC values** incrementing
* **Instruction Fetch** from ROM
* **IF/ID** Pipeline values
* **Register File read/write** operations
* **ALU results**
* **Memory read/write** values
* **Writeback to Registers**

---

## 🛠️ Tools Used

* **Vivado 2024.2** (Simulation only)
* **Verilog HDL**

---

## 📸 Screenshots (Waveforms)

> Include waveform screenshots showing each stage:
>
> * `pc`, `if_pc`, `id_pc`
> * `instruction`, `rd1`, `rd2`
> * `alu_result`, `mem_out`, `write_data`

---

## 🤝 Acknowledgements

This project was completed as part of my learning journey in **Computer Architecture** and **Digital Design**. Special thanks to the OpenAI tools for guidance and simulation setup.

---

## 🔗 Author & Links

* **Author**: \[Your Name]
* **LinkedIn**: \[Your LinkedIn Profile Link]
* **GitHub Repository**: \[GitHub Repo Link]

---

## 📌 How to Run

1. Open **Vivado 2024.2**
2. Create a new project
3. Add all Verilog files and `tb_top.v`
4. Run behavioral simulation
5. View waveforms and verify pipeline behavior

---

## 📣 Coming Soon

Planned extensions:

* Branch instructions
* Hazard detection
* Forwarding logic
* More ALU operations

---
