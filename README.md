# Coursera Data Science 

Here follows a description of the first of the two course projects. Scroll down to see the description of the second. Submissions for the first and second course projects can be viewed in StatInfProj.pdf and StatInfProj2.pdf in this repository, respectively.

## Statistical Inference Course Project 1

### Goal

The topic of the first of the two projects is to verify and illustrate the claims of the Central Limit Theorem in the case of an exponential random variable. By simulation, we check that the sample mean has mean approximately equal to that of the original random variable, and that its standard deviation is approximately equal to that of the original random variable, divided by the square root of the sample size. We also check that the sample mean is approximately normal.

### Data

The data used in this project is simulated using the `rexp()` function in R. Care was taken to make the exercise reproducible by setting the random number generator using the `set.seed()` function.

### Methods

We simulate 1000 samples of size 40 from the exponential distribution. We then plot a histogram of the means of these 1000 samples. We mark the mean of these 1000 means on this histogram along with the theoretical mean, and see that they are close. This visualization is accompanied by a direct calculation of the difference between the two. Next, we similarly mark the standard deviation of the 1000 means on the histogram along with the theoretical standard deviation. We see that they are close, and provide the direct calculation of the difference. Finally, we superimpose the theoretical gaussian distribution over the histogram. We observe that the histogram seems to follow this normal distribution closely. Thus the Central Limit Theorem is verified in this case.

## References

The Central Limit Theorem is extrememly well-known, so information about it can be found in most textbooks on statistics. For the reader's convenience, we provide links to two sources on the subject:

[http://mathworld.wolfram.com/CentralLimitTheorem.html](http://mathworld.wolfram.com/CentralLimitTheorem.html)

[https://en.wikipedia.org/wiki/Central_limit_theorem](https://en.wikipedia.org/wiki/Central_limit_theorem)

## Statistical Inference Course Project 2

### Goal

In this second project, we investigate the effect of vitamin C on the tooth growth in Guinea pigs. To quote the documentation of the data used:

"The response is the length of odontoblasts (cells responsible for tooth growth) in 60 guinea pigs. Each animal received one of three dose levels of vitamin C (0.5, 1, and 2 mg/day) by one of two delivery methods, (orange juice or ascorbic acid (a form of vitamin C and coded as VC)."

In this project, we aim to use statistical inference methods to conclude whether the dose levels and delivery methods have an effect on the growth of teeth in Guinea pigs.

### Data

We use the `ToothGrowth` dataset provided in the R `datasets` package. Its documentation can be viewed [here](https://stat.ethz.ch/R-manual/R-devel/library/datasets/html/ToothGrowth.html).

### Methods

We begin our study by plotting the response variable against the predictors to become familiar with the data. We then perform formal statistical analyses for the two predictors. In the case of delivery method, we use a two-sided Student's t-test and find that the effect of delivery method is not significant at the 0.05 level, although it is close (`p-value = 0.06039`). In the case of dose level, we give a 95% t-confidence interval for the effect of each of the three dose levels. We find that the three intervals do not overlap, and our estimate for tooth length increases with dose level. We therefore conclude that dose level is a significant predictor of tooth length in Guinea pigs.

## References

Information about the Studen't t-test can be found [here](https://en.wikipedia.org/wiki/Student%27s_t-test).
Information about t-confidence intervals can be found [here](http://www.stat.wmich.edu/s216/book/node79.html).
