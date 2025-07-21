# 🧠 Text Summarizer with Hugging Face Transformers & Gradio

An interactive web application for abstractive text summarization, powered by Hugging Face Transformers and deployed using Gradio. This project explores how state-of-the-art language models can distill long-form text into concise, informative summaries through a clean, accessible UI.

## 🚀 Project Overview

This application demonstrates an end-to-end NLP pipeline that leverages the **`google/pegasus-large`** model—one of the top-performing models for abstractive summarization. The interface allows users to input large blocks of text (such as news articles or blog posts) and receive coherent, high-quality summaries within seconds.

Key components include:

- Integration of the Hugging Face `transformers` library to access advanced summarization models.
- Customization of model parameters for fine-tuned output length and sampling behavior.
- Deployment using `Gradio` to provide a user-friendly, browser-accessible interface.
- Tokenizer optimization for efficient preprocessing on resource-limited devices.

## 🧰 Technologies Used

- **Python 3.10+**
- **Hugging Face Transformers** — for accessing pre-trained LLMs
- **Gradio** — to create and deploy the web UI
- **Google Pegasus Model** — `google/pegasus-large`, fine-tuned for summarization tasks
- **Tokenizer** — same tokenizer as model for consistency and performance optimization

## 🔍 Why PEGASUS?

The `google/pegasus-large` model was selected for its cutting-edge approach to abstractive summarization, utilizing a unique pre-training strategy called **Gap Sentence Generation (GSG)**. During pre-training, key sentences are removed from long-form documents, and the model learns to reconstruct them—teaching it to focus on essential content. It was later fine-tuned on real-world summarization datasets such as CNN/DailyMail, XSum, and WikiHow, which makes it highly effective for summarizing news and editorial content.

Unlike the default `sshleifer/distilbart-cnn-12-6` model, PEGASUS handles longer token sequences (up to 1024–2048 tokens) and provides more semantically rich summaries.

## ⚙️ Features

- ✍️ Input free-form long text (e.g., news, articles, reports)
- ⚡ Summarize with `google/pegasus-large` using Hugging Face pipeline
- 🎛️ Adjustable model parameters like `min_length`, `max_length`, and `do_sample`
- 🧪 Fast testing in Jupyter + Gradio interface for real-time interaction
- 🖥️ Built for lower-end machines, with performance considerations like tokenizer integration

## 📷 Example Output

**Input:**

> “The Toronto Raptors have decided to extend the contract of head coach Rajaković following a season of defensive improvements and signs of progress, despite a losing record…”

**Summary Output:**

> "The Raptors are retaining coach Rajaković, citing his strong defensive schemes and potential despite recent losing seasons."

---

## 💡 Key Learnings
- Learned to modify default model pipelines and integrate new models with custom tokenizers.
- Experimented with decoding strategies (greedy vs. beam search vs. sampling).
- Overcame hardware limitations (integrated GPU) by optimizing token lengths and minimizing latency.
- Built a clean Gradio UI from scratch that integrates smoothly with backend inference.
