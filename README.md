# 🚀 RISC-V Processor Design: Single-Cycle & Pipelined

This repository presents a Verilog-based implementation of a **RISC-V processor**, demonstrating the progression from a basic **single-cycle architecture** to a more efficient **5-stage pipelined design**. The project highlights key concepts in computer architecture, including performance optimization, modular hardware design, and instruction execution flow.

---

## 🏗️ Architectural Overview

Two processor designs are implemented to illustrate architectural evolution:

### 1. Single-Cycle Core
- Executes each instruction in a single clock cycle.
- Utilizes a **merged control unit** (combining main control and ALU control) to simplify logic.
- Supports 64-bit memory operations such as `ld` (load) and `sd` (store).

### 2. Pipelined Core (Advanced)
- Improves performance by dividing execution into five stages:
  - **IF** (Instruction Fetch)  
  - **ID** (Instruction Decode)  
  - **EX** (Execute)  
  - **MEM** (Memory Access)  
  - **WB** (Write Back)  
- Enables overlapping instruction execution for higher throughput.
- Designed to enhance clock efficiency and overall performance.

---

## 👥 Team Contributions

The project was divided into modular components, with each member responsible for a key subsystem:

| Task | Member | Responsibilities |
| :--- | :--- | :--- |
| **Task 1** | **Farah Awadalla** | ALU design and implementation of arithmetic and logic operations (`add`, `sub`, `and`, `or`, `xor`, `sll`, `srl`) |
| **Task 2** | **Mariam Mahmoud** | Control unit design, instruction decoding, and generation of control signals |
| **Task 3** | **Shaza** | Register file (32 registers) and immediate generator for 64-bit values |
| **Task 4** | **Taghreed Oyoun** | Program counter logic, branching, and next-instruction selection |
| **Task 5** | **Dalia Nassar** | System integration, memory handling, and full processor simulation |

---

## 🛠️ Technical Specifications

### Supported Instruction Set

- **R-Type:** `add`, `sub`, `and`, `or`, `xor`, `sll`, `srl`  
- **I-Type Arithmetic:** `addi`, `andi`, `ori`, `xori`  
- **Memory Access:** `ld`, `sd` (64-bit support)  
- **Control Flow:** `beq` (branch if equal)  

### Implementation Details

- **Word-aligned memory addressing** for both instruction and data memory  
- **Synchronous design** with:
  - Synchronous writes to the register file  
  - Asynchronous reads from the register file  
- Modular and scalable hardware structure  

---

## 💻 Simulation & Tools

- **Hardware Description Language:** Verilog  
- **Development Environment:** Xilinx Vivado (Simulation Mode)  
- **Verification:** Comprehensive testbenches validating:
  - Program counter behavior  
  - ALU operations  
  - Memory read/write correctness  

---

## ▶️ Getting Started

1. Clone the repository:
   ```bash
   git clone <https://github.com/maryaam5/Architecture>
