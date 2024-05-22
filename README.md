<center><h1>Improving Chess Strategies with Deep RL Methods</h1></center>

It is a dual agent game

## Problem Statement
The main aim of the project is to create a smart system that learns to play chess on its own using reinforcement learning methods

## Environment
PettingZoo is a multi-agent reinforcement learning platform that offers various environments for conducting complex interaction studies between agents. One such environment is the chess game provided within PettingZoo’s classic collection. This setup allows for the exploration of complex agent interactions within a structured and strategic game setting, making it an ideal testbed for developing and testing advanced reinforcement learning (RL) algorithms.
* Action space: The environment provides a discrete action space with 4672 possible actions
* Observation Space: The observation shape is defined as (8, 8, 111), which likely represents a structured format for the chess board where each piece and possible move is encoded within this multidimensional array.
* Agents: There are 2 agents Player_0, Player_1
* Rewards: +1 if agent wins, -1 if the agent looses and 0 if the game is draw
