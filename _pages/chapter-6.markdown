---
layout: single
title: Chapter 6 - Point Estimation
permalink: /chapter-6/
toc: True
sidebar:
  nav: "navside"
---

# The Concept of Inference
Every day, we face personal decisions. Whether we will bring raincoats or invest in stock A, every decision has consequences. It is difficult to determine the correct decision as there are too many factors to be considered. We may consider the weather and market forecast as a guide, which is better than random guessing.

In previous chapters, we have shown that simply visualizing our data can bring important information that was previously unknown. We make conclusions from the graph, but oftentimes, others would disagree with what we say. !provide example. It is important to know that our intuition is not that great and can be easily fooled. Here, statistics help us to make better decisions by providing selective tools that boost our intuition.

Statistical inference involves drawing conclusions about the population using the data of the sample. We attempt to ‘generalize’ the result found in a small part of the population to the entire population. It is a completely valid technique and is being used all the time.

{: .notice--primary}
**Example**\\
During an economic census, instead of visiting every house and every family, we run a survey on various locations with much smaller samples, aggregating and generalizing the result while also accounting the data from the previous census. We may see different results from different surveys, since the sample taken or the methodologies may be different. Both surveys are valid assuming that their statistical methodologies are valid, too.

Statistics help us estimate the ‘true’ characteristics of a population without actually asking the entire population. This way, we can adjust how many samples are needed and the degree of certainty we get. The characteristics of interest could be mean, proportion, variance, etc. These are what we call **population parameters**. The sample characteristics are called **statistics**.

{: .notice--primary}
**Example**\\
It is also applicable to the basketball player case before. Suppose we wanted to know the average height of all 200 students in Venera High School. Instead of measuring the height of each student, we pick 8 basketball players as the sample and measure their height instead. Then, we can generalize the result by saying that the students in Venera High School have an average height of 182 cm. This would be a valid claim, if the basketball players are representative of the population. In reality, basketball players are usually taller than average since it gives them an advantage. Therefore, the average of 182 cm may be too high for the rest of the population. This highlights the difficulties of sampling, which we will discuss more in Ch. Sampling Procedures.

# Estimation vs. Hypothesis Test
We divide the topic of inference into two main parts: estimation and hypothesis test. 

In **estimation**, we attempt to estimate (or ‘approximate’) the population parameter by using samples. We want to answer, “What is the population’s parameter value?”.

In **hypothesis tests** (also known as statistical tests), we test a hypothesis about the population parameter. We want to answer, “Does the population parameter satisfy a specified condition? e.g Is the population mean > 3?”.

<div class="notice--primary">

<b>Example</b><br>
Consider a study in which we wish to find the effectiveness of a drug product in reducing fever. Each patient’s body temperature is measured before he/she receives the drug and 6 hours after the drug is administered. The data can be used to make inferences about the population either by estimation of hypothesis tests.
<br><br>
<b>By estimation</b>:	“What is the mean decrease in body temperature for the population?”
<br>
<b>By hypothesis test</b>: “Is the mean decrease in body temperature greater than 1?”
<br><br>
In estimation, we want to simply know the parameter value, whereas in hypothesis tests, we want to know whether the value satisfies a given condition.
</div>

# Estimating the Mean
Let’s say that we are interested in estimating the population mean. Remember that we can use the sample to estimate the population. A sample statistic that we can use is the sample mean. After all, the sample mean should be our best ‘guess’ for the population mean, right? But, we may also use the median, geometric mean, or any other central values. How do we know which statistic is the most appropriate one? 

These questions will be answered in another course, ‘Mathematical Statistics’. We will not discuss their derivation here. Instead, we will acknowledge the known ones.

In order to estimate the population parameter, the best ‘point estimate’ is its sample counterparts (with some exceptions). In this case, the sample mean is our best point estimate for the population mean. 

add note

## Confidence Interval
Since we only use samples to calculate the mean, we expect to find some error (the population mean might be slightly different from our sample mean). How do we account for the error? 

In many cases, we may wish to calculate the range of possible values for the mean, also known as the interval. #connect to previous example In previous example, we may # and say that the population ‘true’ mean is 99% ‘guaranteed’ to be in this interval. The interval is known as the **confidence interval (CI)** and the percentage is called the **level of confidence**.

It is common to set the CI to be 95%. Some researchers in quantum physics and other fields may prefer a much higher CI (97.5%, 99%, 99.9%, etc) to ensure high degree of confidence when testing a hypothesis, while others allow lower CI (80%, 90%, etc). In the future, we will discuss more about CI.

### Calculating Confidence Interval, Part I
The level of confidence is generally written as $100(1-\alpha)\%$, where $\alpha$ can be any number between 0 and 1. We can change the value of  as needed. The  is special. It is used to find the Z-value, and the Z-value is needed to calculate the confidence interval.

The Z is a value of a standard normal distribution. Since add note

The higher the confidence, the wider the interval. It means that increasing confidence will result in a lower precision, and vice versa. If the interval is too wide, it would not be informative. If the confidence is too low, the interval may fail to contain the true mean. It is possible to increase confidence while keeping the interval narrow by increasing the sample size.

