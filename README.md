
### Project Structure
The project consists of the following files and directories:
- `.streamlit/config.toml`: Configuration file for Streamlit settings, including server settings and theme customization.
- `README.md`: A brief description of the project.
- `app.py`: The main application script containing the core logic and functionalities.
- `requirements.txt`: A list of dependencies required to run the application.

### Configuration (`.streamlit/config.toml`)
- Sets the maximum upload size for files to 400 MB.
- Customizes the theme with specific colors for primary, background, secondary background, and text.

### Main Application Script (`app.py`)
The script is divided into several classes and functions, each responsible for different aspects of the application:

#### Config Class
- Defines configuration parameters such as chunk size, chunk overlap, temperature, model name, embedding model, and vector store path.

#### PDFProcessor Class
- Contains methods to extract text from PDF documents and split the text into manageable chunks.

#### VectorStore Class
- Manages the creation, saving, and loading of a vector store using text chunks and embeddings.

#### CivilEngineerChain Class
- Defines a custom prompt template for the AI model, outlining the expertise areas and responsibilities of the AI Civil Engineering Assistant.
- Creates a question-answering (QA) chain using the specified model and prompt template.

#### StreamlitUI Class
- Manages the Streamlit user interface, including page setup, sidebar configuration, document processing, chat history management, and user input handling.
- Provides methods to process uploaded PDF documents, clear chat history, and generate responses to user questions.

#### Main Function
- Loads environment variables, configures the Google Generative AI API, and initializes and runs the Streamlit application.

### Dependencies (`requirements.txt`)
The application requires the following Python packages:
- `streamlit`: For building the web application interface.
- `google-generativeai`: For interacting with Google's generative AI models.
- `python-dotenv`: For loading environment variables from a `.env` file.
- `langchain`: For managing language models and text processing.
- `PyPDF2`: For extracting text from PDF documents.
- `chromadb`: For managing vector databases.
- `faiss-cpu`: For efficient similarity search and clustering of dense vectors.
- `langchain_google_genai`: For integrating LangChain with Google Generative AI.

### Summary
The "AI Civil Engineer" Streamlit application is designed to assist civil engineers by providing detailed technical analysis and answers to engineering-related questions. Users can upload project documents in PDF format, which are then processed to extract text and create text chunks. These chunks are stored in a vector store, enabling efficient similarity search. The application uses a custom prompt template to generate responses based on the context and questions provided by the user. The user interface allows for document uploads, question input, and chat history management, making it a comprehensive tool for civil engineering assistance.,
Mahantesh Hiremath: improve README.md,
Navigator: Based on the retrieved document, here is an improved version of the `README.md` file for the AI Civil Engineer Streamlit app:


# AI_CIVIL_ENG
AI Civil Engineer

## Overview
AI Civil Engineer is a Streamlit application designed to assist civil engineers by leveraging AI to analyze and answer engineering-related questions based on uploaded project documents. This tool aims to provide detailed technical analysis and support for various civil engineering domains.

## Features
- **PDF Document Processing**: Upload and process multiple PDF documents to extract and analyze text.
- **Text Chunking**: Split extracted text into manageable chunks for efficient processing.
- **Vector Store Management**: Create, save, and load vector stores for similarity search.
- **Custom QA Chain**: Generate responses to engineering questions using a custom prompt template and AI model.
- **User Interface**: Intuitive Streamlit interface for document upload, question input, and chat history management.

## Project Structure

├── .streamlit
│   └── config.toml
├── README.md
├── app.py
└── requirements.txt
```

## Configuration
### `.streamlit/config.toml`
```toml
[server]
maxUploadSize = 400

[theme]
primaryColor = "#cebde0"
backgroundColor = "#2f1f42"
secondaryBackgroundColor = "#220e06"
textColor = "#c7e5b0"
```

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/AI_CIVIL_ENG.git
   cd AI_CIVIL_ENG
   ```

2. Create a virtual environment and activate it:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install the required dependencies:
   ```sh
   pip install -r requirements.txt
   ```

4. Set up environment variables:
   - Create a `.env` file in the project root directory.
   - Add your Google API key:
     ```env
     GOOGLE_API_KEY=your_google_api_key
     ```

## Usage
1. Run the Streamlit application:
   ```sh
   streamlit run app.py
   ```

2. Open your web browser and navigate to the provided URL (usually `http://localhost:8501`).

3. Upload your project documents (PDF) using the sidebar.

4. Ask your engineering-related questions in the chat input box.

## Dependencies
- `streamlit`
- `google-generativeai`
- `python-dotenv`
- `langchain`
- `PyPDF2`
- `chromadb`
- `faiss-cpu`
- `langchain_google_genai`

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Acknowledgements
Special thanks to the developers and contributors of the libraries and tools used in this project.

```

This improved `README.md` provides a comprehensive overview of the project, including its features, installation instructions, usage guidelines, and more.
