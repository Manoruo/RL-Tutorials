
# Reinforcement Learning Terminology 

## Model types

1. Model based: Agent relies on simulation to make predictions about the current state of the world and follows a pre-defined policy based on that.

2. Model free: Agent interacts with environment on its own and learns an optimal policy through trial and error + feedback. 

### Approaches to RL
1. Policy based: Policy is learned directly where each state is mapped to the best corresponding action.

2. Deterministic policy based: Policy that maps state to one action

3. Stochastic Policy based: Policy that outputs a probability distrubtion over actions given a state.

Notes: Policy is usually trained with neural network to select what action to take given a state. Depending on experience recieved neural network will re-adjust.

2. Value based: A value function is trained that maps each state to the expected value of being at that state. Outputs how good a state / state-action pair is.

Notes: The output of value function doesnt define what actions the agent should take. We have to specify the strategy to take the action (i.e. Greedy Stategy or Epsilon-Greedy Strategy) 

#### More on Value based

1. State-value function: This returns how good being in that state is. The value is determined by starting at that state and following the policy until the end.

2. Action-Value function: This calculates how good an action is at a given state. This is determined by starting at a given state taking the action and following the policy till the end.

Notes: For value based methods, we always have to define the policy/strategy expliclity (Greedy Strategy, Epsilon-Greedy Strategy, etc.)

### Types of policy algorithms 

1. Online-learning: The same policy is used at training time and inference time.

2. Offline-learning: A different policy is used at training time and inference time.

### Learning Stratagies
1. Monte Carlo (MC): Learning happens at the end of the episode. Update value function / policy function at end of episode

2. Temporal Difference (TD): Learning happens at each step. We update value function (or policy function) at each step.

Notes: You may see SARS (State_t, Action_t, Reward_t+1, State_t+1)


## Q Learning 

1. Q Learning: The algorithm we use to train our Q-function (an action-value or value function)

2. Q Function: The value function that tells us how good a state-action pair is.

3. Q-table: The actual mechanism used by the Q Function to "look up" the value for a state action pair. This is the "memory"

4. Having an optimal policy in QLearning amounts to having an optimal q-function

Notes: Q Learning takes a TD approach to train its value function + is an off-policy based method. The Q means Quality. 

