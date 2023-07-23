# PDF_chatbot - a Multi-PDF Chat App 

This is a Python application that allows you to chat with multiple PDF documents using natural language. It utilizes OpenAI's API and Facebook's Faiss library for semantic search to provide accurate responses based on the content of the loaded PDFs.

## How it Works

The app follows these key steps:

1. PDF Loading: The user can load multiple PDFs into the application.

2. Text Extraction: The text content is extracted from the PDFs. 

3. Embedding Generation: Vector embeddings are generated for the extracted text chunks using OpenAI's text embedding API.

4. Indexing: The text embeddings are indexed using Faiss for efficient similarity search.

5. User Input: The user provides a natural language query via the chat interface.

6. Embedding Lookup: The user query is converted to an embedding vector and compared against the indexed PDF embeddings. 

7. Response Generation: The most similar PDF text chunks are retrieved and used to generate a response with OpenAI's text generation API.

## Installation

It's recommended to run this app in a Python 3.8 virtual environment. 

Clone the repository to your local machine.

```git clone https://github.com/corymullins/PDF_chatbot.git```

Create and activate a virtual environment:

```
python3 -m venv pdfbot
source pdfbot/bin/activate
```

Install requirements:

```pip install -r requirements.txt```

## Usage

1. Obtain an API key for OpenAI, add it to `.env` 

2. Run `streamlit run .\app.py`

3. Load PDFs using the upload button. 

4. Chat with the bot in natural language about the PDF contents.
