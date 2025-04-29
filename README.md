# Document QA ChatBot

A Flask-based web application that allows users to upload documents (PDF, Word, Excel) and ask questions about their content. The application leverages Large Language Models (LLMs) from Google Gemini and Groq to provide intelligent responses based on document content.

![Document Upload Interface](https://github.com/AdarshXKumAR/Document-AI-ChatBot/blob/main/demo1.png)

![Question Answering Interface](https://github.com/AdarshXKumAR/Document-AI-ChatBot/blob/main/demo2.png)

## Features

- **Document Upload**: Support for PDF, Word (.docx), and Excel (.xlsx/.xls) files
- **Multiple LLM Support**: Choose between Google Gemini and Groq for responses
- **Vector Embeddings**: Uses HuggingFace embeddings for efficient document indexing
- **Interactive UI**: User-friendly interface with drag-and-drop functionality
- **Responsive Design**: Works well on both desktop and mobile devices

## Technologies Used

- **Backend**: Flask (Python)
- **Frontend**: HTML, JavaScript, Tailwind CSS
- **Document Processing**:
  - PyPDF for PDF processing
  - python-docx for Word documents
  - pandas for Excel files
- **AI/ML**:
  - Google Generative AI (Gemini)
  - Groq API (Mixtral model)
  - LlamaIndex for document indexing
  - HuggingFace embeddings

## Setup Instructions

### Prerequisites

- Python 3.8+
- API keys for Google Gemini and Groq

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/username/document-qa-chatbot.git
   cd document-qa-chatbot
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env.local` file in the project root with your API keys:
   ```
   GEMINI_API_KEY=your_gemini_api_key_here
   GROQ_API_KEY=your_groq_api_key_here
   ```

### Running the Application

1. Start the Flask server:
   ```bash
   python app.py
   ```

2. Open your browser and navigate to:
   ```
   http://127.0.0.1:5000
   ```

## Usage

1. **Upload a Document**: 
   - Click the upload area or drag and drop a supported file (PDF, Word, Excel)
   - Wait for the document to be processed and indexed

2. **Ask Questions**:
   - Select your preferred LLM (Gemini or Groq)
   - Type your question in the text area
   - Click "Ask Question" and wait for the response

## Project Structure

```
document-qa-chatbot/
├── app.py              # Main Flask application
├── templates/
│   └── index.html      # Frontend HTML template
├── uploads/            # Directory for uploaded files (created automatically)
├── requirements.txt    # Python dependencies
└── .env.local          # Environment variables (API keys)
```

## Requirements

See `requirements.txt` for the full list of dependencies. Main packages include:

```
flask
werkzeug
python-dotenv
google-generativeai
groq
llama-index
sentence-transformers
pypdf
python-docx
pandas
openpyxl
```

## Limitations

- Maximum file size is limited to 16MB
- Processing large documents may take time
- Response quality depends on the selected LLM and document content clarity

## Future Improvements

- Add authentication to secure document uploads
- Implement document history for users
- Add support for more file formats (e.g., text, markdown)
- Improve response formatting with markdown support
- Add chat history functionality

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- [Google Generative AI](https://ai.google.dev/)
- [Groq](https://groq.com/)
- [LlamaIndex](https://www.llamaindex.ai/)
- [HuggingFace](https://huggingface.co/)
- [Tailwind CSS](https://tailwindcss.com/)
