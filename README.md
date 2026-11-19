# Telecom Customer Support RAG API

A Retrieval-Augmented Generation (RAG) API built with Python and FastAPI to generate responses to telecom customer support tickets using internal knowledge documents.

## Features

- Upload and index TXT, MD, and CSV documents.
- Split documents into chunks and generate embeddings.
- Store and retrieve document embeddings using FAISS.
- Generate context-aware responses using Google Gemini.
- Track token usage and query execution time.
- Cache models and the FAISS index to reduce repeated loading operations.

## Technologies

- Python
- FastAPI
- LangChain
- Google Gemini
- Hugging Face Embeddings
- FAISS
- Docker

## API Workflow

1. Upload knowledge documents through `/api/v1/ingest`.
2. Split documents into chunks and generate embeddings.
3. Store the embeddings in the FAISS vector database.
4. Submit customer support tickets through `/api/v1/query`.
5. Retrieve relevant context and generate a response using Gemini.

## Project Structure

- `config/` – Application configuration.
- `core/` – AI model initialization and caching.
- `models/` – Request and response schemas.
- `routers/` – API endpoints.
- `services/` – Document ingestion and RAG logic.
- `vectorstore/` – FAISS database management.
- `logger/` – Application logging.
- `test/` – Tests.
