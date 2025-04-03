# RAG-ChatBot

RAG-ChatBot is a Retrieval-Augmented Generation (RAG) system that combines document ingestion, vector-based retrieval, and large language models (LLMs) to provide intelligent responses based on ingested documents. The system supports multiple LLM providers, including OpenAI, Anthropic, and Google Gemini, and allows users to query the system through a React-based frontend.

## Features

- **Document Ingestion**: Supports ingestion of various file formats, including PDFs, DOCX, CSVs, images, and videos.
- **Vector-Based Retrieval**: Uses FAISS for efficient similarity search on document embeddings.
- **LLM Integration**: Supports multiple LLM providers (OpenAI, Anthropic, Google Gemini, and custom APIs).
- **React Frontend**: Interactive chat interface with settings and source display.
- **REST API**: Exposes endpoints for querying, ingestion, and system status.

## Project Structure

```
.
├── .gitignore
├── README.md
├── requirements.txt
├── test.py
├── data/
│   ├── csv/
│   ├── docx/
│   ├── images/
│   └── pdfs/
├── frontend/
│   ├── package.json
│   ├── public/
│   └── src/
└── src/
    ├── __init__.py
    ├── api.py
    ├── document_processor.py
    ├── embeddings.py
    ├── gemini_interface.py
    ├── llm_interface.py
    ├── main_application.py
    ├── rag_system.py
    ├── text_processor.py
    └── vector_store.py
```

## Installation

### Backend

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/RAG-ChatBot.git
   cd RAG-ChatBot
   ```

2. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up environment variables:
   - `OPENAI_API_KEY`: Your OpenAI API key.
   - `ANTHROPIC_API_KEY`: Your Anthropic API key.
   - `GEMINI_API_KEY`: Your Google Gemini API key.

4. Run the backend server:
   ```bash
   python src/api.py
   ```

### Frontend

1. Navigate to the `frontend` directory:
   ```bash
   cd frontend
   ```

2. Install Node.js dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

   The frontend will be available at [http://localhost:3000](http://localhost:3000).

## Usage

### Document Ingestion

1. Enter a file or directory path in the "Ingest Documents" panel on the frontend.
2. Click the "Ingest" button to process and store the documents in the vector store.

### Querying

1. Type a question in the input box on the frontend.
2. Click "Send" to query the system. The response will be displayed in the chat interface.

### Settings

1. Click the "Settings" button in the header to configure:
   - LLM provider (OpenAI, Anthropic, Gemini, or custom API).
   - API key and model name.
   - Whether to include sources in responses.

### API Endpoints

- **Query**: `/api/query` (POST)
- **Ingest**: `/api/ingest` (POST)
- **System Status**: `/api/status` (GET)

## Supported File Formats

- **Text Documents**: PDF, DOCX, CSV
- **Images**: JPG, PNG, BMP, TIFF
- **Videos**: MP4, AVI, MKV, etc.

## Technologies Used

- **Backend**: Python, Flask, FAISS, Sentence Transformers
- **Frontend**: React, Create React App
- **LLM Providers**: OpenAI, Anthropic, Google Gemini
- **Vector Search**: FAISS

## Contributing

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add feature-name"
   ```
4. Push to your branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.