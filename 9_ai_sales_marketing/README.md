
# Table of Contents

-   [What will you learn?](#orgcee987b)
    -   [Problem: personalization at scale](#org03b035f)
    -   [Marketing sample problems](#org7a3cd89)
    -   [Predicting churning customers](#org109b3d7)
    -   [Measuring algorithm performance](#org5662ac3)
    -   [Accuracy, precision and recall](#org0311811)
        -   [Definitions](#org8432080)
        -   [Business use](#orgc8053dc)
        -   [Health care application](#org9bb84b1)
    -   [Perform automatic customer segmentation](#org109c6ac)
        -   [Unsupervised learning = finds labels](#org01e44c3)
        -   [Supervised vs. unsupervised learning](#orgf4dfbd0)
    -   [Concepts](#orgc92bdfc)
    -   [Discussion](#orgda459db)
-   [References](#orgcdc281b)



<a id="orgcee987b"></a>

# What will you learn?

-   Using supervised vs. unsupervised ML
-   Customer churn and segmentation decisions
-   Measuring algorithm performance
    
    Image source: [Mauro/Valigi (2021)](#orgcb9fdcd), chapter 3


<a id="org03b035f"></a>

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


<a id="org7a3cd89"></a>

## Marketing sample problems

-   Identifying which customers are likely to leave your service
    ("churn")
-   Identifying which customers are likely to buy a new service
-   Identifying simlar customer groups (customer segmentation)
    
    Remember the basic process:
    
    ![img](./img/ml.png)


<a id="org109b3d7"></a>

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
    
    *Which phase is missing in this model?*


<a id="org5662ac3"></a>

## Measuring algorithm performance

-   Statistical vs. practical metrics:
    -   Link between stats and decisions not obvious
-   Dealing with errors:
    
    -   Not all errors are the same
    
    *Table: confusion matrix - predictions vs. truth*
    
    ![img](./img/confusion.png)


<a id="org0311811"></a>

## Accuracy, precision and recall


<a id="org8432080"></a>

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

*Image: illustration of precision and recall metrics*

![img](./img/precisionrecall.png)

*Table: How to use accuracy, precision and recall metrics*

![img](./img/metrics.png)


<a id="orgc8053dc"></a>

### Business use

*Image: focus depends on cost of losing vs. retaining customers*

![img](./img/business.png)


<a id="org9bb84b1"></a>

### Health care application

*Image: Implications of confusion on cancer detection*

![img](./img/cost.png)


<a id="org109c6ac"></a>

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


<a id="org01e44c3"></a>

### Unsupervised learning = finds labels

> "In unsupervised learning, an algorithm is fed with unlabeled
> examples, and is asked to devide the examples into groups that
> share some similarities."

*Image: How a clustering algorithm works*

![img](./img/clustering.png)


<a id="orgf4dfbd0"></a>

### Supervised vs. unsupervised learning

*Image: Input/output differences between supervised and
unsupervised learning*

![img](./img/difference.png)


<a id="orgc92bdfc"></a>

## Concepts

&#x2026;


<a id="orgda459db"></a>

## Discussion

![img](./img/discussion.gif)

-   What are the issues with each of the pattern identification
    methods listed above (gut feeling/EDA/AI)
-   What are some principal technical issues with supervised and
    unsupervised learning?
-   What is the potential cost of letting AI make more and more
    decisions in sales and marketing?


<a id="orgcdc281b"></a>

# References

<a id="org38ac8ba"></a> Hellstrom (21 Feb 2020). A Tour of End-to-End Machine
Learning Platforms [Blog]. [Online: databaseline.tech.](https://databaseline.tech/a-tour-of-end-to-end-ml-platforms/)

<a id="orgcb9fdcd"></a> Mauro/Valigi (2021). Zero to AI - a nontechnical,
hype-free guide to prospering in the AI era. Manning. [Online:
manning.com](https://www.manning.com/books/zero-to-ai).

<a id="orge70d617"></a> Stanford HAI (Sep 23, 2020). Andrew Ng: Bridging AI's
Proof-of-Concept to Production Gap [video]. [Online: youtube.com](https://youtu.be/tsPuVAMaADY).

<a id="org262a5d7"></a> Russel/Norvig (2021). AI a Modern Approach 4th
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
