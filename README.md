# 🧠 LLM-Based Mortgage Transcript Field Extractor

> Extracts structured loan application data (1003 Form) from call transcripts using LLaMA 2 and Streamlit.

---

## 🚀 Overview

This project uses a fine-tuned LLM (Meta’s LLaMA 2) to extract borrower information from customer service call transcripts related to mortgage applications. The model outputs a structured JSON with field names, values, and confidence scores—streamlining the loan origination process from raw call data.

The tool features a clean Streamlit UI for interaction and provides instant results, even handling incomplete or malformed inputs gracefully.

---

## 🎯 Features

- 🤖 Built with `LLaMA 2 (meta-llama/Llama-2-7b-chat-hf)`
- 🔍 Extracts 1003 Form fields (e.g., Borrower Name, Loan Amount)
- 📈 Confidence scores for every extracted field
- 🧪 Handles partial/incomplete transcripts
- 🖼️ Interactive Streamlit frontend
- 🔁 REST API endpoint for external integration

---

## 🧠 Model & Tech Stack

| Category         | Details                                  |
|------------------|------------------------------------------|
| Model            | LLaMA 2 7B Chat (HuggingFace)            |
| Libraries        | Hugging Face Transformers, PyTorch       |
| UI               | Streamlit, pyngrok                        |
| Language         | Python                                   |
| Deployment       | Local / Colab (NVIDIA A100 GPUs)         |
| Output Format    | JSON with field name, value, confidence  |

---

## 🧪 Test Scenarios

| Type     | Description                                 |
|----------|---------------------------------------------|
| ✅ Positive | Complete transcripts parsed accurately      |
| ❌ Negative | Missing or empty fields handled gracefully  |
| ⚠️ Edge     | Invalid inputs return clear error messages  |

Sample output:
```json
{
  "fields": [
    {
      "field_name": "Borrower Name",
      "field_value": "John Doe",
      "confidence_score": 0.95
    },
    {
      "field_name": "Loan Amount",
      "field_value": "$250,000",
      "confidence_score": 0.90
    }
  ]
}
