# collab-compet with deep reinforcement learning

## about
This repository is an implementation of deep reinforcement learning,
for the third project of [Udacity Nanodegree program "Deep Reinforcement Leraning."](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893)
The environment is based on "[Unity Tennis](https://github.com/ostamand/tennis)",
where the two agents are required to continue playing a game as long as possible.

## environment
 - states : The state consists of 8 kinds of values,
for the position and the velocity of the ball and the racket.
Each agent has own observation of states.
 - actions : The agent has 2 continuous values as an action.
 - rewards : +0.1 if an agent successfully hit the ball
 and -0.01 if an agent missed to hit the ball or succeeded but the ball went outside of the boundary.
 - This is an episodic task,
 and the goal is to achieve an average score better than +0.5
 over 100 consecutive episodes,
 where a better score of the two agents is chosen for each episode.


## installation
You need to work with python 3.6.13.
Otherwise, you may fail installation some package,
especially an old version of tensorflow.
In addition, it is recommended to create with a new virtual environment
and work in it for the following processes.

[Unity ML-agents](https://github.com/openai/gym) and numpy need to be installed in adavance. 

```
pip install gym
pip install gym[box2d]
```

You also need to download a zip file of the Unity environment as follows:
 - [for linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
 - [for mac](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
 - [for 64-bit windows](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
 - [for 32-bit windows](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

It is convenient to unzip the downloaded zip file above
under the repository directory you will create next.


Then, after cloning this repository, go to the "deep-reinforcement-learning" submodule and install necessary libraries as below:

```
git clone https://github.com/maedamaeday/UdacityRL_p3.git --recursive
cd UdacityRL_p3/deep-reinforcement-leraning/python
pip install .
cd ../../
```

Note that you need "--recursive" option in cloning the repository
to incorporate deep-reinforcement-learning submodule properly.

Finally, create IPython kernel as below to run ipynb files:

```
python -m ipykernel install --user --name env_name --display-name "env_name"
```

Please replace "env_name" with your virtual environment.

## run training and watch trained agent actions
"my_Tennis.ipynb" is the main file of this repository.
The first part is taken from the sample code provided by Udacity,
and learning part for this is added (from cell #5).

Before running the notebook,
you need to specify the Unity environment in the cell #2,
following instructions in the notebook.

The details of the model architecture, training method and its performance is
summarized in [Report.md](Report.md)