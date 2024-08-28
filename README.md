# MDP REPRESENTATION
## Developed BY : Ragul A C
## Register Number : 212221240042

## AIM:
The aim of this experiment is to create a Markov Decision Process (MDP) representation and implement it in Python to model the decision-making process in a medical treatment scenario.
## PROBLEM STATEMENT:

### Problem Description
The problem involves managing the treatment of patients who can be in one of three states: healthy, mildly sick, or seriously sick. The objective is to determine whether to administer treatment or not for a mildly sick patient, considering the potential outcomes and rewards associated with each action.

### State Space
State 0: Healthy
State 1: Mildly Sick
State 2: Seriously Sick

{Healthy, Mildly Sick, Seriously Sick} -> {0, 1, 2}


### Sample State
State: Healthy
Healthy -> 0
(The patient is Healthy, represented numerically as 0.)
### Action Space
Action 0: Treat
Action 1: Not Treat

{Treat, Not Treat} -> {0, 1}



### Sample Action
Action: Treat
Treat -> 0
(The action taken is to Treat patient, represented numerically as 0.)

### Reward Function
R = { +1 , if the patient state is changed to healthy state or not, otherwise -1}

Transition to healthy state: +1
Staying sick: -1
Terminal states: No reward
### Graphical Representation
![graph1](https://github.com/user-attachments/assets/cc0d8c34-1c67-4848-b94f-91eda11c14f4)


## PYTHON REPRESENTATION:
```python
import gym
import gym_walk
#P = gym.make('BanditWalk-v0').env.P
# Creating Dictionary
# MDP Representation in Python
P = {
    0: {
        0: [(0.0, 0, 0, True), (0.0, 1, 0, True), (0.0, 2, 0, True)],
        1: [(0.0, 0, 0, True), (0.0, 1, 0, True), (0.0, 2, 0, True)]
    },
    1: {
        0: [(0.9, 0, 1, False), (0.0, 1, -1, True), (0.1, 2, -1, False)],
        1: [(0.0, 0, -1, True), (0.0, 1, -1, True), (0.0, 2, -1, True)]
    },
    2: {
        0: [(0.0, 0, -1, True), (0.0, 1, -1, True), (0.0, 2, -1, True)],
        1: [(0.0, 0, -1, True), (0.0, 1, -1, True), (0.0, 2, -1, True)]
    }
}



P

```

## OUTPUT:
![newout](https://github.com/user-attachments/assets/00d2ef54-7384-48f4-b271-d41d3c2202d8)


## RESULT:
The Markov Decision Process (MDP) has been successfully represented using Python dictionaries. Each state-action pair contains information about possible transitions, transition probabilities, associated rewards, and whether the next state is terminal or not. This representation can be used for further analysis and decision-making algorithms such as reinforcement learning.






