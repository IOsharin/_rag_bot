pip freeze > requirements.txt
# RAG Chatbot (Russian)

## Описание
Этот проект демонстрирует консольный чат-бот на русском языке, основанный на Retrieval-Augmented Generation (RAG) подходе. Бот отвечает на вопросы пользователя, используя базу данных (ChromaDB) и при необходимости обращаясь к DuckDuckGo для поиска в интернете.

## Технологии
- Python 3.9+
- [ChromaDB](https://github.com/chroma-core/chroma)
- [LangGraph](https://pypi.org/project/langgraph/) и LangChain Core
- [DuckDuckGo Search](https://pypi.org/project/duckduckgo-search/)
- [Sentence Transformers](https://www.sbert.net/)
- Локально развернутая LLaMA (через OpenAI-совместимый API)

## Структура проекта
- `src/data_ingestion/`: скрипты для индексирования данных RuBQ в ChromaDB
  - `ingest_rubq.py` и т. д.
- `src/llm_service/`: тестирование локальной LLM
  - `test_local_llm.py`
- `basic_ver_chatbot.py`, `rag_chatbot_langgraph.py`, `rag_chatbot.py`: различные варианты бота
  - **basic_ver_chatbot.py** — простой RAG-бот
  - **rag_chatbot.py** — консольный RAG-бот с историей диалога
  - **rag_chatbot_langgraph.py** — вариант с использованием LangGraph
- `requirements.txt`: зависимости проекта

## Установка
1. Склонируйте репозиторий:
   ```bash
   git clone https://github.com/IOsharin/_rag_bot
   cd _rag_bot