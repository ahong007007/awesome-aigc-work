SFT监督微调算法、 RM模型模型机理和训练算法、 RLHF和PPO强化学习；  
不仅仅是算法本身，还会时刻与数据、人类标注反馈数据、数据飞轮机制相互结合关联

**openAI对RLHF的原始描述**  

• We trained this model using Reinforcement Learning from Human Feedback (RLHF), using the same methods
as InstructGPT, but with slight differences in the data collection setup. We trained an initial model using supervised
fine-tuning: human AI trainers provided conversations in which they played both sides—the user and an AI
assistant. We gave the trainers access to model-written suggestions to help them compose their responses. We
mixed this new dialogue dataset with the InstructGPT dataset, which we transformed into a dialogue format.  
• To create a reward model for reinforcement learning, we needed to collect comparison data, which consisted of two
or more model responses ranked by quality. To collect this data, we took conversations that AI trainers had with the
chatbot. We randomly selected a model-written message, sampled several alternative completions, and had AI
trainers rank them. Using these reward models, we can fine-tune the model using Proximal Policy Optimization.
We performed several iterations of this process.  
• ChatGPT is fine-tuned from a model in the GPT-3.5 series, which finished training in early 2022. You can learn
more about the 3.5 series here. ChatGPT and GPT 3.5 were trained on an Azure AI supercomputing infrastructure  

**RLHF算法三部曲**

先不管枝叶算法（思维链、红蓝对抗、宪法原则嵌入、无害性嵌入、涌现、情景/上下文学习、少/零样本学习等）

<Training language models to follow instructions with human feedback>![1](https://user-images.githubusercontent.com/22077027/234273781-a5db6940-3316-4f2b-9d05-29a513df6525.JPG)
