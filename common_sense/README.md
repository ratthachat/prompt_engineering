# Commonsense Reasoning in Story Comprehension

_Reference: Marvin Minsky, [The Emotion Machine](https://web.media.mit.edu/~minsky/), Chapter 6. Simon & Schuster, 2006_

## Introduction
**"Fred told the waiter he wanted some chips" .**

By reading this one sentence, it is amazing that us, human being, know many related (highly possible) information, not written in the sentence at all.

We know Fred was in a restaurant. We know Fred was a customer dining here (and he might feel somewhat hungry). We know that the waiter and Fred were only few feet apart. We know Fred wanted a potato chips, not some wood chips. We know that within several minutes, the chips should be ready for Fred. And many more.

How do we all know that? This is the power of **commonsense**. 

Without commonsense, from the above sentence, we would not be able to guess the relevant information of the given context e.g. the locations, feeling, motivations, events-before and events-after.

Supplied by  **a lot of** commonsense information, _even with a very short original information_ like the above sentence, human is usually able to imagine a sufficient information as if she can _"see"_ the whole context. Thus, commonsense reasoning implicitly helps human to _understand_ the whole picture, and hence able to make a reasonable decision and action regarding to an original given information. 

## Why it matters

Each human individual has accumulatively learned commonsense for several years through real-world interaction, visual perception, formal education and also from communication with other human.

Since the commonsense is by definition _common_ to most human, we usually ignore them when we communicate (speaking or writing).

In the current paradigm of large-language models (LLMs) where a machine learn knowledge mostly from unsupervised texts. Even though the amount of texts fed into the learning process is extremely enormous, _most commonsense information are mostly not explicitly written in those texts. Recent literatures have found out that even a large model usually lacks of commonsense_, see [this blog](https://agi.miraheze.org/wiki/GPT3_and_Commonsense_Reasoning) for more details.

A lack of commonsense reasoning is therefore one of the fundamental reason why LLMs still cannot generate a consistent and highly reasonable texts like human, especially in a long text writing (e.g. a whole book writing).

## What's this prompt doing
This prompt is designed to _test_ a commonsense reasoning of each LLM model on a given story context. 

Given a story context, it will generate texts which are its reasoning on 8 principal commonsense dimensions. See example below. Details of these commmonsense reasoning analysis of large-language model can be found in [this blog](https://agi.miraheze.org/wiki/GPT3_and_Commonsense_Reasoning). 

With the output texts where a model tries to infer on a story, we could see whether a model really understand hidden commonsense information or not. If not, in which reasoning dimensions are the weakness of the current model.

**Input Example (after prompt) - a Story Context**
```
Alien race seeking refuge landed on earth on a small island in the south pacific. 
For a hundred years they've managed to keep the island cloaked and secret from our human population. 
But now they've exhausted the resources.
```

**Output Example**
![image](https://github.com/ratthachat/prompt_engineering/blob/main/common_sense/alien_best.png)

The full prompt to generate this kind of commonsense analysis can be found [here](https://github.com/ratthachat/prompt_engineering/blob/main/common_sense/gpt3_commonsense_prompt.ipynb). As explained in the blog, we illustrate 10 story contexts on various story genres where each story has to be tested one by one. 

**Suggested Parameters:** 

* GPT-3 Davinci, Temperature 0.3, Top-p 0.99.
Top-p is suggested to be 0.99 so that we eliminate the long-tail outlier which mostly goes out of context

* Jurassic Jumbo , Temperature 0.7, Top-p 0.99. Here the good temperature is 0.7 since Jurassic has 250k candidate tokens (5x of GPT-3). When sampling, we can see that top-10 tokens are very similar and will lead to the same sentence. Therefore, we have to increase optimal temperature a bit more than GPT-3 so that alternative tokens will got a chance.
