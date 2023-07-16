# Stock Trading Bot

The Stock Trading Bot is an implementation of a stock trading agent using reinforcement learning with Deep Q-Learning. 


## Code Explanation

- **Imports**: The necessary libraries and modules are imported, including numpy (np), pandas (pd), TensorFlow (tf), datetime, itertools, argparse, re, os, pickle, and matplotlib.pyplot.

- **Data Loading**: The get_data() function reads stock price history data from a CSV file and returns it as a numpy array.

- **MultiStockEnvironment**: This class represents the environment in which the agent operates. It initializes the environment with stock price history data and provides methods for resetting the environment, taking a step, and getting the current observation/state.

- **ReplayBuffer**: This class represents the replay buffer used for storing and sampling transitions for reinforcement learning. It initializes the replay buffer with a specified maximum size and provides methods for storing transitions and sampling a batch of transitions.

- **Action Neural Network**: The action_NN() function creates a neural network model for action selection. It takes the input dimension, number of possible actions, and other parameters as inputs and returns a compiled Keras model.

- **DQNAgent**: This class represents the Deep Q-Network (DQN) agent for reinforcement learning. It initializes the agent with the state and action sizes, replay buffer, discount factor, exploration rate, and neural network model. It provides methods for updating the replay buffer, selecting actions, performing replay to update the Q-network, and saving/loading the model weights.

- **Utility Functions**: The code includes several utility functions such as make_dir() for creating directories, plot_rewards() for visualizing rewards, and get_scaler() for generating a scaler for normalizing state values.

- **Training and Testing**: The code includes two blocks for training and testing the stock trading bot. The training block performs a specified number of episodes and updates the agent's Q-network using the DQN algorithm. The testing block uses a pre-trained agent and evaluates its performance on the test dataset.

- **Saving Models and Rewards**: The code saves the trained agent model and the portfolio values achieved during training and testing.

## Requirements

- Python 3+
- Tensorflow
- Numpy
- Pandas
- Scikit-learn
- Matplotlib

## Installation

1. Clone the repository:

   ```shell
   git clone https://github.com/christianadebambo/stock-trader-bot-RL.git
   ```
   
## Usage

The solution can be reproduced by running the Jupyter notebook
