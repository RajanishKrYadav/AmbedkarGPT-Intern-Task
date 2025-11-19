# 🕉️ Ambedkar RAG Application --- AI Chatbot for Dr. B. R. Ambedkar PDFs

This project is an **AI-powered Retrieval-Augmented Generation (RAG)
chatbot** designed specifically to answer questions related to **Dr. B.
R. Ambedkar**.\
It reads multiple PDF documents, converts them into embeddings, and uses
a local Llama 2 model to generate accurate, context-based answers.

------------------------------------------------------------------------

## 🚀 Features

-   📄 Reads all PDFs from the `data/` folder\
-   🔍 Uses FAISS for fast document search\
-   ✂️ Splits PDFs into meaningful chunks\
-   🧠 Embeddings created using MiniLM\
-   🤖 Local Llama-2-7B-GGML model for offline inference\
-   💬 Conversational memory (multi-turn chat)\
-   🎨 Streamlit-based chat interface using `streamlit_chat`

------------------------------------------------------------------------

## 📂 Project Structure

    project/
    │
    ├── data/
    │   └── *.pdf                   # Ambedkar-related PDF files
    │
    ├── llama-2-7b-chat.ggmlv3.q4_0.bin   # Local Llama model
    │
    ├── app.py                      # Main application
    │
    └── README.md

------------------------------------------------------------------------

## 🛠️ Installation

### 1. Clone the repository

``` bash
git clone <your-repo-url>
cd project
```

### 2. Create a virtual environment

``` bash
python -m venv venv
venv\Scriptsctivate     # Windows
source venv/bin/activate  # Mac/Linux
```

### 3. Install dependencies

``` bash
pip install -r requirements.txt
```

Example `requirements.txt`:

    streamlit
    streamlit_chat
    langchain
    langchain-community
    sentence-transformers
    faiss-cpu
    ctransformers
    pypdf

------------------------------------------------------------------------

## ▶️ How to Run

``` bash
streamlit run app.py
```

This will open the app at:

    http://localhost:8501/

------------------------------------------------------------------------

## 💡 How the Ambedkar RAG Works

1.  Loads Ambedkar PDFs from `/data`\
2.  Splits them into chunks using LangChain\
3.  Generates embeddings with MiniLM\
4.  Stores them in FAISS vector database\
5.  Queries are matched to the most relevant PDF chunks\
6.  Llama-2 model generates answers grounded in Ambedkar literature\
7.  Chat history is stored for smooth conversation flow

------------------------------------------------------------------------

## ❓ Usage Examples

Ask questions like:

-   "What was Dr. B. R. Ambedkar's contribution to the Indian
    Constitution?"\
-   "Explain Ambedkar's views on social justice."\
-   "Summarize this chapter from the PDF."\
-   "Tell me key points from Annihilation of Caste."

The answers will be based on the PDF content.

------------------------------------------------------------------------

## 🐛 Troubleshooting

### FAISS Import Error:

``` bash
pip install faiss-cpu
```

### Llama model not loading:

Ensure this file exists:

    llama-2-7b-chat.ggmlv3.q4_0.bin

### streamlit_chat missing:

``` bash
pip install streamlit-chat
```

------------------------------------------------------------------------

