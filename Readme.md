# 📝 Data Generation using RAG (Retrieval-Augmented Generation)

Welcome to the **Data Generation using RAG** repository! This project leverages **Retrieval-Augmented Generation (RAG)** to generate and refine smart contract data, helping developers create, manage, and improve data generation structures effectively. RAG enhances traditional generation models by adding a retrieval component, making it ideal for producing accurate, context-rich data.

## 🌟 Features

- **Contextual Data Generation**: Combines retrieval and generation models to provide highly accurate and context-aware data.
- **Domain-Focused**: Tailored prompts and retrieval specifically designed for domain-specific data generation.
- **Error Correction**: Automatically refines code by catching errors, correcting, and retrying compilation.
- **Customizable Configurations**: Adjustable parameters to fit various use cases.
- **Storage of Valid Contracts**: Compiled, error-free contracts are stored for easy reference and reuse.

## 🛠 Configuration
The configuration can be customized in the main script:

- **Retrieval Model Parameters**: Modify retrieval settings to optimize document extraction.
- **Generation Parameters**: You can set parameters like token limit, temperature, and prompt format for model generation.
- **Error Correction**: Define the max retry limit and set preferences for handling errors during data generation.

## Set Environment Variables

Update your `.env` file to include your OpenAI Key credentials. Add the following environment variables to the file:
```bash  
OPENAI_API_KEY=your_openai_api_key
```

## 🚀 Getting Started
Clone the Repository:

```bash  
git clone https://github.com/MuhammadFaraz123/Data-Generation-Using-RAG-Retrieval-Augmented-Generation.git
cd Data-Generation-Using-RAG-Retrieval-Augmented-Generation
```
Install Dependencies:

```bash  
pip install -r requirements.txt
```

Run the Pipeline: To generate data with RAG, run:

```bash  
python main.py
```

## How It Works
- **Retrieve**: The retriever component searches for relevant documents based on the input prompt. These documents contain contextual information relevant to the data type, category, and parameters.
- **Augment**: The retrieved documents are combined with the input prompt, enriching the context for accurate data generation.
- **Generate**: The augmented prompt is passed to the generation model, which creates data according to the specified requirements.
- **Correct**: Generated data are checked for syntax or logic errors. If errors are found, the data undergoes automatic correction and retry until a compilable data is produced.
