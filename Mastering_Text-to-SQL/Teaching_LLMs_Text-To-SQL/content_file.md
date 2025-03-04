# Text-to-SQL Models

Text-to-SQL is a specialized application of Natural Language Processing (NLP) that enables AI models to translate natural language business queries into structured SQL commands. This capability allows businesses to interact with databases using everyday language instead of requiring SQL expertise.

Large Language Models (LLMs) are not inherently capable of converting natural language queries (NLQs) into SQL. They must be trained using **Supervised Fine-Tuning (SFT)** on high-quality datasets consisting of **NLQ-SQL pairs** to ensure accuracy and relevance. This training process is where AI trainers play a crucial role—by curating, refining, and validating datasets to improve model performance.

<img height="329" width="602" src="${PRIVATE_IMAGE_INTRO_1}" />

## Supervised Fine-Tuning (SFT) for Text-to-SQL

Supervised Fine-Tuning (SFT) is a method of training LLMs using labeled datasets that explicitly map input data (natural language queries) to expected output data (SQL queries). SFT directly teaches the model how to respond to structured queries by learning from correct examples.

### How SFT Works in Text-to-SQL Training

As an AI trainer, you would create a structured dataset containing **NLQ-SQL pairs**, ensuring the queries reflect realistic business scenarios. The dataset should cover a diverse range of query complexities and edge cases.

:::tip
### Your Role as an AI Trainer

1. **Crafting High-Quality NLQs**
   * Resemble real-world business analysis questions.
   * Consider various phrasings and wordings to teach the model robustness.
   * Avoid ambiguity to ensure clear and precise SQL translation.
2. **Writing Correct SQL Queries**
   * For every NLQ, you must provide a corresponding accurate and optimized SQL query that retrieves the correct results.
:::