
# Table of Contents

-   [AI applications that might change the world](#orga4bb81f)
-   [Agents and environments](#orgbd1496b)
    -   [Microworld-view](#org2cb2de7)
    -   [Rational agent success](#orgc1410f7)
    -   [Example: robotic vacuum-cleaner](#org94bdf42)
    -   [Definition of a rational agent](#orga3ae865)
    -   [Process view](#org16e3ba3)
-   [Task environments](#org430e761)
    -   [Current research](#org9ddfa4e)
    -   [Remote Mars rover navigation](#org02fbd03)
    -   [PEAS example: automated taxi driver](#org2628541)
    -   [PEAS Challenge](#org475e24e)
    -   [Task environment properties](#org4227a5d)
    -   [Environment of the automated taxi driver](#org4087b7f)
    -   [Systemic interpretation](#org228fee9)
    -   [Homework](#org4b4b113)
-   [Agent structure and types](#org239b125)
    -   [Table-driven agent programs](#org18e44b3)
    -   [Simple reflex agents](#org76a0329)
    -   [Model based agents](#org1705f1d)
    -   [Goal based agents](#org98a7807)
    -   [Utility based agents](#orgbe9b833)
    -   [Learning agents](#orgd3d0adc)
    -   [All types](#org1c2393c)
    -   [Other classifications](#orgef2f209)
-   [AIMA Exercises](#org98e8f4d)
    -   [Briefing: DIY](#orgb412eb6)
    -   [Relationship between evolution and &#x2026;](#org8c10df1)
    -   [Syllogisms](#orgfeaa7f7)
    -   [PEAS](#orgaefe93e)
    -   [Glossary](#org4b48f71)
    -   [Coding](#org2c11199)
    -   [Hardware](#orgb1557ff)
-   [References](#orgff8124c)
    -   [Publications](#orgc930aa2)
    -   [Websites](#org2cd68e5)
-   [Whiteboards](#org87ae5d4)



<a id="orga4bb81f"></a>

# AI applications that might change the world<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-right" />

<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-right">No</th>
<th scope="col" class="org-left">AI APPLICATION</th>
<th scope="col" class="org-left">TYPE</th>
<th scope="col" class="org-left">AI FIELD</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-right">1</td>
<td class="org-left">Alexa/Siri/<a href="https://mycroft.ai/">MyCroft</a></td>
<td class="org-left">Conversational agent</td>
<td class="org-left">Natural Language Processing</td>
</tr>


<tr>
<td class="org-right">2</td>
<td class="org-left">Autonomous vehicles</td>
<td class="org-left">Driving agent</td>
<td class="org-left">Pattern recognition</td>
</tr>


<tr>
<td class="org-right">3</td>
<td class="org-left">Autonomous drones</td>
<td class="org-left">Delivery agent</td>
<td class="org-left">Pattern recognition</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-right">4</td>
<td class="org-left"><a href="https://neuralink.com/">Neuralink</a></td>
<td class="org-left">Brain support agent</td>
<td class="org-left">Neuroscience</td>
</tr>


<tr>
<td class="org-right">5</td>
<td class="org-left"><a href="https://about.fb.com/news/2021/09/introducing-ray-ban-stories-smart-glasses/">Facebook Glass</a></td>
<td class="org-left">Social media agent</td>
<td class="org-left">Pattern recognition</td>
</tr>


<tr>
<td class="org-right">6</td>
<td class="org-left"><a href="https://www.jarvis.ai/">Automatic writing</a></td>
<td class="org-left">Writing agent</td>
<td class="org-left">Natural Language Processing</td>
</tr>


<tr>
<td class="org-right">7</td>
<td class="org-left"><a href="https://openai.com/blog/openai-codex/">Automatic programming</a></td>
<td class="org-left">Programming agent</td>
<td class="org-left">Natural Language Processing</td>
</tr>
</tbody>
</table>


<a id="orgbd1496b"></a>

# Agents and environments

The purpose of this section is to bridge the gap between AI ideas
and practice. To do this, we adopt the rational agent approach
promoted in [AIMA](#org6d281a3), and implemented in day-to-day AI systems, like
robot vacuum cleaners that operate in the real world, or
personalized shopping apps that operate in virtual commercial space.

The abstract insights about rational agents are useful as an
analytic framework, much like the distinction between supervised and
unsupervised learning that we will look at next.

These lecture notes corresponds to some of the chapter 2 content of
the textbook ([Russell/Norvig](#org6d281a3), 2021).


<a id="org2cb2de7"></a>

## Microworld-view

The diagram shows a world- or space-oriented view of an agent and
its environment. The microworld view is less intuitive than the
process-view<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup> - think about your learning as a student: you
don't dwell on the fact that you move from your personal into
classroom space - and it would be difficult to see how to optimize
this spatial movement (for learning). Instead, you operate - like
an agent - with process steps (go to class, listen to lecture, do
exercise, take notes etc.). It is easier to think of input and
output and optimizing functions when following a process<sup><a id="fnr.3" class="footref" href="#fn.3">3</a></sup>.

![img](./img/agents.png)

Source: [AIMA](#org6d281a3) - agent-world vs. environment view


<a id="orgc1410f7"></a>

## Rational agent success

Success of a rational agent in this simple picture depends on:

1.  the performance measure that defines success
2.  the agent's knowledge of the environment
3.  the actions that the agent can perform
4.  the agent's percept sequence to date


<a id="org94bdf42"></a>

## Example: robotic vacuum-cleaner

The microworld of the vacuum cleaner has a known boundary, and it
is divided in subspaces that the agent can navigate. In each
subspace, there is an unspecified amount of dirt. The overall
mission is to clean the space.

![img](./img/vacuum.png)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">ASPECT</th>
<th scope="col" class="org-left">EXAMPLE</th>
<th scope="col" class="org-left">FUNCTIONS</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Performance</td>
<td class="org-left">Award cleanliness</td>
<td class="org-left">Maximize</td>
</tr>


<tr>
<td class="org-left">Environment</td>
<td class="org-left">Spatial dimensions</td>
<td class="org-left">Minimize</td>
</tr>


<tr>
<td class="org-left">Actions</td>
<td class="org-left">Movements + sucking</td>
<td class="org-left">Table</td>
</tr>


<tr>
<td class="org-left">Perceptions</td>
<td class="org-left">Location + dirt</td>
<td class="org-left">Table</td>
</tr>
</tbody>
</table>

Can such a simple agent behave irrationally, too?<sup><a id="fnr.4" class="footref" href="#fn.4">4</a></sup>

It is worth noting that irrational behavior in humans can lead to
unforeseen (and unforeseeable) innovations and optimizations, but
also, of course, to destructive behavior. In fact, one could argue
that controlled irrationality is the core of creative behavior and
originality.


<a id="orga3ae865"></a>

## Definition of a rational agent

> "For each possible percept sequence, a rational agent should select
> an action that is expected to maximize its performance measure,
> given the evidence provided by the percept sequence and whatever
> built-in knowledge the agent has." ([AIMA](#org6d281a3))


<a id="org16e3ba3"></a>

## Process view

The definition suggests a process-oriented description of the
behavior of a rational agent. Such a process is shown in the BPMN
diagram below.

![img](./img/agents_and_environments.png)


<a id="org430e761"></a>

# Task environments

The greatest challenge for the agent is operating in a given
environment. To design agents that can manage this challenge, we
classify different types of environments.


<a id="org9ddfa4e"></a>

## Current research

Recent article: "Solving the Robot Off-Loading Problem": helping
robots choose when to communicate with the cloud without latency or
lost data issues ([Myers, 2021](#org22e38ef)).

![img](./img/drone.jpg)


<a id="org02fbd03"></a>

## Remote Mars rover navigation

In 2015, the then-VP of the German software giant SAP demonstrated
remote control of a Mars rover during an SAP developers conference
presentation - using the 2015 feature film "The Martian" as a
prompt.

Since the presentation is quite long, I cut it into 7 different
parts and put it into [this playlist](https://youtube.com/playlist?list=PL6SfZh1-kWXnWedFzgEwt6R6zhjdBxJsT) for classroom use. The demo
uses every software layer indicated in the diagram below. And
rather than only talk about stuff, the presenter shows how it is
done and how all these different systems work together.

Of course, the talk is steeped in technical and commercial language
that you will not understand - but hopefully, with my comments
(below each video) and the glossary below, you'll be able to follow
the story. Enjoy!

![img](./img/sap.png)

Image explanation: SAP system architecture on premise (local, at
the company) vs. cloud (non-local, at a server center) - this is
the so-called SAAS (Software As A Service) business model. "HANA"
refers to a database technology. "SAP ERP" and "S4/HANA" are
information systems that support the entire company value chain -
from production to customer delivery. These are the largest
available information systems, and SAP is the leading provider of
such systems. In fact, it'll be difficult to find a large company
anywhere that does not run its processes using SAP. The "cloud
platform" contains all sorts of new services, some of them
AI-driven, like "Analytics" and "Internet of Things".


<a id="org2628541"></a>

## PEAS example: automated taxi driver

PEAS description for an automated taxi driver (transport agent):

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">PERFORMANCE MEASURE</th>
<th scope="col" class="org-left">ENVIRONMENT</th>
<th scope="col" class="org-left">ACTUATORS</th>
<th scope="col" class="org-left">SENSORS</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Safe, fast, legal, comfy trip, max profits, min accident</td>
<td class="org-left">Roads, traffic, police, pedestrians, customers, weather</td>
<td class="org-left">Steering, accelerator, brake, signal, horn, display, speech</td>
<td class="org-left">Camera, radar, GPS, speedometer, engine, accelerometer, microphone, touchscreen</td>
</tr>
</tbody>
</table>

> "Virtual task environments (not in the physical world) can be as
> complex as real ones." ([AIMA](#org6d281a3))

**What do you think:** are AUGMENTED reality environments more, less,
or equally complex?<sup><a id="fnr.5" class="footref" href="#fn.5">5</a></sup>


<a id="org475e24e"></a>

## PEAS Challenge

Identify PEAS elements for each of these agent types!

-   Medical diagnosis system
-   Satellite image analysis system
-   Part-picking robot
-   Refinery controller
-   Interactive English tutor
    
    [[Solution](https://github.com/birkenkrahe/ai482/blob/main/5_ai_agents/img/challenge.png), [AIMA](#org6d281a3) table 2.5]

All of these applications are present today in their respective
industrial environments - health care, weather forecasting,
factories, processing plants, and online learning platforms.

Notice how when you think about actuators and sensors, you might
automatically think of humanoid robots. However, the most efficient
solution need not be humanoid (using human behavior, or physiology
as a design blueprint) - except when humans are directly involved
(health care, tutoring).


<a id="org4227a5d"></a>

## Task environment properties

The following properties is a taxonomy akin to a classification of
insects or plants in nature: like these, the properties of agents
refer to an evolving ecology. Also, they are used to explore and,
in a way, define machine "intelligence".

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">PROPERTY</th>
<th scope="col" class="org-left">OPTIONS</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">1) Observability</td>
<td class="org-left">Fully, partially or unobservable<sup><a id="fnr.6" class="footref" href="#fn.6">6</a></sup></td>
</tr>


<tr>
<td class="org-left">2) Multiplicity</td>
<td class="org-left">single or multi-agent</td>
</tr>


<tr>
<td class="org-left">3) Performativity</td>
<td class="org-left">competitive or cooperative</td>
</tr>


<tr>
<td class="org-left">4) Determinacy</td>
<td class="org-left">deterministic, non-deterministic or stochastic<sup><a id="fnr.7" class="footref" href="#fn.7">7</a></sup></td>
</tr>


<tr>
<td class="org-left">5) Causality</td>
<td class="org-left">sequential or episodic</td>
</tr>


<tr>
<td class="org-left">6) Stativity</td>
<td class="org-left">static or dynamic or semidynamic (score<sup><a id="fnr.8" class="footref" href="#fn.8">8</a></sup>)</td>
</tr>


<tr>
<td class="org-left">7) Temporality</td>
<td class="org-left">Discrete or continuous (state/time)</td>
</tr>


<tr>
<td class="org-left">8) Physicality</td>
<td class="org-left">Known or unknown (laws)</td>
</tr>


<tr>
<td class="org-left">9) Virtuality</td>
<td class="org-left">Virtual or real</td>
</tr>


<tr>
<td class="org-left">10) Locality</td>
<td class="org-left">Local or non-local</td>
</tr>
</tbody>
</table>


<a id="org4087b7f"></a>

## Environment of the automated taxi driver

Let's look at the automated taxi driver as an example:

1.  **Observability:** The environment is partially observable - for
    example, the agent cannot observe (or even find out directly)
    what other drivers are thinking.
2.  **Multiplicity:** The agent could treat another vehicle as an
    object or as an agent, too. Which relationship it is depends on
    the design of both vehicles involved: are any messages exchanged
    between them, or are there decisions where one agent's actions
    depend on the other? For example, if the taxi agent has a sensor
    that is directly fed data from the other vehicle, they'd form a
    two-agent system whose actions depend on one another.
3.  **Performativity:** this applies only to multi-agent systems. The
    taxi environment is both cooperative (with other non-taxi
    vehicles), and competitive (with other taxi drivers).
4.  **Determinacy:** the taxi environment is non-deterministic since
    the behavior of traffic cannot be predicted with
    certainty. Certain aspects (e.g. traffic density, weather
    conditions etc.) are stochastic and can be predicted with
    quantities attached to them ("10% probability of rain during
    this trip").
5.  **Causality:** short term, episodic actions, have long-term
    consequences for the taxi agent - the agent has to think ahead
    based on the past driving history and its past actions. For
    example, when it suddenly begins to rain, it has to adjust its
    breaking behavior.
6.  **Stativity:** the driving environment changes continuously,
    requiring agent responses ("The street is wet, what do you want
    to do?") and adjustments.
7.  **Temporality:** taxi driving is a continous state and a continous
    time problem - speed and location of the taxi change all the
    time, and they change smoothly, not abruptly. Driving actions
    are also continuous. Sensor input itself is discrete (digital
    signals) but is treated as continuous (distributions are
    smoothed).
8.  **Physicality:** some of the environment is unknown e.g. when the
    journey starts. This means that the taxi driver needs to learn
    properties of its environment that cannot be hard-coded at the
    start of the journey.
9.  **Virtuality:** the automated taxi driver has both a virtual
    (testing and simulation) environment and a real
    environment. Performance, actuation and sensing are relevant for
    both environments but only the real environment is productive.
10. **Locality:** the taxi driver deals with both local and non-local
    data, e.g. construction sites along the road are non-local,
    while road signs encountered during the drive are local. For
    the performance, local data are more relevant.

> "The hardest [agent task environment] case is partially observable,
> multiagent, nondeterministic, sequential, dynamic, continous, and
> unknown."  ([AIMA](#org6d281a3))

Here are examples for some of these categories.

![img](./img/environments.png)

[Image source: [AIMA](#org6d281a3) table 2.6]


<a id="org228fee9"></a>

## Systemic interpretation

These properties define the agent as a system with a boundary
between itself and the environment, with elements (actuators,
sensors), and relationships between these elements. This means that
the properties are not limited to AI systems - you could use them
to describe other cybernetic systems, like heating systems.


<a id="org4b4b113"></a>

## Homework

Pick any of the online exercises for this chapter of [AIMA](#org6d281a3) (ch. 2)
and work out a solution, or sketch a path towards a solution
(e.g. by describing what one might do, in which order), or sketch
specific problems and issues for discussion, and present in class
(for: Friday October 1).

Several of the exercises (from ex. 7) relate to material that we
have not covered yet (structure of agent programs and types of
agents), but we will have, before fall break. I think it might be
cool to continue working on some of these exercises for the
remainder of the term. You can also easily turn them into
presentations.


<a id="org239b125"></a>

# Agent structure and types

![img](./img/agents.jpg)

Sources: [Iacobelli, 2015](#org74a52c8) & [AIMA ch.2](#org6d281a3).


<a id="org18e44b3"></a>

## Table-driven agent programs

![img](./img/apple.jpg)

> "The key challenge for AI is to find out how to write programs that
> [&#x2026;] produce rational behavior from a smallish [algorithmic]
> program rather than from a vast [lookup] table." [AIMA](#org6d281a3):67


<a id="org76a0329"></a>

## Simple reflex agents<sup><a id="fnr.9" class="footref" href="#fn.9">9</a></sup>

Requires: condition-action rules

Example: vacuum robot (smart home).

The agent acts according to a `rule` whose condition
matches the current `state`, as defined by the `percept`.

Pseudocode:

![img](./img/simplecode.png)

Figure:

![img](./img/simple.png)


<a id="org1705f1d"></a>

## Model based agents

Requires: model on how the agent's world evolves

Example: portfolio agent (stock market).

![img](./img/model.png)


<a id="org98a7807"></a>

## Goal based agents

Requires: explicit goal-checking

![img](./img/goal.png)


<a id="orgbe9b833"></a>

## Utility based agents

Requires: utility function.

![img](./img/utility.png)


<a id="orgd3d0adc"></a>

## Learning agents

Requires: modifies own functions

![img](./img/learning.png)


<a id="org1c2393c"></a>

## All types

![img](./img/all_types.png)


<a id="orgef2f209"></a>

## Other classifications

There are, of course, other classifications. Here is another,
widely cited one, by [DeLaurentis (2005)](#org64a2444). In this model, simple
reflex ("reactive"), utility and goal-based agents are labelled as
having "a set solution path" (i.e. a rule set). In fact, this
taxonomy is vulnerable: the relationships of the new five
categories suggested by this author are not obviously logically
related. Remember: if the logic of a taxonomy, a classification
scheme, is not obvious and can be tested, it is (almost) worthless,
because you cannot use it to place things uniquely into categories
(which is the only point of having a taxonomy in the first place).

![img](./img/types.jpg)


<a id="org98e8f4d"></a>

# [AIMA Exercises](https://aimacode.github.io/aima-exercises/agents-exercises/)


<a id="orgb412eb6"></a>

## Briefing: DIY

You find the briefing below. For my part, I have looked through the
exercises and sketched thoughts, extensions and issues with some of
these. Over to you&#x2026;

> With the 4th edition (2021), the exercises for AIMA are online
> only, open for submissions from everyone. I thought it might be fun
> to see if we can contribute to the world-wide effort to understand
> AI and where it's going. So here's the idea:
> 
> Your job:
> 
> Pick one of more of the AIMA online exercises for chapter 2,
> "Intelligent Agents".  Work out a solution, or sketch a solution
> path, or list issues that you can see for answering any of these
> exercises.  Present your findings (informally or formally) on
> Friday, October 1, in our last session before the fall break.


<a id="org8c10df1"></a>

## Relationship between evolution and &#x2026;

The difficulty for me with this exercise is that evolution is
empirically challenged: it is not directly observable, and hence
evolutionary claims and hypothesis cannot be verified
experimentally. In fact, evolution is continously undergoing
paradigmatic changes (cp. [Pigliucci, 2009](#orgc61c8e7)).

My personal doubt of evolutionary theory is anchored in its
inability to explain the origin of language (cp. [Wolfe, 2016](#org5c27e1d)).


<a id="orgfeaa7f7"></a>

## Syllogisms

The many assertions of exercise 4 are very interesting: this is an
excellent opportunity to check one's grasp on logic. AIMA makes
certain assumptions and provides definitions, and you need to check
if these assertions follow or not.


<a id="orgaefe93e"></a>

## PEAS

We did something like exercise 5 and 6 in class: giving a PEAS
description of various tasks. This is a great exercise to build a
checklist of automated or automatable activities surrounding daily
activities. You can then proceed to check if any of these already
have agents supporting them or not. And if not, you might have
found a niche!


<a id="org4b48f71"></a>

## Glossary

Exercise 7 is a glossary exercise: I have repeatedly shown you how
and why I think it is really important to have short definitions
ready - it demonstrates your understanding and enables you to move
on through papers, discussions, etc.


<a id="org2c11199"></a>

## Coding

If I find the time (not this term, I am afraid), I will have a look
at the GitHub code repo for AIMA. Or perhaps one of you wants to
present and explain some of the code - e.g. for an application like
the simple utility agent "vacuum cleaner".


<a id="orgb1557ff"></a>

## Hardware

Not an answer but another question that I have because most of the
discussion in AIMA (apart from the last couple of chapters) is
about software. What is actually involved in building a real robot?

I have a great book reference: [Bhaumik, 2018](#org2181867). Perhaps a basis for a
future special course at Lyon? Or for a summer school project?


<a id="orgff8124c"></a>

# References


<a id="orgc930aa2"></a>

## Publications

<a id="org2181867"></a> Bhaumik A (2018). From AI to Robotics. [CRC Press](https://www.routledge.com/From-AI-to-Robotics-Mobile-Social-and-Sentient-Robots/Bhaumik/p/book/9780367572099). ([ebook](https://www.amazon.com/AI-Robotics-Arkapravo-Bhaumik/dp/0367572095/ref=sr_1_2))

<a id="org7741ecb"></a> Bee Z (24 Jan 2021). Grammarly is Garbage, and Here's Why
[Video]. [Online: YouTube.com](https://youtu.be/Q5rB9jDbTPU).

Chen M et al (14 Jul 2021). Evaluating Large Language Models Trained
on Code. Preprint: [arxiv:2107.03374](https://arxiv.org/abs/2107.03374).

<a id="org64a2444"></a> DeLaurentis DA (2005). Understanding Transportation
as System-of-Systems Design Problem. In: Proc. 43rd AIAA Aerospace
Sciences Meeting and Exhibit, Reno, US-NV, 10???13
January. [doi.org/10.2514/6.2005-123](https://arc.aiaa.org/doi/10.2514/6.2005-123)

<a id="orgb3ad3ae"></a> D??rner D (1990). The logic of failure. In:
Phil. Trans. R. Soc. Lond. B 327:463-473.

Facebook (9 Sep 2021). Introducing Ray-Ban Stories: First-Generation
Smart Glasses. [Online: fb.com.](https://about.fb.com/news/2021/09/introducing-ray-ban-stories-smart-glasses/)

<a id="org74a52c8"></a> Francisco Iacobelli (May 15, 2021). intelligent Agents Intro
[video]. [Online: youtube.com](https://youtu.be/UjQ1AzSvCp8?t=1308).

<a id="orgb6bc959"></a> Matloff N (2020). Probability and Statistics for Data
Science: Math + R + Data. CRC Press.

<a id="org22e38ef"></a> Myers A (8 Sept 2021). Solving the Robot Off-Loading
Problem. [Online: hai.stanford.edu](https://hai.stanford.edu/news/solving-robot-loading-problem).

<a id="orgc61c8e7"></a> Pigliucci M (2009). The Evolution of Evolutionary
Theory. In: Philosophy Now 71. [Online: philosophynow.org](https://philosophynow.org/issues/71/The_Evolution_of_Evolutionary_Theory). ([GDrive](https://drive.google.com/file/d/1hDnImlOIh_mWv1Jzjvpw7SuR0xAr6-n4/view?usp=sharing))

<a id="org4686f5a"></a> Reed Floren (1 April 2021). Jarvis.ai How to Write Blog
Posts in 10 Minutes with Conversion.AI [Video]. [Online: youtube.com](https://youtu.be/z5_3S5nKfWQ?t=540).

<a id="org6d281a3"></a> Russell S/Norvig P (2021). AI - A Modern Approach (4th
ed). Pearson.

<a id="org5c27e1d"></a> Wolfe T (2016). The Kingdom of Speech. ([Wikipedia](https://en.wikipedia.org/wiki/The_Kingdom_of_Speech))


<a id="org2cd68e5"></a>

## Websites

-   mycroft.ai - MyCroft AI speech assistant
-   openai.com - OpenAI Codex for natural language translation to code
-   neuralink.com - brain interface software and hardware
-   jarvis.ai - blog writing software


<a id="org87ae5d4"></a>

# Whiteboards

-   [September 20, 2021](https://drive.google.com/drive/folders/1cVty0VxQ2pU99cOk8LD-rJPsOi0pOm7Z?usp=sharing)
-   September 22, 2021
-   September 24, 2021


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> 1-3 came from course participants (see [whiteboard, Sept 20](https://drive.google.com/drive/folders/1cVty0VxQ2pU99cOk8LD-rJPsOi0pOm7Z?usp=sharing)), 4-7
are my personal opinion. "Automatic writing" includes AI-driven
spell-checking apps like Grammarly (beware - cp. [Bee 2021](#org7741ecb), though the
[Grammarly engineering blog](https://www.grammarly.com/blog/engineering/) is quite interesting). Quote from a video
demonstrating jarvis.ai ([Reed Floren, 2021](#org4686f5a)): "I've created a 1000 word
article in minutes on a topic that I really know nothing about."

<sup><a id="fn.2" href="#fnr.2">2</a></sup> Much like in probability: these are usually introduced via state
spaces (e.g. the different combinations when rolling a dice). A better
way of thinking about probability is as a process of creating one
record after another - essentially an event log of stochastic
events. Cp. [Matloff (2020)](#orgb6bc959).

<sup><a id="fn.3" href="#fnr.3">3</a></sup> You could also look at the job of learning in terms of incoming
or outgoing data, or different data formats. This would be closer to
computer processing and further from the human experience.

<sup><a id="fn.4" href="#fnr.4">4</a></sup> The answer is yes: whenever the maximizing or minimizing
functions are not executed well, e.g. because of lack of environmental
knowledge, or because the performance measure is ill-defined, or
because of faulty sensor data. In the case of the Rumba: not moving
(action), or not sucking (action), not respecting the boundaries
(environment), stopping short of cleaning well because of faulty
rewarding (performance), etc.

<sup><a id="fn.5" href="#fnr.5">5</a></sup> The answer depends on the measure of "complexity". For the sake
of argument, one could assume the complexity of the real world to be
"1", and of a completely static virtual world "0". Alternatively, you
have to use a complexity measure that can be quantified and
e.g. implemented in a program like D??rner's in "The logic of failure"
([D??rner, 1990](#orgb3ad3ae)).

<sup><a id="fn.6" href="#fnr.6">6</a></sup> "Unobservable" in principle means that the agent has no sensors
in all task environments (it must have some data otherwise it could
not perform its optimization strategy).

<sup><a id="fn.7" href="#fnr.7">7</a></sup> AIMA distinguishes between non-deterministic (aka uncertain) and
stochastic (aka uncertain but with a quantifiable probability).

<sup><a id="fn.8" href="#fnr.8">8</a></sup> In a semidynamic environment, the enviroment itself does not
change but a performance score does - chess with a clock is an
example: when the clock is ticking, the performance time changes even
though the board is static.

<sup><a id="fn.9" href="#fnr.9">9</a></sup> IMHO, these illustrations are not very clear and should be
replaced by proper modeling diagrams in BPMN or UML (use case
diagrams). This will be an assignment for the parallel "data modeling"
class!
