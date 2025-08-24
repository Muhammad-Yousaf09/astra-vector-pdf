# 📄 PDF Query with LangChain & Astra DB

A **Question-Answering (QA) application** that enables querying information directly from PDF documents.  
This project combines **LangChain**, **OpenAI embeddings**, and **Astra DB (Cassandra with Vector Search)** to build an intelligent pipeline that retrieves relevant PDF chunks and generates answers using a Large Language Model (LLM).

---

## ✨ Features
- 📑 **Upload & Read PDFs** using `PyPDF2`
- 🔎 **Chunking & Embedding** of PDF text with **OpenAI embeddings**
- 🗄️ **Vector Search with Astra DB (Cassandra)** powered by **CassIO**
- 🤖 **Question Answering** with OpenAI LLM (via LangChain)
- ⚡ Quick & Scalable semantic search pipeline

---

## ⚙️ Prerequisites
Before running the notebook, make sure you have:
1. An **Astra DB (Serverless Cassandra with Vector Search)** instance → [Get Astra DB](https://www.datastax.com/astra)
2. An **Astra DB Application Token** with role **Database Administrator**
3. Your **Astra DB ID**
4. An **OpenAI API Key** → [Get API Key](https://platform.openai.com/)

---

## 📦 Installation

Clone the repo and install dependencies:

```bash
git clone https://github.com/Muhammad-Yousaf09/astra-vector-pdf.git
cd astra-vector-pdf

# Install required packages
pip install cassio datasets langchain openai tiktoken PyPDF2
```

---

## 🚀 Usage

1. Open the notebook:

   ```bash
   jupyter notebook astra_db_pdfquery.ipynb
   ```

2. Set your environment variables:
   ```python
   ASTRA_DB_APPLICATION_TOKEN = "your_astra_db_token"
   ASTRA_DB_ID = "your_astra_db_id"
   OPENAI_API_KEY = "your_openai_api_key"
   ```

3. Run the notebook cells:
   - Load and read your PDF
   - Create embeddings & store vectors in Astra DB
   - Ask questions in natural language and get AI-powered answers

---

## 📊 Example Workflow

1. Upload a **research paper PDF**  
2. The system chunks and embeds the PDF text  
3. Store embeddings in **Astra DB**  
4. Ask:  
   ```
   "What is the main contribution of this paper?"
   ```  
5. The system retrieves relevant sections and generates an answer using OpenAI’s LLM

---

## 📂 Project Structure

```
astra-vector-pdf/
│── astra_db_pdfquery.ipynb   # Main notebook
│── README.md                  # Project documentation
└── requirements.txt           # (Optional) Dependencies file
```

---

## 🔮 Future Improvements
- Add **Streamlit UI** for interactive PDF Q&A  
- Support for **multiple PDFs**  
- Integration with **open-source LLMs** (e.g., LLaMA, Falcon)  
- Advanced **chunking strategies** for better context retrieval  

---

## 🤝 Contributing
Contributions are welcome! Please open an issue or submit a pull request.

---

## 📜 License
This project is licensed under the **MIT License**.
