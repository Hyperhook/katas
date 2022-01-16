# Intro

Spiders are amazing creatures, their ability to put traps to catch their pray is famous, but what happens when they try to hunt their own species?
Let's create a scenario to see if we can trap a spider while being a spider!

## Requirements

Create an turn-based application where our spider will chase another spider.
We have 10 moves to catch our prey, if we fail, our spider dies.
On each turn we will control the spider and pass it a command that orders it where to move to, out of bound moves are not allowed as we should only move within the map.
The map should be printed at each turn so we can see how the game is developing.

### Rules
- The starting distance between our spider and our prey is 2 spaces.
- The starting positions can be random.
- Each spider can only move on their turn.
- The prey spider has to try and escape us, it shouldn't try to go towards our direction.
- Each spider has to follow the existing paths, no new paths can be created.
- We have 10 turns to play.
- If our spider catches it's prey, the game ends and we win.
- If our spider fails to catch it's prey, the game ends and we lose.

### Map

     / - - O - O - O - O
    /      |   |   |   |
    |  / - O - O - O - O
    | /    |   |   |   |
    O - -  O - O - O - O
    | \    |   |   |   |
    |  \ - O - O - O - O
    \      |   |   |   |
     \ - - O - O - O - O
