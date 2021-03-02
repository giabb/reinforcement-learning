# Reinforcement Learning using SAC algorithm and Ant-v2 gym environment

This project has been developed during the 2019 Reinforcement Learning Course held py [Prof. Capobianco](http://robertocapobianco.com/) at [Sapienza University of Rome](https://www.uniroma1.it/).

The algorithm used in this project is the [Soft Actor-Critic algorithm](https://arxiv.org/abs/1812.05905) . More details on the implementation in the next sections.

## Summary

  - [Getting Started](#getting-started)
  - [Some Specifications](#some-specifications)
  - [Authors](#authors)
  - [License](#license)
  - [Acknowledgments](#acknowledgments)

## Getting Started

The project contains only a Jupyter Notebook file. Meet the prerequisite and use it.

### Prerequisites

- Python 3.5+
- Jupyer ``` pip install jupyterlab ```
- [MuJoCo](http://www.mujoco.org) 
	- I suggest [this article](https://medium.com/@ganeshprasanna/setting-up-mujoco-7a5ee62cf6dc) to install it. It worked on Ubuntu 18.04, Python 3.7.5 and mujoco200.
	- You will need a MuJoCo license.
- Gym ``` pip install gym ```
- Stable Baselines [installation](https://stable-baselines.readthedocs.io/en/master/guide/install.html)
- Numpy ``` pip install numpy ```
- Scipy ``` pip install scipy ```
- TQDM ``` pip install tqdm ```

## Some specifications

The environment where the tests are taken is the MuJoCo environment [Ant-v2](https://gym.openai.com/envs/Ant-v2/) . The target of this environment is to let the Ant walk as fast as possible, as long as possible. The ant is a hierarchical structure with the "torso" as the main object, and the 4 legs as the children:

![img_ant](https://raw.githubusercontent.com/giabb/reinforcement-learning/main/md_media/ant.jpg = 200x)

The observation space is a 111-dim space:

|          Torso Height         |  1  |
|:-----------------------------:|:---:|
|       Torso Orientation       |  4  |
|          Joint Angles         |  8  |
| Velocities (angular + linear) |  6  |
|        Joint Velocities       |  8  |
|        External Forces        |  84 |
|        Total dimension        | 111 |

The reward function is [defined here](https://github.com/openai/gym/blob/master/gym/envs/mujoco/ant.py#L10) .

You can find a video of the final execution [here](https://github.com/giabb/reinforcement-learning/blob/main/md_media/The%20Walking%20Ant.mp4) .


## Authors

  - **Giovanbattista Abbate** - [giabb](https://github.com/giabb)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

- **Billie Thompson** - *Provided README Template* - [PurpleBooth](https://github.com/PurpleBooth)
