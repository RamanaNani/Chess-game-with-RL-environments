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

## Methodology
We trained one agent with DQN and other agent with MCTS and made them to play aganist each other.
### MCTS Agent
This agent uses the Monte Carlo Tree Search to determine its moves. By analysing the MCTS tree, it identifies the most advantageous move based on the child node with the highest win rate or the most visits, depending on the selection strategy employed. This method ensures that the decisions are backed by a thorough eval- uation of potential outcomes, reflecting the most strategic and promising actions as determined by the MCTS.
### DQN Agent
Contrasting with the MCTS-based approach, the DQN-based agent selects moves based on a policy derived from a Deep Q-Network. This network evaluates the po- tential reward of each legal move from the current game state, guiding the agent to choose actions that maximize expected returns based on learned value functions. While the MCTS agent relies on exploration and simulation, the DQN agent op- erates on learned experiences, potentially offering more consistent performance against varying strategies. We trained DQN agent for 500 episodes and then first evaluated its performance aganist random agent.

## Observation
The MCTS algorithm is performing better when compared to DQN algorithm. This because the DQN algorithm only considers the best move based on the cur- rent state where as the MCTS algorithm can simulate the future possible steps which is useful to make long-term strategic decisions. MCTS is mainly suitable for environments like chess with high branching factor and complex decision trees whereas DQN doesnot perform well and able to generalize better in these types of environments unless it is extensively trained. The DQN requires large number of samples in these types of environments because every game may evolve differently but MCTS simulates the future states and takes best move which does not require any training data. The DQN algorithm may overfit the training data and struggles in the case of novel moves whereas MCTS adapts to every novel move and does not overfit.
