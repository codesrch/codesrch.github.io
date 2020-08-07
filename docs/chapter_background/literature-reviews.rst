=====================
Literature Survey
=====================

MEASURING THE RELIABILITY OF REINFORCEMENT LEARNING ALGORITHMS (ICLR-2020)
------------------------------------------------------------------------------------------------------------
This paper :cite:`rl_reliability_metrics` designed a set of matrics and statistics for evaluating the reliability of the reinforcement learning algorithms. It focuses on variability and risk, both during training and after learning (on a fixed policy). These metrics can be considered general-purpose and backed up by complementary statistical tests to enable rigorous comparisons on these metrics. In this paper, we first describe the desired properties of the metrics and their design, the aspects of reliability that they measure, and their applicability to different scenarios. We then describe the statistical tests and make additional practical recommendations for reporting results. The metrics and accompanying statistical tools is open-sourced at https://github.com/google-research/rl-reliability-metrics.

MEASURING THE RELIABILITY OF REINFORCEMENT LEARNING ALGORITHMS (ICML-2020)
------------------------------------------------------------------------------------------------------------
"A fundamental trait of intelligence is the ability to achieve goals in the face of novel circumstances, such as making decisions from new action choices. However, standard reinforcement learning assumes a fixed set of actions and requires expensive retraining when given a new action set. To make learning agents more adaptable, we introduce the problem of zero-shot generalization to new actions. We propose a two-stage framework where the agent first infers action representations from action information acquired separately from the task. A policy flexible to varying action sets is then trained with generalization objectives. We benchmark generalization on sequential tasks, such as selecting from an unseen tool-set to solve physical reasoning puzzles and stacking towers with novel 3D shapes. Videos and code are available at https://sites.google.com/view/action-generalization."

CURL: Contrastive Unsupervised Representations for Reinforcement Learning (ICML 2020)
----------------------------------------------------------------------------------------
This paper :cite:`srinivas2020curl` shows how image-based features can be used to train RL agents efficiently. CURL first extract high-level features from raw pixels using contrastive learning and then performs off-policy control. CURL outperforms prior pixel-based methods on complex tasks in the DeepMind Control Suite and Atari Games showing performance gains. 

A Distributional View on Multi-Objective Policy Optimization [ICML 2020] [MORL, RL]
----------------------------------------------------------------------------------------
This paper :cite:`abdolmaleki2020distributional` provides a distributional view of Multi-objective reinforcement learning (MORL) that enables the scale-invariant encoding of preferences. 
Their theoretical grounding comes from considering RL as an inference perspective of MORL. In experiments, they show their model outperform scalarized approach on multi-objective tasks.

Revisiting Fundamentals of Experience Replay [ICML 2020]
----------------------------------------------------------------------------------------
This paper :cite:`fedus2020revisiting` finds: Larger size experience replay substantially increase the performance
of certain algorithms and leaving others unaffected, n-step returns are uniquely beneficial while other techniques confer
limited benefit for sifting through larger memory.

HIGH-DIMENSIONAL CONTINUOUS CONTROL USING GENERALIZED ADVANTAGE ESTIMATION [ICLR 2016]
----------------------------------------------------------------------------------------
This paper :cite:`Schulman2016HighDimensionalCC` address sample efficiency using value functions to reduce the variance of policy gradient estimates at the cost of some bias, using an exponential-weighted estimator of the advantage function that is analogous to TD(\lambda). 
They usse trust region optimization proceduce to make the policy stable and make sure stable improvement despite nonstationarity of the incoming data.



----------------------------------------------------------------------------------------




----------------------------------------------------------------------------------------



----------------------------------------------------------------------------------------


==================
Evolution
==================

Evolutionary Reinforcement Learning for Sample-Efficient Multiagent Coordination (ICML 2020)
----------------------------------------------------------------------------------------------
"We introduce Multiagent Evolutionary Reinforcement Learning (MERL), a split-level training platform that handles the two
objectives separately through two optimization processes. An evolutionary algorithm maximizes
the sparse team-based objective through neuroevolution on a population of teams. Concurrently, a gradient-based optimizer trains policies to only maximize the dense agent-specific rewards. The gradient-based policies are periodically added to the evolutionary population as a way of information transfer between the two optimization processes. This enables the evolutionary algorithm to use skills learned via the agent-specific rewards toward optimizing the global objective. Results demonstrate that MERL significantly outperforms state-of-the-art methods, such as MADDPG, on a number of difficult coordination benchmarks."