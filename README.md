# Prime Matrix Sieve (Table of 9)

An discovery of a new geometric and arithmetic pattern for distributing prime numbers within a 9-column matrix. The pattern demonstrates how prime numbers rotate around specific numerical centers (the orange cells) based on fixed mathematical relationships.

## 📌 Core Concept of the Pattern

When numbers are arranged in a grid with 9 columns (ordered sequentially from right to left as shown in the matrix), the **orange cells** act as central points of symmetry. 

All prime numbers (with the exception of the three initial anomalous primes: `2`, `3`, and `5`) are guaranteed to fall exclusively within the **green cells** surrounding these orange centers. It is mathematically impossible for any other prime number to appear in the white cells.

![Prime Matrix Grid](Images/primes.jpeg)

## 📐 Grid Navigation & Matrix Rules

The entire matrix operates on precise horizontal and vertical stepping rules that allow seamless navigation between the centers and their surrounding elements:

### 1. Rotation Around an Orange Center ($O$)
Each orange cell ($O$) is surrounded centrally by a pattern of key positions (green cells eligible to be primes), easily accessed via:
* **Top/Key Number:** $O - 11$
* **Right Number:** $O - 1$
* **Left Number:** $O + 1$
* **Bottom/Axial Number:** $O + 11$

### 2. Horizontal Translation Between Centers ($\pm 6$)
* To move from a **Right Orange Center** to the corresponding **Left Orange Center** on the same row, **add 6** to its value ($O_{Right} + 6 = O_{Left}$).
* Conversely, to move from a **Left Center** back to the **Right Center**, **subtract 6** ($O_{Left} - 6 = O_{Right}$).

### 3. Vertical Translation Between Rows ($+ 30$)
* To move vertically from any orange center to the center directly underneath it in the next section, **add 30** to its value ($O_{Current} + 30 = O_{Below}$).

> **Note:** The only prime numbers that do not fit into this surrounding rotation are the foundational primes in the first row: `2`, `3`, and `5`.

---

## 🧪 Proof and Examples From the Matrix

### 🔹 Verifying Horizontal Stepping ($\pm 6$)
* **Row 2:** Start at Right Center ($\mathbf{12}$). Move left: $12 + 6 = \mathbf{18}$ (Left Center).
* **Row 5:** Start at Right Center ($\mathbf{42}$). Move left: $42 + 6 = \mathbf{48}$ (Left Center).
* **Reverse:** Start at Left Center ($\mathbf{78}$). Move right: $78 - 6 = \mathbf{72}$ (Right Center).

### 🔹 Verifying Vertical Stepping ($+ 30$)
* From Center $\mathbf{12}$ to the center below it: $12 + 30 = \mathbf{42}$.
* From Center $\mathbf{42}$ to the center below it: $42 + 30 = \mathbf{72}$.
* From Center $\mathbf{18}$ to the center below it: $18 + 30 = \mathbf{48}$.
* From Center $\mathbf{48}$ to the center below it: $48 + 30 = \mathbf{78}$.

### 🔹 Verifying the Surrounding Rotations
* **Around Center $O = 12$:**
  * Top: $12 - 11 = 1$ | Right: $12 - 1 = 11$ | Left: $12 + 1 = 13$ | Bottom: $12 + 11 = 23$
* **Around Center $O = 78$:**
  * Top: $78 - 11 = 67$ | Right: $78 - 1 = 77$ | Left: $78 + 1 = 79$ | Bottom: $78 + 11 = 89$

---

## 🧠 Mathematical Explanation

The structure of this 9-column grid perfectly maps the properties of modular arithmetic. The vertical step of **$+30$** represents the primorial $\mathbf{2 \times 3 \times 5 = 30}$. By cycling every 30 numbers, the grid automatically filters out all multiples of 2, 3, and 5. 

Combined with the horizontal shifts ($\pm 6$), this layout flawlessly aligns the remaining potential prime candidates into the green columns, leaving the white areas strictly populated by composite numbers.

## 🚀 How to Contribute?
Feel free to open an `Issue` or submit a `Pull Request` if you write a script (Python / JavaScript) that generates this matrix dynamically for numbers greater than 100.
