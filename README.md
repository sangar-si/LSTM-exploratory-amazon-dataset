# LSTM-exploratory-amazon-dataset
**Part 3** : Exploratory analysis done on Amazon Polarity dataset of huggingface.  

# Dataset
**Dataset** : Amazon polarity dataset comprises of Amazon reviews labeled as positive or negative. The task being taken up is classification. Notebook contains *frac* variable which can be set between 0 to 1 which represents the fraction of data to be considered for training. Note that if we are working with the entire dataset, preprocessing and training will take a long time.  

To speed up preprocessing, it is divided into smaller portions with each thread working on one portion. Finally they are concatinated together.

# Model
We go with a Sequential model containing 4 LSTM units with dropout between units and a FCC layer with 16 x 1. The choice of activation function is ReLU in the first FCC layer followed by Sigmoid in the output layer. Since we have only one output unit, we go with BinaryCrossEntropy Loss which works well for this task. We choose Adam optimizer with learning rate of 0.0001.

# Preprocessing
1. Combining Title and Review into one entity
2. Lemmatization
3. Removing non-alphabets
4. Tokenize
5. Convert to lower case
6. Remove stop words

# Metric
Training accuracy : 87.49%  
Test accuracy : 86%



