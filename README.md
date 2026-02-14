---
title: Fundamental Rights Chatbot
emoji: 📚
colorFrom: blue
colorTo: purple
sdk: gradio
sdk_version: 4.0.0
app_file: app.py
pinned: false
---

# 📚 Fundamental Rights Chatbot

An AI-powered chatbot that answers questions about **Part III of the Indian Constitution** (Fundamental Rights) using Retrieval-Augmented Generation (RAG).

## 🌟 Features

- **Intelligent Q&A**: Ask questions about Fundamental Rights in natural language
- **Accurate Answers**: Retrieves relevant context from the Constitution using vector search
- **Legal Expertise**: Specialized in Indian Constitutional Law (Part III)
- **User-Friendly Interface**: Simple Gradio interface for easy interaction

## 🔧 Technology Stack

- **LangChain**: RAG pipeline orchestration
- **FAISS**: Vector database for semantic search
- **HuggingFace Transformers**: 
  - Embeddings: `sentence-transformers/all-MiniLM-L6-v2`
  - LLM: `google/flan-t5-large`
- **Gradio**: Web interface
- **PyPDF**: PDF document processing

## 📖 How to Use

1. Type your question about Fundamental Rights in the input box
2. Click Submit or press Enter
3. The chatbot will retrieve relevant sections and provide a detailed answer

### Example Questions

- What is Article 21?
- What are the six freedoms guaranteed by Article 19?
- What is Article 17?
- Explain the Right to Equality
- What does Article 22 say about arrests?

## 💡 Tips for Better Answers

- Be specific about article numbers if you know them
- Ask about rights, freedoms, or protections
- For lists, explicitly ask for "all freedoms" or "all rights"

## 📋 Requirements

The following dependencies are required (see `requirements.txt`):

```
langchain
langchain-community
langchain-core
langchain-huggingface
sentence-transformers
faiss-cpu
transformers
pypdf
gradio
torch
```

## 📄 Dataset

This chatbot uses `part3.pdf` which contains Part III of the Indian Constitution dealing with Fundamental Rights (Articles 12-35).

## 🚀 Running Locally

```bash
# Clone the repository
git clone <your-repo-url>
cd <repo-name>

# Install dependencies
pip install -r requirements.txt

# Ensure part3.pdf is in the root directory

# Run the application
python app.py
```

## ⚙️ Configuration

Key parameters that can be adjusted in `app.py`:

- **Chunk Size**: 600 characters (for text splitting)
- **Chunk Overlap**: 150 characters
- **Retrieval**: Top 3 most relevant chunks
- **Max Tokens**: 512 new tokens per response
- **Temperature**: 0.3 (for more focused responses)

## 📝 License

This project is for educational purposes. Constitutional text is in the public domain.

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## ⚠️ Disclaimer

This chatbot is for informational purposes only and should not be considered legal advice. Always consult with a qualified legal professional for legal matters.
