# data-extraction-automation

Web scraping pipelines combined with LLM-powered extraction to turn unstructured web content into clean, structured data.

## What this covers

- **Scrapers** — Site-specific scraping modules using BeautifulSoup and Playwright
- **LLM extraction** — Structured data extraction via OpenAI function calling and Pydantic schemas
- **Transformers** — Data cleaning, normalization, and deduplication
- **Storage** — Output to JSON, CSV, SQLite, and PostgreSQL

## Stack

- Python 3.10+
- BeautifulSoup, Playwright, Scrapy
- LangChain (for LLM extraction pipelines)
- Pydantic, pandas
- pytest, ruff

## Structure

```
scrapers/        # Web scraping modules (one per source)
extractors/      # LLM-powered extraction pipelines
schemas/         # Pydantic models for expected output shapes
transformers/    # Data cleaning and transformation
storage/         # Output adapters (file, database, API)
tests/           # Fixtures with sample HTML/data
examples/        # Usage examples
```

## Setup

```bash
pip install -e .
cp .env.example .env
pytest
```

## License

MIT
