Research Proposal
==================

Generalization remains one of the most fundamental challenges 
in reinforcement learning and agents often overfit to large 
training sets 
:cite:`zhang2018natural,cobbe2018quantifying,justesen2018illuminating,juliani2019obstacle`. 
An effective solution is to learn skill which can be used in various context of the environment.

In the tower of Hanoi paper, we showed how short-horizon skills can be leveraged in long-horizon tasks. 
The short-horizon skill learning environment is similar to the long-horizon task where the later has more 
objects, thus more challenging. The actions set is similar. In this work, we extend our skill learning 
approach to tackle different environments. We will demonstrate the skill transfer from one environment 
to the different environments. We will use the Progen OpenAI environment to demonstrate our algorithms. 
Progen consists of 16 different environments with different action sets and a diverse environment, thus challenging. 
We will develop an algorithm to demonstrate the generalization of reinforcement learning.

-------------------------------------------------
Artificial Intelligence for Scientific Discovery
-------------------------------------------------

- Leverage existing scientic knowledge to advance the scientic discovery.
- Build autonomous agents to discover new knowledge and thus improve the boundary of basic and advance science.

Conferences: https://2020.midl.io/


Robotic surgery, work done, building system, but use model-based. Task dependent. RL used in robotics but applying them in surgery is difficult because long horizon and safety concern. Also data in surgery is scare thus tough to generate data (environment) for all type of surgical procedure. 
Masudur want to build RL algorithm that is workable in long horizon, - demonstrated RL applicability in long horizon task, Tower of Hanoi - similar to surgical procedure, used for training.
Now Masudur want to build algorithm that can perform safely by incorporating constraints into RL agent ( safety assurance). Still tackling long-horizon is a challenges thus developing algorithm that can work better in long-horizon tasks. (extension of tower hanoi - better, without given plan).
Another challenge is generalizability across the environment - thus Masudur is working on to build RL algo that can work better (feasibility, make RL usable for the safety-critical system (surgery)). Procgen, bsuite environment for testing. 
Challenge:
Log-horizon
Safety critical
Generalizability

The proposed algorithm will help to make RL usable in the safety-critical domain and the newly proposed algorithm will improve the state of the art of RL research.

