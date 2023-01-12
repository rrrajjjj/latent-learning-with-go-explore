# Latent Learning with Go-Explore
This project replicates the findings from Edward Tolman's Latent Learning experiment using reinforcement learning. The goal of the project is to figure out if reinforcement learning can be used to replicate the findings of classical psychological experiments. All the code and documentation can be found in the main notebook in the repository. 

## The Latent Learning Experiment
In 1948, psychologist Edward Tolman published a seminal paper in Cognitive Science [1] where he introduced the idea of latent learning. The experiment involved rats navigating a maze to find food. The rats were divided into three groups: a group that received no reward during training, a group that received a reward at the end of each training trial, and a group that received a reward only after a delay.

The results of the experiment showed that the rats in the group that received no reward during training (the "latent learning" group) performed just as well as the rats in the group that received a reward at the end of each training trial when a reward was eventually introduced. This suggests that the rats in the latent learning group had learned the layout of the maze during training, despite not receiving any immediate reward for doing so.

## Replicating Latent Learning with Go-Explore
Learning without rewards or with sparse rewards has been a widely studied problem in reinforcement learning and the Go-Explore algorithm from OpenAI [2] tackles that problem performing remarkably well at Atari's infamous Montezuma's Revenge. I've implemented a bare bones version of the algorithm for a very simple maze environment and the rat-like agent is trained in a similar manner to the rats in Tolman's experiment, with three different training conditions: no reward, immediate reward, and delayed reward. The results of the simulation show that the agent trained with no reward during training (the "latent learning" condition) performs just as well as (even slightly better than) the agent trained with an immediate reward when a reward is eventually introduced.

![Screenshot from 2023-01-12 21-40-25](https://user-images.githubusercontent.com/70520320/212176400-e8249361-e8af-44e0-ad03-9627eea44937.png)

## Conclusion
This project demonstrates that reinforcement learning can be used to replicate the findings of classical psychological experiments like Tolman's latent learning experiment. The results of the simulation support the idea that RL agents, much like Tolman's rats, can explore their environment learn even in the absence of reinforcement and they can demonstrate the learned behavior when the reinforcement is introduced.

## References
1. Tolman, E. C. (1948). Cognitive maps in rats and men. Psychological Review, 55(4), 189–208.
2. Ecoffet, Adrien, et al. "First return, then explore." Nature 590.7847 (2021): 580-586.

## Acknoledgements 
The maze environment has been created using [mazelab](https://github.com/zuoxingdong/mazelab). 

This project has been undertaken as a class project for the **Systems Design, Integration, and Control** class at Universitat Pompeu Fabra. 
