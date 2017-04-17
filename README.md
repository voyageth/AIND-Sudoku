# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: 
[Naked twins](http://www.sudokudragon.com/sudokustrategy.htm#XL2104) is sudoku exclude possibilities strategy.
![after](https://d17h27t6h515a5.cloudfront.net/topher/2017/January/5877cc78_naked-twins-2/naked-twins-2.png)
"F3" and "I3" is naked twins. 
Some unit that contains that twins(column 3), other peer can not have naked twins's values. 
As a result, "D3" and "E3" can not have {2,3}.
We reduce the number of possibilities for "D3" and "E3" and solve the naked twins problem.


# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: Add diagonal constraint to main diagonal boxes. 
The two main diagonals, the numbers 1 to 9 should all appear exactly once
For example, "A1" can has {1, 2, 4, 9} and "A9" can has {2, 6, 8}.
With diagonal constraint, If E5 has value 2, "A1" and "A9" can not has value 2. 
So "A1"'s possibilities are {1,4,9} and "A9"'s are {6,8}.
We reduce the number of possibilities for "A1" and "A9" by diagonal constraint.
![diagonal](https://d17h27t6h515a5.cloudfront.net/topher/2017/January/587467eb_diagonal-sudoku/diagonal-sudoku.png)
 

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.

q