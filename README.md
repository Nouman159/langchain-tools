# Semantic Researcher PDF

A comprehensive project demonstrating advanced AI-powered document analysis and structured output generation using LangChain, Google Gemini, and various machine learning techniques.

## 📋 Project Overview

This project showcases three main capabilities:

1. **Semantic PDF Retrieval** - Extract and search through PDF documents using semantic embeddings
2. **Structured Output Generation** - Generate structured responses from LLMs using various schema formats
3. **AI Tool Integration** - Implement and use custom tools with Large Language Models

## 🗂️ Project Structure

```
semantic-researcher-pdf/
├── research.pdf                 # Sample PDF document for testing
├── semantic-retrieval.ipynb     # PDF processing and semantic search
├── structured-output.ipynb      # Structured LLM responses
├── tools.ipynb                  # LLM tool calling examples
├── requirements.txt             # Python dependencies
├── venv/                        # Python virtual environment
└── README.md                    # This file
```

## 🚀 Features

### 1. Semantic PDF Retrieval (`semantic-retrieval.ipynb`)
- **PDF Document Loading**: Load and parse PDF files using PyPDFLoader
- **Text Chunking**: Split large documents into manageable chunks
- **Semantic Embeddings**: Generate vector embeddings using Google Gemini
- **Vector Storage**: Store embeddings in an in-memory vector database
- **Similarity Search**: Find relevant content based on semantic similarity
- **Batch Processing**: Process multiple queries efficiently

### 2. Structured Output Generation (`structured-output.ipynb`)
- **Pydantic Models**: Define structured schemas for LLM responses
- **TypedDict Support**: Alternative schema definition method
- **JSON Schema**: Direct JSON schema integration
- **Few-Shot Prompting**: Improve output quality with examples
- **Custom Parsing**: Extract structured data from raw LLM responses
- **Streaming Support**: Real-time structured output generation

### 3. AI Tool Integration (`tools.ipynb`)
- **Tool Definition**: Create custom tools using Pydantic and TypedDict
- **Tool Binding**: Integrate tools with language models
- **Function Calling**: Enable LLMs to call external functions
- **Result Parsing**: Process and validate tool execution results

## 🛠️ Prerequisites

- Python 3.8 or higher
- Google API key for Gemini models
- LangSmith API key (optional, for tracing)

## 📦 Installation

### 1. Clone the Repository
```bash
git clone <repository-url>
cd semantic-researcher-pdf
```

### 2. Set Up Virtual Environment
```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Linux/Mac:
source venv/bin/activate
# On Windows:
venv\Scripts\activate
```

### 3. Install Dependencies
```bash
# Install all dependencies from requirements.txt
pip install -r requirements.txt

# Or install manually:
# pip install langchain langchain-community langchain-google-genai
# pip install langchain-core langchain-text-splitters
# pip install pypdf pydantic typing-extensions
# pip install jupyter notebook
```

### 4. Obtain API Keys

#### Google Gemini API Key:
1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create a new API key
3. Keep it secure for use in notebooks

#### LangSmith API Key (Optional):
1. Visit [LangSmith](https://smith.langchain.com/)
2. Create an account and generate an API key
3. Used for advanced tracing and monitoring

## 🚦 How to Run

### 1. Start Jupyter Notebook
```bash
jupyter notebook
```

### 2. Run Individual Notebooks

#### A. Semantic PDF Retrieval
1. Open `semantic-retrieval.ipynb`
2. Run the first cell and enter your LangSmith API key (optional)
3. Run the Google API setup cell and enter your Gemini API key
4. Execute all cells to see PDF processing and semantic search in action

**What it demonstrates:**
- Loading a 110-page React.js PDF document
- Creating 768-dimensional embeddings
- Performing similarity searches for questions like:
  - "What are benefits of React.js?"
  - "How react components communicate?"
  - "How to setup webpack in React?"

#### B. Structured Output Generation
1. Open `structured-output.ipynb`
2. Enter your Google Gemini API key when prompted
3. Run cells progressively to see different structured output examples

**What it demonstrates:**
- Generating jokes with structured format (setup, punchline, rating)
- Using different schema formats (Pydantic, TypedDict, JSON)
- Creating conversational vs. structured responses
- Few-shot prompting for better results
- Custom JSON parsing from LLM responses

#### C. AI Tool Integration
1. Open `tools.ipynb`
2. Enter your Google Gemini API key
3. Execute cells to see tool calling functionality

**What it demonstrates:**
- Defining mathematical tools (add, multiply)
- Binding tools to language models
- Automatic tool selection and execution
- Parsing tool call results

## 🔧 Configuration

### Environment Variables (Optional)
```bash
export GOOGLE_API_KEY="your-gemini-api-key"
export LANGSMITH_API_KEY="your-langsmith-api-key"
export LANGSMITH_TRACING="true"
```

### PDF Document
The project includes a sample `research.pdf` (React.js documentation). You can replace it with any PDF document for testing.

## 💡 Use Cases

### For Developers
- **Document Analysis**: Build applications that can understand and search through large documents
- **Structured APIs**: Create LLM-powered APIs that return consistent, structured data
- **AI Tool Integration**: Enhance applications with AI-powered function calling

### For Researchers
- **Academic Paper Analysis**: Extract specific information from research papers
- **Literature Review**: Find relevant sections across multiple documents
- **Data Extraction**: Convert unstructured text into structured datasets

### For Business Applications
- **Document Q&A Systems**: Build internal knowledge bases
- **Report Generation**: Create structured reports from unstructured data
- **Process Automation**: Use AI tools to automate complex workflows

## 🔍 Technical Details

### Vector Embeddings
- **Model**: Google's `models/embedding-001`
- **Dimensions**: 768
- **Storage**: In-memory vector store (suitable for prototyping)

### Text Processing
- **Chunk Size**: 1000 characters
- **Overlap**: 200 characters
- **Splitter**: RecursiveCharacterTextSplitter

### Language Model
- **Provider**: Google Gemini
- **Model**: `gemini-2.0-flash`
- **Capabilities**: Text generation, structured output, tool calling

## 🚨 Troubleshooting

### Common Issues

1. **API Key Errors**
   - Ensure your Google Gemini API key is valid
   - Check API quotas and billing settings

2. **PDF Loading Issues**
   - Verify the PDF file exists and is readable
   - Some PDFs may require different loaders

3. **Memory Issues**
   - Large PDFs may consume significant memory
   - Consider using persistent vector stores for production

4. **Import Errors**
   - Ensure all dependencies are installed
   - Activate your virtual environment

### Getting Help
- Check the LangChain documentation: https://python.langchain.com/
- Google Gemini API docs: https://ai.google.dev/
- Open an issue in the repository for specific problems

## 📈 Next Steps

### Enhancements
- **Persistent Storage**: Implement Chroma or Pinecone for vector storage
- **Multi-Document Support**: Process multiple PDFs simultaneously
- **Advanced Retrieval**: Implement hybrid search (semantic + keyword)
- **Web Interface**: Create a Streamlit or Gradio frontend
- **API Deployment**: Deploy as a REST API using FastAPI

### Performance Optimization
- **Batch Processing**: Process multiple documents in parallel
- **Caching**: Implement embedding caching for faster responses
- **Async Operations**: Use async/await for better performance

## 📄 License

This project is for educational purposes. Please ensure compliance with the terms of service for Google Gemini API and any PDF documents you process.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

---

**Happy Learning!** 🎉

This project demonstrates the power of modern AI tools for document analysis and structured data generation. Experiment with different PDFs, modify the schemas, and explore the possibilities! 