## REPORT ON SARSA

SARSA is an on-policy algorithm where, in the current state, S an action, A is taken and the agent gets a reward, R and ends up in next state, S’ and takes the next action, A’ in S’. It is called an on-policy algorithm because it updates the policy based on actions taken. The difference between SARSA and Q-learning is that **SARSA** chooses an action following the same current policy and updates its Q-values whereas **Q-learning** chooses the greedy action, that is, the action that gives the maximum Q-value for the state, that is, it follows an optimal policy.

### ANALYZING THE PROGRAM

The red rectangle must arrive in the circle, avoiding triangle.

The SARSA agent learns every time step from the sample <s,a,r,s’,a’>.  When the agent starts running it initializes the Q-table with a value of 0.0.  Repeating for each episode the agent:

 - Initializes the State, S
 - Choose a random Action, A from State, S using the epsilon- greedy policy
 - Repeat for each step of episode: The agent takes Action , A observing the Reward, R and the next State, S’. It then chooses the next Action, A’ from S’ using the policy derived from the Q-function update rule until the end of the episodes.

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/SARSA/sarsaqfxn.PNG)

Basically, the Q-value is updated taking into account the action, A’ performed in the state, S’ in **SARSA** as opposed to Q-learning where the action with the highest Q-value in the next state, S’ is used to update Q-table.
In this program the agent gets a reward of -100 when it enters any of the two triangles and a reward of 100 when it enters the circle.

Below are screenshots from the program:

|  |  |
|--|--|
| ![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/SARSA/sarsastart.PNG) | ![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/SARSA/sarsa1.png) |


### ADDING A THIRD TRIANGLE WITH -1 REWARD

When the third triangle was added to the grid, it takes a longer  time for the agent to converge compared to the original code.

The following codes were used:

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/SARSA/adtc.PNG)

![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/SARSA/addreward.PNG)


**Screenshots from the program:** The circled values shows the reward for the various images when the agent encounters it.

|  |  |
|--|--|
|![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/SARSA/addtriinitial.PNG)  |![enter image description here](https://github.com/SANDRAKUMI/Machine_Learning_Final-Exam/blob/master/SARSA/addretriangle.png)  |


**By Sandra Kumi/20185122**
