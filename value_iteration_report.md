## MACHINE LEARNING HOMEWORK 3 REPORT

###  Value Iteration Report

Grid world with reinforcement learning. The rectangle must reach the circle without encountering the triangles.

## Execution of the original code

Command used : python value_iteration.py

Below is screenshot of the execution of the code:

|Initial Stage|Final Stage|
|--|--|
| ![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/value%20iteration/originitial.PNG) | ![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/value%20iteration/origfinal.PNG) |

 - At the first stage, all grids have an initial value of 0 and they are updated using the **Calculate** button.
 - The grids (4,3) and (3,4) besides the circle (destination) has a value of 1 because they are closer to the reward.
 


## Changing the initial values to random values

Modify the initial value of the value_table from `0` to random distribution between `0 to 1`.

![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/value%20iteration/random.PNG)

Due to the random values used, the time taken for the rectangle to reach the circle takes a longer time compared to the original code.
Below is screenshot of the execution of the code:

|Initial Stage  |Final Stage |
|--|--|
|![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/value%20iteration/2initial.PNG) | ![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/value%20iteration/2final.PNG) |


##  Add one more triangle with reward = -1 at (3,4)

![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/value%20iteration/addt.PNG)
![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/value%20iteration/adtri.PNG)


Below is the screenshot of the initial stage and final stage:

|Initial Stage  | Final Stage |
|--|--|
|![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/value%20iteration/addtinitial.PNG)  |![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/value%20iteration/adtfinal.PNG)  |


**By Sandra Kumi/20185122**


