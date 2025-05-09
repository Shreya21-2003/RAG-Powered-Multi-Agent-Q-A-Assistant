# 🧠 Text File Q&A App using Streamlit

This is a lightweight Streamlit web app that allows users to upload `.txt` files and ask questions related to their content. It performs basic text parsing and retrieves relevant responses based on keyword matches.

---

## 📦 Features

- ✅ Upload `.txt` files
- ✅ Ask natural language questions
- ✅ Retrieve and display relevant answers
- ✅ Minimal and user-friendly interface
- ✅ Built entirely using Streamlit

---


---

## 🧪 Architecture Overview

1. **Data Ingestion**
   - User uploads `.txt` files via the UI.
   - Files are read and split into manageable chunks using LangChain's `CharacterTextSplitter`.

2. **Vector Store Creation**
   - Embeddings are created for each chunk using `OpenAIEmbeddings`.
   - Chunks are stored in a FAISS in-memory vector database for semantic retrieval.

3. **Retrieval and LLM Integration**
   - A `RetrievalQA` chain is built using OpenAI’s GPT model.
   - User questions are matched against document content using FAISS similarity search.
   - The most relevant chunks are passed to the LLM to generate a final answer.

---

## 🚀 How to Run the App

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/llm-doc-qa.git
cd llm-doc-qa

1. **Install dependencies**
2.**Add OpenAI API Key**
3.**Start the App**
