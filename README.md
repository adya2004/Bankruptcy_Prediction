# Bankruptcy Prediction Using NLP

This application leverages state-of-the-art natural language processing (NLP) techniques for bankruptcy prediction. It uses advanced models for knowledge extraction, summarization, and knowledge graph representation to generate insightful reports about financial risks.

## Models Used

- **LLAMA**: Used for knowledge extraction and summarization.
- **Neo4j**: For representing extracted knowledge in the form of a knowledge graph.
- Summarization models:
  - **T5 (Base and Large)**
  - **Facebook BART**
  - And other summarization models.

## Steps to Use the Application
```text
NOTE: Go to pythonscripts folder to follow the below given instructions
```
### Step 1: Create Virtual Environments
Create two separate Python virtual environments for different dependencies.

1. Run the following command to install LangChain dependencies:
   ```bash
   pip install -r LangchainRequirements.txt
   ```
2. Install normal dependencies:
   ```bash
   pip install -r NormalRequirements.txt
   ```

### Step 2: Set Up the `.env` File
Configure your API keys in a `.env` file to ensure proper access to required services. The `.env` file should include keys for:
- LLM API
- Neo4j database

### Step 3: Preprocess Text
To preprocess the text data, pass the location of your file as an argument to `Preprocess_text.py`.

Example command:
```bash
python Preprocess_text.py <your file location>
```
This will generate a preprocessed file at a specified location.

### Step 4: Extract Knowledge and Summarization
Use the `Summarization_and_KExtraction.py` script to extract knowledge and generate embeddings. Pass the location of the preprocessed file as an argument.

Example command:
```bash
python Summarization_and_KExtraction.py <preprocessed file location>
```
This will generate a JSON file containing the summary and embeddings.

### Step 5: Generate Final Report
Pass the generated JSON file to `ReportGeneration.py` to create the final PDF report. The report will be saved in the `output` folder.

Example command:
```bash
python ReportGeneration.py <json file location>
```

## Outputs
- **JSON File**: Contains the knowledge graph embeddings and summaries.
- **PDF Report**: Comprehensive analysis in PDF format, saved in the `output` folder.

Follow these steps sequentially to analyze financial data effectively and generate actionable insights.

The final pdf report looks like the following
![Screenshot 2024-11-08 121425](https://github.com/user-attachments/assets/c13fcbbb-153c-44f5-b32f-ac7489457e6d)

