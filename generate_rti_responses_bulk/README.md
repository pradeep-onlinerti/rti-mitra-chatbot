This script reads a CSV or Excel file containing RTI numbers and user queries,
sends the queries to an LLM-powered chatbot (e.g., RTI Mitra) via an OpenAI-compatible API,
and generates individual HTML files and one combined HTML document with the drafted RTI responses.

Features:
- Handles missing and duplicate RTI numbers
- Supports Markdown rendering of responses
- Provides both individual and consolidated HTML output
- Logs processing time for each RTI

Requirements:
- Python 3.7+
- pandas, requests, markdown, python-dotenv

Usage:
    Place your input file (CSV or XLSX) at the specified INPUT_PATH.
    Configure API_URL and MODEL_ID as needed.
    Run the script to generate HTML files in the OUTPUT_DIR.
