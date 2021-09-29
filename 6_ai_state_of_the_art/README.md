
# Table of Contents

-   [Machine learning](#orga22104c)
-   [AI research-to-production gap](#org29e4537)
    -   [Small data](#org7c48978)
    -   [Generalization and robustness](#org3d9de95)
    -   [Change management](#org09bc124)
        -   [A naive model](#org0b21ede)
        -   [Ideal process model](#org6812611)
        -   [Building blocks](#org4e9b06c)
        -   [Glossary](#org9e215bc)
    -   [Efficiency vs. resilience](#orgcff08a1)
    -   [Full cycle of machine learning projects](#orga8cf0f1)
    -   [Glossary](#org0f1b1ce)
        -   [To be Scientific or not to be Scientific](#org90b1a96)
        -   [Cloud and edge implementation](#org46ebfc3)
        -   [Design pattern](#org4aa06c7)
        -   [Softmax model](#org7bb6a82)
        -   [Hyperparameters](#orgbf69919)
        -   [Bounding box](#org9451412)
        -   [DevOps/MLOps](#org21b5138)
    -   [Summary](#orgb259fac)
    -   [Further information](#orgb1a6d90)
-   [References](#org2237804)



<a id="orga22104c"></a>

# Machine learning

After looking at the [history of AI](https://github.com/birkenkrahe/ai482/tree/main/4_ai_history), and some of the foundations of a
dominant AI methodology ([intelligent agents](https://github.com/birkenkrahe/ai482/tree/main/5_ai_agents)), we need to take stock
of what AI actually achieves today, and why it's such a hot
topic. It turns out that most of the running AI applications
("production AI") is related to machine learning (ML), i.e. learning
agents, especially supervised learning - recognizing (= classifying)
known patterns learnt from big data samples. Ng's first definition
of ML is Samuel's seminal 1959 definition ([stanfordonline,
2020](#orgf1e9991))<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>:

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


<a id="org29e4537"></a>

# AI research-to-production gap

In this video AI researcher Andrew Ng addresses three issues to
explain why ML is not more successful in the real world ([Stanford
HAI, 2020](#orgd1cac13)). Many academic research results are spectacular, but in
real settings, e.g. hospitals, you don't find AI (except in
embedded, i.e. invisible systems like cameras, sensors etc.).

For details, see student session protocols. Here you find only
technical glossary additions and stuff that was left out of the
protocols.


<a id="org7c48978"></a>

## Small data

Examples for [small data algorithms](https://youtu.be/tsPuVAMaADY?t=1054) include GANs and GPT-3.

GANs stands for Generative Adversarial Network (cp. [Wikipedia](https://en.wikipedia.org/wiki/Generative_adversarial_network)),
which is a game theoretical ML application where two neural
networks learn by competing with each other. Originated
in 2014. Here is a nice video introduction ([Serrano, 2020](#org3d760c2)).

GPT-3 is the Generative Pre-trained Transformer 3 (cp. [Wikipedia](https://en.wikipedia.org/wiki/GPT-3))
used especially in natural language processing (NLP), e.g. to
simulate human language. Originated in 2020. Here is an example of
such a simulated conversation between two GPT-3 trained AIs
([Soslow, 2021](#org2cf851e)).


<a id="org3d9de95"></a>

## Generalization and robustness

It doesn't seem to me as if this problem is well understood though
the problem setting is clear: humans environments are too complex
for using AI applications developed and tested in the lab.

![img](./img/xray.jpg)

*Image: an old X-ray machine (Source: [vintage.es](#org6615ec7))*


<a id="org09bc124"></a>

## Change management

Change is a hugely complex issue, partly because of the generality
of the concept, and partly because of the deep-seated knowledge
that behavioral change is usually hard to bring about - the harder,
the more established a behavior is. There is a hundred years of
management literature alone written about it. And of course, almost
all of the serious fiction literature of the world is about
transformative, real change. Still, it is not clear to me if
"change management" isn't an oxymoron.


<a id="org0b21ede"></a>

### A naive model

![img](./img/naive.png)

(Source: Society of competitive intelligence)


<a id="org6812611"></a>

### Ideal process model

![img](./img/accenture.png)

(Source: Accenture)


<a id="org4e9b06c"></a>

### Building blocks

![img](./img/siemens.png)

(Source: SIEMENS)


<a id="org9e215bc"></a>

### Glossary

-   [Explainable AI?](https://pubmed.ncbi.nlm.nih.gov/33375658/) ([Linardatos et al, 2020](#orga6d3974)) - XAI
    
    > The field of Explainable Artificial Intelligence (XAI) [&#x2026;] is
    > concerned with the development of new methods that explain and
    > interpret machine learning models,

-   [AI Auditing?](https://www.ey.com/en_gl/assurance/how-artificial-intelligence-will-transform-the-audit) ([Boillet, 2018](#org830cd19)) - Risk analysis


<a id="orgcff08a1"></a>

## Efficiency vs. resilience

We didn't really do this topic justice, which is hot right now
because of the pandemic: some argue that society needs to refocus
from optimizing processes to identifying and building structures
that can take pressure and survive crisis situations. This is not
necessarily a contradiction - much depends on one's definitions of
efficiency vs. resilience. I mentioned the origins of the Internet
and packet switching technology as a prime example of resilient
infrastructure design (cp. [Leiner et al, 1997](#org57c7f7d)).

Here is a modern attack on the "relentless pursuit of efficiency"
by a computer scientist whose title says it all: "Engineers and
economists prize efficiency, but nature favors resilience – lessons
from Texas, COVID-19 and the 737 Max" ([Vardi, 2021](#orgef4a7ae)). In the
comments, you find a few voices disagreeing with this simplistic
setup. In computer science at least, both efficiency and resilience
are important design criteria.

I mentioned this curve from a 2009 article analysing resilience in
the light of the 2008 global financial crisis ([Lietaer et al,
2009](#org0f7dd3e)). It is used to illustrate "Sustainability" as a function of
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
(2021)](#org259a068) that attacks deep learning research and production as
non-sustainable in terms of energy expenditure. Similar arguments
are being put forward against blockchain mining (cp. [Sedlmeir et
al, 2020](#org5d76743), for a systematic, scientific discussion)<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup>.


<a id="orga8cf0f1"></a>

## Full cycle of machine learning projects

The image shows Ng's puzzle picture for machine learning. Coding is
a small part of this picture. The Lyon College data science program
is an attempt to capture many, if not all aspects of this picture,
with different courses (like AI, and modeling), specializations
(like business information systems, and TinyML), techniques (like
Scrum) and tools (like R, and GitHub).

![img](./img/full.png)


<a id="org0f1b1ce"></a>

## Glossary

Even when listening to a talk for a large audience (of experts -
each of which is an expert in his or her tiny area of
specialization), you come across a lot of technical terms and
concepts. When watching such videos or reading blogs you should
always be building your own glossary of terms. It will
progressively make your reading faster and easier, and aid your
understanding of state of the art publications.


<a id="org90b1a96"></a>

### To be Scientific or not to be Scientific

Even today (2021), not only 10 years ago, as Ng claims, many
scientists wouldn't call ML or AI especially scientific. The
reason is that new areas, and especially interdisciplinary areas
(like data science) are considered "under-theorized". I came
across this label in an article on theoretical biology
([Cepelewicz, 2020](#org6eb70e8)): apparently, biology does (so far) not have a
proper concept of what an "individual" is. Some researchers from
the Santa Fe institute for complexity science came up with a
stochastic (mathematical) definition that allows to describe
individuals as well as collections of individuals (like
swarms). Personally, I don't find the theory very convincing at
all, but the point is that even a science like biology (certainly
a few hundred years old already) is still "under-theorized", does
not have "enough" theory, which means that many problems cannot be
described formally and therefore not be investigated
systematically (except empirically, by making experiments,
counting insect legs etc.).

Computer science (and AI/ML as part of it), is in a similar
situation. Ng's suggestion is not to push the theory, but approach
it from a practical perspective, as an engineering science (like a
craft with extra computing power).


<a id="org46ebfc3"></a>

### Cloud and edge implementation

[TinyML](https://www.tinyml.org/) - machine learning at low power on embedded devices. Here's
an example that would've been sci-fi only a few years back:
"Flying Microchips The Size Of A Sand Grain" ([Neuman, 2021](#org41987e6)).

![img](./img/tiny.png)

I've just about decided to invest some of my 2021-22 research
money from the college into buying gear for TinyML experiments in
class. It's not all that expensive (cause it's tiny) - [see "The
Future of Machine Learning is Tiny"](https://www.arducam.com/raspberry-pi-pico-tensorflow-lite-micro-person-detection-arducam/) - and it might make some cool
applications for the data science ML class<sup><a id="fnr.3" class="footref" href="#fn.3">3</a></sup>.


<a id="org4aa06c7"></a>

### Design pattern

[Check out this tutorial](https://www.tutorialspoint.com/design_pattern/design_pattern_overview.htm) for design patterns in software
development. There is a good book on design patterns for
self-study from HeadFirst Labs ([Freeman et al, 2004](#org270ec49)).

The image ([Heer/Agrawala 2006](#org270ec49)) shows a system diagram of 21
various software design patterns.

![img](./img/pattern_map.gif)


<a id="org7bb6a82"></a>

### Softmax model

This is a logistic regression type model (here is a [technical
tutorial](http://ufldl.stanford.edu/tutorial/supervised/SoftmaxRegression/)), which is common in ML because it performs a binary
classification.


<a id="orgbf69919"></a>

### Hyperparameters

Values to control the learning process - not derived during
training. They depend on the model used. An example would be the
number of layers of a deep learning neural network, which remain
unchanged as part of the algorithmic model.


<a id="org9451412"></a>

### Bounding box

Image processing tool ([explanation](https://keymakr.com/blog/what-are-bounding-boxes/)). Bounding boxes are a form of
labelling image data by drawing a box around classifiable areas.


<a id="org21b5138"></a>

### DevOps/MLOps

The IBM definition of DevOps ([Crawford, 2019](#orgdce2fdb)):

> "DevOps outlines a software development process and an
> organizational culture shift that speeds the delivery of higher
> quality software by automating and integrating the efforts of
> development and IT operations teams – two groups that
> traditionally practiced separately from each other, or in silos."


<a id="orgb259fac"></a>

## Summary

-   AI experiences a proof-of-concept to production gap
-   This leads to delayed development and use
-   Challenges include: data, resilience, change
-   AI in practice/production favors debugging skills
-   AI should become an engineering discipline


<a id="orgb1a6d90"></a>

## Further information

Andrew Ng further outlines his ideas on healthcare in [this long
panel discussion](https://hai.stanford.edu/events/healthcares-ai-future-conversation-fei-fei-li-andrew-ng). Earlier this year, he launched a "campaign for
data-centric" (instead of model/algorithm-centered) AI ([Press,
2021](#orgbcf15ad)).


<a id="org2237804"></a>

# References

<a id="org830cd19"></a> Boillet J (Jul 20, 2018). How AI will transform the
audit [video]. [Online: ey.com](https://www.ey.com/en_gl/assurance/how-artificial-intelligence-will-transform-the-audit).

<a id="org6eb70e8"></a> Cepelewicz J (July 16, 2021). What Is an Individual?
Biology Seeks Clues in Information Theory [Blog]. [Online:
quantamagazine.com.](https://www.quantamagazine.org/what-is-an-individual-biology-seeks-clues-in-information-theory-20200716/)

<a id="orgdce2fdb"></a> Crawford A (2019). DevOps [website]. [Online: ibm.com.](https://www.ibm.com/cloud/learn/devops-a-complete-guide)

<a id="orgd73c083"></a> Freeman et al (2004). Head First Design
Patterns. Sebastopol: O'Reilly. [Online: oreilly.com.](https://www.oreilly.com/library/view/head-first-design/0596007124/)

<a id="org270ec49"></a> Heer J/Agrawala M (2006). Software Design Patterns for
Information Visualization. In: IEEE Transactions on Visualization
and Computer Graphics (TVCG), 12(5). [Online: berkeley.edu.](http://vis.berkeley.edu/papers/infovis_design_patterns/)

<a id="org57c7f7d"></a> Leiner et al (1997). Brief History of the Internet. In:
Comm. of the ACM Feb 1997. [Online: internetsociety.org.](https://www.internetsociety.org/internet/history-internet/brief-history-internet/#f3)

<a id="org0f7dd3e"></a> Lietaer et al (2009). Options for Managing a Systemic
Bank Crisis. In: Sapiens 2(1). [Online: journals.openedition.org](https://journals.openedition.org/sapiens/747).

<a id="orga6d3974"></a> Linardatos et al (2020). Explainable AI: A Review of Machine
Learning Interpretability Methods. In: Entropy 23(1).  [doi:
10.3390/e23010018. PMID: 33375658; PMCID: PMC7824368](https://pubmed.ncbi.nlm.nih.gov/33375658/).

Michael (May 5, 2021). Image Processing Techniques: What Are
Bounding Boxes? [Blog]. [Online: keymakr.com](https://keymakr.com/blog/what-are-bounding-boxes/).

<a id="org6615ec7"></a> n.a.(3 Feb 2016). 15 Incredible Vintage Photos of People
Getting X-Rays Over the Decades [website]. [Online: vintage.es](https://www.vintag.es/2016/02/incredible-vintage-photos-of-people.html).

<a id="org41987e6"></a> Neuman S (Sept 23, 2021). Flying Microchips The Size Of A
Sand Grain Could Be Used For Population Surveillance [blog]. [Online:
npr.org](https://www.npr.org/2021/09/23/1040035430/flying-microchip-sand-grain-northwestern-winged).

<a id="orgbcf15ad"></a> Press G (June 16, 2021). Andrew Ng Launches A Campaign For
Data-Centric AI. [Online: forbes.com](https://www.forbes.com/sites/gilpress/2021/06/16/andrew-ng-launches-a-campaign-for-data-centric-ai/?sh=d11550874f57).

<a id="org5d76743"></a> Sedlmeir et al (2020). The Energy Consumption of
Blockchain Technology: Beyond Myth. In: Business & Information
Systems Engineering 62:599-608. [Online: link.springer.com](https://link.springer.com/article/10.1007/s12599-020-00656-x).

<a id="org3d760c2"></a> Serrano L (May 5, 2020). A Friendly Introduction to
Generative Adversarial Networks (GANs) [video]. [Online: youtube.com](https://youtu.be/8L11aMN5KY8).

<a id="org2cf851e"></a> Jack Soslow (Apr 13, 2021). Two AIs talk about becoming
human. (GPT-3) [video]. [Online: youtube.com](https://youtu.be/jz78fSnBG0s).

<a id="orgd1cac13"></a> Stanford HAI (Sep 23, 2020). Andrew Ng: Bridging AI's
Proof-of-Concept to Production Gap [video]. [Online: youtube.com](https://youtu.be/tsPuVAMaADY).

<a id="orga36689c"></a> Stanford HAI (Apr 29, 2021). Healthcare's AI Future: A
 Conversation with Fei-Fei Li & Andrew Ng. [Online: stanford.edu](https://hai.stanford.edu/events/healthcares-ai-future-conversation-fei-fei-li-andrew-ng).

<a id="orgf1e9991"></a> stanfordonline (Apr 17, 2020). Lecture 1 - Stanford CS229:
Machine Learning - Andrew Ng (Autumn 2018) [video]. [Online:
youtube.com](https://youtu.be/jGwO_UgTS7I?t=2180).

<a id="org259a068"></a> Thompson et al (24 Sep 2021). Deep Learning's Diminishing
Returns. [Online: spectrum.ieee.org](https://spectrum.ieee.org/deep-learning-computational-cost).

UFLDL Tutorial (n.d.) Softmax Regression [Website]. [Online:
ufldl.stanford.edu.](http://ufldl.stanford.edu/tutorial/supervised/SoftmaxRegression/)

<a id="orgef4a7ae"></a> Vardi MY (May 18, 2021). "Engineers and economists prize
efficiency, but nature favors resilience – lessons from Texas,
COVID-19 and the 737 Max".

Warden P (Feb 3, 2021). The Future of Machine Learning is Tiny
[Blog]. [Online: arducam.com](https://www.arducam.com/raspberry-pi-pico-tensorflow-lite-micro-person-detection-arducam/).


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

<sup><a id="fn.3" href="#fnr.3">3</a></sup> As I have just learnt, this course (DSC 205) is called
"Introduction to Advanced Data Science" for bureaucratic reasons
having to do with the Lyon college course catalog, but it's going to
be about ML. The other thing I want to spend my money on is
parallelization (this will be a joint project with David Sonnier):
[building a DIY supercomputer](https://medium.com/@leerbardon/build-a-diy-supercomputer-a6461b2087d3)!
