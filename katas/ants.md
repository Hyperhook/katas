## Intro
Ants have amazing skills, from [lifting 5000 times their weight](https://entomologytoday.org/2014/02/11/ants-can-lift-up-to-5000-times-their-own-body-weight-new-study-suggests/) to naturally resorting to heuristics when solving problems, this kata pays a little homage to our little fellows in the observing of emergent behaviour.

We'll have an application that has an ant running on a grid, and we will pass rules to it to observe its behaviour. This is also known as a [Langton's Ant](https://en.wikipedia.org/wiki/Langton%27s_ant).

Example:
Considering the rules:
 - At a white square turn 90° clockwise, flip the color of the square, move forward one unit.
 - At a black square, turn 90° counter-clockwise, flip the color of the square, move forward one unit.
 
This is how the first 200 steps of the ant would look like with the rules above (using the notation 'RL'):

![Ant animation](https://upload.wikimedia.org/wikipedia/commons/0/09/LangtonsAntAnimated.gif)

## Rules

- The code **must** be tested, do it for the ants.
- The grid must be shown after every step so we can observe it.
- We must be able to stop the code after `x` iterations.

## Harder version
To make things more interesting we can change the amount of colors we are using, this still follows the convention of using `'L'` and `'R'` for defining in which direction to turn, this of course depends on the grid, if you decide to implement an hexagonal grid for example, you open up the following notations as well:
- `U` turns 180°
- `R1` turns 60° clockwise
- `R2` turns 120° clockwise
- `L1` turns 60° counter-clockwise
- `L2` turns 120° counter-clockwise
