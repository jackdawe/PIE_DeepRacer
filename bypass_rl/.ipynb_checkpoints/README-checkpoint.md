# Bypass the Reinforcement Learning

This notebook implement the idea of Yves P.
The goal is to compute the optimal trajectory outisde of AWS, and totally bypass the RL algorithm, by forcing the model to follow the trajectory.

There are several steps in this idea: 
 - Compute the best possible trajectory 
 - Compute an action space from this trajectory
 - Compute the optimal trajectory, using this action space
 - Build the reward function using this trajectory

Note: there is one main incertitude in this algorithm. We are not sure that the model is really able to follow our trajectory in the physical model of AWS.
This should be tested and we should adjust a physical parameter (typically the highest acceleration, or highest braking) to ensure the trajectory is feasible.