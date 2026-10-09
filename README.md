# Multi-Agent AI Travel Planner

A Streamlit travel planner powered by a LangGraph workflow. The existing backend coordinates flight search, hotel search, itinerary generation, and a final response, with PostgreSQL-backed checkpointing.

## Requirements

- Python 3.10 or newer
- PostgreSQL
- API keys for Groq, AviationStack, and Tavily

## Setup on Windows

From the project directory, create and activate a virtual environment, then install the dependencies:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

Create a PostgreSQL database named `langgraph_memory`, then copy `.env.example` to `.env` and fill in your API keys and PostgreSQL connection URL. Never commit `.env`.

Start the application:

```powershell
streamlit run frontend.py
```

Open the local URL printed by Streamlit, usually <http://localhost:8501>.

## Configuration

The application reads these variables from `.env`:

- `GROQ_API_KEY`
- `AVIATIONSTACK_API_KEY`
- `TAVILY_API_KEY`
- `DATABASE_URL`
