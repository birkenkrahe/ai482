

# What will you learn?

-   Machine learning (ML) modeling basics
-   <del>Using supervised and unsupervised ML</del>
-   <del>Identifying customer groups / churn / upselling</del>
-   <del>Case study: using AI on electric grid data</del>
-   <del>Case study: mining retail analytics with AI</del>


# ML basics

Following Mauro/Valigi (2021), we use an online real estate platform
as an example to illustrate how machine learning can work.

The core business problem is matching sellers and buyers. The core
value is the house price. We want to build a machine learning (ML)
model that predicts house prices based on real estate market data.

When a new house comes on the market, we want the AI to predict a
price based on other comparable houses. The AI computes a similarity
measure.

Source of all images: [Mauro/Valigi, 2021](#orgc0e1099).


## Problem

Image: Machine learning problem: predict the best price for homes
listed on a real estate platform.

![img](./img/problem.png)


## Process

Image: Machine learning phases - training, deployment,
inference.

![img](./img/ml.png)


## Data

Image: Table with features and labels for several examples.

![img](./img/data.png)

Both features and labels are variables. Features are
given/independent, and labels are targets/dependent. The label
variables are what we want to predict.

![img](./img/data1.png)

The available data is split into training and test sets. The
training data is used to make the model learn, and the test data is
used to test the model on unknown data, simulating the real-world
application.


## Programming

How does this kind of program relate to traditional rule-based
programming?

![img](./img/programming.png)


## Concepts

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">ML algorithm ("the AI")</td>
<td class="org-left">Allows computers to learn from data</td>
</tr>


<tr>
<td class="org-left">Features</td>
<td class="org-left">Model input, characteristics of an object that the AI can learn from</td>
</tr>


<tr>
<td class="org-left">Label</td>
<td class="org-left">Model output or target we want the AI to predict</td>
</tr>


<tr>
<td class="org-left">Training</td>
<td class="org-left">Phase when the AI is fed with past features to learn patterns</td>
</tr>


<tr>
<td class="org-left">Model</td>
<td class="org-left">Output of the training phase, capable of making predictions</td>
</tr>


<tr>
<td class="org-left">Inference</td>
<td class="org-left">Phase in which the model is used with new examples</td>
</tr>


<tr>
<td class="org-left">Training data</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">Test data</td>
<td class="org-left">&#xa0;</td>
</tr>
</tbody>
</table>

Image: illustration of a supervised learning algorithm.

![img](./img/supervised.png)  


## Discussion

-   How does machine learning relate to the "intelligent agents"
    concept?
-   What do you think are the advantages and disadvantages of this
    approach?


# References

<a id="orgc0e1099"></a> Mauro/Valigi (2021). Zero to AI - a nontechnical,
hype-free guide to prospering in the AI era. Manning. [Online:
manning.com](https://www.manning.com/books/zero-to-ai).

