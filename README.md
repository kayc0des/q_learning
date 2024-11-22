# Q-Learning for FrozenLake Environment

This project demonstrates how to implement the Q-learning algorithm to train an agent in the FrozenLake-v1 environment using Python and the OpenAI Gym library.

## Overview

The FrozenLake environment is a reinforcement learning problem where an agent navigates a grid world to reach a goal. The grid contains safe tiles, holes (danger), and a goal tile. The agent must learn an optimal policy to maximize its cumulative reward while avoiding the holes.

## Requirements

To run this implementation, you need the following libraries:

- Python 3.10+
- gym (Version 0.25.2)
- numpy (Version 1.26.4)

## Files and Code Structure

- Main Code: Implements Q-learning for training an agent in the FrozenLake environment.
- Q-Table: Stores the Q-values for all state-action pairs, updated during training.
- Reward Metrics: Tracks and calculates average rewards every 1,000 episodes.

## Training Algorithm: Q-Learning

Q-learning is an off-policy reinforcement learning algorithm that uses a Q-table to estimate the quality of actions taken from each state.

### Key Parameters

- Learning Rate (α): Determines the step size for Q-value updates.
- Discount Factor (γ): Balances immediate rewards with future rewards.
- Exploration Rate (ε): Guides the trade-off between exploration and exploitation.

### Train Flow
1. Initialize:
    - Q-table with zeros.
    - Parameters: learning rate, discount factor, exploration rate.

2. Episode Loop:
    - Start from a random state.
    - Select an action based on exploration-exploitation trade-off.
    - Observe the reward and next state.
    - Update the Q-value for the state-action pair.
    - Repeat until the episode ends or the maximum steps are reached.

3. Decay Exploration RateInitialize:
    - Gradually reduce exploration rate to favor exploitation in later episodes.

## Results

- Q-Table: The Q-table represents the learned policy. Each value corresponds to the expected reward for taking a specific action in a given state.

- Performance: Average reward per 1,000 episodes
