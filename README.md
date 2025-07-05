# Multi_News

This is a Streamlit web app that takes multiple news article URLs, fetches their content, summarizes each using Google Gemini (Generative AI), and then combines the summaries to extract common insights, consistent facts, conflicting claims, and key trends.

🚀 Features
✅ Extracts article text automatically from multiple URLs.
✅ Summarizes each article individually using Gemini 1.5 Pro.
✅ Analyzes the summaries to find:

Common facts across all articles.

Conflicting or mismatched claims.

Overall research summary and key trends.

✅ Displays individual summaries for transparency.

🛠 Tech Stack
Python

Streamlit for the web interface

Google Gemini (via google.generativeai) for text summarization & analysis

BeautifulSoup & Requests for web scraping

🔧 Setup Instructions
1️⃣ Clone the repository

bash
Copy
Edit
git clone https://github.com/Shivaniikongara/multi-news-summarizer.git
cd multi-news-summarizer
2️⃣ Install the required packages

Make sure you’re in a virtual environment or have Python 3.8+ installed.

bash
Copy
Edit
pip install streamlit google-generativeai beautifulsoup4 requests
3️⃣ Set up your Google Gemini API key

Replace this line in app.py:

python
Copy
Edit
genai.configure(api_key="YOUR_API_KEY")
with your actual Gemini API key.

Or, better practice, set it as an environment variable:

bash
Copy
Edit
export GOOGLE_API_KEY="YOUR_API_KEY"
and load it in Python:

python
Copy
Edit
import os
genai.configure(api_key=os.getenv("GOOGLE_API_KEY"))
4️⃣ Run the app

bash
Copy
Edit
streamlit run app.py
✍️ How to Use
Open the web app in your browser (Streamlit usually runs at http://localhost:8501).

Paste multiple news article URLs into the text area (one URL per line).

Click on "🔍 Analyze All Links".

The app will:

Fetch & clean the text from each article.

Use Gemini to summarize each.

Compare summaries to find common facts, conflicting claims, and key insights.

View the combined summary at the top and expand to see individual article summaries.
