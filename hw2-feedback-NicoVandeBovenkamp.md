### ***Project 2 Feedback***

***Nico Van de Bovenkamp***
***

**Overall:** Good work on your exploratory analysis plan! You definitely are on track on the analysis, but try and spend some time on python code/syntax and the language/terms we use in class.

**Some notes**

* **Q.4** Be mindful of how you drop values and 'storing' versus just applying a method. In order to ensure that you have a 'cleaned' dataset, it's best practice to separate your dataframes like so:
```python
df_cleaned = df_raw.dropna()
```
This way you aren't performing your `.corr() ` on `df_raw`
* **Q.9** When discussing distributions, usually we like to discuss the distribution of each variable (or pairings of variables) separately. You can discuss multi-nomial distributions (ie. the distributions of how all of these things will behave) but usually we will look at each one. Your answer is definitely right, but be specific about the distribution of *each* variable.

Also, think about how you could apply statistical tests (like a test for normal distributions) to this data in order to inform your reasoning and the model you will build.

* **Q.13** Good point in the data model, but try and think about what model you will/could use. In the next HW we will use a logit/logistic regression, but think about why and research other types of models too! There is no such thing as a one-model solution!
