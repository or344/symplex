# 📐 Linear Programming Solver (Simplex Method)

A comprehensive, web-based tool for solving Linear Programming (LP) problems using the **Simplex Method**. Built with HTML, JavaScript, and Math.js, this project is designed for students and researchers to visualize the step-by-step optimization process.

## ✨ Key Features

* **Multiple Solving Methods:**
    * **Big-M Method:** Handles $\ge$ and $=$ constraints automatically using artificial variables.
    * **Two-Phase Method:** Separates the solution into Phase 1 (feasibility) and Phase 2 (optimality).
* **Step-by-Step Derivation:** Displays every iteration of the tableau, including pivot selection, row operations, and ratio tests.
* **Smart Symbolic Display:** Utilizes a hybrid approach for Big-M; calculations are performed numerically (for stability) but displayed symbolically (e.g., $M - 5$) for educational clarity.
* **Math Visualization:** Integrates **MathJax** to render complex mathematical formulas and fractions in LaTeX format.
* **Responsive UI:** Clean, modern interface built with **Bootstrap 5**.

## 📂 Project Structure

This repository contains two main solvers:

### 1. `index.html` (Big-M / Revised Simplex)
The primary solver using the **Revised Simplex** algorithm combined with the **Big-M** technique.
* **Feature:** Solves problems requiring artificial variables without user intervention.
* **Logic:** Implements a numerical approximation ($M=10,000$) for the backend logic while rendering the output in symbolic form ($M$) to mimic manual calculation.

### 2. `two_phase.html` (Two-Phase Method)
A specialized solver for the **Two-Phase Method**.
* **Phase 1:** Minimizes the sum of artificial variables to find a basic feasible solution.
* **Phase 2:** Optimizes the original objective function using the solution from Phase 1.
* **Manual Mode:** Includes a feature to manually input Phase 2 coefficients, allowing students to practice the transition logic between phases.
