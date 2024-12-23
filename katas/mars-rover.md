# Instructions:

A robotic rover is to be landed by NASA on a plateau on Mars.

This plateau, which is curiously rectangular, must be navigated by the rover so that their onboard cameras can get a complete view of the surrounding terrain to send back to Earth.

Your task is to develop an API that moves the rover around the plateau.

In this API, the plateau is represented as a 10x10 grid, and a rover has state consisting of two parts:

- Its position on the grid (represented by an X,Y coordinate pair)
- The direction the compass is facing (represented by a letter, one of  `N`, `S`, `E`, `W`)

The starting position of the rover is `0:0:N`

# Input

The input to the program is a string of one-character move commands:

`L` and `R` rotate the direction the rover is facing
`M` moves the rover one grid square forward in the direction it is currently facing.
If a rover reaches the end of the plateau, it wraps around the end of the grid.

# Output

The program's output is the final position of the rover after all the move commands have been executed. The position is represented as a coordinate pair and a direction, joined by colons to form a string. For example: a rover whose position is `2:3:W` is at square (2,3), facing west.

## Examples
given an input `MMRMMLM` then the output should be `2:3:N`
given an input `MMMMMMMMMM` gives output `0:0:N` (due to wrap-around)

![mars-rover-animation](https://www.codurance.com/hs-fs/hubfs/MarsRoverAnimation.gif?width=1298&name=MarsRoverAnimation.gif)

# Interface

There are no restrictions on the design of the public interface.

A public interface to the API **could** look something like this:

```python
class Rover:
  def execute(self, command: str) -> str:
    ...
```

# Rules:
The rover receives an string of commands e.g. `RMMLM` and returns the finishing point after the moves e.g. `2:1:N`
The rover wraps around if it reaches the end of the grid.

Credit: Google Code Archive
