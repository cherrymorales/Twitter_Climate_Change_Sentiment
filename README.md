# Twitter Climate Change Sentiment Analysis

This project explores the public discourse on climate change by analyzing a dataset of Twitter posts related to the topic. We employ both Latent Dirichlet Allocation (LDA) and BERTopic, two powerful topic modeling techniques, to extract meaningful insights and uncover key themes. The analysis is based on the **Twitter Climate Change Sentiment Dataset** obtained from Kaggle.

## Project Overview

Climate change is a critical global issue with far-reaching impacts. Understanding the public sentiment and the major themes in discussions surrounding climate change can inform policy decisions and drive collective action. This project utilizes a Twitter dataset to analyze sentiment and topic models, providing insights into the nature of conversations around climate change.

The analysis incorporates both **Latent Dirichlet Allocation (LDA)** and **BERTopic** to extract and visualize the underlying themes in tweets. These two approaches allow for a nuanced exploration of the data, combining word frequency analysis with the semantic relationships between words.

## Key Features

- **Sentiment Analysis**: The dataset contains sentiment labels categorizing the tweets into four sentiment groups: pro, news, neutral, and anti.
- **Topic Modeling**: 
  - **LDA**: A probabilistic model that uncovers latent topics in the data based on word frequency.
  - **BERTopic**: A neural network-based topic modeling method that leverages pre-trained BERT models to capture semantic relationships between words.
- **Visualizations**: Word clouds and topic charts are provided to aid in the interpretation of the discovered topics.

## Files in the Repository

- **`Twitter_Climate_Change_Sentiment.ipynb`**: The Jupyter Notebook that walks through the analysis, from data loading to model training and evaluation.
- **`README.md`**: Project documentation.

## Data Source and Pre-processing

The analysis leverages the **Twitter Climate Change Sentiment Dataset** from Kaggle. This dataset contains **43,943** tweets categorized into four sentiment groups:

- Pro (22,962 tweets)
- News (9,276 tweets)
- Neutral (7,715 tweets)
- Anti (3,990 tweets)

The dataset has already been collected and pre-labeled with sentiment categories. Pre-processing steps in this analysis include tokenizing the text, removing stopwords, and preparing the data for LDA and BERTopic modeling. These steps ensure the dataset is clean and ready for topic modeling.

> **Note:** The dataset used in this project was obtained from [Kaggle](https://www.kaggle.com/code/nicolemeinie/sentiment-analysis-twitter-on-climate-change) and not collected using the Twitter API.

## Topic Modeling

### Latent Dirichlet Allocation (LDA)
LDA is a probabilistic model that discovers latent topics in the dataset by analyzing word frequency patterns. Each topic is represented by a list of keywords that are most representative of that topic. Word clouds are used to visualize these keywords, where the size of a word reflects its importance.

### BERTopic
BERTopic enhances traditional topic modeling by incorporating **BERT** embeddings, allowing the model to capture more complex semantic relationships between words. This results in topics that are more coherent and contextually relevant. 

### Results and Visualizations
- **LDA Word Clouds**: Visualizations of the most common terms in each sentiment category (e.g., “hoax,” “scam,” and “denial” for anti-climate change sentiment; “help,” “action,” and “real” for pro-climate action sentiment).
- **BERTopic Bar Charts**: Displays the top topics and their relevance scores. Example topics include discussions around energy solutions, global warming, and weather patterns, among others.

## Evaluation

To evaluate the topic models:
- **LDA**: We use **perplexity**, a common metric to evaluate the quality of probabilistic models. The results suggest that the model performs better for the "Pro" and "News" sentiments compared to "Anti" and "Neutral."
- **BERTopic**: We utilize BERTopic's built-in visualization tools, such as `visualize_topics()` and `visualize_barchart()`, to assess topic coherence and relevance.

## Installation and Usage

### Clone the Repository

```bash
git clone https://github.com/yourusername/twitter_climate_change_sentiment.git
cd twitter_climate_change_sentiment
```

### Running the Notebook

Launch the Jupyter Notebook and execute the cells to perform the analysis:

```bash
jupyter notebook
```

## Results and Interpretation

The combination of LDA and BERTopic provides a rich analysis of Twitter conversations on climate change. For instance:

- **LDA Word Clouds**: Visually represent the different stances, with "Anti" sentiment often containing words like "hoax" and "scam," while "Pro" sentiment includes terms like "help" and "real."
- **BERTopic Results**: Highlight topics such as energy action, global warming, and the impact of climate change on agriculture, weather, and polar regions.

## Limitations and Future Work

While this project provides meaningful insights, there are some limitations:
- The dataset focuses only on Twitter. Expanding the analysis to other social media platforms could provide a more comprehensive view of public discourse on climate change.
- Future work may explore alternative topic modeling approaches, such as **Top2Vec** or sentiment-aware topic models, to capture even deeper nuances.

## Contributing

If you'd like to contribute to this project, please fork the repository and use a feature branch. Pull requests are warmly welcome.

## License

This project is open-source and available under the [MIT License](LICENSE).
