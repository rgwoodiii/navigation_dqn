# Report

## implementation

### environment details
For any reinforcement learning implementation, the agent has to interact with their environment. In this case, the environment is represented as a large square floor with blue and yellow bananas scattered throughout. 

### rewards
Per the agent's action, the agent is rewarded according to banana collection; -1 for a blue banana collected and +1 for a yellow banana collected.

### action space
Within the environment, there is a discrete action space of 4. At any point in time, the agent is able 1. move forward, 2. move right, 3. move backwards, or 4. move left.

## algorithm
To train this agent, I utilized the DQN algorithm. The agent will perform an action on the current state according to epsilon-greedy valies. The algorithm performs episodic training until the pre-specified number of episodes has been satisfied or  the agent has solved the environment. (The environment is solved when the average reward over 100 episodes reaches at least 13.) This algorithm utilizes a replay buffer.

Episodes run until the maximum time steps parameter (max_t) has been reached.

### hyper-parameters

- n_episodes: maximum number of training episodes (1000)
- max_t: maximum number of timesteps per episode  (500)
- eps_start: starting value of epsilon, for epsilon-greedy action selection (0.5)
- eps_end: minimum value of epsilon  (0.01)
- eps_decay: multiplicative factor (per episode) for decreasing epsilon (.97)

I tuned the above parameters manually and randomly. It didn't take too long before I was successfully solving the environment in about 300 episodes. I was super excited in my last run to solve it in 108 episodes.

### dqn agent & model
credit to Udacity for model.py & dqn_agent.py. As part of the Deep Q Learning section in the course, we are led through a coding exercise where these files are supplied in order to train your dqn agent. As I have adapted the Deep Q Learning implementation for that coding exercise, some of the boiler plate code as given by udacity has been used here. 

## plot & performance
![image](https://user-images.githubusercontent.com/13371867/123744365-e5985c80-d86b-11eb-9c00-0676df93dc08.png)
- Episode 100	Average Score: 12.19
- Episode 108	Average Score: 13.02
- Environment solved in 108 episodes!	Average Score: 13.02

## improvements

- My hyper-parameter was largely a manual implementation of random search. Random can be ok, if somewhat controlled in a systematic fashion. I would have preferred to implement grid search or random search to determine hyper parameters in the end.

- To mitigate action value over-estimation; I would like to implement Double Q-Learning.

- Rather than uniform sampling from experience, I could use prioritized experience replay to increase the frequency of higher importance experience. 



