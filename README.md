## Reinforcement Q-Learning from Scratch in Python with OpenAI Gym
*Teach a Taxi to pick up and drop off passengers at the right locations with Reinforcement Learning*
ref: https://www.learndatasci.com/tutorials/reinforcement-q-learning-scratch-python-openai-gym/<br>
Most of you have probably heard of AI learning to play computer games on their own, a very popular example being Deepmind. Deepmind hit the news when their AlphaGo program defeated the South Korean Go world champion in 2016. There had been many successful attempts in the past to develop agents with the intent of playing Atari games like Breakout, Pong, and Space Invaders.

Each of these programs follow a paradigm of Machine Learning known as Reinforcement Learning. If you've never been exposed to reinforcement learning before, the following is a very straightforward analogy for how it works.

# Install Liberaries:
* !pip install cmake gym[atari] scipy

# Functions:
* # Q RL training:<br>
    Q_RL_trainig(hyperparameters, env, num_episodes = 100000)<br>
    it takes the hyperparameters as tuple and the environment with num_episodes = 100000 as the default value.
    Returns the q_tabel and  (total_epochs+total_penalties)/num_episodes as a metric
    
* # Q RL Evaluation:<br>
    Q_RL_evaluation(q_table,env,episodes = 100)<br>
    It takes the learned q_table and the environment with episodes = 100 as the default value.<br>
    Then it prints the Average timesteps per episode and the Average penalties per episode.<br>

* # Tune alpha, gamma, and/or epsilon using a decay over episodes:<br>
    tune_alph_gamma_epsilon(alpha_tune, gamma_tune, epsilon_tune ,num_of_iterations = 100000)<br>
    It takes the alpha_tune, gamma_tune, epsilon_tune their values should determine how fast the exponential decay should be.<br>
    with num_of_iterations = 100000 as the default value.<br>
    Then returns alpha_values, gamma_values and epsilon_values as arrayes of the decaied values of length = num_of_iterations<br>
    also it displayes a plot to show the tune output.<br>
    for example: <br>
    ![image](https://user-images.githubusercontent.com/34524576/172079717-dad511a0-d5e7-49ee-8438-27adba942643.png)
 
* # Train with the exponential decay:<br>
    Q_RL_train_exponential_decay(hyperparameters, env, num_episodes = 100000)<br>
    it takes the hyperparameters as a matrix and the environment with num_episodes = 100000 as the default value.<br>
    Returns the q_tabel and  (total_epochs+total_penalties)/num_episodes as a metric<br>
    
# *I tried to find the best hyperparemeter values using the genetic algorithms instead of grid search.*<br>
ref: https://towardsdatascience.com/genetic-algorithm-to-optimize-machine-learning-hyperparameters-72bd6e2596fc

genetic algorithms is more efficient when dealing with many hyperparemetrs compared with grid search.
