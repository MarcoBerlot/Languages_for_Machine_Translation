# Languages_for_Machine_Translation

Learning word embeddings using distribu- tional information is a task that has been studied by many researchers, and a lot of studies are reported in the literature. On the contrary, less studies were done for the case of multiple languages. The idea is to focus on a single representation for a pair of languages such that semantically similar words are closer to one another in the induced representation irrespective of the language. In this way, when data are missing for a particular language, classi- fiers from another language can be used.

## Overview
Implemented the following learning models :
-Minimization of the objective function through a perceptron built in Dynet

## Dependencies
* Python (3.6.4+)
* Natural Language ToolKit (nltk)
```python
import nltk
nltk.download()
```
* Dynet (2.0)
```python
pip install dynet
```


## How to run

Each Notebook contains the study for a different language. In this experiment we supported the following translations: English-Chinese, English-French, English-Italian, English-Spanish. All the visualizaitons are contained in the notebook.

## Results
The process for checking the accuracy of the model consisted of first taking a random subset of the corpus that was not used for training. This subset consists of slightly more common words because the more common words should have more accurate word embeddings.The English word embedding was multiplied by the transformation matrix to create the predicted translated word embedding. The cosine similarity was then generated with each translated word embedding stored in the corpus. The 20 words with the highest cosine similarity were then outputted. Then the English word was translated through Google Translate and compared to the 20 outputted translated words. It was considered a match if the translated word was found in this list of 20 similar words. Results are reported in the following table:

| Language | Least Squares | Normalized Vectors |
|----------|---------------|--------------------|
| French   | 47.1%         | 49.3%              |
| Italian  | 36.4%         | 39.2%              |
| Spanish  | 45%           | 47.24%             |
| Chinese  | 1.1%          | 1.4%               |

#### Note :
All the experiments and hyperparamters are self contained in the respective Jupyter Notebook files.
