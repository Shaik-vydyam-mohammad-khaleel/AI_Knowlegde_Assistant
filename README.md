 ## 📖 Islamic AI Assistant (RAG-based)

An Islamic AI Assistant built using Retrieval-Augmented Generation (RAG) that answers questions strictly from a fixed knowledge base consisting of:

- The Qur’an (English translation)

- Authentic Hadith from Sahih al-Bukhari (English)

The system is designed to minimize hallucinations, avoid personal opinions, and respond safely when information is not found.

## 🚀 Project Overview

This project demonstrates how Large Language Models (LLMs) can be safely grounded in religious texts using a vector database and controlled prompting.

1. Instead of training or fine-tuning an LLM, the assistant:

2. Retrieves relevant passages from a vector store (FAISS)

3. Injects them as context

Generates answers only from retrieved content

## 🧠 Architecture (High Level)


- User Question
      ↓
- Retriever (FAISS)
      ↓
- Relevant Qur’an / Hadith Text
      ↓
- Prompt + Context
      ↓
- Gemini LLM
      ↓
- Final Answer

## 🛠️ Tech Stack

- Python

- LangChain

- FAISS (Vector Database)

- Sentence-Transformers (Embeddings)

- Gemini LLM (Google Generative AI)

- Streamlit (UI – optional)

- Hugging Face Spaces (Deployment)

## 📚 Knowledge Base

- Qur’an (English translation, structured by Surah & Ayah)

- Sahih al-Bukhari Hadith (English, extracted and cleaned from PDFs)

The knowledge base is:

1. Preprocessed

2. Chunked

3. Embedded

4. Stored as a FAISS vector store

Once created, it is loaded at runtime and treated as a read-only knowledge base.

## 🔎 Key Concepts Used

Retrieval-Augmented Generation (RAG)

- Semantic Search

- Vector Embeddings

- Prompt Engineering

- Safety-first LLM design

## ✍️ Prompt Design (Safety First)

The assistant is explicitly instructed to:

- Answer only using retrieved context

- Avoid personal opinions

- Avoid religious rulings (fatwas)

Example refusal:

“Please consult a qualified Islamic scholar.”
