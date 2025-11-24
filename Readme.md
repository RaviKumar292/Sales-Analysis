######### Project Overview #############

This project enables users to query sales data using natural language questions and receive:

Automatically generated SQL

Executed results from a DuckDB analytical store

Professional business insight summaries

LangChain agent reasoning

RAG-enhanced contextual responses on expense and warehouse

The notebook demonstrates an end-to-end applied GenAI analytics workflow.

-----------------------------------------------------------------------------------------------------------

########### Technology Stack ###########

####### Data & Storage #########

Pandas

Parquet Partitioning

DuckDB

####### LLM & AI Components #########

Google Gemini 2.5 Flash-Lite

Natural Language to SQL Generator

Business Insights Generator

LangChain DataFrame Agent

Lightweight RAG

-----------------------------------------------------------------------------------------------------------
############ Setup Instructions ################

######### Install Dependencies ##########

pip install pandas duckdb pyarrow
pip install google-generativeai
pip install langchain langchain-community langchain-experimental

###### Configure API Key #######

import google.generativeai as genai
genai.configure(api_key="YOUR_API_KEY")

-----------------------------------------------------------------------------------------------------------

############### Run Notebook ##########

Open Blend_Assessment_Ravi.ipynb

Execute cells sequentially

Ensure parquet folder path exists

Ask questions using below functions:

ask_sales_question("Which SKU sold the most in 2022?")
ask_insight("What was total quantity sold in 2023?")
agent.invoke("Top selling category last year")
ask_rag("Summarize the major expenses in the report", "expense")

-----------------------------------------------------------------------------------------------------------

############## Limitations #################

No UI
To run LLM features, set: GOOGLE_API_KEY=your_key_here
DuckDB concurrency restricted inside notebooks
The project uses free-tier Google Gemini, which restricts model size and reasoning depth.
