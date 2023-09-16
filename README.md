# Causal Reasoning and Large Language Models Experiment Replication

## Introduction
This repository is a replication of the first experiment from the paper "Causal Reasoning and Large Language Models: Opening a New Frontier for Causality" using the Tübingen cause-and-effect benchmark.

## Results Overview

| Model                                     | Acc. | Wt. Acc. |
|-------------------------------------------|------|----------|
| text-ada-001                              | 0.51 | 0.51     |
| text-babbage-001                          | 0.50 | 0.48     |
| text-davinci-001                          | 0.50 | 0.50     |
| text-davinci-002                          | 0.76 | 0.70     |
| text-davinci-003                          | 0.80 | 0.78     |
| gpt-3.5-turbo                             | 0.74 | 0.76     |
| gpt-3.5-turbo (causal agent)              | 0.85 | 0.84     |
| gpt-3.5-turbo (single-prompt)             | 0.83 | 0.87     |
| gpt-4 (single-prompt)                     | 0.96 | 0.97     |


## File Naming Conventions

### Sys/NoSys:
Files marked with `sys` or `withsys`contain data that have been generated with a system message instructing the model to act as a causal agent. Conversely, those labeled `nosys` have been generated without this system message.

### Double Prompts:
Files marked with `double prompts` indicates that it contains double prompt data. Files without this marking typically contain single-prompt data.

## OpenAI API Usage
The primary interactions with the OpenAI API are located in the `API Code.ipynb` notebook. This code handles:

- Formulating prompts based on the dataset.
- Making requests to the OpenAI API to generate model responses.
- Storing these responses and their respective prompts as JSON files in the `Data` folder.

**Note**: All JSON files generated have been stored in the `Data` folder. If you're looking to rerun the `API Code.ipynb`, please fetch the necessary files from the `Data` folder and not the default directory it references.

## Model Response Analysis
To understand and evaluate the accuracies of different models, refer to notebooks named like `{model-name} analysis.ipynb`. These notebooks focus on:

- Cleaning and standardizing model outputs.
- Assessing accuracy based on model responses in comparison to the ground truth.

## Conclusion
There are notable differences between the results of this replication and the findings of the original paper. These could stem from variations in temperature settings, differing scoring techniques, or sample sizes.

## Feedback & Contributions
Your feedback and contributions are invaluable. If you detect inconsistencies or have ideas for refining the analysis, we encourage issues or pull requests.

