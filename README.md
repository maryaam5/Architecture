# 🚀 RISC-V Processor Design: Single-Cycle & Pipelined

Welcome to the **RISC-V Processor Design** repository. [cite_start]This project features a full Verilog implementation of a functional RISC-V CPU[cite: 7, 33]. [cite_start]Developed for the **CSC311: Introduction to Computer Architecture** course at **Nile University (ITCS)**, Fall '25[cite: 2, 3, 4].

## 🏗️ Architectural Overview

This project transitioned from a foundational architecture to an optimized, high-performance design:

1.  [cite_start]**Single-Cycle Core:** A complete datapath where every instruction executes in one clock cycle[cite: 7, 57]. [cite_start]It features a merged Control Unit for optimized logic[cite: 10, 59].
2.  **Pipelined Core (Advanced):** An evolution of the design into a 5-stage pipeline to increase instruction throughput, handling concurrent execution stages (Fetch, Decode, Execute, Memory, Write-back).

---

## 👥 The Team & Contributions

[cite_start]Following the project's modular design, each member specialized in a critical hardware component[cite: 185, 186]:

| Task | Lead Member | Component & Responsibilities |
| :--- | :--- | :--- |
| **Task 1** | **Farah Awadalla** | [cite_start]**ALU & Arithmetic Logic:** Implementing R-type and shift operations (add, sub, and, or, xor, sll, srl)[cite: 187, 188, 189, 190, 191]. |
| **Task 2** | **Mariam Mahmoud** | [cite_start]**Control Unit:** Merged Main & ALU Control to generate all internal signals (RegWrite, MemRead, ALUSrc, etc.)[cite: 197, 198, 205]. |
| **Task 3** | **Shaza** | [cite_start]**RegFile & ImmGen:** Managing 32 registers (x0=0) and sign-extension for 64-bit immediates[cite: 211, 213, 214, 215, 218, 219]. |
| **Task 4** | **Taghreed Oyoun** | [cite_start]**PC & Branch Logic:** Designing instruction sequencing, branch target calculation, and next-PC selection[cite: 225, 226, 227, 229, 230, 231]. |
| **Task 5** | **Dalia Nassar** | [cite_start]**Integration:** Top-level module integration, instruction/data memory management, and full-core simulation[cite: 236, 244, 245, 252, 256]. |

---

## 🛠️ Technical Specifications

### Supported Instruction Set
[cite_start]The processor handles the following RISC-V instruction categories[cite: 36]:
* [cite_start]**Integer R-Type:** `add`, `sub`, `and`, `or`, `xor`[cite: 37, 40, 41].
* [cite_start]**Logical Shifts:** `sll`, `srl`, `slli`, `srli`[cite: 42, 47].
* [cite_start]**I-Type Arithmetic:** `addi`, `andi`, `ori`, `xori`[cite: 43, 44].
* [cite_start]**Memory Access:** `ld` (Load) and `sd` (Store) using 64-bit doubleword operations[cite: 49, 50, 52, 54].
* [cite_start]**Control Flow:** `beq` (Branch if Equal)[cite: 55, 56].

### Hardware Design Highlights
* [cite_start]**Merged Control Unit:** Directly generates `ALUControl` from opcode, funct3, and funct7[cite: 209].
* [cite_start]**Synchronous Memory:** Register file uses synchronous writes and asynchronous reads[cite: 217].
* [cite_start]**Word-Aligned Addressing:** Optimized for 64-bit data memory and instruction fetching[cite: 240, 243].

---

## 💻 Simulation & Verification

* [cite_start]**Language:** Verilog HDL[cite: 33].
* [cite_start]**Simulator:** Vivado Design Suite[cite: 32, 33].
* [cite_start]**Deliverables:** Includes full simulation waveforms showing PC updates, register writes, and ALU outputs[cite: 126, 129, 132, 134, 147].

### How to Run
1.  Clone this repository.
2.  Open **Vivado** and import the source files from the `src/` directory.
3.  [cite_start]Load the machine code into the **Instruction Memory** module[cite: 160, 166].
4.  [cite_start]Run the top-level testbench to verify correct execution of the test program[cite: 257, 258].

---

## 📜 Academic Integrity
[cite_start]All work submitted in this repository was developed by the team members mentioned above[cite: 264]. [cite_start]External sources or code copying were strictly prohibited per Nile University policy[cite: 265].
