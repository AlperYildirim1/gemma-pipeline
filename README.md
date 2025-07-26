
### Medical Reasoning with Gemma Models

This repository contains the code for our research on improving medical reasoning in Google's Gemma models.

The main idea was to see if we could teach smaller language models not just to give correct answers to medical questions, but to follow a logical, step-by-step reasoning process. We used a few techniques like Supervised Fine-Tuning (SFT) and Group Relative Policy Optimization (GRPO).

### What's in this repository?

The project is split into the training code and several evaluation pipelines:

*   `grpo_gemma.ipynb`: The notebook for the Group Relative Policy Optimization (GRPO) training stage.
*   `makale_gemma_3_4b_test_pipeline_open_ended.ipynb`: Evaluation pipeline for testing the models on complex, open-ended medical problems.
*   `makale_sft_gemma_3_4b_test_pipeline_MMLU.ipynb`: Evaluation pipeline for the medical portions of the MMLU dataset.
*   `makale_sft_gemma_3_4b_test_pipeline_Pubmed.ipynb`: Evaluation pipeline for the PubMedQA dataset.

### How to Run

All notebooks are designed to be run in Google Colab.

1.  Open any of the `.ipynb` files in Google Colab.
2.  **Important:** The test pipelines (`makale_..._test_pipeline_...` files) use GPT-4 as an evaluator. You will need an **OpenAI API key** to run them. The notebooks will prompt you to enter your key.
3.  The first few cells in each notebook will install all the required libraries (like `transformers`, `torch`, `unsloth`, etc.).
4.  Run the cells in order. The notebooks are set up to download the necessary datasets from Hugging Face.

### Note

This code was developed for the paper: "Investigation of Low-Parameter Gemma 3 Models for Medical Reasoning Using CoT-Supported SFT and GRPO". The work was supported by a TÜBİTAK grant (Project No. 5240094).
