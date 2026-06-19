# Task 4: General Health Query Chatbot (Prompt Engineering Based)

## Objective
Build a chatbot that answers general health-related questions using prompt engineering and a free Large Language Model (LLM) via Hugging Face.

---

## Tools & Model

- **LLM:** Mistral-7B-Instruct-v0.1 (free, open-source)
- **API:** Hugging Face Inference API (free tier)
- **Approach:** Prompt Engineering with safety filtering

---

## Libraries Used

```
requests
```

Install with:
```bash
pip install -r requirements.txt
```

---

## Setup — Hugging Face API Key

1. Go to [huggingface.co](https://huggingface.co) and sign up for free
2. Navigate to **Settings → Access Tokens**
3. Click **New Token** → name it → copy the token
4. Paste it in Cell 2 where it says `your_huggingface_token_here`

---

## Steps Performed

### 1. API Setup
- Connected to Hugging Face Inference API
- Used Mistral-7B-Instruct model — free and powerful for health queries

### 2. Prompt Engineering
Designed a system prompt that instructs the model to:
- Act as a friendly medical assistant
- Give clear and simple answers
- Always recommend consulting a real doctor
- Add disclaimers for medical information
- Never diagnose or prescribe medications

### 3. Safety Filter
Built a keyword-based safety filter that blocks harmful queries including:
- Self harm related queries
- Prescription or overdose requests
- Dangerous medical advice requests

### 4. Chatbot Function
- Combines system prompt with user query
- Sends request to Hugging Face API
- Returns clean, safe response
- Handles API errors gracefully

### 5. Test Queries
Tested with example queries from the task:

| Query | Type |
|-------|------|
| What causes a sore throat? | General health |
| Is paracetamol safe for children? | Medication safety |
| What are the symptoms of diabetes? | Disease symptoms |
| How do I overdose on medicine? | Safety filter test |

### 6. Interactive Chat Loop
- Built a while loop for continuous conversation
- User types queries, chatbot responds
- Type 'quit' to exit the chat

---

## Key Findings

- Prompt engineering significantly affects response quality and safety
- System prompts effectively guide the model to stay within safe boundaries
- Safety filters prevent harmful queries from reaching the LLM
- Free models like Mistral-7B perform well for general health queries
- Disclaimers are essential in any medical AI application

---

## How to Run

1. Clone the repository
```bash
git clone https://github.com/elleenfatima05/AI_ML_Internship.git
```

2. Navigate to this task
```bash
cd AI_ML_Internship/Task4
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Get your free Hugging Face API token from [huggingface.co](https://huggingface.co/settings/tokens)

5. Open the notebook and replace `your_huggingface_token_here` with your token

6. Run all cells
```
task4_health_chatbot.ipynb
```

> Note: An active internet connection is required to call the Hugging Face API.

---

## Safety Notice

This chatbot is built for **educational purposes only**. It does not provide real medical advice. Always consult a qualified healthcare professional for medical decisions.

---

## Skills Demonstrated

- Prompt design and engineering
- Using APIs for LLMs via Hugging Face
- Safety handling in chatbot responses
- Building simple conversational agents
- Error handling for API calls
