# **5-Stage Pipelined MIPS32 Processor Design**

## **Overview**  
This project implements a **5-stage pipelined MIPS32 processor** in Verilog, showcasing efficient instruction execution with support for hazard handling, branching, and memory management. The design adheres to the MIPS32 Instruction Set Architecture (ISA) and includes stages for **Instruction Fetch (IF)**, **Instruction Decode (ID)**, **Execution (EX)**, **Memory Access (MEM)**, and **Write Back (WB)**.

The processor is verified using a testbench that simulates the execution of a sequence of instructions and validates the functionality of all pipeline stages.

---

## **Features**  

- **Pipeline Stages:**  
  - **Instruction Fetch (IF):** Fetches instructions from memory.  
  - **Instruction Decode (ID):** Decodes instructions and reads register values.  
  - **Execution (EX):** Performs arithmetic/logic operations and calculates memory addresses.  
  - **Memory Access (MEM):** Loads or stores data to/from memory.  
  - **Write Back (WB):** Writes results back to registers.  

- **Supported Instructions:**  
  - Arithmetic: `ADD`, `SUB`, `MUL`  
  - Logical: `AND`, `OR`, `SLT`  
  - Immediate: `ADDI`, `SUBI`, `SLTI`  
  - Memory: `LW`, `SW`  
  - Branching: `BEQZ`, `BNEQZ`  
  - Halt: `HLT`  

- **Key Features:**  
  - Hazard handling for data dependencies.  
  - Branch prediction and pipeline stalling for branching instructions.  
  - Memory design with 32 general-purpose registers and 1KB data memory.  

---

## **Directory Structure**  

```plaintext
├── pipe_MIPS32.v        # Verilog module implementing the MIPS32 processor
├── tb.v                 # Testbench for verifying the processor
├── README.md            # Project documentation
├── mips.vcd             # Waveform file (output from simulation)
└── Makefile             # Optional: Automate compilation and simulation
