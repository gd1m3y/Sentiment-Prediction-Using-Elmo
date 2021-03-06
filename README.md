# Sentiment-Prediction-Using-Elmo
## introduction
The Aim of this project is to determine whether the sentiment of tweet provided is positive or negative using Elmo.
## Elmo
ELMo is a novel way to represent words in vectors or embeddings. These word embeddings are helpful in achieving state-of-the-art (SOTA) results in several NLP tasks:

![image](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/03/SOTA-ELMo_2-300x257.png)

ELMo word vectors are computed on top of a two-layer bidirectional language model (biLM). This biLM model has two layers stacked together. Each layer has 2 passes — forward pass and backward pass:

![image](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/03/output_YyJc8E.gif)

1. The architecture above uses a character-level convolutional neural network (CNN) to represent words of a text string into raw word vectors

2. These raw word vectors act as inputs to the first layer of biLM

3. The forward pass contains information about a certain word and the context (other words) before that word

4. The backward pass contains information about the word and the context after it

5. This pair of information, from the forward and backward pass, forms the intermediate word vectors

6. These intermediate word vectors are fed into the next layer of biLM

7. The final representation (ELMo) is the weighted sum of the raw word vectors and the 2 intermediate word vectors

## Data
The data is a list of Labeled tweets Which are available in the repo , Also it takes a long time to train the model with the embeddings data so you
can also download the embeddings data from the following link 
* [train_embedding](https://drive.google.com/file/d/1dG9YLU11K9h1iINtN_QJSthv9yF50dTr/view?usp=sharing)

## Model
The Model Used is a basic Logistic Regression Model trained on the elmo_embeddings, attaining a accuracy of 0.83 on test data

## Technology Stack

* Spacy - A NLP Library used for variety of tasks Such as Named entity recognition
* Tensorflow (1.X) - A Deep Learning Framework 
* Tensorflow-hub - A Model library using which we can access the elmo embeddings 
* Numpy - Basic Mathematical library
* re - for performing string operations
* pandas - Data manipulation library
* Pickle - To save the intermediate results
## To-do
* Using different sophisticated models or methodologies to train on embeddings and achieve a better accuracy
* Different Preprocessing steps for a better result
## Contact
Want to contribute ? Contact me at narayanamay123@gmail.com
