# Overview
Reddit is a social news aggregation site and discussion board that houses many interactive communities. These communities, termed *subreddits*, each have a particular thematic focus that collectively spans many aspects of pop culture and beyond. In this study, we attempt to explore the sentimental nature of these various interconnected communities by means of analyzing the user comments posted within them. Our end goal is to realize a reasonably intuitive map of Reddit that encapsulates the sentimental ties among some of its most popular subreddit communities.

# Background
In our endeavor to map the emotional contents of various subreddit communities, we will have to choose some form of sentiment analysis to conduct on each comment observation from our dataset. Sentiment analysis refers to the process of computationally extracting and quantifying the emotions and attitudes expressed through textual data and is a specific subfield of the much broader discipline of natural language processing (NLP). Recent studies within this field, particularly into social media sentiments, have successfully utilized a variety of noisy labels ranging from emoticons to hashtags as effective forms of distant supervision. Following this paradigmn, we will be incorporating a Deep Neural Network for sentiment classification developed by Felbo et. al which can be found on their [Github page](https://github.com/bfelbo/DeepMoji). This work introduces an interesting approach to classifying textual data into sentimental categories of (64) relevant emojis. More specifically, the so-called *DeepMoji* model applies the already well established LSTM architecture to an extensive corpus of tweet-emoji labeled data to learn text-sentiment associations while also incorporating an original approach for transfer learning (referred to by the authors as the "chain-thaw" method) which allows it to generalize to more conventional sentiment classification tasks. Taking inspiration from this work, we will apply the pretrained *DeepMoji* model towards the Reddit comments dataset in the hopes of being able to map some of the top subreddit communities into a low-dimensional embedding of sentiments. This visualization objective is reminiscent of previous works found [here](https://peerj.com/articles/cs-4/) and [here](http://rhiever.github.io/redditviz/#) in that we are trying to bring to light interesting relationships between various subreddit communities. In this case, however, we are less so interested about similarities in concrete subject matter and more so in the emotional connections/disparities between subreddits and of how these diverse communities encourage discussions that involve differential sentimental expressions.
