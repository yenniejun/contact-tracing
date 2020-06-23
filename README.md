# Contact Tracing in Korean and American News

This is part of a larger project to understand data surveillance of different states during the time of the coronavirus pandemic. Specifically, this repo is about scraping and analyzing news sources related to contact tracing in Korean and American news sources.

# Steps

## Gathering News Sources

### Korean News Sources
I scraped the top results from the [Naver News](https://news.naver.com/) portal.
* Search term(s): '코로나 역학조사', '확진자 추적'
* Taking articles from the following Korean newspapers: 조선일보, 중앙일보, 동아일보, 한겨레, 경향신문
* Searching in the date range from January 01, 2020 to the beginning of June

Note: There were a LOT of results (and unfortunately, the filtering of the different newspaper agencies was done on the front-end, and so there was a lot of noise to sift through that took a lot of time). I split up the work into two parts: scraping the URLs, and then scraping the text for each link.


### American News Sources
Scraping American news was more annoying because there was no single portal like Naver News portal to get all of the urls from beforehand. I had to go to each individual news platform, and some of them were more difficult than others to scrape. I had to get rather creative in my scraping endeavors for some platforms (like obsessively searching the network calls...)
* Search term: "contact tracing"
* Taking articles from the following platforms: CNN, Fox, NYT, USA Today, Washington Post (Breitbart and Daily Caller were manually scraped because there were only 20 articles for each about contact tracing)
* Searching in the date range from January 01, 2020 to the beginning of June

Note: Many of the results for the search term "contact tracing" did not actually include anything about contact tracing in the article, so the number of American news articles actually related to contact tracing is fewer than expected



## Text Analysis
* Topic Modeling. I used both Latent Dirichlet Allocation (LDA) and Non-negative Matrix Factorization (NMF) 
* Word Frequency (top most frequent words ... and word clouds... because why not)



# Tools 
* beautiful soup (for scraping)
* nltk (English stop words, lemmatizer, stemmer)
* sklearn (NMF, LDA)
* [KoNLPy](https://konlpy.org/en/latest/) (Korean NLP in Python) (breaking Korean into morphemes)
* [Stopwords Korean](https://github.com/stopwords-iso/stopwords-ko)


# Helpful Articles

* [Topic Modeling with LDA and NMF on the ABC News Headlines dataset](https://medium.com/ml2vec/topic-modeling-is-an-unsupervised-learning-approach-to-clustering-documents-to-discover-topics-fdfbf30e27df)
* [Topic Modeling and Latent Dirichlet Allocation (LDA) in Python](https://towardsdatascience.com/topic-modeling-and-latent-dirichlet-allocation-in-python-9bf156893c24)
* [Mining English and Korean text with Python](https://www.lucypark.kr/courses/2015-ba/text-mining.html)
* [데이터 사이언스](https://ehfgk78.github.io/2018/01/23/DataScience08-KoNLPy/)




