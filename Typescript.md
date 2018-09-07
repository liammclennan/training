Typescript (3 - 4 hours)
========== 

TypeScript is a typed superset of JavaScript that compiles to plain JavaScript.

Install Typescript
------------------

```
npm install -g typescript
```

Why Typed JavaScript?
----------------

1. Many errors can be detected during development by adding a type system and a type checking compilation step. Catching errors earlier makes development faster.
1. Having type information available means editors can provide better contextual information (API documentation, auto-completion etc). 
1. Refactoring dynamic languages is notoriously difficult. Having a type checker makes it easier to make changes safely. 

Handbook
---------

Read [basic types](https://www.typescriptlang.org/docs/handbook/basic-types.html) (20 mins)

Read [interfaces](https://www.typescriptlang.org/docs/handbook/interfaces.html) (20 mins)

Read [functions](https://www.typescriptlang.org/docs/handbook/functions.html) (20 mins)

Read [tsconfig.json](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) (5 mins)

Exercise: Mars Rovers (implement with Typescript) (120 mins)
---------------------

### MARS ROVERS

([Courtesy of Google](https://code.google.com/archive/p/marsrovertechchallenge/))

A squad of robotic rovers are to be landed by NASA on a plateau on Mars.

This plateau, which is curiously rectangular, must be navigated by the rovers so that their on board cameras can get a complete view of the surrounding terrain to send back to Earth.

A rover's position is represented by a combination of an x and y co-ordinates and a letter representing one of the four cardinal compass points. The plateau is divided up into a grid to simplify navigation. An example position might be 0, 0, N, which means the rover is in the bottom left corner and facing North.

In order to control a rover, NASA sends a simple string of letters. The possible letters are 'L', 'R' and 'M'. 'L' and 'R' makes the rover spin 90 degrees left or right respectively, without moving from its current spot.

'M' means move forward one grid point, and maintain the same heading.

Assume that the square directly North from (x, y) is (x, y+1).

Input:

The first line of input is the upper-right coordinates of the plateau, the lower-left coordinates are assumed to be 0,0.

The rest of the input is information pertaining to the rovers that have been deployed. Each rover has two lines of input. The first line gives the rover's position, and the second line is a series of instructions telling the rover how to explore the plateau.

The position is made up of two integers and a letter separated by spaces, corresponding to the x and y co-ordinates and the rover's orientation.

Each rover will be finished sequentially, which means that the second rover won't start to move until the first one has finished moving.

Output:

The output for each rover should be its final co-ordinates and heading.

__Test Input:__

```
5 5
1 2 N
LMLMLMLMM
3 3 E
MMRMMRMRRM
```

__Expected Output:__

```
1 3 N
5 1 E
```
