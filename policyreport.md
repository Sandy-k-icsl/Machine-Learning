## MACHINE LEARNING HOMEWORK 3 REPORT

### Policy Iteration Report

Grid world with reinforcement learning. The rectangle must reach the circle without encountering the triangles.

## Execution of the original code

Command used : python policy_iteration.py

Below is screenshot of the execution of the code:

|Initial Stage|Final Stage|
|--|--|
| ![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/grid%20eva1.PNG) |![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/final%20stage.PNG)  |

 - At the first stage, all grids have an initial value of 0 and they are updated using the **Evaluate** button.
 - The policy will initialized with the value of `0.25` for all actions. Every action has the same chance to be utilized to update the value. The policy will be updated in every click of `Improve` button
 
To get the most efficient result, you need to click the **Evaluate** and **Improve** buttons.

## Changing the initial values to random values

Modify the initial value of the value_table from `0` to random distribution between `0 to 1`.

![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/change.PNG)

Below is screenshot of the execution of the code:

|Initial Stage  |Final Stage |
|--|--|
|![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/sce2.PNG)  |![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/sc2final.PNG)  |


##  Add one more triangle with reward = -1 at (3,4)

![](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/reward.PNG)


Below is the screenshot of the initial stage and final stage:

|Initial Stage  | Final Stage |
|--|--|
|![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/addt.PNG)  | ![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/ftadd.PNG) |


**By Sandra Kumi/20185122**

















