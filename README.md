# Genetic Algorithm: Live squares in Java
-    This is my old implemenation of genetic algorithm in Java. No libraries were used, except UI Java libraries.

## Index
   - [Demo](#Demo "Goto Demo")
   - [Description](#Description "Goto Description")
   - [Structure](#Structure "Goto Structure")

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

4) GA (short description)
brain of individuals:
	Right know, individuals have no idea about walls, and how to properly see apples and poison, due to the lack of my code. (it 	
	is more correct to say "due to the fact of my laziness"). Due to the fact that individuals have no idea about walls, and how to 
	properly see apples and poison, best solution for this current problem is stay on the same spot, do not move. So, gene is going 
	to contain only "look" commands. *GA find this solution. It took 1867 generations (approximately 16-17 hours). Probably, it    	
	could be faster or slowly. It depends on a luck of a mutation. Mutation is the main force of GA*

function FitnessCalc.setSolution("integer with length of 32")
	If FitnessCalc.setSolution("int") was setted, GA is going to work qucker, but GA will give only one solution (our solution.it 	
	will be find approximately in 400-500 generations). Also, if FitnessCalc.setSolution("int") was setted, line 34 in java 	
	FitnessCalc have to be uncommented. If not, it will have no impact.
	If FitnessCalc.setSolution("int") was not setted *FitnessCalc.setSolution("")*, GA is going to work slow, but GA will give 	
	more solutions (first solution will be find approximately in 1700-2000 generations). Also, if FitnessCalc.setSolution("int") was 
	not setted, line 34 in java FitnessCalc have to be commented. If not, it will have an error      				
	(java.lang.arrayindexoutofboundsexception).
