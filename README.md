# DRL2020_ContinuousControl

[//]: # (Image References)

[image1]: https://video.udacity-data.com/topher/2018/June/5b1ea778_reacher/reacher.gif "Reacher Env"
[image2]: https://user-images.githubusercontent.com/10624937/42386929-76f671f0-8106-11e8-9376-f17da2ae852e.png "Kernel"

![Trained Agents][image1]

This repository contains material related to Udacity's [Deep Reinforcement Learning Nanodegree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893) program.  

## Table of Contents

This repository contains the following files:

- Continuous_Control_train.ipynb: The jupyter notebook used for training the agent that solves this environment. The notebook can also be used to visualize the trained agent.

- ddpg_agent.py: Source code for the Deep Deterministic Policy Gradient agent that solves the environment.

- model.py: Source code that defines the network architecture (layers, etc.) for the DDPG agent.

- checkpoint_*_solved.pth: Saved model weights (state dict) for the dqn agent. (4 different files!)

- Reacher_multi.app.zip: Compressed Unity environment that the agent runs in.

- python/: Folder used for installing dependencies

- Report.pdf: Report detailing how this project was completed.

## The Environment

The environment is implemented within Unity ML Agents. More info about these environments can be found [here](https://github.com/Unity-Technologies/ml-agents)

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of the agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

To accelerate training for the agent, we use a multi-agent version of the environment that renders 20 robot arms, each with a different target, simultaneously. The scores of the different arms are averaged.

The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30.

## Installation

To set up your python environment to run the code in this repository, follow the instructions below.

0. Do not use pyenv in combination with conda to manage your environment. If you want to use pyenv, you will have to set the environment to Python 3.6 there. Pyenv's global version setting will overwrite any changes you make in Anaconda.

1. Create (and activate) a new environment with Python 3.6.

- __Linux__ or __Mac__: 
```bash
conda create --name drlnd python=3.6
source activate drlnd
```
- __Windows__: 
```bash
conda create --name drlnd python=3.6 
activate drlnd
```

2. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym. 
(Usually, you can ignore these extra steps:
- Next, install the **classic control** environment group by following the instructions [here](https://github.com/openai/gym#classic-control).
- Then, install the **box2d** environment group by following the instructions [here](https://github.com/openai/gym#box2d).
)

3. Clone the repository (if you haven't already!), and navigate to the `python/` folder.  Then, install several dependencies. (There is also a line in the training notebook to do this.)
```bash
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.  
```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

5. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. (May not need to do this, if you set an environment with pyenv.)

![Kernel][image2]

## Getting started

1. Unpack the Reacher_multi.app file.

2. Open the Continuous_Control_train.ipynb notebook.

3. Run the cells in the notebook to start the unity environment and initialize the DDPG agent. You can train the agent, or you can skip to the end of the notebook to see a trained agent.

4. Close the environment from within the notebook after you're done.

