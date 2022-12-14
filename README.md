# ProtMIMO-CodingChallenge

This is a machine learning (for proteins) coding challenge.  It aims to assess general modeling skills as well as paper reading/implementation skills. It is intended to be done in PyTorch. 

## Instructions
The specific task is to use the Multi-Input Multi-Output (MIMO) architecture from [Havasi et al.](https://arxiv.org/abs/2010.06610) for protein function prediction. This architecture aims to replace traditional ensembles by taking in multiple inputs and predicting multiple outputs aiming to match a single distribution at each output head. For inference they input the same value multiple times and take the average of the multiple predictions made by the MIMO model. Check out the first three pages of their paper for more details. 

Some boilerplate code is provided, especially in `ProtMIMO/data_utils.py` which has code for downloading and processing the GFP (fluorescence) data from [Tasks Assessing Protein Embeddings (TAPE)](https://github.com/songlab-cal/tape) into Pandas DataFrames. A `requirements.txt` is also provided. To install PyTorch with e.g., GPU support, we recommend referencing PyTorch's [official installation materials](https://pytorch.org/get-started/locally/). To help manage imports when e.g., working with integrated development environments (IDEs) such as Visual Studio Code, we recommend installing this project as a Python package using the command `pip3 install -e .` in the project's root directory.

You are expected to do the following in 3 hours or less and you may use any resource available to you (except asking someone else for help or finding an existing solution):
<ul>
  <li>Implement a MIMO model along with helper modules. We recommend using a MIMO MLP and/or a MIMO CNN (preferably both).</li>
  <li>Implement dataloaders that enable you to train and evaluate the MIMO models.</li>
  <li>Train the MIMO models along with a traditional ensemble of regression models to compare to.</li>
  <li>Evaluate the MIMO models and the ensembles and compare their performance on metrics such as mean-squared error (MSE), Pearson correlation, Spearman Rho, and diversity (which can be measured by looking at residual correlations).</li>
  <li>Create visuals such as plots and tables to present your findings. You can put them in the README or in a slide show on Google Drive.</li>
  <li>(Optional) Implement tests for your modeling code.</li>
  <li>(Optional) Use importchecker (https://pypi.org/project/importchecker/) and black formatter (https://black.readthedocs.io/en/stable/) to clean up your code.</li>
</ul>

**Hint**: We recommend first looking at the boilerplate code provided in `ProtMIMO/model.py` and `ProtMIMO/data_utils.py` to get started.
