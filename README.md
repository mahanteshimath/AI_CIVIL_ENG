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
