# FireDronesRL

FireDrones is a multi-agent reinforcement learning (MARL) project where multiple agents (drones) are trained to manage wildfire in a 2D grid forest. Drones compete and collaborate to extinguish the fire quickly.

I hope this project can be used as an example MARL project for beginners in MARL or RLlib.

## Problem Description

**Environment Initialization and Updates**: 10 by 10 grid. On each cell, a tree grows with probability X, and fire ignites on K trees. At each time stamp, fire spreads to a neighboring (8 surrounding cells) with probability Y.

^ might have to simplify problem; fixed ignition point maybe

**State**:

**Action**: At time $t$, a drone can move one cell in one of the eight directions (N, NE, E,...), or spray water (=extinguish fire) if the fire cell is one of its neighboring cells. Drone can enter fire cells (flies over fire).

**Reward**:
+: extinguished fire
-: time, number of trees on fire
-> might wait to have enough trees to be set on fire. remove +?
-> How to reward individual robot's activity?
->

**Assumptions**: $s_t$ (state at time $t$) is fully known

## Requirements

This project uses the following libraries:

-   RLlib (add hyperlink)
-   Gymnasium (add hyperlink)

## Installation

## How to Run

(insert instruction)

**Expected training time**?

### Files

`environment.py`: Defines the wildfire model environment

## Results

## Extending the Project

Here are some additional considerations that can be incoorporated to create more realistic dynamics:

-   Total amount of water each drone can spray is less than or equal to its water capacity
-   Drones must replenish its battery and water
-   Ensure safety distance between fire and drones
-   Add environmental factors (e.g. wind affects fire spread direction)
-   Extendable map with custom grid size
-   etc.

## Useful Tutorials

https://github.com/sven1977/rllib_tutorials/blob/main/ray_summit_2021/tutorial_notebook.ipynb
