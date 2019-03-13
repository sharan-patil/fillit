# fillit
Tetriminos are the individual blocks in the classic tetris game.
Examples:
####   #    ##
      ###   ##
This project takes in a input file with 1-26 tetriminos and outputs the arrangement of all these tetriminos blocks in the smallest square possible. If there are multiple possible smallest squares, the one with all the blocks in their most top-left positions is chosen. The solution 's tetriminos are labelled from 'A' to 'Z' based on the positioning of itself in the input file. There may be blank spaces in the solution filled with '.' characters.
Example of a input file:
....
##..
.#..
.#..

....
####
....
....

#...
###.
....
....

....
##..
.##.
....
Output of the above file:
DDAA
CDDA
CCCA
BBBB

This project uses an iterative backtracking algorithm which works in a 2d array of integers with the tetriminos' coordinates as values. This implementation is much faster than working with character arrays as every step in the backtracking algorithm involves just integer addition. The coordinates of all the teriminos are saved into a global variable after the characters are read from the input file.
