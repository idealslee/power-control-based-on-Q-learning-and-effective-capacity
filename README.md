# power-control-based-on-Q-learning-and-effective-capacity

This is a project based on effective capacity model and reinforcement learning.
The goal is to maximize effective capacity.
There are three main parts.

# QlearningAgent

Used to carry out the learning processes and built Q tables，And make action selections and status and Q table updates
    def act
    
# environment

Establish a channel environment and make value judgments for each step of decision, based on effective capacity

# main

The main program includes several functions for calculating path loss(def cost231), inter-user interference power(def compute_interference_power), signal to interference and noise ratio(def average_SINR_dB & def compute_SINR_due_to_neighbor_loss), effective capacity(def compute_effective_capacity & def compute_EC_due_to_neighbor_loss_SINR), gain from decision making(def get_A_contrib), iterative process of training(def run_agent), and drawing images(def plot_pc_actions & def plot_rewards).

Particularly，line 410 - line 460 judges the state action value through the effective bandwidth theory. If the effective bandwidth increases, the value is positive, otherwise it is negative.
