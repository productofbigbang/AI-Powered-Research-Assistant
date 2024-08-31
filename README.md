

# AI-Powered Research Proposal Generator

This project is an AI-powered research proposal generator that uses the LangChain framework and the Groq language model to create comprehensive research proposals.

## Features

- Extracts data from PDF and Word documents
- Generates research topics, ideas, questions, and hypotheses
- Performs literature reviews
- Develops research methodologies
- Assesses research significance
- Considers ethical implications
- Creates timelines and budgets
- Compiles all components into a final research proposal

## Requirements

- Python 3.7+
- LangChain
- Groq API access
- FAISS
- HuggingFace Transformers
- PyPDF2
- docx2txt

## Installation

1. Clone this repository
2. Install the required packages:

```bash
pip install langchain langchain-groq langgraph faiss-cpu transformers pypdf docx2txt
```

3. Set up your Groq API key as an environment variable:

```bash
export GROQ_API_KEY='your_api_key_here'
```

## Usage

1. Prepare your input documents (PDF or DOCX format) and place them in a known directory.

2. Modify the `inputs` dictionary in the script with your initial ideas and document paths:

```python
inputs = {
    "idea_nodes": ["Your", "Initial", "Ideas"],
    "document_paths": ["path/to/paper1.pdf", "path/to/paper2.docx"],
    "num_steps": 0
}
```

3. Run the script:

```bash
python research_proposal_generator.py
```

4. The script will output progress for each step of the proposal generation process.

5. The final proposal will be printed as a JSON object at the end of the execution.

## Workflow

The research proposal generation follows this workflow:

1. Extract data from documents
2. Generate research topic
3. Generate idea nodes
4. Generate research questions
5. Generate hypothesis
6. Generate literature review
7. Generate methodology
8. Generate significance assessment
9. Generate ethical considerations
10. Generate timeline and budget
11. Compile final proposal

## Customization

You can customize the prompts for each step by modifying the `PromptTemplate` objects in the script. This allows you to tailor the AI's output to your specific needs or research domain.

## Limitations

- The quality of the output depends on the input documents and the performance of the Groq language model.
- Large documents may take significant time to process.
- Ensure you have sufficient API credits for your Groq account.

## Contributing

Contributions to improve the project are welcome. Please submit a pull request or open an issue to discuss proposed changes.

