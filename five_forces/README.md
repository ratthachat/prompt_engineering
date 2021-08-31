# Michael Porter's 5 Forces Analysis

_Reference:_ 
* https://en.wikipedia.org/wiki/Porter%27s_five_forces_analysis
* https://www.investopedia.com/terms/p/porter.asp

## Introduction
**Porter's Five Forces** is a business analysis model that helps to explain why various industries are able to sustain different levels of profitability.
The Five Forces model is widely used to analyze the industry structure of a company as well as its corporate strategy.
1. Competition in the industry
2. Potential of new entrants into the industry
3. Power of suppliers
4. Power of customers
5. Threat of substitute products

## Why it matters
Five force analysis is truly essential when an investor want to invest in a certain company.
This kind of analysis is usually done by business analyst experts and quite costly.

## What's this prompt doing

**Input Example (after prompt) - A Company Name**
```
Coursera
```

**Output Example (Bold fonts are added for readability)**

```
##Overview:
Coursera retains its industry position by improving business efficiency in addressing competitive challenges. 
The firm faces significant threats from substitutes and new entry, yet it has the potential to actively address these external factors through effective strategies. 
For example, Coursera can improve its operations management strategy to enhance business efficiency in addressing competitive challenges. 
In addition, the social networking company can develop innovative products and services that will attract customers. 
These efforts can help the company retain its market share.

**Competitive Rivalry or Competition with Coursera**
Coursera’s competitive rivalry is high, as the company faces competition from other companies offering online courses and related services. 
This element of Porter’s Five Forces Analysis model determines how competitors affect the firm’s industry environment. 
The following external factors lead to the high competitive rivalry against Coursera:

Small number of firms (weak force)
Moderate variety of firms (weak force)
Low switching costs (strong force)

There are only a small number of companies that offer online courses similar to those offered by Coursera. 
Thus, this external factor exerts a weak force against the company’s competitive rivalry. 
However, Coursera faces competition from a moderate variety of firms offering similar products and services. 
In addition, these companies have low switching costs that make it easy for them to shift away from Coursera to other providers of online learning programs. 
This element of the Five Forces analysis shows that Coursera has a hard time maintaining its position in the industry environment because of the strong impact of competitive rivalry. 
Based on this element of the Five Forces analysis model, it is recommended that the company implement strategies that strengthen its position relative to those of rival firms. 
These strategies should include implementing effective operations management approaches that will enhance business efficiency and competitiveness (see Operations Management). 
In addition, Coursera can implement strategies that make its online courses and related services more attractive than those available from substitutes (see Competitive Rivalry). 
Based on these recommendations, Coursera Inc., with an active approach to strategic formulation processes, can develop its competitive advantage in this highly competitive industry environment.

**Bargaining Power of Customers/Buyers against Coursera Inc. (Strong Force)**
Customers exert pressure on Coursera Inc., as they determine what they want from the company’s online learning programs and related services. 
The impact of consumers or buyers on this social networking firm’s industry environment is measured in this element of Porter’s Five Forces Analysis model. 
The following external factors lead to the strong bargaining power of customers/buyers against Coursera:

High demand from buyers (strong force)
High switching costs (strong force)

Coursera’s online courses and related services are highly demanded by consumers. 
This external factor exerts a strong force on the company. In addition, it is easy for students to switch to other online learning programs because of the low switching costs. 
This external factor also exerts a strong force on the company. 
Based on these external factors in the Five Forces analysis, Coursera Inc., as an online education firm under conditions of high demand by buyers and low switching costs, 
faces significant pressure from customers or buyers. To maintain its competitive position in relation to competitor firms (see Competitive Rivalry), 
Coursera has to focus its strategic formulation processes on customer relationships management strategies that will help it gain high satisfaction ratings from these customers. 
These strategies can make Coursera’s business more profitable through higher revenues and profits, among other benefits (see Operations Management). 
In addition, if Coursera does not address this issue involving buyer bargaining power, the firm may face lower business efficiency and profitability in its industry environment. 
In summary, this element of Porter’s Five Forces Analysis model shows that Coursera has a weak position relative to buyers or customers in its industry environment because of high customer bargaining power.

**Threat of Substitutes or Substitution against Coursera Inc. (Strong Force)**
Coursera faces competition from substitute products offered by other providers of online courses and related services similar to those offered by this social networking company.
The impact of substitutes is considered in this element of Porter’s Five Forces Analysis model as one aspect that determines how competitors affect a company’s industry 
environment. The following external factors lead to strong threat of substitutes against Coursera:

High availability of substitutes (strong force)
Moderate cost difference between substitutes and Coursera Inc.(weak force)
High degree of substitution/use for alternatives(strong force)

Coursera provides similar products and services to those provided by other companies offering online courses and Internet-based video lectures for college credit 
at colleges around the world .This fact leads to significant availability for substitute products that could pressure the firm’s performance in its industry environment .
In addition, these substitute products are less expensive than those offered by Coursera .The cost condition also exerts a strong push against this company .
In relation ,the ease with which users can shift their preferences towards alternative providers makes it easy for them shift away from Coursera towards other competitors 
offering comparable products or services .This element is an external factor that exerts a strong push against the business.
```

The full prompt to generate this kind of five forces analysis can be found [here]()

**Suggested Parameters:** 

* GPT-3 Davinci, Temperature 0.3, Top-p 0.99.
Top-p is suggested to be 0.99 so that we eliminate the long-tail outlier which mostly goes out of context

* Jurassic Jumbo , Temperature 0.8, Top-p 0.99. Here the good temperature is 0.7 since Jurassic has 250k candidate tokens (5x of GPT-3). When sampling, we can see that top-10 tokens are very similar and will lead to the same sentence. Therefore, we have to increase optimal temperature a bit more than GPT-3 so that alternative tokens will got a chance.
