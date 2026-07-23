- **Project Objective**: The goal is to implement reinforcement learning through gaming, with a focus on developing an AI model capable of playing Mario and adapting to dynamic environments. [Link to Project](https://pypi.org/project/gym-super-mario-bros/)
  
- **Tools**: Python will be the primary language, with OpenAI Gym serving as the framework for training the AI in various simulated environments, similar to Alphabetix but on a smaller scale. [Link to OpenAI Gym](https://gym.openai.com/)
  
- **Preprocessing Steps**: Before training the AI, data preprocessing is necessary. This includes grayscale conversion and frame stacking. Grayscale conversion simplifies data, while frame stacking provides memory for the AI to recognize patterns in Mario's movements and adversaries' behaviors over time. 
  
- **Installation Requirements**: GPU acceleration (CUDA or ROCm 4.2(beta)) is essential for efficient output display. RL libraries such as Stable-Baselines3, offering algorithms like DQN, are required. [Link to Stable-Baselines3](https://stable-baselines3.readthedocs.io/en/master/)
  
- **Vectorization**: Frame stacking is achieved using VecFrameStack(env, 4, channels_order='last') to enhance the AI's memory within the environment.
  
- **Training the Reinforcement Model**: The Proximal Policy Optimization (PPO) algorithm is chosen for training. Dependencies like os for file path management, PPO for algorithms, and BaseCallback for saving models are imported. A custom class, TrainAndLoggingCallback(BaseCallback), contains code for model training.
  
- **Testing**: Model testing involves loading the trained model from memory or file using methods like model.load or ppo.load, ensuring the AI's adaptability post-training. The code's output opens in a new window upon execution.