### Calculating Confidence Interval, Part II
To calculate the CI of the estimate, we recall previously that if we take a large sample, the sample mean will be approximately normal with mean $\mu$ and standard error $\frac{\sigma}{\sqrt{n}}$. We knew from sampling distribution that if we have the interval $\mu \pm 1.96\sigma/\sqrt{n}$, then 95% of all samples that we take will have mean within this interval. Moreover, if our sample mean is within $\mu \pm 1.96\sigma/\sqrt{n}$, the population mean is guaranteed to be within $\bar{y} \pm 1.96\sigma/\sqrt{n}$. This is shown below.

add note

We may say that $\bar{y} \pm 1.96\sigma/\sqrt{n}$ is the interval estimate (or the CI) of the mean $\mu$ with 95% level of confidence. 

add note commonly used Z-value and CI

## Case When $\sigma$ is Known
The previous section explains when the population deviation is known, regardless of the sample size. It also assumes that the data is roughly normal. We may display a histogram, boxplot, or Q-Q plot to see if our data is normal. We will also discuss a normality test by doing hypothesis test in the next chapter.

If the data is believed to not be normally distributed, we may use another type of parametric distribution called Student's t, which will be discussed in the last case.

## Case When $\sigma$ is Unknown
In the case that the population standard deviation is unknown, we may replace (estimate) $\sigma$ with the sample standard deviation (s). This is a valid argument as long as the distribution is close enough to normal and/or we have a very large sample ( > 30 ).

<div class="notice--primary">

<b>Options to replace $\sigma$</b><br>
<ul>
  <li>Use sample standard deviation</li>
  <li>Use known standard deviation from previous studies</li>
  <li>Use $range/4$</li>
</ul>

</div>

## Case When $\sigma$ is Unknown and Sample Size is Small
When the sample size is small and our sample is not close to normal, using the z-value to compute CI may be misleading. Instead, we should use another distribution called Student’s t (or simply t distribution).

add note

## Sample Size Requirement
It is possible to calculate the (minimum) sample size given a desired error level E (or a given confidence interval width).

Previously, the $100(1-\alpha)\%$ confidence interval of the mean estimate $\bar{y} \pm z_{\frac{\alpha}{2}}\sigma/\sqrt{n}$. 

Let $E = z_{\frac{\alpha}{2}}\sigma/\sqrt{n}$ be our error term. Our confidence interval width is $W = 2E$.

Solving for n, we have $n = \frac{z_{\frac{\alpha}{2}}^2\sigma^2}{E^2}$

We may also replace $E$ with $W/2$.

<div class="notice--primary">

<b>Example</b><br>
Venera High School students often use paper to write notes and work on assignments. The amount of paper used has skyrocketed recently nearing the final exam. The school official wants to monitor the average number of sheets used by a student in a day and develop a strategy to reduce its usage. For the estimates to be useful, they must be within 2 sheets of the true mean. Previous studies have shown that a similar high school student uses 7 sheets a day with a standard deviation of 9.3. How many students should be sampled in order to be 95% confident that the estimated number of sheets used will satisfy the level of accuracy?
<br><br>
<b>Solution</b><br>
Since the school does not know the population standard deviation, it is possible to use the number from previous study in a similar high school. We have $s = 9.3$ and $E = 2$. From the given confidence level of 95%, we have $\alpha = 5\%$ and $z_{2.5\%} = 1.96$. Thus,
<br>
$$\begin{align}
n &= \frac{(1.96^2)(9.3)^2}{(2)^2}\\
&= 83.06
\end{align}$$
<br>
When it comes to determining sample size, it is advisable to round it up to the next integer, 84. Venera High School officials would have to collect a sample size of 84 to obtain an estimate of the mean number of sheets used by students, and to be 95% confident that it is within 7 sheets of the true mean.

</div>

<div class="notice--primary">

<b>Example</b><br>
A company is producing a new kind of faucet, which is expected to flow at a rate of 1.6 gpm. The company incorporated a control system during production, which limits the deviation of the flow rate to 0.3 gpm. As part of the monthly routine, the company wants to investigate the average flow rate of faucets produced with 97.5% degree of confidence and interval width of 0.1. How many faucets should the company sample to correctly determine the true average flow rate?
<br><br>
<b>Solution</b><br>
The company has specified a confidence interval width of $W = 0.1$, which correspond to $E = W/2 = 0.05$. The value of $Z_{0.0125}$ is 2.24. Putting the numbers, we have
<br>
$$\begin{align}
n &= \frac{(2.24^2)(0.3)^2}{(0.05)^2}\\
&= 180.63
\end{align}$$
<br>
We found that the company should sample at least 181 faucets to get an estimate of the mean flow rate within $\pm0.05$

</div>

# Estimating the Difference of Two Means

# Estimating the Proportion

# Estimating the Difference of Two Proportions

# Estimating the Variance

# Estimating the Ratio of Two Variances
