# Problem Statement
In our in-class activity, we practiced “getting to know your data” by loading a dataset, checking its structure, computing descriptive statistics, creating plots, and writing short interpretations about patterns and data quality. This assignment extends that workflow: you will build a Python system that can analyze any dataset a user uploads and automatically produce a clear set of useful data insights.

Your system will accept a CSV file as input (required). It may also accept an optional schema / data dictionary file that describes the columns (e.g., name, type, meaning, units, allowed values, missing-value codes). Your system must still run and produce results even if the schema file is not provided.

You have full access to GenAI tools, including cloud-based models (e.g., ChatGPT, Gemini, Claude) and local/open-source LLMs (e.g., Mistral, DeepSeek, Llama, or similar). You may use GenAI for brainstorming, code assistance, and generating narrative insight. However, you must document your GenAI usage by including a prompt/response log in your repository, and you remain responsible for verifying correctness (i.e., do not present unsupported or hallucinated conclusions as facts).

# Team Overview
Team Members: Rahul Hipparkar, Himanshu Jain

# Datasets used
- Development dataset : Tips
- Inference dataset : Wine quality

# Large Language Model used
gemini-flash-latest


# Repository structure:
- Logs: contain logs for gemini usage
- Output : contain plots, csv files, report (insights) for both development dataset
- requirements.txt : Manage project dependencies
- readme.md: To document team roles, project structure

