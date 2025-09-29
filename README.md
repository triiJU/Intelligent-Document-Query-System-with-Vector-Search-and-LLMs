Intelligent Document Query System with Vector Search and LLMs

A Streamlit-based application that lets you upload or index documents, convert them into embeddings, and ask natural-language questions whose answers are grounded in the original sources. Combines OCR for scanned PDFs with semantic vector search and large language models (LLMs).

## Features

* Multi-format document ingestion (PDF, extendable to DOCX/TXT)
* OCR support for scanned PDFs via Tesseract + Poppler
* Text chunking and embedding generation for semantic search
* Retrieval-Augmented Generation (RAG) for context-aware answers
* Streamlit Web UI for document upload, question answering, and viewing retrieved content

## Setup

1. Clone the repository:

```bash
git clone https://github.com/triiJU/Intelligent-Document-Query-System-with-Vector-Search-and-LLMs.git
cd Intelligent-Document-Query-System-with-Vector-Search-and-LLMs
```

2. Create and activate a Python virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate        # Linux/macOS
.venv\Scripts\activate           # Windows
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Install external binaries:

* **Poppler** (PDF extraction)
* **Tesseract OCR** ([https://tesseract-ocr.github.io/](https://tesseract-ocr.github.io/))
* Add binaries to your system PATH

5. Set environment variables (for LLM or embedding providers) in `.env`:

```
OPENAI_API_KEY=your_api_key
HUGGINGFACEHUB_API_TOKEN=your_api_token
EMBEDDING_MODEL=text-embedding-3-small
LLM_MODEL=gpt-4o-mini
```

## Usage

**Web UI:**

```bash
streamlit run main.py
```

**CLI:**

1. Place your PDF in the desired location
2. Edit `main.py` to point to your PDF
3. Run:

```bash
python main.py
```

## References

* OpenAI / HuggingFace Transformers
* Tesseract OCR
* Streamlit
* ChromaDB
