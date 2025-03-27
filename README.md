# Retrieval-Augmented Generation (RAG) System with LlamaIndex

This project demonstrates building a Retrieval-Augmented Generation (RAG) system using the LlamaIndex library. The system efficiently queries and retrieves relevant information from uploaded documents stored in vector embeddings.

## Features

- **Environment Management:** Securely loads environment variables (e.g., OpenAI API key) from a `.env` file.
- **Document Embedding:** Loads textual data from local directories and generates semantic embeddings.
- **Efficient Retrieval:** Retrieves relevant information based on semantic similarity, optimizing response quality through similarity thresholds.
- **Persistent Storage:** Embeddings are persistently stored on disk to speed up subsequent retrieval operations.

## Installation

Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### Initial Setup

Store your OpenAI API key in a `.env` file:
```env
OPEN_API_KEY=your-api-key
```

### Querying

You can ask questions based on the uploaded documents. The system provides clear, relevant responses along with their sources.

Example questions:
- "What is YOLO?"
- "What are Transformers?"

## Technical Overview

- **Libraries Used:** LlamaIndex, dotenv
- **Persistent Storage:** Stores embeddings in `./storage` to avoid recomputation.

## Example Queries

```python
response = query_engine.query("What is YOLO?")
print(response)
```

## Project Structure

```
.
├── data                  # Directory containing source documents
├── storage               # Persistent storage for embeddings
├── test.ipynb            # Jupyter notebook for experiments
├── README.md             # Project documentation
├── requirements.txt      # Dependencies
└── venv                  # Python virtual environment
```

## Contributing

Feel free to contribute improvements or extensions!
