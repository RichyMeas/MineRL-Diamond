# CS-4644-project
Deep Reinforcement Learning: Mine a diamond
By the team: Herobrine the Miner (Alon Baruch, Jim James, Nan Zheng, Richy Meas)
Project summary:
We aim to train a reinforcement learning agent to play Minecraft and obtain a diamond. The agent’s performance should be robust to random seed, obstacles, and hostile mobs. This is a fairly complex problem as it goes from pixels to both small and large actions, such as crafting items or building structures, so solving it will demonstrate deep reinforcement learning’s capabilities. It is also interesting as Minecraft has an incredibly large upper bound on its state space (as a result of its nearly infinite world size), so high performance in a generalizable manner isn’t possible via classical AI or tabular RL algorithms.
Approach:
We will utilize Deep Q Learning. Since the available inputs in the environment are in the form of a low-resolution, video stream, our neural network will start off with convolution and pooling layers to encode the local game area into some vector. This vector would then be passed through several linear layers to produce our Q value estimates for each action, at which point we will select the action estimated to provide the greatest reward. To simplify gameplay, we will reduce the action space. For instance, instead of allowing all float angles of camera control, we will force the Q learner to pick from a certain preset. 
We will start off by using the baseline Q learning example so we won’t have to waste time writing boilerplate code. Some experiments will include hyperparameter optimization runs and adjusting the action space.
Resources / Related Work & Papers: 
The current state of the art for this problem is a structured approach with a variety of Deep Q Learning and Imitation Learning. In regards to deep reinforcement learning in the minecraft realm, the most widely used strategies are using a convolutional neural network to extract some importance from the current/previous frame(s) and having fully connected layers extract the state action pair. The current objective of obtaining a diamond in 15 minutes is difficult for most Deep Reinforcement Learning agents. The winners in 2019 utilized multiple architectures (DQN, PreDQN, etc) to obtain the diamond with the given action space and reward system.
Some useful resources, research papers, and previous examples are listed below
https://minerl.io/docs/tutorials/index.html
http://cs229.stanford.edu/proj2016/report/UdagawaLeeNarasimhan-FightingZombiesInMinecraftWithDeepReinforcementLearning-report.pdf  
https://hal.archives-ouvertes.fr/hal-02062157/document
https://arxiv.org/pdf/1908.01007.pdf
https://arxiv.org/pdf/1803.08456.pdf 
https://arxiv.org/pdf/2101.11071.pdf
https://arxiv.org/pdf/1904.10079.pdf
https://github.com/minerllabs/baselines 
https://colab.research.google.com/drive/1qU5sEnJPZj7q2KgRDwZ868jlBGerSsK7?usp=sharing 
Dataset: https://minerl.io/dataset/ 
 

