# Sudoku Solver (Python)

This project is a **Sudoku Solver** implemented in Python as part of the **Scientific Computing with Python** certification on **FreeCodeCamp**. It takes an incomplete Sudoku board as input and finds the correct solution using the **Backtracking Algorithm**.

## 🧩 Features

- **Backtracking Algorithm**: Efficiently solves Sudoku puzzles using recursion and constraint propagation.
- **Object-Oriented Approach**: Uses a `Board` class to encapsulate all Sudoku-solving logic.
- **Customizable Input**: Accepts a 9×9 grid as a list of lists.
- **Validations**:
  - Ensures each number placement follows Sudoku rules (row, column, and 3×3 box constraints).
  - Checks for an empty cell and finds the next possible number to place.
- **Printable Board Representation**: Displays both the unsolved and solved Sudoku boards in a user-friendly format.

---

## 🔍 How It Works

The program follows these steps:
1. **Find an empty cell** in the board (denoted by `0`).
2. **Check for valid numbers (1-9)** that can be placed in that position.
3. **Recursively place a number** and attempt to solve the rest of the board.
4. **Backtrack if needed** (i.e., if a placement leads to a dead end, revert it and try another number).
5. **Return the solved board** when all cells are correctly filled.

---

## 🖥️ Code Overview

### `Board` Class
The `Board` class is responsible for handling all Sudoku-solving operations.

- `find_empty_cell()`: Locates the first empty cell (0) in the board.
- `valid_in_row(row, num)`: Checks if `num` can be placed in a row.
- `valid_in_col(col, num)`: Checks if `num` can be placed in a column.
- `valid_in_square(row, col, num)`: Checks if `num` can be placed in its 3×3 subgrid.
- `is_valid(empty, num)`: Combines the above three validation checks.
- `solver()`: Implements the **Backtracking Algorithm** to solve the puzzle.

### `solve_sudoku(board)` Function
- Creates an instance of the `Board` class.
- Prints the **unsolved puzzle**.
- Calls the `solver()` method to solve it.
- Prints the **solved puzzle** if successful, otherwise, notifies that the puzzle is unsolvable.

---

## 📌 Example Input & Output

### Input (Unsolved Sudoku):
```plaintext
Puzzle to solve:
* * 2 * * 8 * * *
* * * * * 3 7 6 2
4 3 * * * * 8 * *
* 5 * * 3 * * 9 *
* 4 * * * * * 2 6
* * * 4 6 7 * * *
* 8 6 7 * 4 * * *
* * * 5 1 9 * * 8
1 7 * * * 6 * * 5
```

### Output (Solved Sudoku):
```plaintext
Solved puzzle:
5 6 2 9 7 8 4 1 3
8 1 9 6 4 3 7 6 2
4 3 7 1 2 5 8 9 6
6 5 8 2 3 1 5 9 4
7 4 1 8 9 5 3 2 6
9 2 3 4 6 7 1 8 7
3 8 6 7 5 4 9 5 1
2 9 4 5 1 9 6 3 8
1 7 5 3 8 6 2 4 5
```

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/sudoku-solver.git
   cd sudoku-solver
   ```
2. Run the script:
   ```bash
   python sudoku_solver.py
   ```

---

## 🛠️ Requirements
- Python 3.x
- No external dependencies required

---


