# NLP Multi Labeled Text Classification
## DBpedia Ontology Classes


The dataset used in this notebook is a subset from the DBpedia set and contains 40,000 training samples and 5,000 testing samples from 14 nonoverlapping classes from DBpedia 2014.

The DBpedia project extracts structured information from Wikipedia editions and combines this information into a cross-domain knowledge base.

The 14 classes in this set are:

    Company
    Educational Institution
    Artist
    Athlete
    Office Holder
    Mean Of Transportation
    Building
    Natural Place
    Village
    Animal
    Plant
    Album
    Film
    Written Work

The data downloaded contains a training set and a test set. The goal of this model is to see if we can predict the correct class based on typing a few sentences. We will use the sentence in the test set to make our predictions.

At the end we achieved an accuracy of 72% vs a validation set.  The confusion matrix for all 14 classes is as follows:

![alt text](https://github.com/mlsmall/NLP-Multi-Labeled-Text-Classification/blob/master/cm.png)



## Tokenization

The first step of processing the texts go is to split the raw sentences into words or tokens. The easiest way to do this would be to split the string on spaces, but we need to be smarter:

- We need to take care of punctuations
- Some words are contractions of two different words, like isn't or don't. They are separated like: "did", "n't".
- We may need to clean some parts of our texts, if there's HTML code for instance
- Content is cleaned for any HTML symbol and lower cased


## Numericalization

Once the tokens have been extracted from the texts, the tokens are converted into integers.

## Training

- The classifier was trained using an LSTM RNN.
- Dropout regularization was used with a keep_prob value of 50%. 
- The model was trained with a learning rate of 1e-7/(2.6^4) for the earier layers and 3e-6 for the later layers.
- Momentum values were used of 0.8 and 0.7 for the earlier and later layers, respectively.
