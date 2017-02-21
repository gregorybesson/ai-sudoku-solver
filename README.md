# AI Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: The first step is to locate naked twins in each unit of the sudoku. For a non diagonal sudoku, we have 27 units. For a diagonal Sudoku, we have 29 units. For each unit, we build an array of naked twins (we use the Counter class of Python). Once we have collected our constraints, we have to propagate it inside the unit by removing the values of the naked twins from the other boxes. 
This additional algorithm makes the number of iterations to solve the sudoku shorter.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: The diagonal sudoku adds 2 units to our algorithm: The right diagonal and the left diagonal. Once we've added these units, our whole algorithm remains the same:

```
diag_units = [['A1','B2','C3','D4','E5','F6','G7','H8','I9'], ['A9','B8','C7','D6','E5','F4','G3','H2','I1']] 
unitlist = row_units + column_units + square_units + diag_units
```

### Install

This project requires **Python 3**.

You'll find the anaconda env file to help you setup the project

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization.

### Code

* `solutions.py` - The program itself.
* `solution_test.py` - The unit tests.
* `PySudoku.py` - This is code for visualizing your solution.
* `visualize.py` - This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py
