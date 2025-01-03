# ReAR
## I. Requirements

- python 3.8
- pandas 2.0.3
- numpy 1.21.6
- imbalanced-learn 0.6.0
- matplotlib 3.7.5
- scipy 1.5.3
- scikit-learn 0.22.2
- cleanlab 0.1.1

## II. Overview of ReAR
![model3](https://github.com/user-attachments/assets/f2f8e66a-5503-4e64-80e0-e872b8e90d65)

## III.Introduction

We proposed the ReAR model, which addressed the challenges of label inaccuracies and knowledge distribution bias. 
This was achieved in two parts: firstly, by utilizing confidence learning to remove app review noise and tackle label inaccuracies. 
Then, the review oversampling component sampled the minority classes in the application reviews, addressing the issue of biased distribution in review knowledge.

## IV. Prepare Dataset

The dataset already exists in the datasets directory of ReAR, with a total of two datasets: Maalej and Panichella.
Also, the labelling guide used for the Pinchella dataset can be found inside this folder.
- **ARDOC.csv**: contains predictions of the ARDOC baseline generated from their Java tool.
- **dim100*.txt**: Contains the word embeddings vectors, where each review is represented by a vector, the average of the individual word vectors.
- ** freqmat*.txt**: Containts a bag of word representation of the reviews.
- ** ldamat*.txt**: Contains LDA representation of the reviews.
- ** sentiment .txt**: Contains the sentiment score generated by [here](http://sentistrength.wlv.ac.uk/).
- ** tenses.txt**: Contains the verb feature as described by the Maalej paper.
- ** tfidf*.txt**: Contains the TFIDF representation of the reviews.

## V. Reproduce All Experiments from Scratch

If you want to reproduce an experiment, first use the following command to enter the experiment folder. 

```
cd RQ$($∈{1,2,3,4,5,6})
```

Next, in the RQ directory, set the relevant references to the hmkrvm_model_train.py file, that is, use the following code in the code to obtain different experimental models:

```
from ExperimentalModel import *
```

Finally, run the model in the experiment using the following command:


```
python hmkrvm_model_train.py
```
The above running code will execute training and testing together, and the model will be saved in the experiment_saved_models/rvm_vs_stateofar directory, and the results will be displayed after the run ends.
