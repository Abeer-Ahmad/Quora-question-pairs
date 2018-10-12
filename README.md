# Quora Question Pairs
A simple approach to the "Quora Question Pairs" [Kaggle competition](https://www.kaggle.com/c/quora-question-pairs) for detecting duplicate questions in QA platforms.
# Elaboration
## 1. Datasets
- Both training and test sets are provided by Kaggle.
- A validation set is created by deducting 10% of the training set.
## 2. Data Preprocessing
Includes the following:
- **Text cleaning:** (tokenization, converting to lowercase, removing puctuations and stopwords, etc.).
- **Text normalization:** (restoring abbreviations).
## 3. Feature Extraction
Using the vocab embedding matrix; where each word is represented by a 300-dimensional feature vector.
## 4. Model
Keras LSTM model:
- Trained over 10 epochs (or more; where early stopping can be used to monitor the model performance).
- Used the manhattan distance similarity metric.
## Results
This model achieves 80.67% validation accuracy, with a log-loss value of 0.416 when submitting to Kaggle.
# Note
This approach was developed using Google Colaboratory with GPU accelerator, synced with Google Drive for file integration.
# Useful Libraries
- [NLTK](https://www.nltk.org/)
- [Word2Vec](https://code.google.com/archive/p/word2vec/)
- [Keras](https://keras.io/)
- [scikit-learn](http://scikit-learn.org/)
# Resources
- [1st Place Solution](https://www.kaggle.com/c/quora-question-pairs/discussion/34355)
- [Some Online Interesting Solutions](https://www.kaggle.com/c/quora-question-pairs/discussion/30260)
- [How to predict Quora Question Pairs Using Siamese Manhattan LSTM](https://medium.com/@eliorcohen/implementing-malstm-on-kaggles-quora-question-pairs-competition-8b31b0b16a07)
