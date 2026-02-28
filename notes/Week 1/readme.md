# MIT 6.004 — Module 1 : Basics of Information

---
Day 1
## What is Information?
Information = reduction of uncertainty, measured in **bits**.
> N bits = 2^N distinct values

---

## Encoding Positive Integers
Binary uses positional notation — each position is a power of 2.

| Decimal | Binary   |
|---------|----------|
| 5       | 0101     |
| 13      | 1101     |
| 255     | 11111111 |

To store number X → find N where **2^N > X**
Example: store 200 → need **8 bits** (2^8 = 256)

---

## Two's Complement (Negative Numbers)
**Steps:** Flip all bits → Add 1

Example: -5 in 8 bits
```
+5    =  0000 0101
Flip  =  1111 1010
+1    =  1111 1011  ← this is -5
```
**Why?** Addition and subtraction become the same hardware operation.
This is how the Beta ALU handles SUB in Lab 3.

---

## Floating Point (IEEE 754)
```
[Sign 1bit] [Exponent 8bits] [Mantissa 23bits]
```
Not all real numbers can be stored exactly.

---

## Key Takeaway
Everything in a computer is just a number — text, images, sounds,
and even CPU instructions. No difference between data and instructions
at hardware level. This is why CPUs are reprogrammable.

