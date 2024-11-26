# Dash Anything
Geometry Dash AI

## Task List
- Read GD screen
- Input commands to GD (jump)
- 

## Usage
If you would like to use the **Dash Anything** bot, documentation on how to use it will be available in the future!

## Methodology
If you would like to know the though process behind the project, feel free to read the things below:

### Input
The idea behind this project is to **only** use visual features! There exists certain tools that allow us to access certain properties about the user while they play (notably through mods), but it would be interesting to at least set a baseline where no additional information is given aside from visual input. In the future, I may be rich enough to buy and use MegaHack but right now I am broke :(.  

The visual input will be fed through certain models to extract **image embeddings**. The two types planned to be used is a **Convolutional Neural Network (CNN)** and a **Vision Transformer (ViT)**. 

### Dataset
Level Distribution is uneven!

### Learning
Using various frameworks:
- Deep Q Learning (DQN)
- Proximal Policy Optimization (PPO)

#### Reward Function
Models built in a RL framework require a reward function to indicate which state/actions are more beneficial for the player. The current planned rewards are listed below. 
- Time Survived/Level percentage (+)
    - Longer you live, the farther in the level you go!
    - Some levels do not end at 100%, so time might be a better metric.
- Dying (-) (end)
- Complete (+++) (end)

## Frequently Asked Questions (FAQ)
### Usage
- Do you plan to make a mobile port?
    - Not currently.
- How about a model for platformer mode?
    - Maybe in the future? But I will focus on this for now.

### Methodology
- Couldn't you also add sound as part of the input?
    - Someone asked me this question before and I thought it was a very interesting point. After all, Geometry Dash is a rhythm-based platformer. Unfortunately I do not have time for it now but in the future it will likely be added. 
- Why doesn't your reward function use jumps?
    - This question may seem a bit weird, so let's recontexualize this question. When you play GD in cube mode, most levels will have **sparse** inputs. In other words, the time where you hold down an input is much more infrequent compared to the time where you don't hold down an input. However, this pattern of inputs will change depending on what game mode you are in. For example, in the wave game mode, the input will be held down for roughly ~50% of the time (I'm just making a random guess here but hopefully the point still makes sense). Ideally you could design a better input model for each game mode but currently I am too lazy to do that.

## Sources
- https://wyliemaster.github.io/gddocs/#/
- https://gdpy.readthedocs.io/en/latest/index.html