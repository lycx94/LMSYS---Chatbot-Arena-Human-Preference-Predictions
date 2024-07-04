# LMSYS - Chatbot Arena Human Preference Predictions
This [competition](https://www.kaggle.com/competitions/lmsys-chatbot-arena/overview) aims to predict which chatbot responses users will prefer in a head-to-head comparison of large language models (LLMs).

## Repository Overview
This repository includes the following key components:

1. lmsys_eda.ipynb: Notebook for exploratory data analysis of the provided dataset.
2. lmsys_finetuning.ipynb: Notebook for fine-tuning LLMs to better predict user preferences.
3. lysms_combined_lgbm.ipynb: Notebook for combining LGBM models with different preprocessing techniques for prediction.

## Data Analysis
- Users have varied preferences, and there is no fact-checking mechanism.
- LMSYS does not allow undoing or redoing annotations.
- Positional Bias: Users might favor the first answer they see, but no significant bias was observed.
- Length Bias: There might be a preference for longer answers.

## Fine-Tuning Large Language Models
- Loads the model in 4-bit using BitsAndBytesConfig.
- Utilizes an adapter and the LoRa method for fine-tuning, focusing on additional parameters rather than the original model weights.


**To fine-tune a different LLM, change the model_id parameter in the notebook to your desired LLM.**

## How to Use
- Explore Data: Start with lysms_eda.ipynb to understand the data and identify any potential issues or biases.
- Fine-Tune Models: Use lmsys_finetuning.ipynb to fine-tune your chosen LLM. Adjust the model_id parameter as needed.
- Combined LGBM Models: Explore lysms_combined_lgbm.ipynb to understand the approach of combining LGBM models with different preprocessing techniques.