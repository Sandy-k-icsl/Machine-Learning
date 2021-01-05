## REPORT ON Q-LEARNING

### ANALYZING THE PROGRAM

The red rectangle must arrive in the circle, avoiding triangle.

### Q-LEARNING PROCESS

 1. Initialize the Q-table
 
In the Q-Table, the columns are the actions and the rows are the states. When the program starts running, <s,a,r,s’> are initiated with a value of 0.0 each. Each Q-table score will be the maximum expected future reward that the agent will get if it takes that action at that state. At each iteration, the values in the Q-table are improved.

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Q_learning/initialise.PNG)

 2. Updating Q-Function

The Q-function is updated with the samples <s,a,r,s’> using the Bellman Optimality Equation which takes two inputs: state (s) and action(a).

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Q_learning/bellman%20eqn.PNG)

 3. Choose and Perform Action

The agent gets action for the state according to the Q-fuunction table and it will pick the action of epsilon policy of greedy. The agent will explore the environment and randomly choose actions. **There are four actions to choose from**: up, down, left, and right. In Q-learning, bad actions information is not included in the current state’s Q-function update

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Q_learning/qfunc.PNG)

 4. Evaluate
 
 After a correct action is chosen and observed an outcome and reward, the Q-function is updated. For this program, if the agent enters the circle, without passing through the triangles it gets a reward of 100. If it enters any of the two triangles it gets a reward of -100.

Below is the screenshot of the program and the circled value shows the reward of the agent whilst it was running

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Q_learning/reward.png)


### ADDING A THIRD TRIANGLE WITH -1 REWARD

The following codes were used:

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Q_learning/tricode.PNG)

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Q_learning/rewardtri3.PNG)


**Screenshots from the program:** The circled values shows the reward for the various images when the agent encounters it.

|  |  |
|--|--|
|![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Q_learning/addtriangle.PNG)  | ![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/Q_learning/addtrireward.png) |


**By Sandra Kumi/20185122**
