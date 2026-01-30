# 🧩 Four Wires (wire4)

> HDLBits – Verilog Basics

---

## 📌 Problem Statement

Create a module with **three inputs** and **four outputs** that behaves like wires and makes the following connections:

* `a → w`
* `b → x`
* `b → y`
* `c → z`

Each output should continuously reflect the value of its connected input.

<img width="815" height="281" alt="image" src="https://github.com/user-attachments/assets/df87b79c-b655-4044-9842-3bd5d4420ebe" />

---

## 🧠 Concept Covered

* **Continuous assignments (`assign`)**
* **Multiple drivers and fan-out**
* **Implicit wire declarations in ports**
* **Concise wiring using concatenation**

---

## 🧱 Module Interface

```verilog
module top_module(
    input  a, b, c,
    output w, x, y, z
);
```

* Inputs `a`, `b`, `c` are driven externally
* Outputs `w`, `x`, `y`, `z` are driven by this module
* Each port is **implicitly a wire** unless declared otherwise

---

## ✅ Verilog Solution

```verilog
module top_module(
    input  a, b, c,
    output w, x, y, z
);
    assign w = a;
    assign x = b;
    assign y = b;
    assign z = c;
endmodule
```

### ✅ Alternative (Concatenation – Compact Form)

```verilog
module top_module(
    input  a, b, c,
    output w, x, y, z
);
    assign {w, x, y, z} = {a, b, b, c};
endmodule
```

---

## 🔍 Explanation

* Each `assign` creates a **continuous connection**
* Input `b` is **fanned out** to two outputs (`x` and `y`)
* No new wires are created — all ports are already wires
* Order of `assign` statements **does not matter**

The concatenation operator `{}` allows multiple connections in **one statement**, improving clarity and compactness.

---

## 🧪 Expected Behavior

* `w` follows `a`
* `x` and `y` both follow `b`
* `z` follows `c`
* Outputs update **immediately** when inputs change

✔️ HDLBits Simulation Status: **SUCCESS**

---

## ⚠️ Common Mistakes

❌ Forgetting one output connection

❌ Assuming `assign` works like procedural assignment

❌ Declaring outputs as `reg`

❌ Mismatching concatenation order

---

## 🎯 Takeaway

> **Continuous assignments describe permanent connections, not execution order.**

This problem reinforces how **fan-out and wiring** work in Verilog.

---

### 🟢 Difficulty

**Easy**

---
