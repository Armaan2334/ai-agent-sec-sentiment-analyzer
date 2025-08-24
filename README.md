SEC + Twitter Sentiment Analyzer (CrewAI Project)
📌 Overview

This project fetches recent SEC filings and tweets from market influencers, then performs sentiment analysis using an LLM.
The goal is to understand how insider activities and thought-leaders’ opinions may affect the financial markets.

It combines:

✅ SEC data (insider trading updates)

✅ Twitter creators’ posts

✅ LLM-based sentiment analysis

✅ JSON output for further visualization

Installation & Setup

STEP - 1
Create & Activate Virtual Environment
python3 -m venv .venv
source .venv/bin/activate   # Linux/Mac
.venv\Scripts\activate      # Windows


STEP - 2
Install Dependencies
pip install crewai litellm langchain feedparser requests beautifulsoup4

STEP - 3
Set Your API Key

This project requires an OpenAI API key (or LiteLLM-compatible key).
export it directly in terminal:
export OPENAI_API_KEY=your_api_key_here

STEP - 4
Usage

Run the script with creators and options:

python crewai_sec_sentiment.py --creators elonmusk BillGates --max-tweets 3 --llm-model gpt-4o-mini

#Example Output (JSON)
{
  "creators": {
    "elonmusk": {
      "text": "Recent activity by elonmusk related to markets.",
      "sentiment": "Positive"
    }
  },
  "insider_trading": [
    {
      "insider": "John Doe",
      "company": "XYZ Corp",
      "activity": "Sold 50,000 shares"
    }
  ],
  "generated_on": "2025-08-23 16:15:39"
}


The output is saved in:

sec_sentiment_output.json
