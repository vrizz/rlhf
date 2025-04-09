# RLHF
[![wandb badge](https://github.com/wandb/assets/blob/main/wandb-github-badge.svg)](https://wandb.ai/valer/rlhf)

![rlhf](https://github.com/user-attachments/assets/db7ce021-a043-4567-8e04-8fffcb8bc700)

An implementation of **Reinforcement Learning from Human Feedback (RLHF)** using Hugging Face's [`trl`](https://huggingface.co/docs/trl) library.

## 🏆 Reward Model Fine-Tuning (`reward_train.ipynb`)
- **Model:** `distilroberta-base`
- **Dataset:** [`trl-lib/lm-human-preferences-descriptiveness`](https://huggingface.co/datasets/trl-lib/lm-human-preferences-descriptiveness) (human-ranked text pairs)
- **Objective:** Learns to score text based on alignment with human preferences for descriptiveness

## 🦾 PPO Fine-Tuning (`ppo_train.ipynb`)
- **Base Model:** GPT-2
- **Reward Model:** [`argilla/roberta-base-reward-model-falcon-dolly`](https://huggingface.co/argilla/roberta-base-reward-model-falcon-dolly)
- **Dataset:** [`argilla/databricks-dolly-15k-curated-en`](https://huggingface.co/datasets/argilla/databricks-dolly-15k-curated-en) (15K instruction-response pairs)
- **Objective:** Improves response quality (e.g., coherence, descriptiveness) on instruction-following tasks
