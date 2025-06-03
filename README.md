# Context-Aware-Document-Retrieval-and-Generation-System with RAG and MongoDB Atlas

This project demonstrates a pipeline for context-aware document retrieval and response generation using Retrieval-Augmented Generation (RAG).

## Overview

- Extracts and processes PDF documents using `PyMuPDF`.
- Generates embeddings for document chunks using `sentence-transformers`.
- Stores processed data in MongoDB Atlas for efficient retrieval.
- Uses a semantic vector search to match user queries.
- Generates intelligent responses using the open-source **Mistral 7B** model.

## Technologies Used

- `PyMuPDF`, `Pandas` – for PDF parsing and preprocessing.
- `SentenceTransformers` – for text embedding.
- `MongoDB Atlas` – as the vector database.
- `Transformers` & `Mistral` – for response generation.

## How it Works

1. PDF text is extracted and cleaned.
2. Text is embedded and stored in MongoDB with a vector index.
3. A user query is embedded and searched against stored vectors.
4. Top-matching results are retrieved and passed to Mistral 7B for response generation.

## Output

Returns relevant content chunks from the PDF and uses them to answer queries contextually.

## Example Use Cases

- Research document assistants  
- Academic paper summarizers  
- Internal knowledge base querying

## Setup Instructions

Before running the notebook, install the required dependencies:

```bash
pip install datasets pandas pymongo sentence-transformers
pip install -U transformers
pip install accelerate
pip install pymupdf
```
## Important Notes
- Ensure your MongoDB Atlas URI is correctly set up and accessible.

- A vector index (vector_index) must be created in your MongoDB collection on the embedding field.

- This project uses the thenlper/gte-large model from Hugging Face for embeddings.

- Mistral 7B or similar LLMs should be available via transformers or your preferred inference pipeline.


