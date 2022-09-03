# Genetic Algorithm: Live squares in Java
-    This is my old implemenation of genetic algorithm in Java. No libraries were used, except UI Java libraries.

## Index
   - [Demo](#Demo "Goto Demo")
   - [Description](#Description "Goto Description")
   - [Structure of outputs](#Structure "Goto Structure")
   - [Final thoughts](#Thoughts "Goto Thoughts")

## Demo
![alt text](https://github.com/DZykov/java-gen-alg/blob/main/img/show_case.png)

![alt text](https://github.com/DZykov/java-gen-alg/blob/main/img/show_case1.png)

https://user-images.githubusercontent.com/38252337/188287893-6bbe11fa-872b-4810-86c8-f23d6d824db1.mp4


## Description

### Environment

Yellow squares are "living organisms" that try to survive in the environment. All living creatures have 100 health points. Every time they perform a move (step to the right/left/up/down), they lose 1 health point. However, creatures can look around them to choose a direction where to move or stay at the same spot. Living organisms spawn randomly every generation/iteration. There are 50 creatures every generation/iteration.

Gray squares are walls. There are generated two walls: vertical and horizontal. Creatures cannot walk through walls. Walls spawn randomly every generation/iteration.

Green squares are apples. When creature steps on an apple, it eats it and gains health points. Apples spawn randomly every generation/iteration.

Red squares are poison. When creature steps on poison, it eats it and loses health points. Poison spawns randomly every generation/iteration.

### Living creatures/yellow squares

The purpose of living creatures is to come up with the best strategy that maximizes their life span.

Living creatures have genes that consist of 32 actions. There 8 possible actions for 1 slot.

|Code|Action                 |
|----|-----------------------|
|0   |move up                |
|1   |move right             |
|2   |move down              |
|3   |move left              |
|4   |look up by 3 squares   |
|5   |look right by 3 squares|
|6   |look down by 3 squares |
|7   |look left by 3 squares |

## Structure

The application returns one file which contains all information about each generation/iteration: number of genearation, life span of generation, and all genes for every individual, 

## Thoughts

I am satisfied with this project. However, the solution to the given problem is trivial: the creature has to stay in one spot to achieve an infinite life span. This is possible, if and only if the whole gene consists of look-up actions.