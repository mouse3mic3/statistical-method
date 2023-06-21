---
layout: single
title: Chapter 2 - The Basic of Statistics
permalink: /chapter-2/
toc: True
sidebar:
  nav: "navside"
---

Statistics is often divided into two: descriptive and inferential. Descriptive statistics focuses on describing or summarizing our data in an informative way. It allows us to understand the data without actually reading all of it. 

There are many ways to describe our data. However, it is important to understand some of the terms in statistics that we will be using.

# Samples and Population
The concept of sampling helps us to reduce the amount of data analyzed, while also still being applicable to the general population.

{: .notice--primary}
**Example**\\
The security agents at the airport are responsible for the security of the airport. To ensure that they keep the highest level of security, every passenger and luggage must be screened and inspected physically by the agents. However, this would be impractical as the number of passengers is very high, thus would take a ludicrous amount of time. Instead of inspecting every single passenger, the agents usually select a random passenger for physical inspection. This way, no individual will be guaranteed an expedited screening and we keep the element of ‘surprise’ in the system.

Understanding the concept of population and sample is very important. Below, we will learn the definition of the terms and the example.

- **Target population**\\
  All objects of interest. It is the complete collection of objects with description that matches our interest.
- **Sample**\\
  A subset of target population.
- **Observational unit**\\
  The object from which we collect data.
- **Sampling unit**\\
  The object that is actually sampled.

<!--
unfortunately, I haven't found a good way to write the following purely in markdown. For examples with bullet points, I will be using html tags.
-->
<div class="notice--primary">

<b>Examples</b><br>
Suppose we want to run a survey to understand how people living in Jakarta would react on an increase in income tax.
<ul>
<li> The <b>target population</b> is all people living in Jakarta, currently working, aged 18 or above, and registered as resident of Jakarta. </li>
<li> Our object of interest is a person, so the <b>observational unit</b> is an individual of the population. </li>
<li> Out of 6 million person in the population group, we randomly select 8000 person as <b>sample</b>. </li>
<li> A list of all resident's name may be used for sampling. The names within the list is the <b>sampling unit</b>. </li>
</ul>

</div>

We usually take a sample systematically, often randomly. This is a method to ensure that everyone in the population is equally likely to be selected as a sample. It also helps eliminate bias in the selection. We will discuss the various sampling strategies in its own chapter.

{: .notice--primary}
**Example**\\
Suppose that we want to know the average IELTS score of all 200 students in Venera High School. We select a sample of 20 students that are our close friends and ask them their score. While this may seem alright, the fact that we prefer to sample the closest person to us is against the idea of random sampling (known as sampling bias). We should not assume that everyone in Venera High School has a similar score to our 20 friends. 

# Central Tendency
It is important to understand and be able to measure the ‘central location’ of our data. Below is the height of basketball players in Venera High School.

| Player Name | Height, in cm |
|:-------------:|:---------------:|
| Haikal      | 180           |
| Adrian      | 178           |
| Leno        | 179           |
| Serena      | 176           |
| Yven        | 180           |
| Sofie       | 182           |
| Rizhal      | 195           |
| Jorginho    | 183           |

## Mean (Average)
We often use the average (mean) of our data to describe its centrality. It is generally a good way to represent a large quantity of data. In the case above, we say that the average height of basketball players in Venera High School is 181.625 cm. It is calculated by the following formula.

$$\begin{align} 
\text{mean} &= \frac{1}{n}\sum_{i}^{n}{x_i} \\
&= \frac{1}{8}(180+178+179+176+180+182+195+183) \\
&= 181.625
\end{align}$$

$x_i$ represents the height of the i-th player. The order does not matter as long as everybody is counted. $n$ represents the number of players, which is $8$.

<!--
==============================
COMPUTE: MEAN
==============================
-->
<details><summary style="font-weight: bold">Compute: Mean</summary><blockquote>

<!--EXCEL-->
<details><summary style="font-weight: bold">Excel</summary><blockquote>
{% highlight plaintext %}

