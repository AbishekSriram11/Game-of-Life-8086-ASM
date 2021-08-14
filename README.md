# GameOfLife8086ASM
Game of Life in 8086 assembly.

A homage to the set of rules put forward by John Horton Conway.

+ Any live cell with fewer than two live neighbours dies, as if caused by under-population.
+ Any live cell with two or three live neighbours lives on to the next generation.
+ Any live cell with more than three live neighbours dies, as if by overcrowding.
+ Any dead cell with exactly three live neighbours becomes a live cell, as if by reproduction.

+ study of a particular pattern of life and apply this rules and stimulate and observe the change to get a new pattern(generation)or change.
+ A stable pattern of life is when each cell has exactly 3 neighbours a 2*2 grid pattern of cells is stable and strong.
+ Glider pattern of cells are energised because its pattern repeat every 4 th cycle cells move and glider pattern again comes at every 4 th cycle(regaularity) independent existance of cells.


Written using the 80x86 assembly instruction set.
Compiled with in DOSBox.

Examples:
![alt text][linearInitial]
![alt text][linearFinal]

+ We implement this in assembler using grid 2d arrays
A dense representation in which all the cells are encoded in a width*height matrix. The dead cells are represented by a zero (or false) and the alive cells are represented by a 1 (or true). The position of a cell on the grid is defined by its position in the matrix.
+ A sparse representation in which only living cells are encoded. Each living cell is represented by its position (int, int) on the grid. All these living cells are aggregated in a dictionary structure.