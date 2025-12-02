


# **Rag AI Study Assistant (RAG Pipeline)**

A production-grade **Retrieval-Augmented Generation system** designed to convert long-form **videos into an intelligent, searchable AI assistant**.
This project demonstrates my capability to build **end-to-end LLM pipelines**, architect **RAG systems**, and design **scalable data + AI workflows** used in modern AI products.

---

## ⭐ **Why This Project Matters**

This repository showcases the **exact skills companies look for** in AI/ML, Data, and DevOps candidates:

### ✔ **Full AI System Design**

Complete pipeline:
**Video → Audio → Transcript → Chunking → Embeddings → Vector Search → LLM Answer Generation**

### ✔ **Real RAG Architecture**

Not a demo. A **working, modular, extendable** RAG pipeline ready for API or product integration.

### ✔ **Practical Data Engineering**

Handling:

* Audio & video preprocessing
* JSON transcript management
* Large text chunking & metadata
* Joblib-based vector DB storage

### ✔ **LLM + Embedding Integration**

Built with retrieval pipelines, optimized prompts, and cosine similarity search.

### ✔ **Production-Friendly Codebase**

Clean, short, and modular scripts that can be plugged into:

* APIs (Flask/FastAPI)
* Internal enterprise pipelines
* Multi-user EdTech systems

---
# How to use this RAG AI Teaching assistant on your own data
## Step 1 - Collect your videos
Move all your video files to the videos folder

## Step 2 - Convert to mp3
Convert all the video files to mp3 by ruunning video_to_mp3

## Step 3 - Convert mp3 to json 
Convert all the mp3 files to json by ruunning mp3_to_json

## Step 4 - Convert the json files to Vectors
Use the file preprocess_json to convert the json files to a dataframe with Embeddings and save it as a joblib pickle

## Step 5 - Prompt generation and feeding to LLM

Read the joblib file and load it into the memory. Then create a relevant prompt as per the user query and feed it to the LLM
---

## 🚀 **What You Can Build With This**

This RAG pipeline can transform **any video content** into a smart, contextual AI assistant.

Perfect for:

### 🏫 **Education**

* Personalized study assistant
* Lecture summarization
* “Ask your class videos” feature
* Competitive exam prep bots

### 🏢 **Corporate / Enterprise**

* Convert **training videos into searchable AI assistants**
* Make **meeting recordings queryable**
* Build **internal knowledge assistants**
* Improve onboarding with instant answers from training sessions

### 🎤 **Content & Media**

* Interview indexing
* Podcast Q&A bots
* YouTube video search tools

If it’s a video, this system can **understand it and answer from it**.

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
   ├── Prompt Engineering
   │
Final AI Answer
```

This mirrors real-world RAG deployments used in industry.

---

## 🔧 **How to Use (Step-by-Step)**

### **1️⃣ Place Your Videos**

Add learning/training videos into:

```
/videos
```

---

### **2️⃣ Convert Video → MP3**

```bash
python video_to_mp3.py
```

Outputs to `/audios`.

---

### **3️⃣ Convert MP3 → Transcript JSON**

```bash
python mp3_to_json.py
```

Outputs to `/jsons`.

---

### **4️⃣ Build Vector Store**

```bash
python preprocess_json.py
```

This script:

* Chunks text
* Generates embeddings
* Stores vector DB in `embeddings.joblib`

---

### **5️⃣ Query the RAG Assistant**

```python
import joblib

df = joblib.load("embeddings.joblib")
# Perform vector search + prompt generation
# Send to your LLM endpoint (Ollama / Groq / OpenAI)
```

Your assistant now answers from **your own content only**.

---

## 🛠️ **Tech Stack**

### **Core**

* Python
* FFmpeg
* Pandas, NumPy
* Scikit-learn (cosine similarity)
* Embedding Model (BGE-M3 or similar)
* Local/Cloud LLM (Ollama, Groq, OpenAI, etc.)

### **Highlights**

* Modular structure
* Vector search pipeline
* Chunking + embeddings
* Highly extensible for API deployment

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
│── process_incoming.py   # Core RAG logic
│── requirements.txt
│── README.md
```

---

## 🔥 **What This Project Demonstrates About Me**

### ✔ Strong understanding of LLM + RAG design

### ✔ Ability to build end-to-end AI systems from scratch

### ✔ Skill in embeddings, chunking, vector search

### ✔ Clean, production-ready code

### ✔ Real-world functionality that can be deployed immediately

This is the same architectural pattern used in:

* Chatbots
* Enterprise knowledge search engines
* Study assistants
* Video indexing systems
* Internal training Q&A bots

---

**👨‍💻 Author:** *Avinash Kamble*

* 🔗 **LinkedIn:** [https://linkedin.com/in/avinashzz](https://linkedin.com/in/avinashzz)
* 🐙 **GitHub:** [https://github.com/avinash-kamble-9](https://github.com/avinash-kamble-9)
* 📧 **Email:** [avinassh116zz@gmail.com](mailto:avinassh116zz@gmail.com)

---

