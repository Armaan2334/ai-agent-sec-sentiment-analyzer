
# CrewAI SEC + Sentiment Project

## Overview
This project demonstrates how to use **CrewAI** with **LiteLLM** to build a pipeline of agents that:
1. Fetch SEC filings (last 48h)
2. Identify insider trading activity (Form 4)
3. Analyze sentiment of 10 X (Twitter) creators
4. Compile results into a final report

## How to Run
1. Create a virtual environment and install requirements:
   ```bash
   pip install crewai litellm langchain feedparser requests beautifulsoup4
   ```

2. Run the script:
   ```bash
   python crewai_sec_sentiment.py --creators elonmusk naval sundarpichai --max-tweets 5
   ```

3. Outputs will be stored in `outputs/` as JSON files.

## Notes
- Requires an OpenAI (or other LiteLLM-supported) API key set as environment variable.
- Extendable to include YouTube transcripts or RAG notes.

