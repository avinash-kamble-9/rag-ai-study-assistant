
# **RAG AI Study Assistant (Retrieval-Augmented Generation Pipeline)**

A production-ready **Retrieval-Augmented Generation (RAG)** system that converts long videos into an intelligent, searchable study assistant.
This project demonstrates a complete end-to-end pipeline for transforming video content into structured, queryable knowledge.

---
## 🚀 **Live Demo**

🎬 **Watch the Demo Video:**
👉 [https://www.youtube.com/watch?v=Jck2tLjsFEA](https://www.youtube.com/watch?v=Jck2tLjsFEA)

---


## 📌 **Overview**

This repository contains a modular pipeline that processes any educational or training video and enables **AI-powered question-answering** directly from the video’s content.

### **Pipeline:**

**Video → Audio → Transcript → Chunking → Embeddings → Vector Search → LLM Answer**

---

## 🧠 **Core Features**

### ✔ **Video-to-Audio Conversion**

Converts MP4 videos into MP3 files using FFmpeg.

### ✔ **Speech-to-Text Transcription**

Transforms MP3 files into clean JSON transcripts.

### ✔ **Text Chunking + Embeddings**

Breaks transcripts into meaningful chunks and generates dense embeddings using **BGE-M3**.

### ✔ **Vector Search Engine**

Performs cosine similarity search to fetch the most relevant chunks.

### ✔ **LLM Integration**

Retrieved context is used to prompt an LLM (Ollama / OpenAI / Groq).

### ✔ **Fully Modular Scripts**

Each step is implemented separately for easy debugging and production adaptation.

---


# 🎥 **Video Sources Used in This Project**

This RAG pipeline was built and tested using content from the following sources:

## **1️⃣ Primary Video Dataset (YouTube Playlist – First 18 Videos Only)**

**Playlist:** *Code With Harry – Python Tutorials For Beginners*
🔗 [https://youtube.com/playlist?list=PLu0W_9lII9agq5TrH9XLIKQvv0iaF2X3w](https://youtube.com/playlist?list=PLu0W_9lII9agq5TrH9XLIKQvv0iaF2X3w)

Only the **first 18 videos** from this playlist were used for:

* Video-to-Audio conversion
* Transcription
* Embedding generation
* RAG-based question answering

---

## **2️⃣ Audio Files (Processed MP3s)**

All MP3 audio files extracted from the videos are stored here:

🔗 **Google Drive Folder:**
[https://drive.google.com/drive/folders/1QSnVSzPltlu5qk4ZF6W04pm-d5X6Z9Fs?usp=drive_link](https://drive.google.com/drive/folders/1QSnVSzPltlu5qk4ZF6W04pm-d5X6Z9Fs?usp=drive_link)

This folder contains the finalized MP3 files that were used for speech-to-text processing.
---
## 🧩 **System Architecture**

```
Videos
   │
   ├── Audio Extraction (FFmpeg)
   │
MP3 Files
   │
   ├── Speech-to-Text
   │
Transcript JSONs
   │
   ├── Chunking + Embeddings (BGE-M3)
   │
Vector Store (Joblib)
   │
   ├── Similarity Search
   │
Relevant Chunks
   │
   ├── Prompt Formation
   │
Final AI Answer
```
---
## 🖼️ RAG Pipeline Architecture  
<p align="center">
  <img src="assets/Rag_pipeline_.png" width="850">
</p>

---

## 🚀 **What You Can Use This For**

This system can convert any video into a smart knowledge assistant.

### 🏫 **Education**

* Personalized AI tutor
* Lecture-based Q&A assistant
* Exam preparation
* Academic research helpers

### 🏢 **Corporate / Enterprise**

* **Meeting recordings → searchable AI assistant**
* **Training videos → instant internal Q&A bot**
* **Onboarding assistant for new employees**
* Support knowledge discovery inside organizations

### 🎙 Content & Media

* Podcast indexing
* YouTube summarization
* Interview search bots

If it's a video, this system can **understand, chunk, and answer from it**.

---

## 🛠️ **Tech Stack**

### **Languages & Tools**

* Python
* FFmpeg
* Pandas & NumPy
* scikit-learn (cosine similarity)
* BGE-M3 embedding model
* Ollama / OpenAI / Groq LLMs

---

## 📁 **Project Structure**

```
rag-ai-study-assistant/
│── jsons/
│── embeddings.joblib
│── video_to_mp3.py
│── mp3_to_json.py
│── preprocess_json.py
│── process_incoming.py
│── app.py
│── static/style.css
│── templates/index.html
│── requirements.txt
│── README.md
```

---
