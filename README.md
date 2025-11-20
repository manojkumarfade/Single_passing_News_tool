# Single_passing_News_tool
# One-Shot News Agent using LangChain + Gemini 2.5 Flash (Colab)

This project is a minimal, clean implementation of a **single-step tool-calling agent** built using:

- **LangChain 0.2+**
- **Gemini 2.5 Flash**
- **Google Colab**
- **News API (or any custom news source)**

The agent answers **only news-related questions** by calling one tool called `news_fetcher`.  
No loops.  
No multi-step agent executor.  
Just one LLM call → one tool call → direct response.

---

## 🚀 Features

- One-shot tool execution (no agent loops)
- Uses LangChain’s new `bind_tools()` API
- News fetched dynamically from NewsAPI
- Works fully inside Google Colab
- Clean tool structure using `@tool` decorator
- Easy to extend to multiple tools or different APIs

---

## 📁 Project Structure
.
├── news_agent.ipynb # Google Colab notebook
├── README.md # Documentation


---

## 🛠️ Setup

### 1. Install Dependencies
!pip install -qU langchain langchain-google-genai requests

## How it works?

1. You ask a question.
2. Gemini decides whether to call the news tool.
3. If yes, it sends structured arguments.
4. The tool fetches news via NewsAPI.
5. You run the tool output and get final headlines.

### 📈 Future Improvements

Feel free to extend this project with:

Multi-source news (Google News RSS, DuckDuckGo, Bing)

Automatic tool execution (no manual run())

Summaries using Gemini

A Streamlit dashboard

Topic auto-classification

Chat-style conversational history
