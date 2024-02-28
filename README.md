# Semantic Search with MongoDB and LLM Frameworks

## Introduction

This Python project demonstrates semantic search using MongoDB and two different LLM frameworks: **LangChain** and **LlamaIndex**. The goal is to load documents from MongoDB, generate embeddings for the text data, and perform semantic searches using both **LangChain** and **LlamaIndex** frameworks.

## Environment Variables

To run this project, you need to set the following environment variables in a `.env` file:

```dotenv
OPENAI_API_KEY=YOUR_OPENAI_API_KEY
MONGODB_URI=YOUR_MONGODB_CONNECTION_URI
MONGODB_COLL=YOUR_MONGODB_COLLECTION
MONGODB_VECTOR_INDEX=YOUR_MONGODB_VECTOR_INDEX
MONGODB_VECTOR_COLL_LANGCHAIN=YOUR_MONGODB_VECTOR_COLLECTION_LANGCHAIN
MONGODB_VECTOR_COLL_LLAMAINDEX=YOUR_MONGODB_VECTOR_COLLECTION_LLAMAINDEX
```

Make sure to replace the placeholder values with your actual API keys and connection details.

## Setup

Install dependencies:

```
pip install -r requirements.txt
```

## Project Overview
### 1. Loading Documents

The project loads documents from the specified MongoDB collection (`MONGODB_COLL`). Ensure that your MongoDB collection contains the text data you want to perform a semantic search on.

### 2. Generating Embeddings
The application generates embeddings for the loaded text data using the LangChain and LlamaIndex frameworks. The embeddings are stored in separate MongoDB collections (`MONGODB_VECTOR_COLL_LANGCHAIN` and `MONGODB_VECTOR_COLL_LLAMAINDEX`).

### 3. Semantic Search
The semantic search is performed using both LangChain and LlamaIndex frameworks. The process involves querying the embeddings collection and retrieving relevant documents based on the semantic similarity of the prompt.

## Additional Information
The `OPENAI_API_KEY` is required for embedding generation using external language models (e.g., OpenAI's GPT).
Make sure to configure MongoDB connection details and collections appropriately.
Check the official documentation for LangChain and LlamaIndex for any additional configuration or usage details.

## Reference
- Atlas Vector Search : [Link to MongoDB Atlas Vector Search](https://www.mongodb.com/products/platform/atlas-vector-search)
- LangChain: [Link to LangChain Documentation](https://python.langchain.com/docs/get_started/introduction)
- LlamaIndex: [Link to LlamaIndex Documentation](https://docs.llamaindex.ai/en/stable/)
