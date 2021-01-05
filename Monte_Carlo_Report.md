## MACHINE LEARNING FINAL EXAM REPORT

###  Monte Carlo Report

The Monte Carlo method for reinforcement learning learns directly from episodes of experience without any prior knowledge of MDP transitions. The agent only gets reward at the end of the episodes. The agent makes better decisions with each iteration.

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Monte_Carlo/monte%20eqn.PNG)

**HOW MONTE CARLO WORKS IN THE GRID WORLD EXAMPLE**

 - This Grid World  example uses 1000 episodes
 - The agent always start at  the same  starting point
 - At the end of the episode, there is a list of State, Actions, Rewards, and New States
 - For every episode, agent updates q function of visited states
 - Get action for the state according to the q function table
 - By running more and more episodes,  the agent will learn to play better and better

Below are screenshots for the  program and how it runs:

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Monte_Carlo/montecarlorunning.gif)

 
 ![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Monte_Carlo/cmd.PNG)


## ADDING A TRIANGLE TO THE GRID

I added another triangle at (3,2) to the grid.

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Monte_Carlo/addtri.PNG)

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Monte_Carlo/addtriangle.PNG)

**How the it runs:**

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Monte_Carlo/montecarloaddtri.gif)




**By Sandra Kumi/20185122**


