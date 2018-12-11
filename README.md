# NLP-Multi-Labeled-Text-Classification
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
