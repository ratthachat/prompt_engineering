# Commonsense Reasoning in Story Comprehension

_Reference: Marvin Minsky, [The Emotion Machine](https://web.media.mit.edu/~minsky/). Simon & Schuster, 2006_

## Introduction
**"Fred told the waiter he wanted some chips" .**

By reading this one sentence, it is amazing that us, human being, know many related (highly possible) information, not written in the sentence at all.

We know Fred was in a restaurant. We know Fred was a customer dining here. We know that the waiter and Fred were only few feet apart. We know Fred wanted a potato chips, not some wood chips. We know that within several minutes, the chips should be ready for Fred. And many more.

How do we all know that? This is the power of **commonsense**. 

## Why it matters
Supplied by commonsense information, _even with a very short original information_ like the above sentence, human is usually able to imagine a sufficient information as if she can _"see"_ the whole context. Thus, commonsense reasoning implicitly helps human to _understand_ the whole picture, and hence able to make a reasonable decision and action regarding to an original given information. 

In contrast, without commonsense, 

As you can see above, in human reasoning and thinking, we all use **a lot of information** induced by a commonsense to analyze and make a decision. Since this commonsense is by definition _common_ to most human, we usually ignore them when we communicate (speaking or writing). Therefore, machine would not understand a situation as good as human.

## What's this prompt doing
A prompt to analyze a given story in 8 principal commonsense reasoning dimensions. Details of these commmonsense reasoning analysis of large-language model can be found in [this blog](https://agi.miraheze.org/wiki/GPT3_and_Commonsense_Reasoning).

The full prompt to generate this kind of commonsense analysis can be found [here](https://github.com/ratthachat/prompt_engineering/blob/main/common_sense/gpt3_commonsense_prompt.ipynb).

**Input Example (after prompt)**
```
Alien race seeking refuge landed on earth on a small island in the south pacific. 
For a hundred years they've managed to keep the island cloaked and secret from our human population. 
But now they've exhausted the resources.
```

**Output Example**
![image](https://github.com/ratthachat/prompt_engineering/blob/main/common_sense/alien_best.png)


