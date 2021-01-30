# Project 1: Navigation

## 1.	Project goal
Train agent to collect yellow bananas while avoid blue bananas using unity engine
## 2.	Environment
This is large, square environment. <br /> 
The state space: 
37 dimensions (agent velocity, ray-based perception,…) <br /> 
The action space: <br /> 
0 - Move forward <br /> 
1 - Move back ward <br /> 
2 - Turn left <br /> 
3 - Turn right <br /> 
This is episodic task and the goal is to get more than or equal +13 point for 100 consecutive episodes.
## 3.	Agent

The agent is implemented base on DQN algorithm. DQN is a Q learning that use TD for estimate value function and use neutral network as function approximator.<br /> 


Q learning big picture. There are 2 steps: Sample and Learn<br /> 
0) Initialization<br /> 
Initialize replay buffer<br /> 
Initialize parameter for neutral network<br /> 
1)Sample (Interact with environment)<br /> 
Choose action A using greedy policy.<br /> 
Take action and get next state, reward<br /> 
Store (state, reward, action, next state) into replay buffer<br /> 
2)Learn:<br /> 
Collect mini batch from Replay Buffer<br /> 
Use neutral network to calculate the target value<br /> 
y_target = reward + gamma*max(Q(next_state,_)) – Q(state,action)<br /> 
calculate delta w<br /> 
update w<br /> 


