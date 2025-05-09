# RAG_BOT
# ChatGroq Demo

A Streamlit-based Retrieval-Augmented Generation (RAG) application using LangChain and Groq LLMs. This project allows you to load documents (web pages or PDFs), split them into chunks, generate embeddings, store vectors in FAISS, and build a question-answering chatbot that retrieves relevant context for accurate responses.

---

## 👉 Features

* **Document Sources**: Load content from web URLs or local PDF directories.
* **Text Splitting**: Automatically split long documents into manageable chunks with overlap to preserve context.
* **Embeddings**: Support for multiple embedding models (Ollama, Hugging Face).
* **Vector Store**: Utilize FAISS for efficient similarity search.
* **Retrieval Chain**: Build a RAG workflow with customizable prompt templates.
* **Streamlit UI**: Interactive web interface for easy question input and result exploration.

---

## 📁 Repository Structure

```plaintext
├── app_web.py               # Streamlit app loading web documents
├── app_pdf.py               # Streamlit app loading PDF documents
├── test_docs/               # Directory for sample PDF files
├── requirements.txt         # Python dependencies
├── .env                     # Environment variables for API keys
└── README.md                # Project documentation
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/chatgroq-demo.git
cd chatgroq-demo
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Set Up Environment Variables

Create a `.env` file in the project root with the following keys:

```dotenv
GROQ_API_KEY=your_groq_api_key
OPENAI_API_KEY=your_openai_api_key  # if using OpenAI embeddings
```

### 4. Run the App

#### Web Document Loader

```bash
streamlit run app_web.py
```

#### PDF Document Loader

```bash
streamlit run app_pdf.py
```

Open your browser at `http://localhost:8501` to interact with the demo.

---

## ⚙️ Configuration

* **Embedding Models**: Change `OllamaEmbeddings()` or `HuggingFaceEmbeddings(model_name="all-MiniLM-L6-v2")` in the code to switch models.
* **Text Splitter**: Adjust `chunk_size` and `chunk_overlap` in `RecursiveCharacterTextSplitter` for different chunk granularity.
* **LLM Settings**: Modify `model_name` and other parameters in `ChatGroq()` initialization.

---

## 🤝 Contributing

1. Fork the repository
2. Create a new branch: `git checkout -b feature/YourFeature`
3. Make your changes and commit: `git commit -m "Add YourFeature"\`
4. Push to the branch: `git push origin feature/YourFeature`
5. Open a Pull Request

Please ensure code is well-documented and follows PEP8 conventions.

---

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
