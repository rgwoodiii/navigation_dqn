# navigation_dqn
As part of the Deep reinforcement learning nano degree with Udacity, this is an implementation of the DQN algorithm to train an agent how to optimally maximize yellow banana collection.

## environment details
For any reinforcement learning implementation, the agent has to interact with their environment. In this case, the environment is represented as a large square floor with blue and yellow bananas scattered throughout. 

### rewards
Per the agent's action, the agent is rewarded according to banana collection; -1 for a blue banana collected and +1 for a yellow banana collected.

### action space
Within the environment, there is a discrete action space of 4. At any point in time, the agent is able 1. move forward, 2. move right, 3. move backwards, or 4. move left.

### task success
In order to successfully complete our episodic task, the agent is required to obtain an average score of at least 13 bananas over 100 episodes.




