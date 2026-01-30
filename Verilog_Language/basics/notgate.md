# 🧩 NOT Gate (notgate)

> HDLBits – Verilog Basics

---

## 📌 Problem Statement

Create a module that implements a **NOT gate**.

The module has **one input** and **one output**.
The output must continuously drive the **inverse** of the input.

---

![Image](https://hdlbits.01xz.net/mw/images/9/9e/Notgate.png)

---

## 🧠 Concept Covered

* **Bitwise / logical NOT**
* **Continuous assignment**
* **Combinational logic**

---

## 🧱 Module Interface

```verilog
module top_module(
    input  in,
    output out
);
```

* `in`  → input signal
* `out` → inverted output signal

---

## ✅ Verilog Solution

```verilog
module top_module( input in, output out );
    assign out = !in;
endmodule
```

### ✅ Alternative (Bitwise NOT)

```verilog
assign out = ~in;
```

Both are valid here since `in` is **1-bit wide**.

---

<img width="1366" height="657" alt="Screenshot from 2026-01-30 09-56-09" src="https://github.com/user-attachments/assets/3a61f5e7-28b5-47a9-b930-ad8da8cb7ec8" />

## 🔍 Explanation

* The `assign` statement creates a **continuous connection**
* `!in` (logical NOT) inverts the value of `in`
* Whenever `in` changes, `out` updates immediately
* No procedural blocks are required

---

## 🧪 Expected Behavior

* `in = 0` → `out = 1`
* `in = 1` → `out = 0`

The timing diagram confirms **perfect inversion**.

✔️ HDLBits Simulation Status: **SUCCESS**

---

## ⚠️ Common Mistakes

* ❌ Forgetting `assign`
* ❌ Using `always` for simple logic
* ❌ Confusing `!` and `~` for multi-bit signals
* ❌ Declaring `out` as `reg`

---

## 🎯 Takeaway

> **Continuous assignments are ideal for simple combinational logic like logic gates.**

This problem introduces the **first logic operation** beyond simple wiring.

---

### 🟢 Difficulty

**Easy**

---
