## Causal research in Data Science: With reflections on ML fairness and Data monetization

If you are reading this post, chances are, you have already encountered the phrase "causal inference" or "causal research" in the contemporary literature. Althouh this phrase may seem new, we learn to survive using the causal inference. Like we have learned over a period of time that: if someone is bitten by a snake chances of survival is very low, low rainfall is likely to cause lower agricultural yield resulting in the inflation of the food prices, when there is a positive news, stock market is likely to surge, and that a better education is positively correlated with the salary. In summary, we have learned relationships like poison causes death, low rainfall causes rise in food prices, positive news positively impacts stock market, education is necessary for a better renumeration. 

Causal analysis helps us understand, "how"and "why", causes influence their effect. However, there can be certain cases when it may appear that the two phenomenon are related, but it may not be due to a causal relationship. For example, if we study any data we will find a correlation between yellow fingers and lung cancer, but yellow finger is not a cause of the lung cancer.
In the subsequent sections, we will discuss this phenomenon through examples, we will analyze cases when there is a strong association without causation. Which leads us to the famous quote _"correlation is not causation"_ which all of us hear during the first few months of our career from wise looking men.

### Causal research: An overview
Causal research is a very common technique in domains such as Economics, Health and Social sciences where it is extremely crucial to correctly estimate the effect of a particular intervention on the outcome of interest. However, in the world of Machine Learning and Artifical Intelligence, since our focus is more on improving the predictive accuracy of a model rather than understanding the interplay between the variables (among input variables and the outcome), application of causal inference is still in its infancy. 
Although it is un-common to find an exhaustive causal inference performed for common Machine Learning problems, a few techniques that can explain the contribution of each input variable and the outcome, like shapley values, have become popular now a days. But if we are not aware of the causal structure of the underlying data, although we may estimate the association between variable of interest and the outcome correctly, by failing to understand the causal relationships, we may still be at a huge disadvantage.

There are two main reasons why causal inference is not commonly performed while solving a ML problems:
1. We are most interested in the predictive power of a variable rather than its causal relationship with the outcome
2. A few input variables can be the outcomes of other models, hence it may become daunting task to determine the relationship between variables

Causal research will become more and more important in the coming years and is likely to become mainstream due to these reasons:
1. As data is taking the centerstage, firms interested in monetizing their data would like to understand the causal relationship between variables and outcomes of interest in order to correctly value their data assets, similarly institutions investing in the data would like to pay for the variables that are the cause of the outcome of interest rather than just associated with the outcome
2. It will enable firms devise efficient strategies, internet firms are already using causal inference for better understanding the reasons behind a phenomenon, like Google uses causal inference to determine why a page is ranked in a particular manner
3. Causal inference is an important technique to identify and measure bias in a ML model which makes that model unfair, once the source of bias is identified, appropriate corrective measures can be taken to mitigate those biases
4. More and more researchers are getting interested in this domain

### Importance of causal research: Motivation
To understand the situations in which it becomes extremely important to understand the right causal relationship, we will look at a simple example. 

__Example-1:__
The table given below represents the outcome of the test of effectiveness of a medicine on a population, participants in the test and control groups and their recovery status is shown below:

_Treatment group:_

|   | Treatment group  | Recovered with treatment  | Recovery rate  |
|---|---|---|---|
| Male  |100   | 20  |  20% |
| Female  | 100  |  50 | 50%  |
|Overall   | 200  | 70  | 35%  |

_Control group:_

|   | Control group  | Recovered without treatment  | Recovery rate  |
|---|---|---|---|
| Male  |100   | 16  |  16% |
| Female  | 500  |  224 | 45%  |
|Overall   | 600  | 240  | 40%  |


It can be observed that:
1. The overall recovery rate is __40%__ in the control group which is higher than __35%__ recovery rate in the test group
2. Within the sub groups - namely __males__ and __females__, recovery rate of the test group is higher than the control group

Based on the above findings, what shall we conclude about the effectiveness of the medicine ? 
We have encountered a _paradox_, although recovery rate is better within the test sub-groups,overall, recovery rate of the test group is lower than that of the control group. This paradox was first discovered by Simpson, hence it is called _Simpson's paradox_.

We will solve this mystery after learning basics of causal inference. We will also learn about structural causal models which provides us with the capability to put down the assumptions about causal relationship behind a dataset. We will primarly deal with SCM's which can be represented using _directed acyclic graphs_ (__DAG's__). These tools will enable us to represent our understanding of the relationships present in a dataset as well as determine cause and effects present in the data.

### Representing causal assumptions: DAG's

If a phenomenon "A" causes an event or another phenomenon "B" then we say that A causes B. This is represented by diagram shown in figure-1.
Let us revisit the cause and effect relationships we mentioned at the begning and identify "A"and "B":

1. If someone is bitten by a snake chances of survival is very low - Here, A (snake bite) causes B (death)
2. Low rainfall is likely to cause lower agricultural yield resulting in the inflation of the food prices - A (low rainfall) causes B (rise in food prices)
3. When there is a positive news stock market is likely to surge  - A(poistive news) causes B(rise in stock prices)
4. A better education is positively correlated with the salary - A (better education) causes B(rise in salary)

An inquisitive reader will be quick to point out that in all the cases mentioned above, there are multiple intermediate stages which are trigerred before the final effect is realized. For example, it is not the snake-bite itself which causes death, but in fact the poison released by snake bite causes blod clot which may result in cardiac arrest that  results in death. The beauty of causal inference is that we can just focus on cause and effect of interest without bothering about the subsequent intermediate stages. The cause and effect of interest are usually measured variables, although the strength of association will vary depending upon whether there is a common unmeasured/measured cause. We will study this scenario when there is a common cause of both A (cause) and B (effect) of interest.


```
- Explain Simpson's paradox
- Discuss causal models through DAGs
- Role of causal analysis in ML fairness - With example
- Causal analysis for identifying the most important data attributes - With example
```





**My Bold Text, in red color.**{: style="color: red; opacity: 0.80;" }



You can use the [editor on GitHub](https://github.com/codesrepo/codesrepo.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.


### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/codesrepo/codesrepo.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
