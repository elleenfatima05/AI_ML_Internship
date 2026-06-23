# Task 5: Mental Health Support Chatbot (Fine-Tuned)

## Objective
Fine-tune a small language model to respond empathetically to mental health conversations using transfer learning techniques.

---

## Model & Dataset

- **Base Model:** DistilGPT2 (lightweight, fast to fine-tune)
- **Dataset:** Estwld/empathetic_dialogues_llm (structured version of Facebook AI's EmpatheticDialogues)
- **Platform:** Google Colab with Tesla T4 GPU
- **Training Samples:** 1,000 conversations
- **Epochs:** 2

---

## Libraries Used

```
transformers
datasets
torch
accelerate
```

Install with:
```bash
pip install -r requirements.txt
```

> Note: This notebook was built and run on Google Colab due to GPU requirements for fine-tuning.

---

## Steps Performed

### 1. Environment Setup
- Installed transformers, datasets, torch, and accelerate libraries
- Verified Tesla T4 GPU availability on Colab

### 2. Dataset Loading
- Loaded `Estwld/empathetic_dialogues_llm` dataset — 19,533 multi-turn conversations
- Each conversation includes a situation, emotion label, and dialogue turns between user and assistant

### 3. Model Loading
- Loaded DistilGPT2 as the base pretrained model
- Configured tokenizer with padding token for proper batching

### 4. Data Preprocessing
- Converted multi-turn conversations into a single text format: `User: ... Therapist: ...`
- Tokenized text with max length of 128 tokens
- Selected 1,000 samples to keep training time manageable

### 5. Fine-Tuning
- Used Hugging Face `Trainer` API for fine-tuning
- Trained for 2 epochs with batch size 8
- Used mixed precision (fp16) for faster GPU training
- Training completed in approximately 5-10 minutes on T4 GPU

### 6. Testing the Fine-Tuned Model
Tested the fine-tuned chatbot with sample mental health queries:
- "I feel really anxious today."
- "I am stressed about work and cannot sleep."
- "I feel lonely and do not know what to do."

---

## Key Findings

- Fine-tuning allows a general-purpose model to specialize in empathetic, context-aware responses
- DistilGPT2 is lightweight enough to fine-tune on free Colab GPU in under 10 minutes
- 2 epochs on 1,000 samples is sufficient to observe a behavioral shift toward empathetic responses
- The fine-tuned model responds more contextually than the base DistilGPT2 model
- Training with more data and additional epochs would further improve response quality and coherence

---

## How to Run

1. Open [Google Colab](https://colab.research.google.com)
2. Upload `task5_mental_health.ipynb`
3. Set Runtime → Change runtime type → T4 GPU
4. Run all cells from top to bottom

> Note: This task requires GPU access. Running on CPU is possible but significantly slower and not recommended.

---

## Disclaimer

This chatbot is built for **educational purposes only** as part of an AI/ML internship. It is not a substitute for professional mental health support. If you or someone you know is struggling, please reach out to a licensed mental health professional or a crisis helpline.

---

## Skills Demonstrated

- Fine-tuning pretrained language models
- Working with Hugging Face Transformers and Datasets libraries
- GPU-accelerated model training
- Data preprocessing for conversational AI
- Text generation and evaluation
