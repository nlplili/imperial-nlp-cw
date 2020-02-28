# NLP Coursework


This repository contains all the code and the instructions to replicate the results, for the Sentence-level Quality Estimation Shared Task 2020, as part of the Imperial College London Natural Language Processing course. The details of the task are discussed here: https://competitions.codalab.org/competitions/22831. Pearson score obtained on the blind test set was 0.0972.

# Structure

- ```Features_models.ipynb``` contains the code used to generate our top performing submission.
- ```Embeddings_models.ipynb``` contains the code for creating an LSTM model and performs parameter tuning. However, the top performing result for this method was 0.0819.
-  The `Google API` folder contains two sub-folders `Translations` and `Similarities`. 
    -  The `Translations` folder contains the translated text for each sentence in the training set, using an adhoc script.
    -  The `Similarities` folder has a value for each sentence, describing how close the two translations are. The exact method used is detailed in Section 4.2 of the report.


# Setup
1. Clone the repository.
2. Run ```jupyter notebook``` and open ```Features_models.ipynb``` or ```Embeddings_models.ipynb```.
3. Execute the cells in order to replicate the performance discussed in the report.

  ## 3Α. Feature extractions and embeddings with Linear Regressors and MLP
  Open ```Features_models.ipynb```, run all the cells in sections 1 and 2 which import different libraries and load different classes for embeddings and pre-processing. Run all cells in section 3A if using embeddings as input to the regression model or run 3B if using features as input to the model. If using features as input, then run all cells under section 4 and one of the subsections in section 4 where 4A is feature selection using Variance Threshold, 4B is feature selection using RFE (Recursive Feature Elimination) and 4C is without appling any feature selection. Then run section 5 which loads the validation data and computes validation features/embeddings. After that, run section 6A if you want to train and validate Linear Regression models or run section 6B if you want to train and validate Neural Network models (MLP). Finally, run section 7 to load the test data, compute test features/embeddings and predict the scores.
  ## 3B. Embeddings with NN models
  The ```Embeddings_models.ipynb``` file has code for running the sentence averages to the best performing Multilayer perceptron model. It then has code for the hyperparameter search of the LSTM model, training the best LSTM model and trying it with FastText and BERT embeddings. 
