## Steps to Use the Application

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

