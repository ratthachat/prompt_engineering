# Michael Porter's 5 Forces Auto Analysis by Large Language Models
![image](https://github.com/ratthachat/prompt_engineering/blob/main/five_forces/five_forces.png)

## Introduction
**Porter's Five Forces** is a business analysis model that helps to explain why various industries are able to sustain different levels of profitability.
The Five Forces model is widely used to analyze the industry structure of a company as well as its corporate strategy. These five forces include:

1. Competition in the industry
2. Potential of new entrants into the industry
3. Power of suppliers
4. Power of customers
5. Threat of substitute products

_Reference:_ 
* https://en.wikipedia.org/wiki/Porter%27s_five_forces_analysis
* https://www.investopedia.com/terms/p/porter.asp

## What's this prompt doing
This prompt is a prototype that can be used to _automatically_ generate five forces analysis for _any companies_ that large language models known at the pretraining time.

## Why it matters
Five force analysis is truly essential when an investor want to invest in a certain company.
The analysis together with a company's strategy will be used to predict the company's future in the long run, and therefore its fundamental valuation.

This kind of analysis is usually done by business analyst experts and is therefore costly. Hence, only the big companies are usually covered.
The auto analysis of five forces, if feasible, will democratize fundamental information of the small and medium companies for investors.

This prototype is far from perfect, but still provides some insights for the investors as illustrated in an example below. Note that the analysis provided by human is usually imperfect too.

Moreover, by random sampling, many different analysis could be generated, and can be thought of as different points of view of many analysts.
As investors need to understand company's risks as clear as possible, the different points of view are indeed valuable in risk management.

# Example
**Input Example (after prompt) - A Company Name**
```
Coursera
```

**Output Example from GPT-3 (Texts are cut, bolded and underlined for readability)**
![image](https://github.com/ratthachat/prompt_engineering/blob/main/five_forces/coursera_five_forces_snippet.jpg)

Note that GPT-3 already has information about the Coursera company from pretraining phase and we haven't include any information beside the prompt which is not related to Coursera. The full prompt to generate this kind of five forces analysis can be found [here]()

## Suggested Parameters

* GPT-3 Davinci, Temperature 0.3, Top-p 0.99.
Top-p is suggested to be 0.99 so that we eliminate the long-tail outlier which mostly goes out of context

* Jurassic Jumbo , Temperature 0.8, Top-p 0.99. Here the good temperature is 0.8 since Jurassic has 250k candidate tokens (5x of GPT-3). When sampling, we can see that top-10 tokens are very similar and will lead to the same sentence. Therefore, we have to increase optimal temperature a bit more than GPT-3 so that alternative tokens will got a chance.

From few experiments, we observe that the output of GPT-3 is a little more of higher quality than Jurassic Jumbo.

