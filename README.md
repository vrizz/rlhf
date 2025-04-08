# RLHF
![rlhf](https://github.com/user-attachments/assets/db7ce021-a043-4567-8e04-8fffcb8bc700)

A minimal implementation of reward model training and PPO fine-tuning with the [Hugging Face trl library](https://huggingface.co/docs/trl/en/index).

🏆 `reward_train.ipynb`:  This notebook fine-tunes "distilroberta-base" as a reward model using the "trl-lib/lm-human-preferences-descriptiveness" dataset, which contains human-ranked text pairs (preferred vs. rejected responses). The trained reward model learns to assign scores that reflect alignment with human preferences for descriptiveness.

🦾 `ppo_train.ipynb`: This notebook fine-tunes GPT-2 using reinforcement learning with Proximal Policy Optimization (PPO), where the model's responses are evaluated and improved based on a reward signal from the "argilla/roberta-base-reward-model-falcon-dolly" classification model, while training is performed on the "argilla/databricks-dolly-15k-curated-en" dataset, which contains 15,000 curated instruction-response pairs.
