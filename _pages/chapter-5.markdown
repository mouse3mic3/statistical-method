---
layout: single
title: Chapter 5 - Data Distribution
permalink: /chapter-5/
toc: True
sidebar:
  nav: "navside"
---

# Data Distribution
add note

If our data is distributed similarly to one of the known type of data distribution, then future analysis will be much easier since we can use the properties of known distribution. Our data is simply a collection of random variables. These kind of random variables are called 'parametric'. If we believe that our data does not match any of the known distribution, we call that 'non-parametric'.

# Discrete Probability Distribution
We recall that a discrete random variable is a variable that can only have countable number of values. 

<div class="notice--primary">

<b>Examples</b><br>
Below are some examples of discrete variables
<ul>
<li>Number of people involved in an accident</li>
<li>The number of pen bought by each students</li>
<li>The age difference between oldest and youngest siblings</li>
</ul></div>

## Bernoulli Distribution
The Bernoulli random variable only has two possible values, 0 or 1. It is like answering a yes-or-no question, either we get a 'yes' or a 'no'. Although simple, it forms the basic foundation of many distributions.

{: .notice--primary}
**Example**\\
Suppose we have a coin with two sides (head and tail). The probability for us to get either side of the coin is 50:50. We throw it and get the response, either a head or tail. The response here is a Bernoulli random variable.

### Properties
Bernoulli random variable has the following properties.
- Experiment consists of 1 trial.
- Each trial results in one of two outcomes. It is usually labeled as ‘Success’ and ‘Failure’.
- The probability of a ‘Success’ is .
- The probability of a ‘Failure’ is (1-).
- The Bernoulli random variable X is the outcome. Either 1 for ‘Success’ or 0 for ‘Failure’.

In the example of the coin toss above, we can choose head as the 'Success' or the tail as the 'Success', depending on what we need.

### Formulas
Let $X$ be a Bernoulli random variable ($x$ is the outcome of a coin toss, either $1$ or $0$). It is denoted by $X \sim Ber(\pi)$. Recall that we use uppercase $X$ to denote a random variable, and lowercase $x$ to denote its value.
- **Probability Mass Function**
  
  $$\begin{align}
  P(X = x) &= \pi^{x}(1-\pi)^{1-x}\\
  \text{or}\\
  P(X = 1) &= \pi\\
  P(X = 0) &= 1-\pi
  \end{align}$$

  where \\
  $\pi$ : probability of success, and\\
  $1-\pi$ : probability of failure.

- **Expectation**
  
  $$E[X] = \pi$$

- **Variance**
  
  $$Var(X) = \pi(1-\pi)$$

### Examples

## Binomial Distribution
In Bernoulli, we only run the trial once (i.e we toss the coin once). In Binomial, we toss the coin many times (or similarly, many coins at once). We are interested in the number of heads or tails. The number of heads or tails is a Binomial random variable.

### Properties
- Experiment consists of n identical trials.
- Each trial results in one of two outcomes. It is usually labeled as ‘Success’ and ‘Failure’.
- The probability of a success in a trial is , and  is the same for every trial.
- The trials are independent. The outcome of a trial does not influence the outcome of another trial.\\
  Suppose we toss a fair coin 5 times in a row. On the first toss, we get Head. We still don’t know the outcome of the next tosses and the coin remains exactly the same.
- The Binomial random variable X is the number of ‘Success’ observed during n trials.

As such, Binomial and Bernoulli random variables are related. Binomial with $n = 1$ is a Bernoulli.

### Formulas
Let $X$ be a Binomial random variable, that is $X \sim Bin(n, \pi)$. 
- **Probability Mass Function**
  
  $$\begin{align}
  P(X = x) &= \frac{n!}{x!(n-x)!}\pi^{x}(1-\pi)^{1-x}\\
  \end{align}$$

  where \\
  $x$ : number of success in $n$ trials\\
  $n$ : number of trials\\
  $\pi$ : probability of success in a single trial\\
  $n! = n(n - 1)(n - 2)(n - 3)\cdots(3)(2)(1)$

  The $!$ is known as a factorial operator. An example would be 4! (referred to as four factorial).

  $$4! = 4(4 - 1)(4 - 2)(4 - 3) = (4)(3)(2)(1) = 24$$

  Moreover, the expression $\frac{n!}{x!(n-x)!}$ is known as a combination. We may write it in the form of ${n \choose x}$.


- **Expectation**
  
  $$E[X] = n\pi$$

- **Variance**
  
  $$Var(X) = n\pi(1-\pi)$$

## Geometric Distribution

## Hypergeometric Distribution

## Poisson Distribution

## Other Discrete Distribution

# Continuous Probability Distribution
## Uniform Distribution

## Normal Distribution

## Exponential Distribution

## Chi-Square Distribution

## Other Continuous Distribution

# Sampling Distribution

# Skewness

# Kurtosis
Kurtosis is often said to be ‘the measure of sharpness of a distribution’. Looking at the following figure, it may sound reasonable. But, this description is incorrect. Kurtosis is a measure of the tails and not the peak. High value means more ‘heavy-tailed’ distribution, meaning that we may expect more extreme values.

Of note, there are some softwares that display excess kurtosis rather than kurtosis. Excess kurtosis is found by subtracting 3 from kurtosis. Excess kurtosis is designed such that its value is centered on 0 (as opposed to 3). The normal distribution has kurtosis of 3.

