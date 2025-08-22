# RTI Mitra – Batch RTI HTML Response Generator (Jupyter Notebook)

This Jupyter notebook automates the process of drafting RTI (Right to Information) applications using a chatbot (like RTI Mitra) and saving the results as HTML files. It supports both individual HTML outputs and a combined summary file for review.

---

## 🚀 Features

- Reads RTI numbers and user queries from CSV or Excel files
- Calls an OpenAI-compatible API to generate RTI drafts
- Outputs:
  - Individual HTML files per RTI
  - A combined HTML file for bulk viewing
- Handles:
  - Missing RTI numbers (`skip` or `autofill`)
  - Duplicate RTI numbers (`suffix` or `error`)
- Supports Markdown rendering, newline preservation, and basic error display

---

## 🛠️ Requirements

- Python 3.7+
- Jupyter Notebook or JupyterLab
- Install required packages using:

```bash
pip install pandas requests markdown python-dotenv
```

---

## 📁 File Structure

```
.
├── generate_rti_html_responses.ipynb   # Main notebook
├── NonTemplateRTIs.csv                 # Input data file (example)
├── rti_html_outputs/                   # Folder for individual HTML files
└── RTI_Mitra_All.html                  # Combined output file
```

---

## ⚙️ Configuration

Edit the config cell at the top of the notebook:

```python
INPUT_PATH = "NonTemplateRTIs.csv"           # Input file path (CSV or XLSX)
OUTPUT_DIR = "rti_html_outputs"              # Directory to store individual HTMLs
COMBINED_HTML = "RTI_Mitra_All.html"         # Combined output HTML file
API_URL = "http://localhost:3001/api/v1/openai/chat/completions"
MODEL_ID = "rti-mitra"
```

If authentication is required, add this to your `.env` file:

```env
ANYTHINGLLM_API_KEY=your_api_key_here
```

---

## 📝 Input Format

Your input file must contain the following columns (headers are case-insensitive and auto-normalized):

- `RTINumber` – a unique identifier for each RTI
- `User Query` – the query to send to the chatbot

Other accepted variants:
- `RTINumber`, `RTI Number`, `rti_number`
- `UserQuery`, `Message`, `Query`, `User Message`

---

## ▶️ How to Run

1. Open `generate_rti_html_responses.ipynb` in Jupyter Notebook or JupyterLab
2. Step through the notebook and run each cell sequentially
3. Once completed:
   - Individual HTMLs will be saved in the `rti_html_outputs/` directory
   - A combined HTML file (`RTI_Mitra_All.html`) will contain all responses

---

## 📊 Output Example

Each HTML file includes:
- **RTI Number** (as a heading)
- **User Query** (user’s original question)
- **Drafted RTI** (response from the chatbot)
- Optional: error message in red, if the API fails

---

## 🧪 Testing Tips

- Use  test file  `TestInput.csv` to know input format.
- Try toggling the `ON_MISSING_RTI` and `ON_DUPLICATE_RTI` config values to test error handling

---

## 🤝 Contributing

If you'd like to contribute:
- Follow existing structure and commenting style
- Submit a PR or share suggestions

---

## 📜 License

This tool is part of the [OnlineRTI / RTI Mitra](https://onlinerti.com) initiative  
Contact: [support@onlinerti.com](mailto:support@onlinerti.com)

---

## 👥 Maintainers

- RTI Mitra Team (OnlineRTI)
- https://onlinerti.com
