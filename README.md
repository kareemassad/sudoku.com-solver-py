# Sudoku.com Expert Puzzle Solver

A program that uses the backtracking algorithm and the Python Selenium Library to solve an expert sudoku board live on sudoku.com.

![](https://github.com/kareemassad/sudoku-solver-py/blob/master/img/full-gif-99comp.gif)

## How to run

1) Install all packages in your project directory

```bash
$ pip install -r requirements.txt
```

2) Make sure that you are using the appropriate web driver for your browser. The default implementation is for Chrome.

3) Run selen.py using

```bash 
$ py selen.py
```

4) Modify solving paramaters in selen.py

## Implementation

This program uses the backtracking algorithm to solve the Sudoku puzzle.

1) Locate the empty spaces in the project. To start we will be using the number 0 to place them as Sudoku only uses numbers between 1-9.
2) Attempt to place numbers 1-9 in the place of the 0.
3) Check if the digit is valid in the current spot based on the current board.
   1) If valid, recursivly attempt to fill the board.
   2) If invalid, reset the entry just filled and try again.
4) Once the board is full, the puzzle is solved.

The program then uses the Selenium Python library to open an instance of chrome with the url : Sudoku.com/expert/. It then copies the board, solves it, then inputs it back into the site using the given numpad.

## Credits 
Credits to TechWithTim for parts of his Sudoku Solver

## License 
This project is under the MIT Licence for Open Source.
