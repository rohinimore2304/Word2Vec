# Project Title: Word2Vec

word2vec_nlp.ipynb: The Jupyter Notebook that contains the implementation of the Word2Vec model, training, and evaluation.

# Requirements

To run the code, you'll need the following Python packages:

gensim

nltk

pandas

numpy

## You can install the necessary dependencies with:

bash

Copy

Edit

pip install -r requirements.txt

# Steps
# 1. Data Preprocessing
In the first step, the text data is preprocessed. This includes:

Remove HTML Tags

Removing stopwords

Lowercasing

You can find the preprocessing code in the notebook (word2vec_task.ipynb).

# 2. Training the Word2Vec Model
   
The Word2Vec model is trained on the preprocessed data using the gensim library. We use the following parameters:

Size: 100 (dimension of the word vectors)

Window: 5 (the maximum distance between the current and predicted words within a sentence)

Min_count: 1 (ignores all words with total frequency lower than this)


# 3. Model Evaluation
Once the model is trained, it is evaluated by performing word similarity tasks. You can try querying the model with words like:

model.wv.most_similar('king')
model.wv.most_similar('computer')

# 4. Saving and Loading the Model
   
The trained model is saved in the models/ folder. You can load it using the following command:

model = gensim.models.Word2Vec.load('models/word2vec.model')

