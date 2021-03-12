# Developing a twitter bot using language modelling

A language model is something which has learnt the grammar of a language. We can use a language model to estimate the probability of correctness of a particular sentence. For tweet generation, the model was trained on 2016 Presidental Election tweets which were scraped from Twitter.

First, unigram, bigram and trigram frequency distributions were calculated using *nltk* library of Python, then their probability distributions were calculated using various smoothing techniques like [Good-Turing Smoothing](https://en.wikipedia.org/wiki/Good%E2%80%93Turing_frequency_estimation), [Kneser-Ney Smoothing](https://en.wikipedia.org/wiki/Kneser%E2%80%93Ney_smoothing).

After getting the n-gram probability distributions, the model has the capability to generate tweets when given a context word. Using a novel algorithm, the model was able to prepend and append words to the context word and generate a tweet of a given length.

Till now, the generated tweets did not have proper structure. So the next step is to introduce a Parts of Speech template, which can be used to filter only those tweets which follow the rules in the template.

And there you go, you have a bot which generates tweets on a context word
