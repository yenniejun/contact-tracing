# Contact Tracing in Korean and American News

This is part of a larger project to understand data surveillance of different states during the time of the coronavirus pandemic. Specifically, this repo is about scraping and analyzing news sources related to contact tracing in Korean and American news sources.

# Steps

## Gathering News Sources

### Korean News Sources
I scraped the top results from the [Naver News](https://news.naver.com/) portal.
* Taking articles from the following Korean newspapers: 조선일보, 중앙일보, 동아일보, 한겨레, 경향신문
* Searching in the date range from January 01, 2020 to the beginning of June

Note: There were a LOT of results (and unfortunately, the filtering of the different newspaper agencies was done on the front-end, and so there was a lot of noise to sift through that took a lot of time). I split up the work into two parts: scraping the URLs, and then scraping the text for each link.



### American News Sources





# Tools 
* beautiful soup (for scraping)
* nltk
* sklearn
* [KoNLPy](https://konlpy.org/en/latest/) (Korean NLP in Python)