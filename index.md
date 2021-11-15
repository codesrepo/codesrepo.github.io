## Causal research in Data Science: With reflections on fairness and data monetization

If you are reading this post, chances are, you would have encountered, at least once, the phrase "causal inference" or "causal research" in the contemporary literature. Causal research is a very common technique in domains such as economics and drug discovery, where it is extremely crucial to correctly estimate the effect of a particular intervention on the outcome. However, in the world of Machine Learning and Artifical Intelligence models, since our focus is more on improving the predictive accuracy of a model rather than understanding the interplay between input variables and the outcome, causal inference is not frequently applied. 

Although it is un-common to find an exhaustive causal inference performed for the problems which are solved by Machine Learning models, a few techniques which can explain the contribution of each input variable to the outcome, like shapley values, have become popular now a days. But if we are not aware of the causal structure of the underlying data, although we may estimate the association between variable of interest and the outcome correctly, by failing to understand the causal relationship, we may still be at a huge disadvantage.

In the subsequent sections, i'll explain this phenomenon through examples when there is strong association without causation. Which leads us to a famous quote "correlation is not causation" which all of us hear during the first few months of our career from wise looking men. 

There are two main reasons why causal study is not common while solving ML problems:
1. It can be a daunting task to take consider of variables for causal analysis when underlying causal structure is poorly understood
2. We are most interested in the predictive power of a variable rather than its causal relationship

Causal research will become more and more important in the coming few years and is likely to become mainstream due to these reasons:
1. As data is taking the centerstage, firms interested in monetizing their data would like to understand the causal relationship between variables and outcomes of interest to correctly value their data assets, similarly institutions investing in the data would pay for variables that are the cause of outcome
2. It will enable firms device efficient strategies, internet firms are already using causal inference for better understanding the reason behind a phenomenon, like Google uses causal inderence to determine why a page is ranked the way it is
3. More and more researchers are interested in this domain





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
