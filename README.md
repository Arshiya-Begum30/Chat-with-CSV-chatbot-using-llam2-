# Chat-with-CSV-chatbot-using-llam2-

# Chat with CSV using Llama2 🦙

This repository contains a Streamlit web application that allows you to chat with your CSV data using the Llama2 model. The application leverages LangChain, FAISS, and HuggingFace embeddings to provide a conversational interface for querying CSV data.

## Features

- Upload a CSV file and interact with its contents through a chat interface.
- Uses Llama2 model for generating responses.
- Employs HuggingFace embeddings and FAISS for efficient retrieval of relevant data.
- Maintains chat history for contextual conversations.

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/chat-with-csv.git
    cd chat-with-csv
    ```

2. **Create a virtual environment and activate it:**

    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3. **Install the required dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Run the Streamlit application:**

    ```bash
    streamlit run app.py
    ```

2. **Upload your CSV file:**
    - Use the file uploader in the sidebar to upload your CSV file.

3. **Chat with your CSV data:**
    - Enter your queries in the provided text input and get responses based on the contents of your uploaded CSV.

## Project Structure

- `app.py`: Main application file containing the Streamlit app code.
- `requirements.txt`: Contains the list of Python dependencies required for the project.
- `vectorstore/`: Directory to store the FAISS vector database.

## Code Overview

### Load the LLM

The `load_llm` function loads the locally downloaded Llama2 model with specified parameters.

### Streamlit Application

- **File Upload:**
    - Users can upload a CSV file which is then processed and loaded using `CSVLoader`.

- **Embeddings and FAISS:**
    - The uploaded data is converted to embeddings using HuggingFace's `sentence-transformers/all-MiniLM-L6-v2`.
    - FAISS is used to create a vector store from the embeddings for efficient retrieval.

- **Conversational Retrieval Chain:**
    - The Llama2 model and FAISS retriever are used to create a conversational retrieval chain.
    - User queries are processed, and responses are generated based on the CSV data.

### Chat Interface

- The chat interface maintains a session state to store chat history.
- Users can enter queries and receive responses in a conversational format.

## Dependencies

- streamlit
- streamlit_chat
- langchain
- faiss-cpu
- sentence-transformers

Ensure all dependencies are installed by running:

```bash
pip install -r requirements.txt
```

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.

---

Feel free to reach out with any questions or suggestions. Happy chatting! 🦙

