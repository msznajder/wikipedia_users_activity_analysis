# Wikipedia users activity analysis

In this project we will analyze Wikipedia users activity logs. The analysis is based on Wikimedia Foundation user behaviours dataset that can be found [here](https://github.com/wikimedia-research/Discovery-Hiring-Analyst-2016).

To see the analysis open above Jupyter notebook file or click [here](https://github.com/msznajder/wikipedia_users_activity_analysis/blob/master/wikipedia_users_activity_analysis.ipynb).

## Framing the problem

The analysed dataset contains event logging data which is used by Wikimedia to track a variety of performance and usage metrics to help them build various metrics and make data-driven strategic decisions.

The aim of this analysis is to answer the following questions:

* What is the daily overall click through rate: the proportion of search sessions where the user clicked on one of the results displayed? How does the daily overall click through rate change day-to-day? How does the day-to-day click through rate vary between groups?

* Which results - in terms of position of the result link selected by the user on the search result page - do people tend to try first? How does the results people tend to try first change day-to-day?

* What is the daily overall zero results rate: the proportion of searches that yielded 0 results? How does the zero results rate change day-to-day? How does the day-to-day zero results rate vary between groups?

* What is the relationship between the session length and the number of pages visited in one session?

That means that we will build two metrics needed to answer these questions: click through rate and zero results rate. With them we will analyse different aspects of user activity and also we will explore between variables relations.

## Summary

We analyzed dataset with user behaviour event logging data in order to analyze four different user behaviour aspects in two different test groups.

We observed that the overall click through rate is at 0.2421 level meaning that about 24.21% of overall searches ends with user clicking on a one of returned links. It varies a bit from day to day but in general it keeps close to the mean with rather small standard deviation of 0.005. The click through rate varies between the two test groups. For group a the overall click through rate is 0.2858 and for group b it is 0.1514. Group b day-to-day click through rate is significantly lower than a group day-to-day click through at p<.05. This suggests that treatment applied to group b significantly lowered click through rate in b group - which is not what we aim for - and the group b treatment should not be implemented for all users.

We could see that overall users by far tend to try first search result first. The distribution is positively skewed, so even though the mean here is 2.35, the better central tendency measure will be median value which is as we expected 1. The mean result users tend to try first on average changes very little from day to day circulating around the overall mean 2.35 and median 1 meaning that people in general tend to open first result in search page.

The overall zero results rate is 0.1849 meaning that 18% of all searches ends with zero results. It varies rather minimally with standard deviation of 0.005. The difference between the overall zero results rate for group a and b is minimal: a has 0.1843 value and b has 0.1862 value. However the difference is not significant.

We saw that the average session length is 125.43 seconds with large standard deviation of 250.41 seconds. The average number of pages visited in one session 0.58 pages with standard deviation of 1.18. And as for the relationship between the two there is a positive correlation between session length and number of pages visited and it is quite strong with 0.504 value. The result is kind of intuitive and tells us that when the user spends more time on platform she/he tends to visit more pages.
