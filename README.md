# RAG Q&A System

A production-ready Retrieval-Augmented Generation (RAG) system built with FastAPI, LangChain, and Qdrant.

## Features

- **Document Processing**: Upload and process PDF, TXT, and CSV files
- **Semantic Search**: Vector-based document retrieval using Qdrant
- **AI-Powered Q&A**: GPT-4o-mini for intelligent answers
- **Streaming Responses**: Real-time answer generation
- **RAGAS Evaluation**: Quality assessment for RAG responses
- **LangSmith Tracing**: Monitoring and debugging support

## Quick Start

```bash
# Install dependencies
uv pip install -r requirements.txt

# Set environment variables
cp .env.example .env  # Configure your API keys

# Run locally
uvicorn app.main:app --reload
```

## API Endpoints

- `POST /query` - Ask questions with RAG
- `POST /query/stream` - Streaming responses
- `POST /documents/upload` - Upload documents
- `GET /health` - Health check

## Deployment

Automated CI/CD pipeline deploys to AWS App Runner on push to `features` branch.

## Tech Stack

- **Framework**: FastAPI
- **LLM**: OpenAI GPT-4o-mini
- **Vector DB**: Qdrant Cloud
- **Orchestration**: LangChain
- **Evaluation**: RAGAS
- **Monitoring**: LangSmith
