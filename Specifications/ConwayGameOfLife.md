# Conway's Game of Life
This kata is not for the faint of heart :)

## Background Information
* The universe of the Game of Life is an infinite two-dimensional orthogonal grid of square cells.
* Each cell is in one of two possible states, alive or dead. 
* Every cell interacts with its eight neighbours: cells that are horizontally, vertically, or diagonally adjacent. 
* At each step in time, the following transitions occur:
  * Any live cell with fewer than two live neighbours **dies**, as if caused by under-population.
  * Any live cell with two or three live neighbours **lives** on to the next generation.
  * Any live cell with more than three live neighbours **dies**, as if by over-population.
  * Any dead cell with exactly three live neighbours becomes a live cell, as if by reproduction.

* The initial pattern constitutes the seed of the system. 
* The first generation is created by applying the above rules simultaneously to every cell in the seed—births and deaths occur simultaneously, and the discrete moment at which this happens is sometimes called a tick (in other words, each generation is a pure function of the preceding one). 
* Repeat to create further generations.

* There should be no explosive growth.
* There should exist small initial patterns with chaotic, unpredictable outcomes.
* There should be potential for von Neumann universal constructors.

### Patterns:
* Still patterns: Block, Behive, Float, Boat
* Oscillator patterns: Pulsar, beacon, blinker, toad, pulsar, pentadecathlon
* Spaceship patterns: Glider, LightWeight SpaceShip (LWSS)

## Further Challenges:
Here are some things that you should try when solving this kata (these rules can be used with any kata):
- Don't use any primitive types
- Don't use any if/else statements
- No method can have more than 4 lines
