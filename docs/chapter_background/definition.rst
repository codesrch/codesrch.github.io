======================
Definition
======================

Categorical Distribution
	Used for discrete action of reinforcement learning.
	"In probability theory and statistics, a categorical distribution 
	(also called a generalized Bernoulli distribution, multinoulli distribution) 
	is a discrete probability distribution that describes the possible results of a 
	random variable that can take on one of K possible categories, with the probability 
	of each category separately specified. The K-dimensional categorical distribution is 
	the most general distribution over a K-way event; any other discrete distribution over 
	a size-K sample space is a special case. The parameters specifying the probabilities of 
	each possible outcome are constrained only by the fact that each must be in the range 0 
	to 1, and all must sum to 1." [wikipedia]

Markov Chain

Markov Decision Process

Partially Observed Markov Decision Process
 
Some Points about RL:
======================
- RL task is defined in terms of reward function.

Goal of reinforcement learning:
--------------------------------
:math:`p_{\theta}(s_1, a_1, .., s_T, a_T)=p_{\theta}(\tau)= p(s_1)\prod_{t=1}^T\pi_{\theta}(a_t|s_t)p(s_{t+1}|s_t, a_t)`.

The states and actions are randomly distributed, so we have to take expectation of this reward under their distribution under the trajectory, :math:`p_{\theta}(\tau)`, induced by the initial state and the transition dynamics of the MDP and the current policy :math:`\pi_\theta`. 

:math:`\theta^* = {argmax}_{\theta} 
E_{\tau \sim p_{\theta}(\tau)}[\sum_t r(s_t, a_t)]`  

State-action marginal
	:math:`p_\theta(s_t, a_t)` at time :math:`t`.  

Q(quality)-function:
	Q-function depend on the policy(:math:`\pi`) , thus :math:`Q^{\pi}`.

	:math:`Q^{\pi}(s_t, a_t)=\sum_{t'=t}^T E_{\pi_\theta}[r(s_{t'}, a_{t'})|s_t,a_t]`. total reward from taking :math:`a_t` in :math:`s_t`.   

	In many RL settings evaluating this quantity exactly is usually intractable, and thus in practice we approximate this quantity. Expectation can be estimated through samples and there are many ways to sampling.

Value Function:
	:math:`V_\pi(s_t)=\sum_{t'=t}^T E_{\pi_\theta}[r(s_{t'}, a_{t'})|s_t]` 

	:math:`V_\pi(s_t)=E_{a_t \sim \pi(a_t|s_t)}[Q^\pi(s_t, a_t)]`

	Value function is the average of Q-value at a stage (intuitively).
Final RL Objective:
	:math:`E_{s_1 \sim p(s_1)}[V^\pi(s_1)]` 

Fixed Point Iteration:
	Q-learning usages fixed point iteration. In numerical analysis, fixed-point iteration is a method of computing fixed points of iterated functions[wikipedia].

Multi-variate normal distributed

	









Confirmation Bias
	A tendency to seize upon information that confirms our preferred position or initial hypothesis. 


======================
Library and Tools
======================

Mlflow
	MLflow_ is an open source platform to manage the ML lifecycle, including experimentation, reproducibility, deployment, and a central model registry. `Pytorch with mlflow`_ is an option.

.. _Mlflow: https://mlflow.org/
.. _Pytorch with mlflow: https://www.mlflow.org/docs/latest/python_api/mlflow.pytorch.html

TensorBoard
	TensorBoard_ provides the visualization and tooling needed for machine learning experimentation: Tracking and visualizing metrics such as loss and accuracy Visualizing the model graph (ops and layers) Viewing histograms of weights, biases, or other tensors as they change over time Projecting embeddings to a lower dimensional space Displaying images, text, and audio data Profiling TensorFlow programs.
	Tensorboard can be used `within Pytorch framework`_ too.

.. _TensorBoard: https://www.tensorflow.org/tensorboard
.. _within Pytorch framework: https://pytorch.org/docs/stable/tensorboard.html
