## Notebook Description

This notebook showcases how to train a DistilBERT model to classify toxic comments using PyTorch.

### Table of Contents

- Importing Libraries
- Loading Dataset
- Creating Custom PyTorch Dataset
- Creating Dataloaders
- Model Design
- Training, Predicting, and Evaluation
- Saving and Loading Saved Model

<a name="importing-libraries"></a>

1. #### Importing Libraries
   The necessary libraries are imported at the beginning of the notebook. These libraries include torch, pandas, numpy, transformers, sklearn, tqdm, and others.

<a name="loading-dataset"></a>

2. #### Loading Dataset
   The cleaned dataset is loaded using the pd.read_csv() function from the pandas library. The dataset is preprocessed by removing any rows with missing data. The dataset includes columns for "toxic", "severe_toxic", "obscene", "threat", "insult", and "identity_hate".

<a name="creating-custom-pytorch-dataset"></a>

3. #### Creating Custom PyTorch Dataset
   A custom PyTorch dataset is created using the ToxicCommentDataset class. This class preprocesses the data, tokenizes the text, and creates input features and labels.

<a name="creating-dataloaders"></a>

4. #### Creating Dataloaders
   Dataloaders are created for the training, test, and validation datasets using the DataLoader class from PyTorch. The dataloaders are used to efficiently load the data during training and evaluation.

<a name="model-design"></a>

5. #### Model Design
   The DistilBERT model (a smaller version of the Bert Transformer model is used) is used to classify toxic comments.

<a name="training-predicting-and-evaluation"></a>

6. #### Training, Predicting, and Evaluation
   The model is trained on the training dataset using the train() function. After training, the model is used to make predictions on the test dataset. Evaluation metrics loss is calculated using the sklearn library.

<a name="saving-and-loading-saved-model"></a>

7. #### Saving and Loading Saved Model
   The trained model is saved using torch.save() function and loaded using the load_state_dict() function. The saved model can be loaded and used for prediction or further training.

The code snippets are provided for each of these sections to make the notebook easy to follow and reproduce. The model's performance can be evaluated using the loss metric. The state of the trained model is then saved as a pickle file, which can be loaded later for future predictions
