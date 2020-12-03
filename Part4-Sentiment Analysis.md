# Sentiment Analysis:

![](https://www.upgrad.com/blog/wp-content/uploads/2019/04/70862042.png)

Sentiment Analysis is the process of determining whether a piece of writing is positive, negative or neutral. A sentiment 
analysis system for text analysis combines natural language processing (NLP) and machine learning techniques to assign
weighted sentiment scores to the entities, topics, themes and categories within a sentence or phrase. Sentiment analysis 
helps data analysts within large enterprises gauge public opinion, conduct nuanced market research, monitor brand and product 
reputation, and understand customer experiences. In addition, data analytics companies often integrate third-party sentiment 
analysis APIs into their own customer experience management, social media monitoring, or workforce analytics platform, in order 
to deliver useful insights to their own customers.


## Working of Sentiment Analysis:

![](https://i.ytimg.com/vi/qoyp8pBtCZ0/maxresdefault.jpg)

Basic sentiment analysis of text documents follows a straightforward process:

1. Break each text document down into its component parts (sentences, phrases, tokens and parts of speech)
1. Identify each sentiment-bearing phrase and component
1. Assign a sentiment score to each phrase and component (-1 to +1)
1. Optional: Combine scores for multi-layered sentiment analysis

For example:

* Terrible pitching and awful hitting led to another crushing loss. *
* Bad pitching and mediocre hitting cost us another close game.*

Both sentences discuss a similar subject, the loss of a baseball game. But you, the human reading them, can clearly see that 
first sentence’s tone is much more negative.

Your brain figures this out by looking for and interpreting sentiment-bearing phrases – that is, words and phrases that carry a tone 
or opinion. These usually appear as adjective-noun combinations. In the examples above, the sentiment-bearing phrases are:

Terrible pitching | awful hitting | crushing loss

Bad pitching | mediocre hitting | close game

You have encountered words like these many thousands of times over your lifetime across a range of contexts. And from these experiences, 
you’ve learned to understand the strength of each adjective, receiving input and feedback along the way from teachers and peers.

When you read the sentences above, your brain draws on your accumulated knowledge to identify each sentiment-bearing phrase and interpret 
their negativity or positivity. Usually this happens subconsciously. For example, you instinctively know that a game that ends in a “crushing 
loss” has a higher score differential than the “close game”, because you understand that “crushing” is a stronger adjective than “close”.

Interestingly, computer sentiment analysis works (almost) the same way.

## 7 basic functions of Text Analystics:
There are 7 basic steps involved in preparing an unstructured text document for deeper analysis:

1. Language Identification
1. Tokenization
1. Sentence Breaking
1. Part of Speech Tagging
1. Chunking
1. Syntax Parsing
1. Sentence Chaining
Each step is achieved on a spectrum between pure machine learning and pure software rules. Let’s review each step in order, and discuss the 
contributions of machine learning and rules-based NLP.

## Sentiment library:

Much in the way your brain remembers the descriptive words you encounter over your lifetime and their relative “sentiment weight”, a basic sentiment 
analysis system draws on a sentiment library to understand the sentiment-bearing phrases it encounters.
Sentiment libraries are very large collections of adjectives (good, wonderful, awful, horrible) and phrases (good game, wonderful story, awful performance, 
horrible show) that have been hand-scored by human coders. This manual sentiment scoring is a tricky process, because everyone involved needs to reach some 
agreement on how strong or weak each score should be relative to the other scores. If one person gives “bad” a sentiment score of -0.5, but another person 
gives “awful” the same score, your sentiment analysis system will conclude that that both words are equally negative.

What’s more, a multilingual sentiment analysis engine must maintain unique libraries for each language it supports. And each of these libraries must be 
maintained constantly: scores tweaked, new phrases added, irrelevant phrases removed.

## Simple, rules-based sentiment analysis systems
Once the sentiment libraries are prepared, software engineers write a series of guidelines (“rules”) to help the computer evaluate the sentiment expressed 
towards a particular entity (noun or pronoun) based on its nearness to known positive and negative words (adjectives and adverbs).

To continue our baseball example, an engineer might create search rules that look like:

(pitching) near (good, wonderful, spectacular)

(pitching) near (bad, horrible, awful)

These queries return a “hit count” representing how many times the word “pitching” appears near each adjective. The system then combines these hit counts using 
a complex mathematical operation called a “log odds ratio”. The outcome is a numerical sentiment score for each phrase, usually on a scale of -1 (very negative)
to +1 (very positive).


## Part of Speech tagging in sentiment analysis
Even before you can analyze a sentence and phrase for sentiment, however, you need to understand the pieces that form it. The process of breaking a document down
into its component parts involves several sub-functions, including Part of Speech (PoS) tagging.

Part of Speech tagging is the process of identifying the structural elements of a text document, such as verbs, nouns, adjectives, and adverbs.

Most languages follow some basic rules and patterns that can be written into a computer program to power a basic Part of Speech tagger. In English, for example, a 
number followed by a proper noun and the word “Street” most often denotes a street address. A series of characters interrupted by an @ sign and ending with “.com”, 
“.net”, or “.org” usually represents an email address. Even people’s names often follow generalized two- or three-word patterns of nouns.

Nouns and pronouns are most likely to represent named entities, while adjectives and adverbs usually describe those entities in emotion-laden terms. By identifying 
adjective-noun combinations, such as “terrible pitching” and “mediocre hitting”, a sentiment analysis system gains its first clue that it’s looking at a sentiment-bearing 
phrase.

Of course, not every sentiment-bearing phrase takes an adjective-noun form. “Cost us”, from the example sentences earlier, is a noun-pronoun combination but bears 
some negative sentiment.

Accurate part of speech tagging is critical for reliable sentiment analysis, so it’s important that a rules-based system account for these variations.

## How negators and intensifiers affect sentiment analysis
Consider a hotel review that reads,

The bed was super comfy. The chair wasn’t bad, either.
A simple rules-based sentiment analysis system will see that comfy describes bed and give the entity in question a positive sentiment score. But the score will be 
artificially low, even if it’s technically correct, because the system hasn’t considered the intensifying adverb super. When a customer likes their bed so much, 
the sentiment score should reflect that intensity.

Even worse, the same system is likely to think that bad describes chair. This overlooks the key word wasn’t, which negates the negative implication and should 
change the sentiment score for chairs to positive or neutral.

Here’s another example:

The food was pretty good, but I won’t bother coming back.
A simple rules-based sentiment analysis system will see that good describes food, slap on a positive sentiment score, and move on to the next review.

But you (the human reader) can see that this review actually tells a different story. Even though the writer liked their food, something about their experience 
turned them off. This review illustrates why an automated sentiment analysis system must consider negators and intensifiers as it assigns sentiment scores.

## Othr ways:

1. Multi-layered sentiment analysis 
1. Hybrid sentiment analysis system


### Multi-layered sentiment analysis:
Imagine a Yelp review that says,

The linguini was great, but the room was way too dark.
In this document, linguini is described by great, which deserves a positive sentiment score. But room is described negatively. Depending on the exact 
sentiment score each phrase is given, the two may cancel each other out and return neutral sentiment for the document.

As this example demonstrates, document-level sentiment scoring paints a broad picture that can obscure important details. In this case, the culinary 
team loses a chance to pat themselves on the back. But more importantly, the general manager misses the crucial insight that she may be losing repeat 
business because customers don’t like her dining room ambience.

Sophisticated sentiment analysis systems solve this problem by assigning sentiment scores not just to documents, but to individual entities, topics, 
themes and categories as well. The result is a system that, given the same Yelp review, can return:

Entity sentiment: “linguini” (+0.5)
Entity sentiment: “room” (-.25)
Theme sentiment: “dark” (-.25)
Category sentiment: “dining” (+.25)
In this case, the positive entity sentiment of “linguini” and the negative sentiment of “room” would partially cancel each other out to influence a 
neutral sentiment of category “dining”. This multi-layered analytics approach reveals deeper insights into the sentiment directed at individual people, 
places, and things, and the context behind these opinions.


###  Hybrid sentiment analysis system:

Hybrid sentiment analysis systems combine machine learning with traditional rules to make up for the deficiencies of each approach.

![](https://www.lexalytics.com/images/diagrams/sentiment-phrases.png)

Rules-based sentiment analysis, for example, can be an effective way to build a foundation for PoS tagging and sentiment analysis. But as we’ve seen, 
these rulesets quickly grow to become unmanageable. This is where machine learning can step in to shoulder the load of complex natural language processing 
tasks, such as understanding double-meanings.

Most hybrid sentiment analysis systems combine machine learning with software rules across the entire text analytics function stack, from low-level tokenization 
and syntax analysis all the way up to the highest-levels of sentiment analysis.
