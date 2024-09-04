# MDP REPRESENTATION
## Developed BY : Ragul A C
## Register Number : 212221240042

## AIM:
The aim of this experiment is to create a Markov Decision Process (MDP) representation and implement it in Python to model the decision-making process in a medical treatment scenario.


## PROBLEM STATEMENT:

### Problem Description
The problem involves managing the treatment of patients who can be in one of three states: healthy, mildly sick, or seriously sick. 
The objective is to determine whether to administer treatment or not for a mildly sick patient, considering the potential outcomes and rewards associated with each action.

### State Space
State 0: Healthy
State 1: Mildly Sick
State 2: Seriously Sick
{Healthy, Mildly Sick, Seriously Sick} -> {0, 1, 2}

### Sample State
# State: Healthy
# Healthy -> 0
# (The patient is Healthy, represented numerically as 0.)

### Action Space
Action 0: Treat
Action 1: Not Treat
{Treat, Not Treat} -> {0, 1}

### Sample Action
Action: Treat
Treat -> 0
(The action taken is to Treat the patient, represented numerically as 0.)

### Reward Function
 R = { +1 , if the patient state is changed to a healthy state, otherwise -1}

 Transition to healthy state: +1
 Staying sick: -1
 Terminal states: No reward

### Graphical Representation
![WhatsApp Image 2024-09-04 at 08 54 10_56eef3a3](https://github.com/user-attachments/assets/9ffcf007-a465-447c-ac94-1e4a1a5df8e7)


## PYTHON REPRESENTATION:
```python
import random

# MDP Representation in Python
# States: 0 = Healthy, 1 = Mildly Sick, 2 = Seriously Sick
# Actions: 0 = Treat, 1 = Not Treat

P = {
    0: {  # Healthy
        0: [(1.0, 0, 0, True)],  
        1: [(1.0, 0, 0, True)]   
    },
    1: {  # Mildly Sick
        0: [(0.7, 0, 1, False),  
            (0.2, 1, -1, False),  
            (0.1, 2, -1, False)], 
        1: [(0.0, 0, -1, True),   
            (0.8, 1, -1, False),  
            (0.2, 2, -1, False)] 
    },
    2: {  # Seriously Sick
        0: [(0.3, 1, -1, False), 
            (0.7, 2, -1, False)], 
        1: [(0.0, 0, -1, True), 
            (0.0, 1, -1, True),
            (1.0, 2, -1, False)] 
    }
}
P
~~~

## OUTPUT:
![Screenshot 2024-09-04 084324](https://github.com/user-attachments/assets/6424ff4e-0537-42a5-97ec-8355ebac1fbc)




## RESULT:
The Markov Decision Process (MDP) has been successfully represented using Python dictionaries. Each state-action pair contains information about possible transitions, transition probabilities, associated rewards, and whether the next state is terminal or not. This representation can be used for further analysis and decision-making algorithms such as reinforcement learning.






