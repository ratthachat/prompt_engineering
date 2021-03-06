This repository is a personal collection of everything related to prompting which can be thought of as **a new kind of programming.**

**Contents**
* What is prompting and how can we use it?
* My own prompt collection 
    - **expert system prompts:** a step-toward human expert on making thinking and decision-making process in a complex task
    - **commonsense analysis prompts:** extraction of human commonsense, i.e. hidden thinking process, when human makes a reasoning on a given context
* Related literatures on prompt engineering and auto-prompt generation

# Prompting is a new kind of programming

To understand the potential of prompting as a new way of programming or coding, let us consider the example of classifying whether someone tweeter's sentiment is positive or negative (ie. Sentiment analysis):

```
Tweet: "This new music video blew my mind" 
Sentiment: Positive

Tweet: "I hate it when my phone battery dies." 
Sentiment: Negative
```

In conventional programming such as Python, one of the easiest way to achieve this classifier would to use the following Huggingface code:
```python
>>> from transformers import pipeline
>>> classifier = pipeline('sentiment-analysis')

>>> results = classifier(["This new music video blew my mind",
...            "I hate it when my phone battery dies."])
>>> for result in results:
...     print(f"label: {result['label']}, with score: {round(result['score'], 4)}")
```
Then, we will get the following results:
```python
label: POSITIVE, with score: 0.996
label: NEGATIVE, with score: 0.999
```

