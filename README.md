# Matrix Operations in ARM Assembly (Real-Time Image Processing Concept)

##  Overview

This project implements **3×3 matrix operations in ARM Assembly Language** and demonstrates how low-level arithmetic operations form the foundation of **real-time image processing systems** such as filtering, edge detection, and enhancement.

The program performs:

* Matrix Addition (Brightness / Blending)
* Matrix Subtraction (Edge Difference)
* Matrix Multiplication (Convolution-like filtering)

The code is executed and verified using the **CPUlator ARMv7 Online Simulator**.

---

##  Aim

To understand and implement matrix-based computations at the instruction level using ARM assembly and relate them to real-time image processing operations.

---

##  Concept

Every grayscale image can be represented as a **matrix of pixel intensities**.

Many image processing operations are actually matrix operations:

| Image Operation          | Matrix Operation             |
| ------------------------ | ---------------------------- |
| Brightness change        | Addition                     |
| Edge detection           | Subtraction                  |
| Filtering (Blur/Sharpen) | Multiplication (Convolution) |

This project shows how embedded processors perform such tasks internally.

---

##  Features

* Pure ARM Assembly implementation
* Register-level memory addressing
* Loop-based computation
* Triple nested loop multiplication
* Works on ARMv7 architecture
* Demonstrates convolution logic

---

##  Matrices Used

Matrix A:

```
1 2 3
4 5 6
7 8 9
```

Matrix B:

```
9 8 7
6 5 4
3 2 1
```

---

##  Output

### Addition (Brightness)

```
10 10 10
10 10 10
10 10 10
```

### Subtraction (Edge Difference)

```
-8 -6 -4
-2  0  2
 4  6  8
```

### Multiplication (Filter Operation)

```
 30  24  18
 84  69  54
138 114  90
```

---

##  Tools Used

* ARMv7 Architecture
* Assembly Language
* CPUlator ARM Simulator
  [https://cpulator.01xz.net/?sys=arm](https://cpulator.01xz.net/?sys=arm)

---

##  How to Run

1. Open CPUlator:
   [https://cpulator.01xz.net/?sys=arm](https://cpulator.01xz.net/?sys=arm)

2. Paste the assembly code into the editor

3. Click **Assemble & Load**

4. Run the program

5. Check results in **Memory View**

   * `resultAdd`
   * `resultSub`
   * `resultMul`

---

##  Project Structure

```
matrix-arm/
│── code.s
│── README.md
```

---

##  Working Principle

### Step 1 — Data Initialization

Matrices stored in memory (.data section)

### Step 2 — Addition Loop

Sequential element-wise addition

### Step 3 — Subtraction Loop

Difference between corresponding pixels

### Step 4 — Multiplication

Triple nested loop:

```
C[i][j] = Σ A[i][k] * B[k][j]
```

### Step 5 — Store Result

Results written into dedicated memory blocks

---

##  Real-World Applications

* Surveillance cameras
* Mobile camera processors
* Robotics vision
* Autonomous vehicles
* Medical imaging
* Embedded DSP systems

---

##  Learning Outcomes

* Understanding ARM registers & addressing modes
* Assembly loop construction
* Memory indexing
* Embedded image processing basics
* Relation between math and hardware computation

