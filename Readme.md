
# **RAG AI Study Assistant (Retrieval-Augmented Generation Pipeline)**

A production-ready **Retrieval-Augmented Generation (RAG)** system that converts long videos into an intelligent, searchable study assistant.
This project demonstrates a complete end-to-end pipeline for transforming video content into structured, queryable knowledge.

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

# **How to Use This RAG Pipeline**

## **Step 1: Add Your Videos**

Place all source videos inside:

```
/videos
```

---

## **Step 2: Convert Videos → MP3**

```bash
python video_to_mp3.py
```

This creates audio files under `/audios`.

---

## **Step 3: Convert MP3 → Transcript JSON**

```bash
python mp3_to_json.py
```

Outputs structured transcripts under `/jsons`.

---

## **Step 4: Build Vector Store (Embeddings)**

```bash
python preprocess_json.py
```

This script performs:

* Text cleaning
* Chunking
* Embedding generation
* Saving embeddings to `embeddings.joblib`

---

## **Step 5: Query the RAG Assistant**

Example:

```python
import joblib

df = joblib.load("embeddings.joblib")

# Perform vector search + create prompt
# Send prompt to your LLM API
```

Your assistant will answer questions strictly based on your video content.

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
rag/
│── videos/
│── audios/
│── jsons/
│── embeddings.joblib
│── video_to_mp3.py
│── mp3_to_json.py
│── preprocess_json.py
│── process_incoming.py
│── requirements.txt
│── README.md
```

---

## 👤 **Author**

**Avinash Kamble**
*AI/ML & Cloud Enthusiast*

* 🔗 LinkedIn: [https://linkedin.com/in/avinashzz](https://linkedin.com/in/avinashzz)
* 🐙 GitHub: [https://github.com/avinash-kamble-9](https://github.com/avinash-kamble-9)
* 📧 Email: [avinash116zz@gmail.com](mailto:avinash116zz@gmail.com)

---

