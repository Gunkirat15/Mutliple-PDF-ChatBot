# 📚 Chat with Multiple PDFs

This project is a Streamlit-based application that allows users to upload multiple PDF files and interact with the content by asking questions. The app uses **LangChain**, **OpenAI Embeddings**, and **FAISS** to retrieve answers based on the content of the uploaded PDFs.

## Features

- Upload multiple PDF documents and extract text for interactive queries.
- Split large text documents into manageable chunks for efficient processing.
- Utilize **OpenAI Embeddings** for semantic search across document content.
- Conversational interaction powered by **ChatOpenAI** and **FAISS**.
- Memory retention for ongoing conversation context.

## Tech Stack

- **Python**
- **Streamlit** for UI and handling user inputs.
- **PyPDF2** for extracting text from PDFs.
- **LangChain** for text processing and conversational AI.
- **FAISS** for vector-based document retrieval.
- **OpenAI Embeddings** for text vectorization.
- **Dotenv** for loading environment variables.

## Installation

1. Clone this repository:

    ```bash
    git clone https://github.com/yourusername/multi-pdf-chat.git
    cd multi-pdf-chat
    ```

2. Install the dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Create a `.env` file and add your OpenAI API key:

    ```bash
    OPENAI_API_KEY=your_openai_api_key
    ```

4. Run the Streamlit app:

    ```bash
    streamlit run app.py
    ```

## How It Works

1. **Upload PDFs**: Users can upload multiple PDF files via the sidebar.
2. **Text Extraction**: The app uses `PyPDF2` to extract text from the PDFs.
3. **Text Chunking**: The extracted text is split into chunks using `CharacterTextSplitter` for better processing.
4. **Vector Store**: The text chunks are embedded using `OpenAIEmbeddings` and stored in a FAISS vector store for fast retrieval.
5. **Conversational Chain**: A conversational retrieval chain is established, allowing users to ask questions, with responses based on the uploaded documents.

## Usage

1. Upload PDF files from the sidebar.
2. Ask questions related to the content of the PDFs.
3. Receive responses based on the documents using the conversational retrieval chain.

## SEE IT IN ACTION -> https://mutliple-pdfs-chatbot.streamlit.app

## Folder Structure

```bash
📦multi-pdf-chat
 ┣ 📂htmlTemplates
 ┃ ┣ 📜bot_template.html
 ┃ ┣ 📜css.html
 ┃ ┗ 📜user_template.html
 ┣ 📜app.py
 ┣ 📜requirements.txt
 ┗ 📜README.md
