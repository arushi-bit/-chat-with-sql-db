# Chat with SQL DB

A Streamlit app that lets you chat with a SQL database (SQLite or MySQL) using a LangChain SQL agent powered by Groq's Llama 3.3 70B model.

## Features

- Chat interface to query a database using natural language
- Supports a local SQLite database (`student.db`) or a custom MySQL connection
- Streams the agent's reasoning steps in the UI via `StreamlitCallbackHandler`

## Setup

1. Clone the repo and install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

2. Create a `.env` file in the project root with your Groq API key:

   ```
   GROQ_API_KEY="your-groq-api-key"
   ```

3. (Optional) Generate the sample SQLite database:

   ```bash
   python sqlite.py
   ```

## Usage

Run the Streamlit app:

```bash
streamlit run app.py
```

Then, in the sidebar:

- Choose to use the local SQLite database or connect to your own MySQL database
- Enter your Groq API key
- Start chatting with your database in the main window

## Tech Stack

- [Streamlit](https://streamlit.io/) — UI
- [LangChain](https://www.langchain.com/) — SQL agent & toolkit
- [Groq](https://groq.com/) — LLM inference (`llama-3.3-70b-versatile`)
- SQLite / MySQL — database backends