Use the function AVERAGE(...)
=AVERAGE(180,178,179,176,180,182,195,183)

{% endhighlight %}
</blockquote></details>

<!--R-->
<details><summary style="font-weight: bold">R</summary><blockquote>
{% highlight r %}

#Use the function mean(...)
mean(c(180,178,179,176,180,182,195,183))

{% endhighlight %}
</blockquote></details>

<!--Python-->
<details><summary style="font-weight: bold">Python</summary><blockquote>
{% highlight python %}

#Import statistics library and use the function mean(...)
import statistics
statistics.mean([180,178,179,176,180,182,195,183])

{% endhighlight %}
</blockquote></details>
</blockquote></details>
<br>

We now know that the player's height is around 181.625 cm, which is quite high since only two players are actually taller than the average. This is one of the downsides of the mean. It can be influenced by extreme values, which are values that are very far away from the rest. These are what we call ‘outliers’. Rizhal is much taller than the rest, which causes the mean to be higher.

## Median
Another measure of centrality is the median. It is also used to represent the central location of our data, however, it does not get influenced by extreme values. The median is the midpoint of our ordered data. If n (number of data) is even, we take the average of the two midpoints. In our case above, we have 8 players (even).

{: .text-center}
Ordered data: 176,178,179,**180,180**,182,183,195

$$\begin{align} 
\text{median} & = \frac{x_4+x_5}{2} \\ 
& = \frac{180+180}{2} \\ 
& = 180 
\end{align}$$

<!--
==============================
COMPUTE: MEDIAN
==============================
-->
<details><summary style="font-weight: bold">Compute: Median</summary><blockquote>

<!--EXCEL-->
<details><summary style="font-weight: bold">Excel</summary><blockquote>
{% highlight markdown %}

Use the function MEDIAN(...)
=MEDIAN(180,178,179,176,180,182,195,183)

{% endhighlight %}
</blockquote></details>

<!--R-->
<details><summary style="font-weight: bold">R</summary><blockquote>
{% highlight r %}

#Use the function median(...)
median(c(180,178,179,176,180,182,195,183))

{% endhighlight %}
</blockquote></details>

<!--Python-->
<details><summary style="font-weight: bold">Python</summary><blockquote>
{% highlight python %}

#Import statistics library and use the function median(...)
import statistics
statistics.median([180,178,179,176,180,182,195,183])

{% endhighlight %}
</blockquote></details>
</blockquote></details>
<br>

The median also split our data into two groups. The first group contain all values that are lower than the median (to the left) and the second group contain all values that are higher than the median (to the right).

## Mode
The mode represents a value that occurs most often. In the case above, we know that 180 cm occurs twice, while other heights only occur once. Therefore, the mode is 180.

The mode is rarely used when we deal with continuous data (data that contains many decimal values, which we will talk later). However it can be useful when we deal with categorical data or binned data.

## Other Measure of Central Tendency
Other measures that may be used are geometric mean and trimmed mean. These are rarely used, but may be useful in certain use cases.

# Variability
We can already describe the central location of our data, however, we still don’t know how ‘spread out’ it is. The basketball player's height is not exactly 181.625 cm, but somewhere around that number. How do we measure that ‘aroundness’? How far is it from the average value?

{: .notice--primary}
**Example**\\
The concept of measuring variability is more prominent in the case of manufacturing. Suppose that a manufacturer is producing water bottles. Each bottle has the same volume and is supposed to hold exactly 750 mL of water. However, during production, the water inside the bottles varies from 740 mL to 760 mL. Machines are not perfect and may accidentally pour in more or less water than needed. A variability is bound to happen everywhere and it is important for us to measure it. Reducing the variability is usually associated with a more consistent and reliable production process. We will talk more about this in Ch. Experiment Design.

## Range

## Variance

## Standard Deviation

## Interquartile Range (IQR)

# Discrete and Continuous

