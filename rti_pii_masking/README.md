This folder contains scripts related to masking personal data like names, addresses, govt ID card numbers etc.

🚀 How to Use This Script

1. Install Dependencies

Make sure you have the required Python packages installed:

pip install pandas openpyxl python-dotenv requests

2. Prepare Your .env File

Create a .env file in the root directory of your project with the following content:

ANYTHINGLLM_API_KEY=your_api_key_here

3. Prepare Your Input File

Your Excel input file (e.g. rti_inputs.xlsx) should have columns containing RTI text (like Query) and optionally a Number column for tracking.

The input file can have columns containing data which needs to be masked. As of now these need to be in following names 

columns_to_mask_pii = ["Title", "User Description", "Drafter Modified Title", "Drafter Modified Description"]


4. Run the Script

Place the file in the project directory or provide the full path.

In a Jupyter Notebook load the file and run it.

This will process data in batches, mask personal information using AnythingLLM, and save the final result as a single Excel file provided in the file(e.g MaskedOutput.xlsx )
