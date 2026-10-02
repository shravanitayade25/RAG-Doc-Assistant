# RAG doc Assistant

A local **PDF Document Q&A System** built with **Python, Streamlit, RAG, Llama 3.2, Ollama, Embedchain, and ChromaDB**.

The application allows users to upload a PDF document and ask questions about its content. It uses Retrieval-Augmented Generation (RAG) to retrieve relevant information from the document and generate answers using a locally running Llama 3.2 model.

## Features

* Upload PDF documents
* Preview the uploaded PDF
* Extract and store document content
* Retrieve relevant information using RAG
* Ask questions about the uploaded document
* Generate answers using Llama 3.2
* Runs locally using Ollama
* No OpenAI API key required
* Chat history during the current session
* Clear chat history

## Tech Stack

* **Python**
* **Streamlit**
* **Llama 3.2**
* **Ollama**
* **Embedchain**
* **ChromaDB**
* **RAG (Retrieval-Augmented Generation)**

## How It Works

1. The user uploads a PDF document.
2. The document is processed and added to the knowledge base.
3. ChromaDB stores the document embeddings.
4. When the user asks a question, the system retrieves relevant document information.
5. Llama 3.2 processes the retrieved information and generates the answer.
6. The answer is displayed through the Streamlit chat interface.

## Project Structure

```text
chat_with_pdf/
│
├── chat_pdf.py
├── chat_pdf_llama3.py
├── chat_pdf_llama3.2.py
├── requirements.txt
└── README.md
```

The main application for this project is:

```text
chat_pdf_llama3.2.py
```

## Requirements

* Python 3.9+
* Ollama
* Llama 3.2 model
* Required Python packages

## Installation

Install the Python dependencies:

```bash
pip install -r requirements.txt
```

Install Ollama from the official website and download the Llama 3.2 model:

```bash
ollama pull llama3.2:latest
```

Make sure Ollama is running locally.

## Run the Application

Run the Streamlit application:

```bash
streamlit run chat_pdf_llama3.2.py
```

The application will open in your browser.

## Example Usage

1. Open the application.
2. Upload a PDF from the sidebar.
3. Click **Add to Knowledge Base**.
4. Ask questions about the uploaded document.
5. The system retrieves relevant information and generates an answer using Llama 3.2.

## Key Concepts

### Retrieval-Augmented Generation (RAG)

RAG combines document retrieval with a language model. Instead of generating an answer only from the model's existing knowledge, the system first retrieves relevant information from the uploaded document and uses it to generate the response.

### Local LLM

The application uses **Llama 3.2 through Ollama**, allowing the language model to run locally without requiring an OpenAI API key.

## License

This project is intended for educational and portfolio purposes.
