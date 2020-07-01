Introduction
============
I am broadly interested in Artificial Intelligence, Machine Learning, and Robotics. I work on designing and building intelligent learning agents (e.g., RL) which can make interpretable critical decisions under uncertainty.

Two major goals:

- Adapting AI in real-world applications.
- AI for Scientific Discovery

------------
Heighlights
------------

**Solving Tower of Hanoi witth Reinforcement Learning - 2020**

We propose an approach to tackle a similar type of problem by integrating high-level planning into low-level partial sensory input. 
Firstly, we learn low-level skills (e.g., grasp) which are often short-horizon and then apply these learned skills with high-level planning (abstract state-space solution). 
We develop a simulated environment for the classic Tower of Hanoi (TOH) puzzle and evaluate our framework in its ability to solve the puzzle. We successfully train an RL agent (i.e., TD3) on short-horizon skills and then propose three model variations to combine these skills in the puzzle environment which eventually able to solve the Tower of Hanoi.

**Regularizing Sequential Prediction with Logic Constraints - 2020**

We propose two methods to regularize
RNN-based sequential predictions with such domain knowledge
(constraints with weights): (i) PriorLayer, in which the values
of the hidden layer of the RNN are combined with weights
learned from logic constraints in an additional neural network
layer (applied during training), and (ii) Conflation, in which
class probabilities from RNN predictions and constraints weights are combined based on conflation of class probabilities (applied after training). We evaluate both methods for robotic activity classification on simulated OpenAI Gym environment and realworld DESK dataset for surgical robotics. We observe that our proposed approaches boost performance by regularizing LSTMbased networks. In particular, on the Gym dataset, PriorLayer helps to improve accuracy in initial training while avoiding overfitting early, thus boosting the final classification accuracy from
75% to 81% on unseen data. Conversely, Conflation enhanced
the testing accuracy of LSTM from 50% to 71% at the first
epoch, and from 41% to 53% on real Taurus robot data.

**Transferring Dexterous Surgical Skill Knowledge - 2019** :cite:`rahman2019transferring`.

We propose a methodology that uses compact image
representations with kinematic features for surgeme recognition
in the DESK dataset. This dataset offers samples for surgical
procedures over different robotic platforms with a high variability in the setup. 
We performed surgeme classification in two
setups: 1) No transfer, 2) Transfer from a simulated scenario
to two real deployable robots. Then, the results were compared
with recognition accuracies using only kinematic data with the
same experimental setup. The results show that our approach
improves the recognition performance over kinematic data
across different domains. The proposed approach produced a
transfer accuracy gain up to 20% between the simulated and
the real robot, and up to 31% between the simulated robot and
a different robot. A transfer accuracy gain was observed for
all cases, even those already above 90%.

**DESK Dataset - 2019** :cite:`madapana2019desk`.

In this paper, we present the DESK (DExterous
Surgical SKills) dataset. It comprises a set of surgical robotic
skills collected during a surgical training task using three
robotic platforms: the Taurus II robot, Taurus II simulated
robot, and the YuMi robot. This dataset was used to test the
idea of transferring knowledge across different domains (e.g.
from Taurus to YuMi robot) for a surgical gesture classification
task with seven gestures/surgemes. We explored two different
scenarios: 1) No transfer and 2) Domain transfer (simulated
Taurus to real Taurus and YuMi robots). We conducted
extensive experiments with three supervised learning models
and provided baselines in each of these scenarios. Results
show that using simulation data during training enhances the
performance on the real robots, where limited real data is
available. In particular, we obtained an accuracy of 55% on
the real Taurus data using a model that is trained only on the
simulator data, but that accuracy improved to 82% when the
ratio of real to simulated data was increased to 0.18 in the
training set.

---------------------------------------------------------------
Information Retrieval + Software Engineering
---------------------------------------------------------------
**Evaluating How Developers Use General-Purpose Web-Search for Code Retrieval - 2018** :cite:`rahman2018evaluating` 

*Findings*:
A single code query is, in general, larger and uses a smaller
vocabulary than a non-code query (see RQ1).
(2) To retrieve the intended answer, users have to spend more time
on a single code query and have to modify the queries more
often than the non-code queries (see RQ 2).
(3) To complete a code related search task, users require more
queries, more URLs clicked, and overall more time than noncode related search tasks (see RQ 3).

**Toward Optimal Selection of Information Retrieval Models for Software Engineering Tasks - 2019** :cite:`rahman2019toward`.

We provide empirical evidence that the success of IRbased SE tasks depends significantly on the choice of
IR model(s), which in turn depends on the underlying
document type(s), and that careful selection, combination
and tuning of IR models can improve the accuracy of IRbased SE tasks. We propose and evaluate SRCH, our generic framework to
automate IR model selection and tuning for SE tasks. We
also show that SRCH can be used in legacy environments
to improve accuracy. We curate a valuable dataset of 1832 GitHub projects
by retrieving their descriptions, readme contents, class
and method names, imported package usage, and APIs for
project recommendation, where we manually associated
each project with a fine-grained category that describes
its functionalities. Our dataset is publicly available at
https://github.com/masud99r/IR-in-SE

**Recommending GitHub Projects for Developer Onboarding - 2018** :cite:`liu2018recommending`.

We build a recommender system, NNLRank, for the
GitHub projects onboarding. Design nine features to capture developers' onboarding
pattern. Analyze the features that impact the model’s accuracy. Evaluate the model empirically w.r.t. prediction accuracy
and run-time performance.

**Topic Model based Privacy Protection in Personalized Web Search - 2016** :cite:`ahmad2016topic`.

We proposed a Topic-based Privacy Protection solution on client side. In our solution, each user query will be submitted with k additional cover
queries, which will act as a proxy to disguise users' intent from a
search engine. The set of cover queries are generated in a controlled
way so that each query carries similar uncertainty to randomize a
user’s search history while still providing necessary utility for the
search engine to perform personalization. We used statistical topic
models to infer topics from the original user query and generated
cover queries of similar entropy but from unrelated topics. Extensive experiments are performed on AOL search log and the promising results demonstrated the effectiveness of our solution.