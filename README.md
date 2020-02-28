# NLP Coursework


This repository contains all the code and the instructions to replicate the results, for the Sentence-level Quality Estimation Shared Task 2020, as part of the Imperial College London Natural Language Processing course. The details of the task are discussed here: https://competitions.codalab.org/competitions/22831. Pearson score obtained on the blind test set was 0.0972.

# Structure

- ```NLP_models_features.ipynb``` contains the code used to generate our top performing submission.
- ```Embeddings_models.ipynb``` contains the code for creating an LSTM model and performs parameter tuning. However, the top performing result for this method was 0.0819.
-  The `Google API` folder contains two sub-folders `Translations` and `Similarities`. 
    -  The `Translations` folder contains the translated text for each sentence in the training set, using an adhoc script.
    -  The `Similarities` folder has a value for each sentence, describing how close the two translations are. The exact method used is detailed in Section 4.2 of the report.


# Setup
1. Clone the repository.
2. Run ```jupyter notebook``` and open ```NLP_models_features.ipynb``` or ```Embeddings_models.ipynb```.
3. Execute the cells in order to replicate the performance discussed in the report.

  ## 3Α. Executing features code
  
  ## 3B. Executing embeddings code
  The ```Embeddings_models.ipynb``` file has code for running the sentence averages to the best performing Multilayer perceptron model. It then has code for the hyperparameter search of the LSTM model, training the best LSTM model and trying it with FastText and BERT embeddings. 
