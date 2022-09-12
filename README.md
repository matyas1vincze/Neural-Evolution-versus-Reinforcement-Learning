# Neural-Evolution-versus-Reinforcement-Learning
ROLE:

University project for the course "Bio-Inspired AI" taught by Giuseppe Riccardi. It was a team project with the goal to compare different evolutionary algorithms performance in a continuous action enironment.

PROBLEM:

Biologically motivated algorithms can be very different compared to standard machine learning models as they do not typically use gradients to solve the given optimization problem. OpenAI's BipedalWalker-v3 environment offers a difficult challange as the action space is continuous, which makes it suitable to compare the different algorithms performance at this task.

SOLUTION:

We implemented 3 different evolutionary algorithms:
- Genetic algorithm: turning the weights and biases of a fixed structured neural network into a genotype, we can use a population, generations, mutation, crossover, and selection to optimize the networks performance in the environment similar to how natural selection works in the real world | https://link.springer.com/article/10.1007/s11042-020-10139-6
- Covariance Matrix Adaptation Evolution Strategy (CMA-ES): similar to genetic algorithms, but we have multiple and correlated mutation rates - using these thoughout the training we can learn a rotated and shifted covariance matrix adjusted to the fitness landscape | https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.30.2961&rep=rep1&type=pdf
- NeuroEvolution of Augmenting Topologies (NEAT): here we optimize not only the weights of the neural net, but its structure at the same time - starting from a minimal topology, we use similar tactics as in genetic algorithms combined with historical markings (method to apply crossover to neural networks with different topologies) and speciation (not comparing easily optimizable simple topologies with more complex ones) | https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.638.3910&rep=rep1&type=pdf

and one reinforcement learning solution which acted as a baseline for the comparisom:
- Twin-delayed Deep Deterministic Policy Gradients (TD3): builds upon the Deep Deterministic Policy Grandient (DDPG) model, which is a model-free, off-policy, actor-critic reinforcement algorithm suitable for continuous action space environments - TD3 improves DDPG by utilizing double Q-learning, delayed policy updates and target policy smoothing to tackle the commonly occuring Q-value overestimation problem of DDPG resulting in more stable training and less dependence on exact hyperparameter values | https://arxiv.org/abs/1802.09477

IMPACT:

The project was successful as we were able to make a fair comparisom between the different implemented methods and received the best possible grade.
