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



## Text Analysis
* Topic Modeling (using both LDA and NMF)
* Word Frequency (top most frequent words ... and word clouds... because why not)



# Tools 
* beautiful soup (for scraping)
* nltk (English stop words, lemmatizer, stemmer)
* sklearn (NMF, LDA)
* [KoNLPy](https://konlpy.org/en/latest/) (Korean NLP in Python) (breaking Korean into morphemes)
* [Stopwords Korean](https://github.com/stopwords-iso/stopwords-ko)

