# Snake

You will be given an integer n for the size of the territory with square shape.  
On the next n lines, you will receive the rows of the territory.   
The snake will be placed on a random position, marked with the letter **'S'**.  
There will also be food on random positions, marked with **'*'**. The territory may have lair.   
The lair will have two burrows marked with the letter - **'B'**. All of the empty positions will be marked with **'-'**.  
Each turn, you will be given command for the snake’s movement. When the snake moves it leaves a trail marked with **'.'**  
Move commands will be: **"up", "down", "left", "right"**.

If the snake moves to a food, it will eat the food, which will increase food quantity with one.  
If it goes inside to a burrow, it goes out on the position of the other burrow and then both burrows disappear.   
If the snake goes out of its territory, the game is over. The snake needs at least **10** food quantity to be fed.  
If the snake goes outside of its territory or has eaten enough food, the game should end.  
  
### Input  
On the first line, you are given the integer n – the size of the square matrix.  
The next n lines holds the values for every row.  
On each of the next lines you will get a move command.  
  
### Output  
On the first line:    
If the snake goes out of its territory, print: **"Game over!"**  
If the snake eat enough food, print: **"You won! You fed the snake."**  
On the second line print all food eaten: **"Food eaten: {food quantity}"**  
In the end print the matrix.  
    
### Constraints  
The size of the square matrix will be between [2…10].  
There will always be 0 or 2 burrows, marked with - 'B'.  
The snake position will be marked with 'S'.  
The snake will always either go out of its territory or eat enough food.  
There will be no case in which the snake will go through itself.  
  
## Examples    
- Input 
  
6  
\-----S  
\----B-  
\------  
\------  
\--B---  
\--*---  
left  
down  
down  
down  
left
  
- Output  
   
Game over!  
Food eaten: 1    
\----..  
\----.-  
\------  
\------  
\--.---  
\--.---  
  
- Comments  
  
|(1) left|(2) down |(3) down |(4) down |
|:------:|:-------:|:-------:|:-------:| 
| ----S. | ----..  |  ----.. |  ----.. | 
| ----B- | ----.-  |  ----.- |  ----.- |  
| ------ | ------  |  ------ |  ------ | 
| ------ | ------  |  ------ |  ------ | 
| --B--- | --S---  |  --.--- |  --.--- | 
| --\*---| --\*--- |  --S--- |  --.--- | 
  
(3) eat the food: '*' (5, 2)  
(4) the snake goes out from its territory and the program ends  
  
- Input  
7  
--\*\*\*S-  
--\*----  
--\*\*\*--  
---\*\*--  
---\*---  
---\*---  
---\*---  
left  
left  
left  
down  
down  
right  
right  
down  
left  
down  
  
- Output  

You won! You fed the snake.  
Food eaten: 10  
--....-  
--.----  
--...--  
---..--  
---S---  
---\*---  
---\*---  
  
