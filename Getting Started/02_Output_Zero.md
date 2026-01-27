# HDLBits – Getting Started

## 🧩 Problem 2: Zero

### 📌 Problem Statement

This is the second introductory problem in the **HDLBits – Getting Started** section.
After implementing a constant logic `1`, this exercise checks whether you can independently implement a **constant logic `0`** output.

You are required to design a digital circuit with:

* **No inputs**
* **One output**
* The output must **always drive logic `0` (LOW)**

This problem reinforces:

* Verilog module syntax
* Output-only modules
* Continuous assignments
* Understanding synthesis behavior

---

### 📄 Module Declaration

```verilog
module top_module(
    output zero
);
```

> ⚠️ **Important:**
> The module name `top_module` and port name `zero` must remain unchanged for HDLBits to simulate correctly.

---

### 🎯 Design Requirement

* The output `zero` must be permanently tied to logic low (`0`)
* No clocks, registers, or inputs are required
* Expected solution length is **approximately one line**

---

### 💡 Hint (from HDLBits)

> For Quartus synthesis, not assigning a value to a signal usually results in `0`.
> This problem is actually easier than the previous one.

Even so, explicitly assigning the value is considered **good coding practice**.

---

### ✅ Solution (Verilog)

```verilog
module top_module(
    output zero
);
    assign zero = 1'b0;
endmodule
```

---

### 🛠️ Explanation

* `assign` is a **continuous assignment**, ideal for combinational logic
* `1'b0` represents:

  * `1` → bit width
  * `'b` → binary format
  * `0` → logic LOW

This ensures the output `zero` is **always held at ground (0)**.

---

### 🧪 Simulation Result

* Quartus Compilation: ✅ Successful
* ModelSim Simulation: ✅ Outputs match reference
* HDLBits Status: **Success!**

<img width="1364" height="651" alt="image" src="https://github.com/user-attachments/assets/273fa208-7a6c-4394-89a0-3f373673c8c9" />

> ⚠️ **Quartus Warning Observed**

```
Warning (13024): Output pins are stuck at VCC or GND
```

This warning is **expected and harmless** for this problem because the output is intentionally tied to a constant value.

---

### 🧠 Key Takeaways

* Constant outputs can be implemented using continuous assignments
* Synthesis tools may optimize constant signals aggressively
* Explicit assignments improve readability and maintainability
* Warnings must be interpreted **in context**, not blindly avoided

---

### 📈 Progress Update

* ✅ Problem 1: One
* ✅ Problem 2: Zero

---

### ⏭️ Next Steps

Proceed to:

* **Wires**
* **Simple Gates**
* **Vector Logic**

These will introduce **signals, connectivity, and combinational logic design**.

---
