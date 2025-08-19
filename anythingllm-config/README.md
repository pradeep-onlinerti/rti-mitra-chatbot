
 # ⚙️ Workspace Setup Instructions for AnythingLLM

Once you have started a new workspace in AnythingLLM, follow these steps to configure it using the files in this repository:

## 🔧 1. Configure Chat Settings

1. Click the ⚙️ Settings icon for the workspace.

2. Go to the “Chat Settings” tab.

3. Set the following:

   - LLM Provider: Select your preferred model (e.g., OpenAI, Local LLM, etc.)

   - Chat History Limit: 20

   - Prompt:  Copy the content from anythingllm-config/rti_prompt
            and paste it into the Prompt textbox.

   - LLM Temperature: 0.5

## 📚 2. Configure Vector Database

1. In the “Vector Database” tab:

   - Search Preference: Accuracy Optimized

   - Document Similarity Threshold: Medium 

## 🧠 3. Upload Knowledgebase Documents

1. Click the 📁 Upload icon next to the workspace.

2. Select and upload files from:

   - anythingllm-config/knowledgebases/

3. After upload, move to the workspace and click “Save and Embed”.

4. Pin the following documents -
   - RTI_Custom_Drafting_Rules.md
   - RTI_Offline_Application_Filing_Instructions_Template.md
   - RTI_Online_Application_Filing_Instructions_Template.md

## 🔁 Important Notes

1. Any change to chat settings or prompt will only reflect in new chat threads.

2. After changing settings, start a new chat thread to see the effect.
