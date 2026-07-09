# Prime Matrix Sieve (Table of 9)

An discovery of a new geometric and arithmetic pattern for distributing prime numbers within a 9-column matrix. The pattern demonstrates how prime numbers rotate around specific numerical centers (the orange cells) based on fixed mathematical relationships.

## 📌 Core Concept of the Pattern

When numbers are arranged in a grid with 9 columns (ordered sequentially from right to left as shown in the matrix), the **orange cells** act as central points of symmetry. 

All prime numbers (with the exception of the three initial anomalous primes: `2`, `3`, and `5`) are guaranteed to fall exclusively within the **green cells** surrounding these orange centers. It is mathematically impossible for any other prime number to appear in the white cells.

![Prime Matrix Grid](primes.jpeg)

## 📐 Mathematical Rule of the Centers (Orange Cells)

Each orange cell ($O$) is surrounded centrally by a pattern of 4 key positions (green cells eligible to be primes). Any of these 4 numbers can be easily accessed using the following fixed formulas:

1. **Top/Key Number:** $O - 11$
2. **Right Number:** $O - 1$
3. **Left Number:** $O + 1$
4. **Bottom/Axial Number:** $O + 11$

> **Note:** The only prime numbers that do not fit into this surrounding rotation are the foundational primes in the first row: `2`, `3`, and `5`.

---

## 🧪 Proof and Examples From the Matrix

To demonstrate the validity of this rule, here is the application of the formulas on the orange points from the provided image:

### 1️⃣ First Orange Center ($O = 12$)
* $12 - 11 = \mathbf{1}$ (Pattern start)
* $12 - 1 = \mathbf{11}$ *(Prime Number - Green Cell)*
* $12 + 1 = \mathbf{13}$ *(Prime Number - Green Cell)*
* $12 + 11 = \mathbf{23}$ *(Prime Number - Green Cell)*

### 2️⃣ Second Orange Center ($O = 18$)
* $18 - 11 = \mathbf{7}$ *(Prime Number - Green Cell)*
* $18 - 1 = \mathbf{17}$ *(Prime Number - Green Cell)*
* $18 + 1 = \mathbf{19}$ *(Prime Number - Green Cell)*
* $18 + 11 = \mathbf{29}$ *(Prime Number - Green Cell)*

### 3️⃣ Third Orange Center ($O = 42$)
* $42 - 11 = \mathbf{31}$ *(Prime Number - Green Cell)*
* $42 - 1 = \mathbf{41}$ *(Prime Number - Green Cell)*
* $42 + 1 = \mathbf{43}$ *(Prime Number - Green Cell)*
* $42 + 11 = \mathbf{53}$ *(Prime Number - Green Cell)*

### 4️⃣ Fourth Orange Center ($O = 48$)
* $48 - 11 = \mathbf{37}$ *(Prime Number - Green Cell)*
* $48 - 1 = \mathbf{47}$ *(Prime Number - Green Cell)*
* $48 + 1 = \mathbf{49}$ *(Green Cell - Composite: $7 \times 7$)*
* $48 + 11 = \mathbf{59}$ *(Prime Number - Green Cell)*

---

## 🧠 Mathematical Explanation

The orange cells in this 9-column grid represent specific multiples of 6 (specifically taking the forms of $30k + 12$ and $30k + 18$). 

Since all prime numbers greater than 5 must strictly follow the forms of $6k \pm 1$ and cannot end in an even digit or 5, your unique 9-column layout perfectly aligns the grid so that the fixed differences ($\pm 1$ and $\pm 11$) cleanly isolate numbers ending in 1, 3, 7, and 9. These are the only possible endings for larger prime numbers, making this matrix a highly effective visual sieve!

## 🚀 How to Contribute?
Feel free to open an `Issue` or submit a `Pull Request` if you write a script (Python / JavaScript) that generates this matrix dynamically for numbers greater than 100.
