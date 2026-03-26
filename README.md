# Reinforcement Learning Learning Journey

## 1. Motivation

I started learning reinforcement learning out of curiosity about AI, especially large language models (LLMs). 

After studying basic deep learning models such as MLP, CNN, RNN, and Transformer, I realized that although deep learning is powerful at modeling nonlinear mappings between variables, it does not inherently provide a paradigm for optimal decision-making.

In particular, I began to think about the next-token prediction process: a token can be viewed as an action rather than just a prediction. Deep learning provides a way to generate outputs, but not a principled framework for making sequential decisions.

To understand what kind of algorithms can produce such decision-making capabilities, I turned to reinforcement learning.

---

## 2. What I implemented

- Dynamic Programming (DP)
- Monte Carlo (MC)
- Q-learning (Blackjack)
- SARSA
- DQN (CartPole)
- TRPO
- PPO

---

## 3. Key Insights

Reinforcement learning has evolved from early Markov Decision Process (MDP) formulations to modern algorithms such as PPO, but the core abstractions — state (s), action (a), reward (r), value (V), action-value (Q), advantage (A), and policy (π) — have remained largely unchanged.

What has changed significantly is how data is used and how policies are represented and optimized.

Early methods such as DP, MC, Q-learning, and SARSA rely on tabular updates and are limited to discrete and small state-action spaces.  
DQN introduced neural networks to approximate value functions, enabling generalization, but still suffered from instability due to bootstrapping and required techniques like experience replay.

Policy gradient methods, proposed earlier, directly optimize the policy, but only became practically effective with the introduction of trust-region methods (e.g., TRPO, later PPO), which improved training stability and allowed deep neural networks to reliably represent policies.

From my perspective, the most important takeaways are:
- Understanding the structure of the state-action space  
- Designing appropriate objective functions  
- Ensuring stable optimization during training  

---

## 4. Problems & Failures

- Unstable training (high variance in rewards)
- Overestimation bias (max bias in Q-learning/DQN)
- Limited understanding of the role and effect of replay buffer

---

## 5. Future Work

Apply PPO to solve a real-world control problem, especially in practical decision-making or control scenarios.
