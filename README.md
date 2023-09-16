# Causal Reasoning and Large Language Models Experiment Replication

## Introduction
This repository is a replication of the first experiment from the paper "Causal Reasoning and Large Language Models: Opening a New Frontier for Causality" using the Tübingen cause-and-effect benchmark. The results obtained from selected models can be seen in the `results_table.md` file.

## Data Source
The dataset used for this experiment is sourced from the original paper's authors, available on their Github repository. The primary file utilized is `prompts_aug.csv`, which contains cause and effect columns derived from the original txt dataset by Mooij. This file arranges the data into paired variables and features useful augmentations. More information can be found in the `data_details.md` file.

## File Naming Conventions

### Sys/NoSys:
Files marked with `sys` contain data or are related to models that have been generated with a system message instructing the model to act as a causal agent. Conversely, those labeled `nosys` have been generated without this system message.

### Double Prompts:
Files marked with `double prompts` indicate that the data or model output within pertains to scenarios where two separate questions were asked for each pair to ascertain causality. Files without this marking typically contain single-prompt data.

## OpenAI API Usage
The primary interactions with the OpenAI API are located in the `API Code.ipynb` notebook. This code handles:

- Formulating prompts based on the dataset.
- Making requests to the OpenAI API to generate model responses.
- Storing these responses and their respective prompts as JSON files in the `Data` folder.

**Note**: All JSON files generated have been stored in the `Data` folder. If you're looking to rerun the `API Code.ipynb`, please fetch the necessary files from the `Data` folder and not the default directory it references.

### Specifics of Model Interactions
- For models like gpt-3.5-turbo (single-prompt) and gpt-4 (single-prompt), unique prompt formats have been used.
- For gpt-3.5-turbo (causal agent), specific system messages have been passed along with unique prompts.
- Detailed descriptions of model-specific interactions are present within the notebook.

## Model Response Analysis
To understand and evaluate the accuracies of different models, refer to notebooks named `some-model analysis.ipynb`. These notebooks focus on:

- Cleaning and standardizing model outputs.
- Assessing accuracy based on model responses in comparison to the actual data.
- Analyzing and contrasting results across models.

## Conclusion
There are notable discrepancies between the results of this replication and the findings of the original paper. These could stem from variations in temperature settings, differing scoring techniques, or sample sizes. Delve deeper into these nuances in the `conclusion.md` file.

## Feedback & Contributions
Your feedback and contributions are invaluable. If you detect inconsistencies or have ideas for refining the analysis, we encourage issues or pull requests.

