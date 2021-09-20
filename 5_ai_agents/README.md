
# Table of Contents

-   [Agents and environments](#orga021652)
    -   [Microworld-view](#org463ca01)
    -   [Rational agent success](#org9e862a8)
    -   [Example: Vacuum-cleaner "Rumba"](#org11afe01)
    -   [Definition of a rational agent](#org4d4d15c)
    -   [Process view](#org45ff7d3)
-   [AI applications that might change the world](#org70aa6ae)
-   [References](#org31293c8)
    -   [Publications](#org0e857d0)
    -   [Websites](#org992c13a)
-   [Whiteboards](#org2e6a2b5)



<a id="orga021652"></a>

# Agents and environments

The purpose of this section is to bridge the gap between AI ideas
and practice. To do this, we adopt the rational agent approach
promoted in AIMA, and implemented in day-to-day AI systems, like
robot vacuum cleaners that operate in the real world, or
personalized shopping apps that operate in virtual commercial space.

The abstract insights about rational agents are useful as an
analytic framework, much like the distinction between supervised and
unsupervised learning that we will look at next.

These lecture notes corresponds to the chapter 2 content of the textbook
([Russell/Norvig](#org82376c5), 2021).


<a id="org463ca01"></a>

## Microworld-view

The diagram shows a world- or space-oriented view of an agent and
its environment. The microworld view is less intuitive than the
process-view<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup> - think about your learning as a student: you
don't dwell on the fact that you move from your personal into
classroom space - and it would be difficult to see how to optimize
this spatial movement (for learning). Instead, you operate - like
an agent - with process steps (go to class, listen to lecture, do
exercise, take notes etc.). It is easier to think of input and
output and optimizing functions when following a process<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup>.

![img](./img/agents.png)

Source: AIMA - agent-world vs. environment view


<a id="org9e862a8"></a>

## Rational agent success

Success of a rational agent in this simple picture depends on:

1.  the performance measure that defines success
2.  the agent's knowledge of the environment
3.  the actions that the agent can perform
4.  the agent's percept sequence to date


<a id="org11afe01"></a>

## Example: Vacuum-cleaner "Rumba"

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

Can such a simple agent behave irrationally, too?<sup><a id="fnr.3" class="footref" href="#fn.3">3</a></sup>

It is worth noting that irrational behavior in humans can lead to
unforeseen (and unforeseeable) innovations and optimizations, but
also, of course, to destructive behavior. In fact, one could argue
that controlled irrationality is the core of creative behavior and
originality.


<a id="org4d4d15c"></a>

## Definition of a rational agent

> "For each possible percept sequence, a rational agent should select
> an action that is expected to maximize its performance measure,
> given the evidence provided by the percept sequence and whatever
> built-in knowledge the agent has." ([AIMA](#org82376c5))


<a id="org45ff7d3"></a>

## Process view

The definition suggests a process-oriented description of the
behavior of a rational agent. Such a process is shown in the BPMN
diagram below.

![img](./img/agents_and_environments.png)


<a id="org70aa6ae"></a>

# AI applications that might change the world<sup><a id="fnr.4" class="footref" href="#fn.4">4</a></sup>

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
<td class="org-left">Alexa/Siri/[MyCroft](https://mycroft.ai/)</td>
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
<td class="org-left">[Neuralink](https://neuralink.com/)</td>
<td class="org-left">Brain support agent</td>
<td class="org-left">Neuroscience</td>
</tr>


<tr>
<td class="org-right">5</td>
<td class="org-left">[Facebook Glass](https://about.fb.com/news/2021/09/introducing-ray-ban-stories-smart-glasses/)</td>
<td class="org-left">Social media agent</td>
<td class="org-left">Pattern recognition</td>
</tr>


<tr>
<td class="org-right">6</td>
<td class="org-left">[Automatic writing](https://www.jarvis.ai/)</td>
<td class="org-left">Writing agent</td>
<td class="org-left">Natural Language Processing</td>
</tr>


<tr>
<td class="org-right">7</td>
<td class="org-left">[Automatic programming](https://openai.com/blog/openai-codex/)</td>
<td class="org-left">Programming agent</td>
<td class="org-left">Natural Language Processing</td>
</tr>
</tbody>
</table>


<a id="org31293c8"></a>

# References


<a id="org0e857d0"></a>

## Publications

Chen M et al (14 Jul 2021). Evaluating Large Language Models Trained
on Code. Preprint: [arxiv:2107.03374](https://arxiv.org/abs/2107.03374).

Facebook (9 Sep 2021). Introducing Ray-Ban Stories: First-Generation
Smart Glasses. [Online: fb.com.](https://about.fb.com/news/2021/09/introducing-ray-ban-stories-smart-glasses/)

<a id="org5dd53c9"></a> Matloff N (2020). Probability and Statistics for Data
Science: Math + R + Data. CRC Press.

<a id="org82376c5"></a> Russell S/Norvig P (2021). AI - A Modern Approach (4th
ed). Pearson.


<a id="org992c13a"></a>

## Websites

-   mycroft.ai - MyCroft AI speech assistant
-   openai.com - OpenAI Codex for natural language translation to code
-   neuralink.com - brain interface software and hardware
-   jarvis.ai - blog writing software


<a id="org2e6a2b5"></a>

# Whiteboards

-   [September 20, 2021](https://drive.google.com/drive/folders/1cVty0VxQ2pU99cOk8LD-rJPsOi0pOm7Z?usp=sharing)
-   September 22, 2021
-   September 24, 2021


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> Much like in probability: these are usually introduced via state
spaces (e.g. the different combinations when rolling a dice). A better
way of thinking about probability is as a process of creating one
record after another - essentially an event log of stochastic
events. Cp. [Matloff (2020)](#org5dd53c9).

<sup><a id="fn.2" href="#fnr.2">2</a></sup> You could also look at the job of learning in terms of incoming
or outgoing data, or different data formats. This would be closer to
computer processing and further from the human experience.

<sup><a id="fn.3" href="#fnr.3">3</a></sup> The answer is yes: whenever the maximizing or minimizing
functions are not executed well, e.g. because of lack of environmental
knowledge, or because the performance measure is ill-defined, or
because of faulty sensor data. In the case of the Rumba: not moving
(action), or not sucking (action), not respecting the boundaries
(environment), stopping short of cleaning well because of faulty
rewarding (performance), etc.

<sup><a id="fn.4" href="#fnr.4">4</a></sup> 1-3 came from course participants (see whiteboard, Sept 20), 4-7
are my personal opinion.
