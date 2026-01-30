# 🧠 Verilog Language (HDLBits)

Welcome to the **Verilog Language** section of this repository.
This folder contains **concept-wise explanations and solved HDLBits problems**, written to help learners move from **basic structural Verilog** to **advanced procedural and generate constructs**.

Each HDLBits problem has:

* 📄 **One dedicated `.md` file**
* 🧩 Problem understanding
* ✍️ Clean Verilog-2001 solution
* 💡 Key takeaways and common mistakes

> 🎯 Goal: Build **strong Verilog fundamentals** for VLSI, FPGA, ASIC, and competitive exams like **GATE**.

---

## 📂 Folder Structure

```
Verilog_Language/
├── README.md          # This file
├── basics/
├── vectors/
├── modules_hierarchy/
├── procedures/
└── more_verilog_features/
```

Each subfolder mirrors the HDLBits website structure.

---

## 2️⃣ Verilog Language – Contents

---

## 🔹 2.1 Basics

Covers **introductory combinational logic**, wire declarations, and basic gate-level modeling.

| Problem         | Description                     |
| --------------- | ------------------------------- |
| Simple wire     | Direct wire assignment          |
| Four wires      | Multiple independent signals    |
| Inverter        | NOT gate implementation         |
| AND gate        | Basic logic gate                |
| NOR gate        | Universal gate                  |
| XNOR gate       | Equality logic                  |
| Declaring wires | Explicit wire declarations      |
| 7458 chip       | Multi-input combinational logic |

📁 Folder: `basics/`

---

## 🔹 2.2 Vectors

Introduces **multi-bit signals**, slicing, concatenation, and bitwise operations.

| Problem                       | Focus                |
| ----------------------------- | -------------------- |
| Vectors                       | Basic vector usage   |
| Vectors in more detail        | Widths and indexing  |
| Vector part select            | `[msb:lsb]` slicing  |
| Bitwise operators             | &, |, ^, ~           |
| Four-input gates              | Vector logic         |
| Vector concatenation operator | `{}` usage           |
| Vector reversal 1             | Bit ordering         |
| Replication operator          | `{N{signal}}`        |
| More replication              | Advanced replication |

📁 Folder: `vectors/`

---

## 🔹 2.3 Modules: Hierarchy

Focuses on **design hierarchy, reusability, and modular thinking**.

| Problem                      | Concept                    |
| ---------------------------- | -------------------------- |
| Modules                      | Basic module instantiation |
| Connecting ports by position | Positional mapping         |
| Connecting ports by name     | Named port mapping         |
| Three modules                | Multi-level hierarchy      |
| Modules and vectors          | Vector ports               |
| Adder 1                      | Half/full adder            |
| Adder 2                      | Multi-bit adder            |
| Carry-select adder           | Optimized adder            |
| Adder-subtractor             | Arithmetic control         |

📁 Folder: `modules_hierarchy/`

---

## 🔹 2.4 Procedures

Introduces **behavioral modeling** using procedural blocks.

> Procedures allow **sequential statements**, unlike continuous assignments.

| Problem                       | Concept              |
| ----------------------------- | -------------------- |
| Always blocks (combinational) | `always @(*)`        |
| Always blocks (clocked)       | `posedge clk`        |
| If statement                  | Conditional logic    |
| If statement latches          | Latch inference      |
| Case statement                | Multi-way branching  |
| Priority encoder              | Priority logic       |
| Priority encoder with casez   | Don't-care matching  |
| Avoiding latches              | Complete assignments |

📁 Folder: `procedures/`

---

## 🔹 2.5 More Verilog Features

Advanced constructs used in **large-scale and parameterized designs**.

| Problem                          | Feature            |        |
| -------------------------------- | ------------------ | ------ |
| Conditional ternary operator     | `?:`               |        |
| Reduction operators              | `&`, `             | `, `^` |
| Reduction: Even wider gates      | Large fan-in       |        |
| Vector reversal 2                | For-loop logic     |        |
| 255-bit population count         | Counting bits      |        |
| Generate for-loop: 100-bit adder | Structural scaling |        |
| Generate for-loop: BCD adder     | Decimal arithmetic |        |

📁 Folder: `more_verilog_features/`

---

## 📄 Problem File Format (Standard)

Each `.md` file follows this structure:

````
# Problem Name

## 🔹 Problem Statement
(Short explanation of the HDLBits question)

## 🔹 Key Concept
(What this problem teaches)

## 🔹 Verilog Solution
```verilog
// clean, synthesizable solution
````

## 🔹 Explanation

(Line-by-line reasoning)

## 🔹 Common Mistakes

(Typical HDLBits pitfalls)

## 🔹 Takeaway

(One-line summary)

```

---

## 🚀 Who This Is For

- 🎓 ECE / EE students  
- 🔧 VLSI & FPGA beginners  
- 🧠 HDLBits learners  
- 🧪 GATE / core interview prep  
- 🏗️ RTL designers building strong foundations  

---

## ⭐ Tip

> Don’t rush.  
> **Understand why the code works**, not just *what* works.
```
