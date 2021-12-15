# Used Car Data Analysis
---
*This project is for DATS6101 paper, group name PatternSix*

## Background
As it is widely known, for the last year and a half the world has been dealing with an unprecedented event: the corona virus pandemic. While this affected many areas of people’s lives, one thing that many did not talk about was its effects on the global supply chain. People stocked up early on during the pandemic, fearing a potential scarcity in finding some of the most commonly available consumer items. For example, hygienic wipes was one of the most popular scarce items for many months, most large market chains, CVS-target-Safeway, limited people from buying more than one swipe at once.

While the world is recovering from this once in a hundred years phenomena, car market was also hit by the sudden changes. In many countries around the world, it is very hard to find first hand cars (Isidore, 2021) and because of that reason, more and more people are looking to the used car market. For this reason Team PatternSix found it fit to take a deep dive in to the used car market and help potential buyers/sellers to get the best prices for the specific features that they are looking for.

As prospective data scientists, Team PatternSix wanted to take a recent issue at hand just like a true data scientist does and explain the findings using the best up to date data analysis and data visualization techniques. PatternSix found the Belarus Car Market data particularly interesting due to the fact that not only the data set had the necessary amount of multi-level variables but also because of the fact that the team saw that there was a story to tell to the common consumer.

## Introduce of Data
The dataset is collected from various web resources in order to explore the used cars market and try to build a model that effectively predicts the price of the car based on its parameters (both numerical and categorical).

The data is scraped in Belarus (western Europe) on the 2nd of December 2019, with 38521 rows and 18 features. There are 6 numerical features and 12 categorical features.

Dataset Link: https://www.kaggle.com/lepchenkov/usedcarscatalog?select=cars.csv

## Results
Overall, PatternSix’s work involved removing the null values for data pre-processing, data exploratory, normality check, finding the correlation between continuous variables, and finding the mean price difference between multiple categorical variables. The technologies used included a table summary, normality tests, t-test, ANOVA, and Chi-square test. The team used a variety of plots such as bar plot, scatter plot, box plot, Q-Q plot, and histogram to support different tests.

For more details, PatternSix deleted ten null values in the data pre-processing part. Then the team generated a table to show the basic statistical measurements of numeric data. The price of this data offers mean=6640 and standard deviation=6430. The other two measurements that may be considered are skewness and kurtosis. These two statistical values indicated that the data were highly skewed.

Based on these results, PatternSix checked the normality of continuous data by using Q-Q plot, histogram, and Kolmogorov-Smirnov normality test. The normality tests showed significant evidence to reject the null hypothesis. Thus, the price was not a normal distribution. The other continuous variables showed the same results. Therefore, for the future work, if PatternSix needs to use price as the dependent variable to create a regression, the team will transform the data to a normal distribution.

The team used a correlation plot for checking the correlation between continuous variables. Year of production was highly correlated with price with correlation coefficient(cc)=0.7. Odometer value had a negative correlation with year produced (cc=-0.49) and price (cc=-0.42). Engine capacity also had a positive correlation with price (cc=0.30).

After that the team generated other exploratory data analysis for the feature that the team was more concerned about – price.

The bar plot of the average price of the car in different years showed that the vintage cars produced around the year 1965 are pricier than the newer cars. And the price increased steadily after around 1985. The box plots and t-tests suggested the solid statistical significance of the difference between the mean price of vehicles with a warranty and without warranty and diesel and gasoline engine types. In the analysis, one-way and two-way ANOVA were used to check the difference between more than three levels of categorical data and price. The results suggested that color, manufacturer name, and body type had mean price differences.

According to the above analysis, the features that influence the prices of cars in the used car market in Belarus are year of production, body type, manufacture name, engine capacity, odometer value, engine type color, and transmission.

In the second part of the work, PatternSix generated some regressions with price of cars. Combined with testing results from different methods shown in the table, PatternSix decided to choose the Partial Least Square model with variables of coefficient with at least 99% confidence as the final one. 

After conducting the EDA and hypothesis tests on the data, the team has concluded that the initial SMART research question were successful answered.

## References
Ben Ellencweig, Sam Ezratty, Dan Fleming, and Itai Miller. (2019, June 6). Mckinsey & Company. Retrieved from Mckinsey & Company Website:
https://www.mckinsey.com/industries/automotive-and-assembly/our-insights/used-cars-new-platforms-accelerating-sales-in-a-digitally-disrupted-market

Isidore, C. (2021, September 28). Retrieved from CNN Business: 
https://www.wraltechwire.com/2021/09/28/bad-news-car-buyers-chip-shortage-supply-chain-woes-are-worse-than-we-thought/

AC Atkinson (1982). Plots, Transformations and Regression: A Introduction to Graphical methods
of Diagnostic Residual Analysis. Oxford University Press.

DA Belsley, E Kuh and RE Welsch (1980). Regression Diagnostics: Identifying Influential Data and Sources of Collinearity. Wiley.

L.E.Frank, J.H.Friedman. A statistical View of Some Chemometrics Regression Tools. Technometrics, 1993， 35 (2): 109 - 135.
