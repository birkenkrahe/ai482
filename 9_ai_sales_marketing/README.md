
# Table of Contents

-   [What will you learn?](#org9487abe)
    -   [Problem: personalization at scale](#orgbdd5d3d)
    -   [Marketing sample problems](#org11e4a1b)
    -   [Predicting churning customers](#org8f7953f)
    -   [Measuring algorithm performance](#orge799e2f)
    -   [Accuracy, precision and recall](#org1fc961a)
        -   [Definitions](#org427b599)
        -   [Business use](#orgb879385)
        -   [Health care application](#org4470b85)
    -   [Perform automatic customer segmentation](#org86e85c4)
        -   [Unsupervised learning = finds labels](#orgd40f4d3)
        -   [Supervised vs. unsupervised learning](#org96c8057)
    -   [Concepts](#org20bdd33)
    -   [Discussion](#orgbf23c2c)
-   [References](#org330ddce)



<a id="org9487abe"></a>

# What will you learn?

-   Customer churn and segmentation decisions
-   Measuring algorithm performance
-   Using supervised vs. unsupervised ML
    
    ---
    
    Image source: [Mauro/Valigi (2021)](#orge16649f), chapter 3


<a id="orgbdd5d3d"></a>

## Problem: personalization at scale

-   Customers respond best to **personalized** messages<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>
-   AI delivers personalization **at scale**<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup>
    
    ![img](./img/segmentation.png)
    
    > "With AI, you can reach personalization at scale, learning about
    > people from their specific actions and characteristics and targeting
    > them for who they really are and not for the handcrafted bucket they
    > fall into."
    
    *Is this statement true? Is "who you really are" hidden in the
    data that you generate as customers?*


<a id="org11e4a1b"></a>

## Marketing sample problems

-   Identifying which customers are likely to leave your service
    ("churn")
-   Identifying which customers are likely to buy a new service
-   Identifying similar customer groups (customer segmentation)
    
    Remember the basic process:
    
    ![img](./img/ml.png)


<a id="org8f7953f"></a>

## Predicting churning customers

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Churn</td>
<td class="org-left">percentage of customers leaving a business over time</td>
</tr>
</tbody>
</table>

-   Label: customer belongs to one of two classes<sup><a id="fnr.3" class="footref" href="#fn.3">3</a></sup>:
    -   Class 0 = not churned (still active)
    -   Class 1 = customer about to churn (jump ship)
-   Identify features
    
    ![img](./img/ml1.png)
    
    *Which phase is missing in this model?<sup><a id="fnr.4" class="footref" href="#fn.4">4</a></sup>*


<a id="orge799e2f"></a>

## Measuring algorithm performance

-   Statistical vs. practical metrics:
    -   Link between stats and decisions not obvious
-   Dealing with errors:
    
    -   Not all errors are the same
    
    ![img](./img/confusion.png)
    *Table: confusion matrix - predictions vs. truth*


<a id="org1fc961a"></a>

## Accuracy, precision and recall

A critical part of developing ML models is to check for
errors. This is unfortunately not straightforward because of the
stochastic nature of the methods. One has to come up with methods
that eliminate false answers (conditional probabilities).


<a id="org427b599"></a>

### Definitions

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Accuracy</td>
<td class="org-left">What's the ratio of correct vs total predictions?</td>
</tr>


<tr>
<td class="org-left">Precision</td>
<td class="org-left">How many predicted customers were really going to churn?</td>
</tr>


<tr>
<td class="org-left">Recall</td>
<td class="org-left">How many customers who churned were predicted?</td>
</tr>
</tbody>
</table>

![img](./img/precisionrecall.png)
*Image: illustration of precision and recall metrics*

![img](./img/metrics.png)
*Table: How to use accuracy, precision and recall metrics*


<a id="orgb879385"></a>

### Business use

Depending on the model accuracy/recall/precision profile, the
model can be employed either to minimize costs of losing
customers, or of retaining customers. Which is more important
depends on the business model.

For example, the way of winning/retaining customers of a digital
subscription service like Netflix or Spotify is very different
from winning/retaining customers of a real retail location like a
physical Walmart store.

![img](./img/business.png)
*Image: focus depends on cost of losing vs. retaining customers*


<a id="org4470b85"></a>

### Health care application

This example illustrates that eliminating stochastic error can be
a life or death issue - it's not always about selling more stuff.

![img](./img/cost.png)
*Image: Implications of confusion on cancer detection*


<a id="org86e85c4"></a>

## Perform automatic customer segmentation

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Segmentation</td>
<td class="org-left">Group customers who share behaviors and characteristics</td>
</tr>
</tbody>
</table>

Typical marketing questions:

-   Should we group people aged 20-25 or those aged 20-29?
-   Can we put large and small city students in one cluster?
-   Should we put males and females in different clusters?

Ways to decide all depend on **patterns**:

-   Go by your gut feeling ("1980s")
-   Look at the data (EDA) and let marketing decide
-   Let AI cluster customer segments


<a id="orgd40f4d3"></a>

### Unsupervised learning = finds labels

> "In unsupervised learning, an algorithm is fed with unlabeled
> examples, and is asked to devide the examples into groups that
> share some similarities."

*Image: How a clustering algorithm works*

![img](./img/clustering.png)


<a id="org96c8057"></a>

### Supervised vs. unsupervised learning

*Image: Input/output differences between supervised and
unsupervised learning*

![img](./img/difference.png)


<a id="org20bdd33"></a>

## Concepts

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Scaling</td>
<td class="org-left">Speed, usability, storage, concurrent access</td>
</tr>


<tr>
<td class="org-left">Personalization</td>
<td class="org-left">Opposite of standardization (or segmentation)</td>
</tr>


<tr>
<td class="org-left">Churning</td>
<td class="org-left">Likelihood of losing a customer</td>
</tr>


<tr>
<td class="org-left">Error measures</td>
<td class="org-left">Accuracy, precision, recall</td>
</tr>


<tr>
<td class="org-left">Confusion matrix</td>
<td class="org-left">True and false positive or negative predictions</td>
</tr>


<tr>
<td class="org-left">Predictor</td>
<td class="org-left">Label generated by a supervised learning algorithm</td>
</tr>


<tr>
<td class="org-left">Unsupervised learning</td>
<td class="org-left">Clustering problem without labels</td>
</tr>
</tbody>
</table>


<a id="orgbf23c2c"></a>

## Discussion

![img](./img/discussion.gif)

-   What are the issues with each of the pattern identification
    methods listed above (gut feeling/EDA/AI)
-   What are some principal technical issues with supervised and
    unsupervised learning?
-   What is the potential cost of letting AI make more and more
    decisions in sales and marketing?


<a id="org330ddce"></a>

# References

<a id="org9f4cacc"></a> Hellstrom (21 Feb 2020). A Tour of End-to-End Machine
Learning Platforms [Blog]. [Online: databaseline.tech.](https://databaseline.tech/a-tour-of-end-to-end-ml-platforms/)

<a id="orge16649f"></a> Mauro/Valigi (2021). Zero to AI - a nontechnical,
hype-free guide to prospering in the AI era. Manning. [Online:
manning.com](https://www.manning.com/books/zero-to-ai).

<a id="org4ea80ee"></a> Stanford HAI (Sep 23, 2020). Andrew Ng: Bridging AI's
Proof-of-Concept to Production Gap [video]. [Online: youtube.com](https://youtu.be/tsPuVAMaADY).

<a id="orged24647"></a> Russel/Norvig (2021). AI a Modern Approach 4th
ed. Pearson. [Online: aima.cs.berkeley.edu.](http://aima.cs.berkeley.edu/)


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> It is worth noting that strict personalization is
philosophically impossible because humans are not machines (or
animals): our preferences change over time, often irrationally so.

<sup><a id="fn.2" href="#fnr.2">2</a></sup> 'Scaling' is a major efficiency quantity in our times of mass
applications. It relates to the ability of anything to apply to large
numbers - ideally at infinitum. "Scaling laws", or power laws,
describe growth where one quantity grows with a power. Exponential
growth is an example. In IT and application development, scaling is
desired for the number of people - e.g. an application on your phone
should scale to any number of concurrent users. This implies demands
on storage, speed, usability, and other characteristics.

<sup><a id="fn.3" href="#fnr.3">3</a></sup> Note that the choice of label depends on the underlying business
model. Digital services like Netflix or Spotify are easier to deal
with since customers have to actively unsubscribe. Food retail is not
so easy: customers don't tell you that they don't intend to come
back.

<sup><a id="fn.4" href="#fnr.4">4</a></sup> Answer: the testing phase. Once the model has been trained on a
part (usually 75%) of the historic (accurate, real) data, it is tested
using the remaining historic data. If it then performs according to
expectation, it is released "into the wilde", that is deployed to
identify labels from existing feature data sets.
