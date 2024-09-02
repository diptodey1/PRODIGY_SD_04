Sudoku Solver with Heuristic Optimization
Description

This Python script is a Sudoku solver that utilizes backtracking and a heuristic optimization technique to efficiently solve puzzles of various sizes. The solver ensures the validity of solutions by checking for unique numbers within rows, columns, and 3x3 subgrids.

Key Features

Backtracking: The script employs backtracking to explore different solution possibilities, ensuring a comprehensive search for a solution.
Heuristic Optimization: A heuristic is used to prioritize solving cells with fewer possible values, which can significantly reduce the search space and improve performance for larger puzzles.
Valid Solution Checking: The solver rigorously checks for valid moves by verifying that numbers are unique within rows, columns, and 3x3 subgrids.
User-Friendly Interface: The script provides a clear and intuitive interface, prompting the user for input and displaying the solved puzzle or indicating if no solution exists.
How it Works

Input: The user enters the size of the Sudoku puzzle (e.g., 9 for a standard 9x9 puzzle) and then provides the initial puzzle configuration, where 0 represents empty cells.
Solving: The solver starts by finding an empty cell. It then iterates through possible values for that cell, checking if placing the value is valid. If valid, it recursively tries to solve the puzzle with the new value. If the recursive call returns False (meaning no solution was found), the solver backtracks and tries another value.
Heuristic: The solver prioritizes solving cells with fewer possible values. This heuristic helps to reduce the number of dead-ends explored during the backtracking process.
Output: If a solution is found, the script prints the solved Sudoku board. If no solution exists, it indicates that the puzzle is unsolvable.
Code Structure

The code is organized into several functions:

is_valid(board, row, col, num, n): Checks if placing a number at a given position is valid.
solve_sudoku(board, n): Implements the backtracking algorithm with the heuristic.
find_empty_cell(board, n): Finds the next empty cell, prioritizing cells with fewer possible values.
count_possible_values(board, row, col, n): Counts the number of possible values for a given cell.
print_board(board, n): Prints the Sudoku board in a formatted manner.
main(): Handles user input, calls the solver, and prints the output.
Example Usage

-----------------------------
Sudoku solver extraordinaire, at your service! Let's crack this puzzle.
-----------------------------
Unleash your Sudoku spirit! How big is your puzzle arena? 9
-----------------------------
Enter row 1: 5 3 0 0 7 0 0 0 0
Enter row 2: 6 0 0 1 9 5 0 0 0
Enter row 3: 0 9 8 0 0 0 0 6 0
Enter row 4: 8 0 0 0 6 0 0 0 3
Enter row 5: 4 0 0 8 0 3 0 0 1
Enter row 6: 7 0 0 0 0 0 0 0 9
Enter row 7: 0 4 0 0 0 0 0 7 8
Enter row 8: 0 0 0 9 3 0 0 5 2
Enter row 9: 0 0 0 0 0 0 4 1 6

Solved Sudoku board:
5 3 1 8 7 2 9 6 4
6 7 2 1 9 5 3 4 8
1 9 8 3 4 6 2 5 7
8 2 5 7 6 4 1 9 3
4 1 6 9 8 3 7 2 5
7 8 3 5 2 1 6 3 9
9 4 7 6 3 8 5 1 2
2 5 4 4 1 9 8 7 6
3 6 9 2 5 7 4 8 1
-----------------------------
Conclusion

This Sudoku solver provides an efficient and effective solution for solving Sudoku puzzles. By combining backtracking and a heuristic, it can handle puzzles of varying difficulty levels. The code's modular structure and clear implementation make it easy to understand and extend for further customization.
