# MDP REPRESENTATION

## AIM:

To represent a Markov Decision Process(MDP) problem in the following ways.

  1. Text representation
  2. Graphical representation
  3. Python - Dictonary representation

## PROBLEM STATEMENT:


### Problem Description

We need to train a fish to navigate through a maze to reach a target location using reinforcement learning.

### State Space

1. Fish Current Position
2. Distance to target location
3. Obstacles
4. Energy level of fish

### Sample State

Fish Position (3, 5), distance to target 1 to units nearby obstacles.

### Action Space

1. Move Left
2. Move Right
3. Move Up
4. Move Down

### Sample Action

Move Up

### Reward Function

1. Positive reward for getting closer
2. Negative rewards for collide with obstacles

### Graphical Representation()
![RL](https://github.com/ragul-2004/mdp-representation/assets/94367917/43e15dd7-0847-425e-a9cd-a8d0b505097b)



## PYTHON REPRESENTATION:
### NAME : RAGUL A C
### REG NO : 212221240042
```python
P = {
    0:{
        0: [(1.0,0,0.0,True)],
        1: [(1.0,0,0.0,True)],
        2: [(1.0,0,0.0),True]
    },
    1:{
        0: [(1.0,0,0.0,True)],
        1: [(1.0,1,0.0,True)],
        2: [(1.0,2,1.0,True)]
    },
    2:{
        0: [(1.0,1,0.0,True)],
        1: [(1.0,1,0.0,True)],
        2: [(1.0,1,0.0,True)]
        
    }
    3:{
        0:[(1.0,2.0,0.0,True)],
        1:[(1.0,2,0.0,True)],
        2:[(1.0,2.0,0.0,True)]
    }
}
```
## OUTPUT:
```python
{0: {0: [(1.0, 0, 0.0, True)], 1: [(1.0, 0, 0.0, True)], 
    2: [(1.0, 0, 0.0, True)]} 
    
 1: {0: [(1.0, 0, 0.0, True)], 1: [(1.0, 1, 1.0, True)], 
    2: [(1.0, 2, 0.0, True)]},
 2: {0: [(1.0, 2, 0.0, True)], 1: [(1.0, 2, 0.0, True)], 
    2: [(1.0, 2, 0.0, True)]},
 3: {0: [(1.0, 1. 0.0, True)], 1: [(1.0, 1, 0.0, True)], 
    2: [(1.0, 1, 0.0, True)]}
 }
```
## RESULT:

Thus the given Markov Decision Process(MDP) problem is represented in the following ways.

  1. Text representation
  2. Graphical representation
  3. Python - Dictonary representation
