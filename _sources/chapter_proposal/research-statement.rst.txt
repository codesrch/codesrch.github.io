==========================
Research
==========================

Intelligent Agent for Scientific Discovery
=============================================

- Leverage existing scientic knowledge to advance the scientic discovery.
- Build autonomous agents to discover new knowledge and thus improve the boundary of basic and advance science.


Adapting AI Solution to Real-world Problem
============================================================

Combining Structural Knowledge into Data-driven Learning
---------------------------------------------------------

A data-driven learning learn used to identify an interesting pattern, knowledge from the dataset. Often time, a benchmark dataset is used for the training and evaluate the models to see how better the models are to generalize in future tasks. However, a benchmark dataset often represents a static view of the problem and thus the learning model is inherently limited and does not guarantee to perform well in when future task where the dynamics of the problem (e.g., data distribution) changes over time. Thus it is important to develop methodologies to capture the real-worlds dynamics which we call structural knowledge. We propose to combine this structural knowledge with the data-driven learning approach to better model real-world problems. We now discuss the benefit of our approach in two implication contexts: (i) Safety-critical Domains, and (ii) Transfer Knowledge between Domains.

**Implication**: Safety-critical Domains.
Many real-world time-sensitive and high-stake applications
(e.g. surgical robotics, and rescue and recovery) exhibit repetitive nature thus applying data-driven learning is an attractive choice. For instance, in surgical robotics where sequential pattern often exists and  (RNN)-based sequential models is an attractive approach. One limitation of such approaches is the data scarcity. As a result, limited training samples may lead to over-fitting, producing incorrect predictions during deployment. Nevertheless, abundant domain knowledge may still be available, which may help formulate structural knowledge (e.g., using logic constraints). In this context, we proposed a systematic approach to regularize RNN-based sequential prediction by incorporating domain knowledge with logic constraints :cite:`rahman2019regularizing`.
We proposed two methods - adding a layer after hidden unit, and combining class probabilities. We evaluated these methods for robotic activity classification on simulation (Gym) and real-world robotic (DESK - Taurus) dataset. We observe that the proposed methods regularize LSTM-based models and thus boost the performance in the early training epoch, and when limited training data is available.

Besides, our proposed approach can be leveraged to incorporate human preference into the learning system. For example, in the robot-assisted surgery, the surgeon might want the surgery to be done in their preference when the robot is in an autonomous mood. If we allow the robot to learn the surgical procedure from redundant surgery data available from many hospitals, the learning model will not be able to cater to individual surgeon needs. In this regards, we propose to learning such surgeon preference in the form of structural knowledge and then incorporate it into the learning module.
In the future, we would like to explore in the context where we can asses the probabilistic guarantee as to the safety measure of the system which enables the existing models to apply in many real-world safety-critical domains.

**Implication**: Transfer Knowledge between Domains.
For the same task, different domains might exhibit different data distribution which hinders transfer learning between domains. For example, in surgical robotics, a surgical task (e.g., debridement - cleaning wounded area) might be performed by different medical robots. However, these different robotics domains which have different kinematic and visual sensors might generate completely different data distribution, which hinders transfer learning from one domain to the others. Nevertheless, as all the robots perform the same task who share similar context which can be represented in the form of structural context. Thus this structural knowledge can be used to enable transfer learning between domains.

It is challenging to obtain dataset consisting of different domains as described above to test the hypothesis of our proposed approach of combining structural knowledge with data-driven learning. We first developed a benchmark surgical robotic dataset, the DESK (DExterous Surgical SKills) :cite:`madapana2019desk`. It comprises of a set of surgical robotic skills collected during a surgical training task using three robotic platforms: the Taurus II robot, Taurus II simulated robot, and the YuMi robot. 
This dataset was used to test the idea of transferring knowledge across different domains (e.g. from Taurus to YuMi robot) for a surgical gesture classification task with seven gestures/surgemes comprising of multi-modal recognition model which using robotic kinematic and visual data :cite:`rahman2019transferring,madapana2019desk`. We provided baselines in each of these scenarios by conducting extensive experiments with three supervised learning models. We observe that when two domain has similarity in the domain structure (simulator and real Taurus II) the transfer accuracy was better compared to the scenario when the transfer was tested between two different robots (YuMi and Taurus Simulator). This shows the promise to apply structural knowledge combined with the data-driven learning approach. We plan to develop methodology in this transfer scenario and conduct an extensive experiment in this dataset in the future.

AI Driven Dicision-making under Uncertainty
--------------------------------------------

**Encoding Social Norms**.
Morality is an integral part of human decision making. Human often uses moral reasoning to justify their decision when required. Autonomous agents started to play an important role in making critical decisions in our society and it is envisioned that this involvement will be increased tremendously in the future, performing most of the decision-making tasks in society. 
Thus, for practical use, automatic decision-making agents need to make recommendations or decisions that align with ethical norms and values of human society. 
The challenges can be divided into two major steps. Firstly, specify societal values or moral norms into a mathematical model which is interpretable and amenable to incorporating into the automated decision-making systems. 
The challenges here is to take into consideration that moral value varies by society, group or individual. Thus any such modeling of morality must also take into account diverse groups, otherwise, it might risk of promoting values held by a majority and discriminate against minorities.  

Secondly, we need to develop methods to integrate such a model into the learning process. Thus, to take advantage of the remarkable progress in the data-driven learning domain, we aim to propose methods to incorporate existing societal norm in the learning process and thus in critical decision-making.

To this end, we developed a counterfactual reasoning based decision-making algorithm, Moral Thompson Sampling, which makes the decision under uncertainty.
In particular, we leverage a probabilistic causal inference approach to develop measures which enable autonomous agents (i.e., RL agents) to make an optimal decision based on morality along with justifying.
The objective of this agent is to maximize task-specific goal while obeying moral norms imposed by a moral model during the learning process. In a simulated driver-less car scenario, we demonstrated the effectiveness of our algorithm over standard Thompson Sampling :cite:`rahman2019morality`. In the future, we would like to work on generalizing our approach to other decision-making algorithms and domains. Besides, we will develop methods to asses the interpretability and verification guarantee of the proposed solutions.

Broader Impact of AI System
============================
Tremendous success in AI is impacting almost every aspect of human life and it is 
envisioned that it will continue to increase in the future. In the best scenario, 
this technological improvement heavily impacts our living such as producing more 
and quality food at low cost and manpower, giving affordable and safe medical care 
(e.g., robotic surgery). In contrast, the widespread adaptation of the disruptive 
technology in every section would affect the job market and disrupt the current 
economic systems which might disproportionately affect a group of people. 
To reduce the risk of disruption, we believe the both the AI development and 
economic planning needs to happen together to minimize adverse impacts on each other. 
To mitigate such adverse impact, in this regards, we propose to develop evaluation metrics for AI systems which can anticipate such impact on the social-economic system before deployment in real-world.
Such evaluation criteria include to asses the impact of a failure, malfunction, and 
potential misuse of AI systems. Besides, the assessment would include estimating 
the risk of the AI systems when it interacts with the existing human-driven systems. 
We would like to investigate in this research area.

- Transfer learning
- Surgical robotic
- RL in Surgical Robotic [ongoing - toh]


