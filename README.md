# News Research Tool 📈

A Streamlit-based application that allows users to analyze and retrieve information from news articles. This tool utilizes LangChain for building a question-answering system based on user-provided URLs.

---

## Features
- Extracts content from up to 3 user-provided URLs.
- Splits the extracted data into manageable chunks for analysis.
- Builds a FAISS vector store with OpenAI embeddings for efficient retrieval.
- Provides answers to user queries, along with relevant sources.

---

## Prerequisites
- Python 3.8 or higher.
- An OpenAI API key (stored in a `.env` file).
- Required Python packages (listed in `requirements.txt`).

---

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd stock_market_prediction
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   # On Windows:
   .\venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Add your OpenAI API key to a `.env` file:
   ```env
   OPENAI_API_KEY=your_api_key_here
   ```

---

## Usage

1. Run the application:
   ```bash
   streamlit run app.py
   ```

2. Open the Streamlit app in your browser (usually at `http://localhost:8501`).

3. Provide up to 3 URLs in the sidebar and click **"Process URLs"**.

4. Enter a question in the input field and receive the answer along with sources.

---

## File Structure
```
project_root/
├── app.py                # Main Streamlit application
├── requirements.txt      # List of dependencies
├── .env                  # Environment variables (e.g., API keys)
├── venv/                 # Virtual environment folder (not included in repo)
└── README.md             # Project documentation
```

---

## Dependencies
- `streamlit`: For building the web app interface.
- `langchain`: For question-answering and document processing.
- `faiss-cpu`: For vector search and storage.
- `python-dotenv`: For managing environment variables.

---

## Troubleshooting

1. **Virtual Environment Issues:**
   - If you cannot activate the virtual environment on Windows, ensure that PowerShell's execution policy is set to `RemoteSigned`:
     ```powershell
     Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
     ```

2. ModuleNotFoundError:
   - Ensure all dependencies are installed:
     ```bash
     pip install -r requirements.txt
     ```

3. Streamlit Errors:
   - Ensure the `streamlit` command is available. If not, reinstall it:
     ```bash
     pip install streamlit
     ```

---

## Future Enhancements
- Add support for more than 3 URLs.
- Improve error handling and user feedback for failed URL processing.
- Integrate additional embedding models.

---

## License
This project is licensed under the MIT License. See `LICENSE` for more details.

---

## Contributors
- [Venkata Vasista] 

Feel free to suggest or contribute improvements!

