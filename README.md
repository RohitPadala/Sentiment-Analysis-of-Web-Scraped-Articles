# Sentiment-Analysis-of-Web-Scraped-Articles
The website used for web-scraping of the 50 articles is the Morningstar Archive. Set to a single page view of 50 articles per page, the weblink was ethically scraped in accordance to policies of the website and its underlying HTML structure.

Human-readable text was extracted from the HTML response of the articles using the TextBlob library (built upon the NLTK library). TextBlob inherently performs a lot of NLP data cleaning procedures such as tokenization, conversion to lower case and removal of punctuation marks. Nevertheless, the data was further cleaned to exclude all punctuation as well as any stop words while calculating the sentiment polarity and subjectivity scores. Standard dataset of stop words available in the libraries was used. Stemming and Lemmatization were also considered for data pre-processing, but ultimately not included since they didn't alter the polarity score ranges significantly. However, the older version of the code which experimented with Stemming and Lemmatization can also be found in the uploaded files.

Sentiment analysis was carried out using in-built TextBlob functions. The polarity ranges of [-1,-0.1) for negative, [-0.1,0.1] for neutral and (0.1,1] for positive sentiments were arbitrarily chosen.

Note: The code used here has been customized for the website which has been scraped. While the logic and basic template of the code remains mostly the same for different websites, the class names may differ between websites according to their HTML infrastructure. With the necessary changes, the process can be duplicated for other websites.

# Insights:

Firstly, based on the blue histogram, the sentiment polarity scores across the 50 articles can be observed. Most notably, all the polarity values are contained within the (-0.05,0.2) range. This clearly indicates that the language used by the website was largely neutral and professional, with a slight inclination to positive sentiments. This shows that the website doesn't sensationalize its articles to either extremes and delivers news in a mostly neutral tone.

Secondly, based on the red histogram, the sentiment subjectivity scores across the 50 articles can be observed. Most notably, all the subjectivity values are contained within the (0.3,0.5) range. Lower subjectivity values indicate more objective, less opinionated/biased articles. The website, while not abstaining from subjectivity, doesn't let bias take over the articles. This is also corroborated by the large number of contributing authors since different authors would have varying degrees of subjectivity.

