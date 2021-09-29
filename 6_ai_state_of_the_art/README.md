
# Table of Contents

-   [Machine learning](#org1f2bece)
-   [AI research-to-production gap](#org15dd107)
    -   [Small data](#org112cada)
    -   [Generalization and robustness](#orge9940e7)
    -   [Change management](#orgebc71f4)
        -   [A naive model](#orgde41672)
        -   [Ideal process model](#orgec68814)
        -   [Building blocks](#org3dab505)
        -   [Glossary](#org6ff95c1)
    -   [Efficiency vs. resilience](#org11d0121)
    -   [Full cycle of machine learning projects](#orgb485870)
    -   [Glossary](#org180c047)
        -   [To be Scientific or not to be Scientific](#orgcbf27a0)
        -   [Cloud and edge implementation](#org0d09b15)
        -   [Design pattern](#org5858cd8)
        -   [Softmax model](#orgd194534)
        -   [Hyperparameters](#org077aad6)
        -   [Bounding box](#org39bcf66)
    -   [Summary](#org36389d5)
    -   [Further information](#orgbc9220d)
-   [References](#org7ebdb34)



<a id="org1f2bece"></a>

# Machine learning

After looking at the [history of AI](https://github.com/birkenkrahe/ai482/tree/main/4_ai_history), and some of the foundations of a
dominant AI methodology ([intelligent agents](https://github.com/birkenkrahe/ai482/tree/main/5_ai_agents)), we need to take stock
of what AI actually achieves today, and why it's such a hot
topic. It turns out that most of the running AI applications
("production AI") is related to machine learning (ML), i.e. learning
agents, especially supervised learning - recognizing (= classifying)
known patterns learnt from big data samples. Ng's first definition
of ML is Samuel's seminal 1959 definition ([stanfordonline,
2020](#orge0f37fd))<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>:

> Machine learning: field of study that gives computers the ability to
> learn without being explicitly programmed.

Ng gives a list of supervised learning tasks that have successfully
been addressed by machines using a simple I/O model [(Source:
Stanford HAI 2020)](https://youtu.be/tsPuVAMaADY?t=547).

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Input (A)</th>
<th scope="col" class="org-left">Output (O)</th>
<th scope="col" class="org-left">ML application</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">email</td>
<td class="org-left">spam? (0/1)</td>
<td class="org-left">spam filtering</td>
</tr>


<tr>
<td class="org-left">ad, user info</td>
<td class="org-left">click? (0/1)</td>
<td class="org-left">online advertising</td>
</tr>


<tr>
<td class="org-left">phone image</td>
<td class="org-left">scratched? (0/1)</td>
<td class="org-left">visual inspection</td>
</tr>


<tr>
<td class="org-left">audio</td>
<td class="org-left">text transcript</td>
<td class="org-left">speech recognition</td>
</tr>
</tbody>
</table>

In most of these, the AI only needs to classify the input as one of
two kinds (0/1), e.g. in spam filtering: spam or not spam. Audio ML
is more complicated, because it relies on understanding natural
language.


<a id="org15dd107"></a>

# AI research-to-production gap

In this video AI researcher Andrew Ng addresses three issues to
explain why ML is not more successful in the real world ([Stanford
HAI, 2020](#org7c626da)). Many academic research results are spectacular, but in
real settings, e.g. hospitals, you don't find AI (except in
embedded, i.e. invisible systems like cameras, sensors etc.).

For details, see student session protocols. Here you find only
technical glossary additions and stuff that was left out of the
protocols.


<a id="org112cada"></a>

## Small data

Examples for [small data algorithms](https://youtu.be/tsPuVAMaADY?t=1054) include GANs and GPT-3.

GANs stands for Generative Adversarial Network (cp. [Wikipedia](https://en.wikipedia.org/wiki/Generative_adversarial_network)),
which is a game theoretical ML application where two neural
networks learn by competing with each other. Originated
in 2014. Here is a nice video introduction ([Serrano, 2020](#org1bf5086)).

GPT-3 is the Generative Pre-trained Transformer 3 (cp. [Wikipedia](https://en.wikipedia.org/wiki/GPT-3))
used especially in natural language processing (NLP), e.g. to
simulate human language. Originated in 2020. Here is an example of
such a simulated conversation between two GPT-3 trained AIs
([Soslow, 2021](#org0916078)).


<a id="orge9940e7"></a>

## Generalization and robustness

It doesn't seem to me as if this problem is well understood though
the problem setting is clear: humans environments are too complex
for using AI applications developed and tested in the lab.

![img](./img/xray.jpg)

*Image: an old X-ray machine (Source: [vintage.es](#orga56a59f))*


<a id="orgebc71f4"></a>

## Change management

Change is a hugely complex issue, partly because of the generality
of the concept, and partly because of the deep-seated knowledge
that behavioral change is usually hard to bring about - the harder,
the more established a behavior is. There is a hundred years of
management literature alone written about it. And of course, almost
all of the serious fiction literature of the world is about
transformative, real change. Still, it is not clear to me if
"change management" isn't an oxymoron.


<a id="orgde41672"></a>

### A naive model

![img](./img/naive.png)

(Source: Society of competitive intelligence)


<a id="orgec68814"></a>

### Ideal process model

![img](./img/accenture.png)

(Source: Accenture)


<a id="org3dab505"></a>

### Building blocks

![img](./img/siemens.png)

(Source: SIEMENS)


<a id="org6ff95c1"></a>

### Glossary

-   [Explainable AI?](https://pubmed.ncbi.nlm.nih.gov/33375658/) ([Linardatos et al, 2020](#orgfd662af)) - XAI
    
    > The field of Explainable Artificial Intelligence (XAI) [&#x2026;] is
    > concerned with the development of new methods that explain and
    > interpret machine learning models,

-   [AI Auditing?](https://www.ey.com/en_gl/assurance/how-artificial-intelligence-will-transform-the-audit) ([Boillet, 2018](#org8d3a776)) - Risk analysis


<a id="org11d0121"></a>

## Efficiency vs. resilience

We didn't really do this topic justice, which is hot right now
because of the pandemic: some argue that society needs to refocus
from optimizing processes to identifying and building structures
that can take pressure and survive crisis situations. This is not
necessarily a contradiction - much depends on one's definitions of
efficiency vs. resilience. I mentioned the origins of the Internet
and packet switching technology as a prime example of resilient
infrastructure design (cp. [Leiner et al, 1997](#org8ba56e6)).

Here is a modern attack on the "relentless pursuit of efficiency"
by a computer scientist whose title says it all: "Engineers and
economists prize efficiency, but nature favors resilience – lessons
from Texas, COVID-19 and the 737 Max" ([Vardi, 2021](#orgcb9dfb2)). In the
comments, you find a few voices disagreeing with this simplistic
setup. In computer science at least, both efficiency and resilience
are important design criteria.

I mentioned this curve from a 2009 article analysing resilience in
the light of the 2008 global financial crisis ([Lietaer et al,
2009](#org4780b51)). It is used to illustrate "Sustainability" as a function of
"Diversity & Interconnectivity" - all of them difficult to measure
and to separate from one another. The model assumes an analogy
between systems in nature and man-made financial systems.

> Image caption (A): Sustainability curve mapped between the two
> polarities of efficiency and resilience. Nature selects not for
> maximum of efficiency, but for an optimal balance between these two
> requirements. Notice that resilience is roughly two times more
> important than efficiency at the optimum. All natural eco-systems
> operate within a fairly narrow range on each side of the Optimum
> point called the “Window of Viability”. (Lietaer et al, 2009)

![img](./img/2009.png)

Specifically on deep learning, here's a recent article by [Thompson
(2021)](#orgbf38140) that attacks deep learning research and production as
non-sustainable in terms of energy expenditure. Similar arguments
are being put forward against blockchain mining (cp. [Sedlmeir et
al, 2020](#org9fdf8c3), for a systematic, scientific discussion)<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup>.


<a id="orgb485870"></a>

## Full cycle of machine learning projects

![img](./img/full.png)


<a id="org180c047"></a>

## Glossary


<a id="orgcbf27a0"></a>

### To be Scientific or not to be Scientific


<a id="org0d09b15"></a>

### Cloud and edge implementation

[Go tiny with TinyML](https://www.tinyml.org/)


<a id="org5858cd8"></a>

### Design pattern

[Check out this tutorial](https://www.tutorialspoint.com/design_pattern/design_pattern_overview.htm) for design patterns in software
development.


<a id="orgd194534"></a>

### Softmax model

This is a logistic regression type model ([technical tutorial](http://ufldl.stanford.edu/tutorial/supervised/SoftmaxRegression/)),
which is common in ML because it performs a binary classification.


<a id="org077aad6"></a>

### Hyperparameters

Values to control the learning process - not derived during
training. They depend on the model used.


<a id="org39bcf66"></a>

### Bounding box

Image processing tool ([explanation](https://keymakr.com/blog/what-are-bounding-boxes/)). Bounding boxes are a form of
labelling image data by drawing a box around classifiable areas.


<a id="org36389d5"></a>

## Summary

-   AI experiences a proof-of-concept to production gap
-   This leads to delayed development and use
-   Challenges include: data, resilience, change
-   AI in practice/production favors debugging skills
-   AI should become an engineering discipline


<a id="orgbc9220d"></a>

## Further information

Stanford HAI (Apr 29, 2021). Healthcare's AI Future: A Conversation
with Fei-Fei Li & Andrew Ng.


<a id="org7ebdb34"></a>

# References

<a id="org8d3a776"></a> Boillet J (Jul 20, 2018). How AI will transform the
audit [video]. [Online: ey.com](https://www.ey.com/en_gl/assurance/how-artificial-intelligence-will-transform-the-audit).

<a id="org8ba56e6"></a> Leiner et al (1997). Brief History of the Internet. In:
Comm. of the ACM Feb 1997. [Online: internetsociety.org.](https://www.internetsociety.org/internet/history-internet/brief-history-internet/#f3)

<a id="org4780b51"></a> Lietaer et al (2009). Options for Managing a Systemic
Bank Crisis. In: Sapiens 2(1). [Online: journals.openedition.org](https://journals.openedition.org/sapiens/747).

<a id="orgfd662af"></a> Linardatos et al (2020). Explainable AI: A Review of Machine
Learning Interpretability Methods. In: Entropy 23(1).  [doi:
10.3390/e23010018. PMID: 33375658; PMCID: PMC7824368](https://pubmed.ncbi.nlm.nih.gov/33375658/).

<a id="org9fdf8c3"></a> Sedlmeir et al (2020). The Energy Consumption of
Blockchain Technology: Beyond Myth. In: Business & Information
Systems Engineering 62:599-608. [Online: link.springer.com](https://link.springer.com/article/10.1007/s12599-020-00656-x).

<a id="org1bf5086"></a> Serrano L (May 5, 2020). A Friendly Introduction to
Generative Adversarial Networks (GANs) [video]. [Online: youtube.com](https://youtu.be/8L11aMN5KY8).

<a id="org0916078"></a> Jack Soslow (Apr 13, 2021). Two AIs talk about becoming
human. (GPT-3) [video]. [Online: youtube.com](https://youtu.be/jz78fSnBG0s).

<a id="org7c626da"></a> Stanford HAI (Sep 23, 2020). Andrew Ng: Bridging AI's
Proof-of-Concept to Production Gap [video]. [Online: youtube.com](https://youtu.be/tsPuVAMaADY).

<a id="orge0f37fd"></a> stanfordonline (Apr 17, 2020). Lecture 1 - Stanford CS229:
Machine Learning - Andrew Ng (Autumn 2018) [video]. [Online:
youtube.com](https://youtu.be/jGwO_UgTS7I?t=2180).

<a id="orgbf38140"></a> Thompson et al (24 Sep 2021). Deep Learning's Diminishing
Returns. [Online: spectrum.ieee.org](https://spectrum.ieee.org/deep-learning-computational-cost).

<a id="orgcb9dfb2"></a> Vardi MY (May 18, 2021). "Engineers and economists prize
efficiency, but nature favors resilience – lessons from Texas,
COVID-19 and the 737 Max".

<a id="orga56a59f"></a> n.a.(3 Feb 2016). 15 Incredible Vintage Photos of People
Getting X-Rays Over the Decades [website]. [Online: vintage.es](https://www.vintag.es/2016/02/incredible-vintage-photos-of-people.html).


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> In the same lecture, Ng relates another, more recent definition
of the kind of problem that ML addresses, called a "well-posed problem":

> A computer is said to *learn* from experience E with respect to some
> task T and some performance measure P, if its performance on T, as
> measured by P, improves with experience E.

In the language of our last lesson, E is the precept, and T could be
any task, no matter how complex, as long as we can define a P.

<sup><a id="fn.2" href="#fnr.2">2</a></sup> A gamer told me about another impact of blockchain mining
popularity: she said it had become hard to get hold of GPUs (graphical
processors needed for high gaming performance).
