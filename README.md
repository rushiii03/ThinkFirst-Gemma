# ThinkFirst-Gemma
An open-source fine-tuned Gemma model that learns step-by-step reasoning using Tunix on TPUs.
# 🧠 ThinkFirst-Gemma  
### Fine-tuning Gemma to reason step-by-step using Tunix and TPU  

---

## 🚀 Overview  

**ThinkFirst-Gemma** is an open-source project built for the **AI Reasoning Hackathon**.  
Starting from Google’s **Gemma model (Gemma-2B or Gemma-3 1B)**, this project fine-tunes it using **Tunix** on **Google TPUs** to make the model “think before it speaks.”  

Our goal is to create a **transparent, explainable, and step-by-step reasoning model** that not only gives correct answers but also **explains how it arrived at them**.  

> Like our parents always said: “Think first, talk later.”  
> Let’s teach our models to do the same. 🧩  

---

## ✨ Key Features  

✅ Fine-tuned Gemma model for **step-by-step reasoning**  
✅ Uses **Tunix** training pipeline on **TPUs**  
✅ Implements **Structured Fine-Tuning (SFT)** and **GRPO** reward optimization  
✅ Transparent **reasoning traces** for each model response  
✅ Open-source configs, reward functions, and reproducible recipes  

---

## 🏗️ Architecture  

The ThinkFirst pipeline includes:  
1. **Base model:** Gemma 2B or Gemma 3 1B  
2. **Data preparation:** reasoning-based Q&A and explanation datasets  
3. **Fine-tuning:** Tunix framework with SFT and GRPO  
4. **Reward model:** custom reward composition to favor reasoning accuracy and clarity  
5. **Evaluation:** step-by-step reasoning metrics

---

## ⚙️ Training Pipeline  

### Step 1. Environment Setup
```bash
pip install -r requirements.txt

Step 2. Launch Training on TPU

python train.py --config configs/tunix_gemma_config.yaml

Step 3. Fine-tuning Config

model_name: "gemma-2b"
learning_rate: 1e-5
batch_size: 64
optimizer: "adamw"
reward_function: "reasoning_accuracy + explanation_score"
save_dir: "./checkpoints"

Step 4. Evaluate

python evaluate.py --checkpoint ./checkpoints/final_model.pt

## 🔗 Project Links

- [GitHub Repo](https://github.com/RushiSalunke/ThinkFirst-Gemma)
- [Kaggle Demo](https://www.kaggle.com/rushisalunkeeeee/thinkfirst-gemma-demo)
https://huggingface.co/RushiSalunke/ThinkFirst-Gemma
- [YouTube Video](https://youtu.be/PY9s7x9ZumM?si=3TT4wfJ4ot-k2Sbj)
