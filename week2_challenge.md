# Problem
![Robot](https://media.giphy.com/media/I7kkegrRyNrk4/giphy.gif)

You are working with a computer simulation of a mobile robot. The robot moves on an plane, and its movements are described by a command string consisting of one or more 
of the following letters:

* `G` instructs the robot to move forward one step
* `L` instructs the robot to turn left
* `R` instructs the robot to turn right

The robot CANNOT go backwards - poor robot. After running all of the movement commands, you want to know if the robot returns to its original starting location.

For instance, the command `GRGRGRG` would make the robot return to its original starting location.

# Instructions

1. Copy this markdown and paste in your own, privte gist
2. In your private gist, fill out the questions below
4. Submit by the due time as instructed in Zoom

Do not publish your code on a public repl.it or repo or other public means.

## Rewrite the question in your own words:
given a set of corresponding commands, check to see if the robot is at it's starting location.

## What assumptions will you make about this problem if you cannot ask any more clarifying questions? What are your reasons for making those assumptions?
clarifying question: are there bounds? (answered assume infinite plane)

## What are your initial thoughts about this problem? (high level design, 2-3 sentences)
build a grid class, with check location method, logging original position.
build a robot class, (given complexity) command and execution will live inside robot class.

## How would you identify the elements of this problem?

- [ ] Searching of Data
- [ ] Sorting of Data
- [ ] Pattern Recognition
- [x] Build/Navigate a Grid
- [ ] Math
- [ ] Language API knowledge
- [ ] Optimization


## Which data structure(s) do you think you'll use? What pros/cons do you see with that choice?
hash map
pro
easy to access to convert string to command
con
n/a
## Write out a few lines of initial pseudocode: (mid-level design, NOT REAL CODE)
robot should have execute method,
execute method should be able to iterate over the command string and execute actions accordingly,
should be a hash map that maps string to command, G => foward, L => left, R => right
grid has a check location method
grid is initialized with robot location
grid can use a-z 

## Revision
Since we are only concerned about the original position of the robot
we only care about the string input that dictates the movement of the robot, whether that will put the robot in it's original position
perhaps we can codes it with a stack that is mapped to north => south, east => west,
if the stack is empty after the moves, then it is at it original position, else not

## Psuedo 2
assume robot is facing due north as starting position
add movements with "G" command
calculate direction from "G" to the next "G"
let "G" be the command to add to stack
let strings between "G"s decitate direction
