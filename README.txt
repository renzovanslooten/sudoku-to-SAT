CSC 320 Project 2015
SAT-Based Sudoku Solving
Ethan Wipond V00773575

Second and third extended tasks were not attempted. 

Contents:
README.txt --- this file
sudoku-to-cnf.py --- translates sudoku to cnf 
sudoku-to-cnf-alt.py --- alternate encoding (extended task)
cnf-to-sudoku.py --- translates sat solution to sudoku
in.txt --- sample input for sudoku-to-cnf.py

sudoku-to-cnf.py translates partially solved sudoku puzzles into 
CNF formulas suitable for input to the minisat SAT solver. To use:

python sudoku-to-cnf.py -i <sudoku-inputfile> -o <cnf-outputfile>

(A sample input file is provided in in.txt). Then output file can then
be used with minisat:

minisat <cnf-outputfile> <sat-outputfile>

cnf-to-sudoku.py tranlates the set of assinments to variables output
by minisat back into the form of a solved sudoku puzzle. To use: 

python cnf-to-sudoku.py -i <sat-outputfile> -o <sudoku-outputfile>

The formatted, solved puzzle is found in <sudoku-outputfile>.

sudoku-to-cnf-alt is the same as sudoku-to-cnf, but includes the 
alternate, extended encoding given in 'Sudoku as a SAT Problem'. It's 
usage is the same as sudoku-to-cnf.  


