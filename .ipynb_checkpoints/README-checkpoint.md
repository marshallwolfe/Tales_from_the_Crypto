# Tales from the Crypto

Use the news api, NLTK, and Python to determine and compare Sentiment Scores for Bitcoin and Ethereum, tokenize text, investigate Ngrams and word frequencies, create Word Clouds, and create named entity recognition visualizations using SpaCy

Please reference "crypto_sentiment.ipynb" in the Starter_Code folder. 

---

#### News Headlines Sentiment

We used the news api to pull the latest Bitcoin and Ethereum news articles and created a DataFrame of sentiment scores.

We: 

1. Fetched the news articles using `news api`.
2. Created DataFrames populated with Compound, Positive, Negative, and Neutral sentiment scores:
##### Bitcoin Sentiment Scores:
![Bitcoin Sentiment Scores](Images/btc_sentiments.png)

##### Ethereum Sentiment Scores:
![Ethereum Sentiment Scores](Images/eth_sentiments.png)

3. We described the sentiment scores:
![Bitcoin Sentiment Scores Description](Images/btc_describe.png)
![Ethereum Sentiment Scores Description](Images/eth_describe.png)

#### Questions Answered:

* Which coin had the highest mean positive score? 
>
>Ethereum had the highest mean positive score of 0.108667 compared to Bitcoin's 0.031950.

* Which coin had the highest compound score?
>
>Ethereum had the highest max compound score of 0.731600 compared to Bitcoin's 0.401900.

* Which coin had the highest positive score?
>
>Ethereum had the highest max positive score of 0.226000 compared to Bitcoin's 0.110000.

---

#### Tokenizer

We used NLTK and Python to tokenize the text for Bitcoin and Ethereum.

We: 

1. Instantiated a lemmatizer and appended stopwords.
2. Defined a tokenizer function that receives text and then lowercases each word, removes punctuation, and removes stopwords.
3. Created a list of tokenized words for each coin.
4. Added a tokens column to our Bitcoin and Ethereum DataFrames.

---

#### NGrams and Frequency Analysis

Using Counter from the collections library and ngrams from NLTK, we analyzed n-grams and word frequency for each coin.

We:

1. Generated N-grams where N = 2 for both Bitcoin and Ethereum.
##### Bitcoin N-grams where N = 2:
![Bitcoin N-grams](Images/btc_ngrams.png)
##### Ethereum N-grams where N = 2:
![Ethereum N-grams](Images/eth_ngrams.png)

2. Defined a token_count function to generate the top 10 words for each coin:
![Top Words for Bitcoin and Ethereum](Images/top_words.png)

---

#### Word Clouds

Using the WordCloud library and matplotlib, we generated word clouds for Bitcoin and Ethereum to summarize news for each coin.

We:
1. Defined a process_text function that uses regex, re_clean, word_tokenize, and lemmatizer to clean our text.
2. Generated word clouds for both coins:
##### Bitcoin Word Cloud:
![Bitcoin Word Cloud](Images/btc-word-cloud.png)
##### Ethereum Word Cloud:
![Ethereum Word Cloud](Images/eth-word-cloud.png)

---

#### Named Entity Recognition

We built a named entity recognition (NER) model for Bitcoin and Ethereum and visualized the tags using SpaCy.

We:

1. Concatenated all of the Bitcoin text together and all of the Ethereum text together.
2. Created NER visualizations using displacy:

![Bitcoin NER Visualization](Images/Bitcoin_NER_header.png)

![Ethereum NER Visualization](Images/Ethereum_NER_header.png)

3. Listed all entities for Bitcoin and Ethereum.