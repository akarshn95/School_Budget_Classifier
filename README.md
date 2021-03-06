# School_Budget_Classifier
A multi-class classifier that classifies school items giving suitable budget labels based on the description provided. Uses NLP to understand the description and provide labels for each school budget item. The model is trained using 100,000 school budgetting records from the DrivenData School_Budgetting dataset. 

The columns of the school budget data are divided into numerical and text columns which act as predictors to predict the target labels. Each row can have mutiple labels, and the model preditcs the most suitable labels for each entry. The text columns are combined to form a single text desciption feature. The text and numeric features are transformed separately and fed to the LogisticRegression model for training. 


## Running the Model

Get the data, from https://www.drivendata.org/competitions/46/box-plots-for-education-reboot/

To run the notebook, first install the dependencies with:

    pip install -r requirements.txt

Then run:

    jupyter notebook notebooks/code_notebook.ipynb

## About the model

The model is a multiclass LogisiticRegression model implemented using OnevsRestClassifier after scaling, dimension reduction with SelecKBest and transforming the dataset. We have obtained a log loss score of 1.999 after training the model with 100,000 records of the school budgetting dataset.
