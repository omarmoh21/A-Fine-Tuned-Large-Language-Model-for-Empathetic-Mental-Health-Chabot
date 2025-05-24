# Therapy Chatbot: Fine-Tuned LLMs for Mental Health Support

This project explores the development of a mental health therapy chatbot by fine-tuning three state-of-the-art large language models—**LLaMA-3.1-8B-Instruct**, **Qwen/Qwen2-7B-Instruct**, and **Mistral-7B-Instruct-v0.3**—on a curated dataset of mental health-related dialogues. The goal is to evaluate which model provides the most empathetic and helpful responses for users experiencing stress, anxiety, or depression.

## 📌 Project Summary

- **Models Fine-Tuned:** LLaMA-3.1, Qwen2-7B, Mistral-7B
- **Dataset Size:** ~800,000 rows (used 20,000 rows for training due to hardware constraints)
- **Evaluation Method:** Outputs judged using Google’s Gemini API based on empathy, supportiveness, and advice quality
- **Best Performer:** Qwen2-7B-Instruct

## 🧠 Motivation

The need for accessible and emotionally intelligent mental health support is more critical than ever. This project aims to assess the ability of modern open-source LLMs to provide such support when fine-tuned on domain-specific data.

## 🚀 Features

- Fine-tuning pipeline for open-source LLMs
- Dataset preprocessing and sampling
- Response generation for benchmark prompts
- Automated evaluation using Gemini API
- Comparative performance analysis

## 📂 Directory Structure

```
therapy-chatbot/
│
├── data/
│   └── mental_health_dataset_sample from huggingface.
├── models/
│   ├── llama3-finetuned/
│   ├── qwen2-finetuned/
│   └── mistral-finetuned/
├── paper/
│   └── therapy_chatbot_paper.pdf
├── README.md
└── requirements.txt
```

## 🛠️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/omarmoh21/A-Fine-Tuned-Large-Language-Model-for-Empathetic-Mental-Health-Chabot/tree/main
cd therapy-chatbot
```


### 2. Fine-Tune a Model

Make sure you have the dataset and the appropriate model weights (Hugging Face format).

```bash
python scripts/fine_tune.py --model qwen2 --data data/mental_health_dataset_sample.csv
```


### 3. Evaluate with Gemini API

Set your Gemini API key in `.env` or export it directly:

```bash
export GEMINI_API_KEY=your_api_key
python scripts/evaluate_with_gemini.py
```

## 📊 Results Summary

| Model              | Empathy | Supportiveness | Coherence | Overall |
|-------------------|--------:|----------------:|----------:|--------:|
| Qwen2-7B-Instruct | ⭐⭐⭐⭐☆  | ⭐⭐⭐⭐☆          | ⭐⭐⭐⭐⭐    | 🏆 Best |
| LLaMA-3.1-8B      | ⭐⭐⭐☆☆  | ⭐⭐⭐☆☆          | ⭐⭐⭐⭐☆    |        |
| Mistral-7B        | ⭐⭐☆☆☆  | ⭐⭐☆☆☆          | ⭐⭐⭐☆☆    |        |

## 📘 Citation

If you use this work, please cite:

```
@project{therapychatbot2025,
  title={Therapy Chatbot: Comparative Fine-Tuning and Evaluation of LLaMA, Qwen, and Mistral Models for Mental Health Support},
  author={Omar Shehata, Abdelrhman Nasser},
  institution={Nile University},
  year={2025}
}
```

## 🙏 Acknowledgements

Thanks to the open-source communities behind LLaMA, Qwen, and Mistral, and to Google for access to the Gemini API.

---