The code is indeed very simple for an experienced programmer. For comparison, see an example of _not_ using Huggingface [here](https://keras.io/examples/nlp/text_classification_with_transformer/). But wouldn't it be better if we can just use our **everyday-language** as programming like this:

```
>>> Tweet: "I loved the new Batman movie!"
>>> Sentiment: Positive

>>> Tweet: "I am not sure I want this phone. It's too big." 
>>> Sentiment: Negative

>>> Tweet: "This new music video blew my mind" 
```
and get the expected result:
```python
Sentiment: Positive
```

Note that what we did in this example was just giving two examples in natural language, instead of writing a Python code. The given two-examples text is called as a **prompt**.  In short, with **prompting**, coding is done by simply giving few **everyday-language** examples.

## How exactly can we use prompting as a new programming ?
To use prompting as programming like the example above, we need an access to **large-language models (LLMs)**.
We can think of this LLMs as a new programming platform. Therefore, instead of using Python or C++, we use one of the LLMs.

At the moment (August, 2021), there are 3 venues for us to access LLMs 

* **OpenAI's GPT-3**:  We need to submit [this form](https://share.hsforms.com/1Lfc7WtPLRk2ppXhPjcYY-A4sk30) to join the waitlist.
* **AI21's Jurassic**: Everybody can use [Jurassic model](https://studio.ai21.com/) without waiting in the waitlist. Nevertheless, the free version has a limited quota per day.
* **EleutherAI's GPT-J-6B**: An [interactive web demo](https://6b.eleuther.ai/) that does not have a daily limit. *However, GPT-J-6B is the smallest model among the three and its capability on long-text writing could not be compared with the others two.*


## Why prompting ?

The difference between conventional coding and prompting become very elucid when you need a machine to produce human-level outputs like "Blog Writing", "Economic Analysis" and "Chat Bot" where prompting are still relatively easy but conventional programming are extremely difficult (if not impossible).

See my ready-to-use prompt below for this kind of human-level outputs programming.

## Downside of prompting

Prompting also have some downsides. 
* Unstable outputs due to different choices of prompting
* Cost of prompting

First, the prompt has to be carefully designed. Output quality is usually varied due to the quality of the given prompt. In particular, poor-quality prompt would produce a poor-quality output.

The main issue with prompting is: we have too many choices of selecting a prompt text. For examples, in the sentiment analysis example above, we provided two examples (a Batman movie and a big phone), but we could have provided 3-4 examples instead of 2. Also, why don't we provided just 1 example?

In general, _more_ and _diverse_ prompted text usually results in better output than _less_ and _similar_ examples. Therefore, all-else equal, 8-examples prompt is usually better tnan 1- or 2-examples prompt.

We also need examples to be diverse. For instance, the following 2-examples which are _not_ well-diversed would not be better than a single-example prompt.

```
>>> Tweet: "I loved the new Batman movie!"
>>> Sentiment: Positive

>>> Tweet: "I hated the new Batman movie!"
>>> Sentiment: Negative

>>> Tweet: [User input]
```

Another important downside of prompting as a new programming as of now is about its cost. Currently, both GPT-3 and Jurassic give only a few amount of free usage. GPT-3 highest-quality, _Davinci_, model charges $0.06 / 1,000 tokens.

# Prompt Collections
As explained above, since output quality highly depends on quality of a given prompt. _**Prompt engineering**_ is a new field of designing a high quality prompt to best suit the task we want to solve. Hence, prompt engineering becomes very essential to the success of prompting as programming.

There are many existing articles illustrating how we can do a simple prompt engineering for LLMs like GPT-3 or Jurassic on popular tasks like 
* chatbot
* text summarization
* story writing
* text classification, or 
* song writing

Readers may see [this article](https://towardsdatascience.com/20-creative-things-to-try-out-with-gpt-3-2aacee3e2abf) and [this site](https://prompts.ai/) as well as [Jurassic own blog](https://www.ai21.com/blog/ai21-studio-use-cases) for this kind of popular tasks.

The existing prompts are usually able to generate texts in a general aspect. However, in many specific areas where human experts or professionals are needed to write texts e.g. detailed analysis of science, business, economics or politics, the prompts in existing literatures are usually not enough since the existing prompts usually lack of high-quality few examples on each expert task.

## High-Quality Prompts for Expert Systems
In artificial intelligence, an expert system is a computer system emulating the decision-making ability of a human expert. In the early era of artificial intelligence (1970s-1980s), expert systems are designed to solve complex problems by reasoning through bodies of knowledge like if-then rules. However, these if-then rules have been _failed_ to produce a desirable expert system, ended the hype of AI at that time and cause the so-called [AI Winter](https://en.wikipedia.org/wiki/AI_winter).

With the emergence of LLMs and carefully engineered prompts, we now have the new possibility of expert systems. This following is a prompt collection which can be a step-toward an expert-system as followed:

* [Business Analysis using Porter's 5-forces Model](https://github.com/ratthachat/prompt_engineering/tree/main/five_forces)
* Scientific Explanation of Grade-Level Multiple Choices Examinations

## Prompts for Commonsense Analysis
Commonsense is a hidden reasoning process which human use to make a reliable decision and action making. A lack of commonsense reasoning is one of the fundamental reason why LLMs still cannot generate a consistent and highly reasonable texts like human, especially in a long text writing (e.g. a whole book writing).

This prompt is designed to test a commonsense reasoning of each LLM model on a given story context.

* [Commonsense Reasoning in Story Comprehension](https://github.com/ratthachat/prompt_engineering/tree/main/common_sense)

# Related Literatures Regarding Automatic Prompt Generation

* [How many data points is a prompt worth?](https://huggingface.co/blog/how_many_data_points/) - April 2021
* [Calibrate Before Use: Improving Few-Shot Performance of Language Models](https://arxiv.org/pdf/2102.09690.pdf) - June 2021
* [Surface Form Competition: Why the Highest Probability Answer Isn???t Always Right](https://peterwestuw.github.io/surface-form-competition-project/surface_form_competition.pdf) - April 2021
* [The Power of Scale for Parameter-Efficient Prompt Tuning](https://arxiv.org/pdf/2104.08691.pdf) - April 2021
* [Prefix-Tuning: Optimizing Continuous Prompts for Generation](https://arxiv.org/pdf/2101.00190.pdf) - Jan 2021
* [Making Pre-trained Language Models Better Few-shot Learners](https://huggingface.co/blog/how_many_data_points/) - June 2021
* [AutoPrompt: Eliciting Knowledge from Language Models with Automatically Generated Prompts](https://aclanthology.org/2020.emnlp-main.346/) - November 2020
* [Building AGI Using Language Models](https://huggingface.co/blog/how_many_data_points/) - April 2021 (Blog)
* [Methods of prompt programming](https://generative.ink/posts/methods-of-prompt-programming/) - Jan 2021 (Blog)
* [Rationale for a Large Text Compression Benchmark](http://mattmahoney.net/dc/rationale.html) - July 2009 (Blog)
