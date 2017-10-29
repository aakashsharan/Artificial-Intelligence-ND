# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?
A: Every square in a Sudoku board has constraints enforced by the rules of the game. One of the constraints is when two squares of a unit(i.e. a column, row or 3x3 block) has exactly two possible values that can be assigned to the squares, those values may not be assigned to the rest of the squares in the unit. We call such pairs of squares as Naked Twins. Using that kind of elimination is called Naked Twins Technique.

We use constraint propagation to reduce the search space by applying the Naked Twins Technique. This pattern can also be extended to triplets (where three boxes have the same three possibilites) and more.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?
A: A diagonal sudoku is resolved using the same constraint propagation techniques as a regular sudoku: we apply repeatedly the available elimination techniques (elimination, only-choice and naked twins) to every square of the board. The only change we make here is that we add the constraint that no boxes in a same diagonal can take already used digits. By adding the two major diagonals to our list of units, our agent enforces these constraints allowing our sudoku solver to reduce the unsolved boxes in the puzzle for diagonal sudoku in addition to regular sudou.

### Install

This project requires **Python 3**.

We recommend to install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project.
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - Fill in the required functions in this file to complete the project.
* `test_solution.py` - You can test your solution by running `python -m unittest`.
* `PySudoku.py` - This is code for visualizing your solution.
* `visualize.py` - This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the `assign_value` function provided in solution.py
