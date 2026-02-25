# Code for ICLR 2026 Paper: "Incentive-aligned Multi-Source LLM Summaries"

This folder contains the source code for the ICLR 2026 paper titled "Incentive-aligned LLM Summaries". The code allows for the replication of the experiments and results presented in the paper.

---

## Code Structure

The code is provided as Jupyter Notebooks (`.ipynb` files), which can be run in any environment that supports them (e.g., Google Colab, VS Code, a local Jupyter server). 

---

## Prerequisites: Configuring the LLM API

The core logic of our method relies on calls to a large language model (LLM). The provided code includes a self-contained function for making these API calls. To run the notebooks, you will need to configure this function to use your own LLM API provider and credentials. By default, this is configured for gemini-2.5-flash and gemini-2.5-flash-lite to match the experiments in our paper. You will need to supply your own credentials to run the code, and you can easily replace the API function if you prefer a different model suite.

Note: Running these notebooks will incur API usage charges. Please ensure you have set appropriate budget alerts and spending cutoffs on your account to manage total costs.

**Instructions:**

1.  **Locate the API Function**: In the notebooks, find the function gemini_call_sync responsible for making calls to the LLM API. 
2.  **Modify the Function**: Replace the logic inside this function with the client initialization and API call for your chosen LLM provider (e.g., Gemini, OpenAI, Anthropic, open-sourced models, or any other compatible endpoint).
3.  **Add Credentials**: Ensure you provide your API key and any other required credentials (e.g., project ID, project location and api_key).

Specifically, our main experimental result 1 can be obtained by running result1_natural_questions_experiments.ipynb and result1_clasheval_experiments.ipynb, and result 2 can be obtained by running result2_against_uninformative.ipynb. The additional experiment in Appendix L on a real webpages dataset are giving in appendix/appendix_additional_experiment.ipynb. For details, acknoweledgement, and references, please refer to our paper.