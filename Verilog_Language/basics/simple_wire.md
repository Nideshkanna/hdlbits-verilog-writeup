# 🧩 Simple Wire

## 📌 Problem Statement

Create a module with **one input** and **one output** that behaves exactly like a wire.

Any change on the input should **immediately reflect** on the output.

---

![Image](https://hdlbits.01xz.net/mw/images/7/77/Wire.png)

![Image](https://media.licdn.com/dms/image/v2/D5622AQH2AhRlWvSp4w/feedshare-shrink_1280/B56ZdJ5goBHoAo-/0/1749291502939?e=2147483647\&t=_GN0xiYKJbCafm3Tt7P4QpVaOeSlUgHWPKNlvgfG-H0\&v=beta)

---

## 🧠 Concept Covered

### Continuous Assignment (`assign`)

* Verilog **wires are directional**
* Data flows from **driver → sink**
* A **continuous assignment**:

  ```verilog
  assign left = right;
  ```

  continuously drives the right-hand signal onto the left-hand signal

📌 This is **not a one-time assignment** — it updates whenever the RHS changes.

---

## 🧱 Module Interface

```verilog
module top_module(
    input  in,
    output out
);
```

* `in`  → driven by external testbench
* `out` → driven by this module

---

## ✅ Verilog Solution

```verilog
module top_module( input in, output out );
    assign out = in;
endmodule
```

---

<img width="1366" height="657" alt="Screenshot from 2026-01-30 09-34-35" src="https://github.com/user-attachments/assets/dff10fa8-3823-4937-9f1f-db6629529f78" />

## 🔍 Explanation (Line-by-Line)

* `assign out = in;`

  * Creates a **continuous connection**
  * Any change on `in` propagates instantly to `out`
  * This mimics the behavior of a **physical wire**

---

## ⚠️ Common Mistakes

❌ Forgetting `assign`

❌ Using `always` block (unnecessary here)

❌ Declaring `out` as `reg`

❌ Swapping LHS and RHS

---

## 🧪 Expected Behavior

From the timing diagram:

* `out` **perfectly follows** `in`
* No delay
* No mismatch cycles

✔️ **Simulation Status: SUCCESS**

---

## 🎯 Takeaway

> **Continuous assignments are the simplest and cleanest way to model pure combinational connections in Verilog.**

This is the **foundation** for everything that follows in HDLBits.

---
