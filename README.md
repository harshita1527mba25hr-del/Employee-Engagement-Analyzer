#  Employee Engagement Analyzer

##  Overview
This project is an AI-powered Retrieval-Augmented Generation (RAG) application built using Flowise. It enables intelligent question-answering over an employee engagement research document by combining LLMs, embeddings, and vector search.

The system allows users to upload a research file and interact with it conversationally to extract insights related to employee engagement challenges, trends, and key HR factors.

---

##  Key Features
-  Document-based Question Answering  
-  Semantic Search using Vector Embeddings  
-  Conversational AI using LLM (Mistral / Gemini)  
-  Modular workflow built in Flowise  
-  Real-time response generation  

---

##  Architecture Diagram

```text
User Query
   │
   ▼
Conversational Retrieval QA Chain
   │
   ├── Chat Model (LLM - Mistral)
   │
   ├── Memory (Buffer Memory)
   │
   └── Vector Store Retriever
            │
            ▼
      In-Memory Vector Store
            │
            ▼
     Embeddings (Google Gemini)
            │
            ▼
        Document Chunks
            │
            ▼
     Recursive Text Splitter
            │
            ▼
         File Loader (PDF)
```

---

##  Tech Stack
- **Flowise** – AI workflow builder  
- **Mistral AI** – Language Model  
- **Google Gemini Embeddings** – Text embeddings  
- **Vector Store** – In-memory vector database  
- **PDF Loader** – Document ingestion  

---

##  Workflow Steps

### 1. File Upload
- Upload employee engagement research PDF  
- Data is passed to the text splitter  

### 2. Text Splitting
- Recursive Character Text Splitter  
- Chunk Size: 1000  
- Chunk Overlap: 200  

### 3. Embedding Generation
- Use Google Gemini Embeddings  
- Convert text chunks into vectors  

### 4. Vector Storage
- Store embeddings in In-Memory Vector Store  
- Enable fast similarity search  

### 5. Query Processing
- User inputs a question  
- Retriever fetches relevant chunks  

### 6. Response Generation
- Mistral LLM generates answer using retrieved context  
- Conversational chain maintains memory  

---

##  Screenshots

### 🔹 Flowise Workflow
<img width="1845" height="874" alt="Screenshot 2026-04-16 100620" src="https://github.com/user-attachments/assets/7186076a-8b41-4f17-8051-56c1708dad4d" />
<img width="1574" height="862" alt="Screenshot 2026-04-16 100710" src="https://github.com/user-attachments/assets/91a4417e-54c9-447f-b814-950cc39b14f4" />

```

##  Project Structure

```bash
├── screenshots/
│   ├── workflow.png
│   └── output.png
├── README.md
└── flowise_export.json
```

---

##  How to Run

1. Install Flowise  
2. Import the workflow JSON file  
3. Configure API keys:  
   - Mistral API  
   - Google Gemini API  
4. Upload your PDF document  
5. Start asking questions 

---

## Use Cases
- HR Analytics  
- Employee Engagement Insights  
- Research Document QA  
- Academic Projects  

---

##  Future Improvements
- Add persistent vector database (Pinecone, FAISS)  
- Multi-document support  
- UI enhancements  
- Cloud deployment  

---

##  Acknowledgements
- Flowise Community  
- Open-source AI tools  

---

## Author
**Harshita**  
MBA HR | AI & Analytics Enthusiast  
