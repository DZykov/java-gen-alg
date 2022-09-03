# Adventure: Simple todo-cli
-    Simple todo-cli made with python. Supports multiples projects, colours, and repeated tasks. 

## Index
   - [Workflow](#Workflow "Goto Workflow")
   - [Demo](#Demo "Goto Demo")
   - [Installation](#Installation "Goto Installation")
   - [Features](#Features "Goto Features")
   - [Commands](#Commands "Goto Commands")
   - [Structure](#Structure "Goto Structure")
   - [To-Do and Issues](#To-Do-and-Issues "Goto ToDo-and-Issues")


https://user-images.githubusercontent.com/38252337/188287893-6bbe11fa-872b-4810-86c8-f23d6d824db1.mp4

Genes

0 - move up
1 - move right
2 - move down
3 - move left
4 - look up by 3 squares
5 - look right by 3 squares
6 - look down by 3 squares
7 - look left by 3 squares

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
