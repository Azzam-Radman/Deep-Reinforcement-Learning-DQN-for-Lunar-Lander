# 🚀 Lunar Lander - Deep Reinforcement Learning (DQN) Project

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)
![OpenAI Gym](https://img.shields.io/badge/OpenAI%20Gym-0.26.0-yellow.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Stars](https://img.shields.io/github/stars/Azzam-Radman/Deep-Reinforcement-Learning-DQN-for-Lunar-Lander?style=social)

A Deep Q-Network (DQN) implementation to solve the **LunarLander-v2** environment from OpenAI Gym. This project demonstrates how deep reinforcement learning can be used to train an agent to successfully land a lunar module.

## 🌌 Project Overview

This repository contains:
- A complete DQN implementation with experience replay
- Hyperparameter tuning configurations
- Training scripts and evaluation metrics
- Pre-trained models for demonstration
- Visualization tools for tracking agent performance

## 📦 Dependencies

| Package         | Version   |
|-----------------|-----------|
| Python          | ≥ 3.8     |
| TensorFlow      | ≥ 2.0     |
| OpenAI Gym      | ≥ 0.26.0  |
| NumPy           | ≥ 1.19.0  |
| Matplotlib      | ≥ 3.3.0   |
| Pillow          | ≥ 8.0.0   |

Install dependencies with:
```bash
pip install -r requirements.txt
```

## 🧠 DQN Architecture
The implementation features:

Neural Network: 3 dense layers (256, 256, 128 units) with ReLU activation

Experience Replay: Buffer size of 100,000 transitions

Target Network: Soft updates with τ = 0.001

Exploration Strategy: ε-greedy with linear decay

## 🏋️ Training Process
# Example training command
```python train.py \
    --episodes 1000 \
    --batch_size 64 \
    --gamma 0.99 \
    --epsilon_start 1.0 \
    --epsilon_end 0.01 \
    --epsilon_decay 0.995 \
    --learning_rate 0.00025
```

## 🏋️ Training Parameters

| Parameter          | Value                          |
|--------------------|--------------------------------|
| γ (discount factor) | 0.99                          |
| Learning rate      | 0.00025                       |
| Batch size         | 64                            |
| ε decay           | Linear from 1.0 to 0.01 over episodes |

## 📊 Results

After training for **1000 episodes**:
- **Average Reward**: >200 (solved criterion)
- **Training Time**: ~2 hours on CPU (varies by hardware)
- **Success Rate**: ~85% on evaluation runs

## 📚 References
- **Human-level control through deep reinforcement learning (Nature 2015)**
- **OpenAI Gym Documentation**

## 📝 License
This project is licensed under the MIT License - see the LICENSE file for details.
