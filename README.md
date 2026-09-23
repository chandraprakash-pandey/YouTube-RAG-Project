# 🎥 YouTube RAG — Ask Questions About YouTube Videos

A **Retrieval-Augmented Generation (RAG)** project that allows users to ask questions about the content of a YouTube video.

The system extracts the video's transcript, processes it into smaller chunks, converts the chunks into vector embeddings, retrieves the most relevant context for a user query, and uses an LLM to generate a grounded answer.

## 🧠 How It Works

```text
YouTube Video
      │
      ▼
Fetch Transcript
      │
      ▼
Text Splitting
      │
      ▼
Generate Embeddings
      │
      ▼
Vector Store
      │
      ▼
User Question
      │
      ▼
Similarity Search
      │
      ▼
Relevant Context
      │
      ▼
LLM
      │
      ▼
Generated Answer
```

## ✨ Features

* 📺 YouTube video transcript processing
* ✂️ Transcript chunking for efficient retrieval
* 🧠 Semantic vector embeddings
* 🔎 Similarity-based context retrieval
* 🤖 LLM-powered question answering
* 📚 Retrieval-Augmented Generation using LangChain
* 💬 Answers grounded in the video's content

## 🛠️ Tech Stack

* **Python**
* **LangChain**
* **YouTube Transcript API**
* **Vector Embeddings**
* **Vector Database**
* **Large Language Model (LLM)**
* **Jupyter Notebook**

## 🔄 RAG Pipeline

### 1. Transcript Extraction

The system first retrieves the transcript associated with the YouTube video.

### 2. Text Splitting

The transcript is divided into smaller chunks so that relevant sections can be retrieved efficiently.

### 3. Embedding Generation

Each chunk is converted into a numerical vector representation that captures its semantic meaning.

### 4. Retrieval

When the user asks a question, the query is converted into an embedding and compared with the stored transcript embeddings.

The most relevant chunks are selected as context.

### 5. Generation

The retrieved context is passed to the LLM along with the user's question.

```text
Question + Retrieved Context
            │
            ▼
           LLM
            │
            ▼
     Context-Aware Answer
```

This reduces the dependency on the model's pre-trained knowledge and grounds the response in the selected video content.

## 📂 Project Structure

```text
YouTube-RAG-Project/
│
├── rag_using_langchain.ipynb
│   └── Complete RAG implementation
│
└── README.md
```

## 🚀 Getting Started

### Clone the Repository

```bash
git clone https://github.com/chandraprakash-pandey/YouTube-RAG-Project.git
cd YouTube-RAG-Project
```

### Install Dependencies

Create a virtual environment:

```bash
python -m venv venv
```

Activate it:

**Windows**

```bash
venv\Scripts\activate
```

**Linux/macOS**

```bash
source venv/bin/activate
```

Install the required packages:

```bash
pip install langchain
pip install youtube-transcript-api
```

Install any additional dependencies required by the notebook.

## ▶️ Run the Project

Open the notebook:

```bash
jupyter notebook rag_using_langchain.ipynb
```

Run the cells sequentially and provide the required YouTube video information and query.

## 🎯 Example

```text
YouTube Video:
"Introduction to Machine Learning"

Question:
"What is supervised learning?"
```

The RAG pipeline retrieves the relevant portion of the transcript and generates an answer based on that context.

## 💡 Why RAG?

Instead of asking an LLM to answer solely from its pre-trained knowledge:

```text
User Question
      ↓
     LLM
      ↓
   Answer
```

RAG provides relevant external context:

```text
User Question
      ↓
Retrieve Relevant Transcript
      ↓
Question + Context
      ↓
     LLM
      ↓
Grounded Answer
```

This makes the system more suitable for answering questions about **specific video content**.

## 🚀 Future Improvements

* Support multiple YouTube videos
* Add timestamp-based answers
* Add conversational memory
* Improve retrieval with hybrid search
* Add a web-based UI
* Add support for multilingual transcripts
* Add source citations for retrieved transcript chunks

---

### 👨‍💻 Author

**Chandraprakash Pandey**

[GitHub](https://github.com/chandraprakash-pandey)
