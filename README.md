# Vaccine-Development-with-Dynamic-Programming

## Introduction
Vaccine development is a complex and high-risk process that involves multiple stages, from early research to clinical trials. Each stage requires careful decision-making regarding investments, as the success or failure of the project depends on the allocation of resources and the ability to navigate uncertainties. As the CEO of a biotech company, your goal is to evaluate the financial viability of a new vaccine development project while optimizing resource allocation to maximize the expected return.

This project applies dynamic programming to simulate the decision-making process in vaccine development. Using a probabilistic model of state transitions and the associated costs, we compute the value function for each stage of the project. This approach provides a clear roadmap for making optimal investment decisions at each phase of the vaccine development lifecycle.

## Problem Overview
The project is modeled as a Markov Decision Process (MDP) with:
States: Representing different stages of the vaccine development process:

Phase 0 (state 0): Initial state.
Phase 1 with promising results (state 1).
Phase 1 with disappointing results (state 2).
Success (state 3): End state with a $10M reward for selling the patent.
Failure (state 4): Absorbing state.

### Actions:

Invest $100,000 in a state to increase the probability of transitioning to a more favorable state.
Do not invest and proceed with default probabilities.
Transitions: Probabilities dictate the movement from one state to another (e.g., from state 0 to state 1 or 2).

### Rewards and Costs:

A reward of $10M is obtained upon reaching the success state (state 3).
A cost of $100,000 is incurred for additional investments in any state.
Failure (state 4) results in no further rewards.
Discount Factor: The discount factor (0.996) accounts for the time value of money, ensuring future rewards are appropriately weighted.

## Methodologies
Dynamic Programming Approach:

The problem is solved using value iteration or policy iteration, which are standard techniques for solving MDPs.
The value iteration algorithm iteratively computes the value function for each state by considering the expected return from all possible actions, adjusted by the discount factor.

Transition Matrix:
A transition matrix is used to define the probabilities of moving between states for each action.
The probabilities vary based on whether an additional investment is made in the current state.

Value Function Calculation:
The value function, V(s), represents the maximum expected return from state s, accounting for the rewards and the cost of actions.

Optimal Policy Determination:
The optimal policy specifies whether to invest in each state to maximize the total expected return.

## Objective
The objective of this project is to compute the value function vector for all states, which provides:

The financial value of the vaccine development project.
A clear strategy for deciding whether to invest in each state.
By simulating the vaccine development process, the project equips decision-makers with insights into managing risks, optimizing resource allocation, and maximizing expected returns in high-stakes biotech projects.
