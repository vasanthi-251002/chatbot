# S-1 Filing Intelligence Engine

AI service for analyzing **US IPO S-1 filings** using retrieval-augmented reasoning.
The system ingests prospectus PDFs, builds a searchable vector index, answers questions from filing content, and generates structured downside risk analysis.

---

## Features

✔ Upload and index S-1 PDFs
✔ Context-grounded Q&A from filing text
✔ Hedge-fund style red-flag risk analysis
✔ FAISS vector search
✔ Structured JSON outputs
✔ Django-based API service

---

## Architecture

```
S-1 PDF
 → Text Extraction
 → Chunking
 → Embeddings
 → FAISS Index
 → Context Retrieval
 → AI Analysis
 → Structured JSON Output
```

---

## Tech Stack

* Django
* FAISS vector search
* SentenceTransformers embeddings
* Perplexity API
* PyMuPDF
* Google Drive storage

---

## Setup

Install dependencies

```
pip install -r requirements.txt
```

Environment variables

```
PERPLEXITY_API_KEY=your_api_key
FAISS_INDEX_DIR=storage/faiss_s1
```

Run server

```
python manage.py migrate
python manage.py runserver
```

---

## API Endpoints

Upload S-1

```
POST /api/s1/upload/
```

Ask question

```
POST /api/s1/ask/
```

Generate red flag analysis

```
POST /api/s1/redflag/generate/
```

Retrieve stored analysis

```
POST /api/s1/redflag/
```

---

## Purpose

Designed for institutional IPO analysis workflows focused on **downside risk identification and structural weaknesses** in prospectus disclosures.

---

## License

Proprietary / Internal Use

---

If you'd like, I can make an **ultra-minimal 10-line README** or a **developer-focused version**.
