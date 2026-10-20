# Topic Modeling on News Articles

## Project Overview
This project discovers hidden themes in news and discussion articles
using unsupervised Natural Language Processing (NLP).

Two topic modeling approaches are compared:
- Latent Dirichlet Allocation (LDA)
- Non-negative Matrix Factorization (NMF)

## Dataset
- Dataset: 20 Newsgroups
- Original articles: 18,331
- Articles after preprocessing: 18,295
- Categories: Newsgroup discussion categories

Note: The BBC News Dataset was recommended in the task description.
This project uses the 20 Newsgroups dataset as an alternative.

## Methodology
1. Load the news articles.
2. Convert text to lowercase.
3. Remove punctuation, numbers, stopwords, and short words.
4. Create word-count features for LDA.
5. Create TF-IDF features for NMF.
6. Train both models with five topics.
7. Extract the top 10 words for each topic.
8. Compare topic coherence scores.

## Results

| Model | Features | Coherence |
|---|---|---:|
| LDA | Word Counts | 0.5646 |
| NMF | TF-IDF | 0.7045 |

NMF achieved a higher coherence score in this experiment.
This suggests its topics were more coherent under the selected metric.

## Example Topics
NMF identified themes related to:
- Windows and DOS software
- Christianity and religion
- Computer hardware
- Email and help requests
- General discussion

## Technologies
- Python
- Pandas
- NLTK
- Scikit-learn
- Gensim
- Matplotlib

## Files
- `topic_modeling_news.ipynb`: Main notebook
- `topic_modeling_comparison.csv`: Model comparison results
- `README.md`: Project documentation

## How to Run
1. Open the notebook in Google Colab.
2. Install the required libraries.
3. Run the notebook cells in order.

## Conclusion
Both LDA and NMF discovered themes without requiring labelled
training examples. In this experiment, NMF achieved higher topic
coherence than LDA.