
# Table of Contents

-   [What're you going to learn?](#org25939da)
-   [What is intelligence?](#org4ed8b13)
    -   [Search patterns](#org14acddf)
    -   [Group work](#org7cce8d3)
-   [Different approaches to AI](#orgefcd26b)
    -   [Fields of systematic inquiry](#org7403188)
    -   [Fundamental questions](#org91ca191)
    -   [Four approaches](#orga5ecd67)
        -   [Four scenarios](#org5d3ae15)
        -   [Acting humanly ("Turing test" approach)](#org2a44a1f)
        -   [Thinking humanly ("cognitive modeling" approach)](#org3f2c110)
        -   [Thinking rationally ("laws of thought" approach)](#orgd94e04f)
        -   [Acting rationally ("rational agent" approach)](#org6c6ad54)
    -   [Major issues](#orgd2566f1)
    -   [Bounded rationality](#org2060f26)
    -   [Value alignment](#org0c8c969)
    -   [Pros and cons](#orga4ff1bf)
    -   [Asimov's robot laws](#org664f955)
        -   [Which approach fits these laws best?](#org6111bec)
-   [What's next?](#org1e37919)
-   [Any questions?](#org369e96e)
-   [References](#org6cbee69)



<a id="org25939da"></a>

# What're you going to learn?

-   What is intelligence?
-   Different approaches to AI
-   The standard model of AI
-   Bounded rationality
-   The Value alignment problem
-   Asimov's Robot Laws
-   What's next?


<a id="org4ed8b13"></a>

# What is intelligence?

![img](./img/intelligence.gif)


<a id="org14acddf"></a>

## Search patterns

![img](./img/googletrends.png)


<a id="org7cce8d3"></a>

## Group work

![img](./img/groupwork.gif)

-   Get together in groups of 2-3
-   Define INTELLIGENCE (5')
-   Define ARTIFICIAL INTELLIGENCE (5')
-   Briefly present your results (10')


<a id="orgefcd26b"></a>

# Different approaches to AI

![img](./img/fields.gif)

Which fields of inquiry (= disciplines) to use?


<a id="org7403188"></a>

## Fields of systematic inquiry

![img](./img/fields.gif)

-   Language
-   Philosophy
-   Science
-   History


<a id="org91ca191"></a>

## Fundamental questions

![img](./img/humanmachine.jpg)

-   Should we focus on humans?
-   Should we focus on machines?


<a id="orga5ecd67"></a>

## Four approaches

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">&#xa0;</th>
<th scope="col" class="org-left">THOUGHT / LOGIC</th>
<th scope="col" class="org-left">BEHAVIOR / ACTION</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">HUMANITY</td>
<td class="org-left">Cognitive modeling</td>
<td class="org-left">Turing Test</td>
</tr>


<tr>
<td class="org-left">RATIONALITY</td>
<td class="org-left">Laws of Thought</td>
<td class="org-left">Rational Agents</td>
</tr>
</tbody>
</table>


<a id="org5d3ae15"></a>

### Four scenarios

![img](./img/approaches1.png)


<a id="org2a44a1f"></a>

### Acting humanly ("Turing test" approach)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Natural language processing</td>
</tr>


<tr>
<td class="org-left">Knowledge representation</td>
</tr>


<tr>
<td class="org-left">Automated reasoning</td>
</tr>


<tr>
<td class="org-left">Machine learning</td>
</tr>


<tr>
<td class="org-left">Computer vision</td>
</tr>


<tr>
<td class="org-left">Robotics</td>
</tr>
</tbody>
</table>


<a id="org3f2c110"></a>

### Thinking humanly ("cognitive modeling" approach)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Introspection</td>
</tr>


<tr>
<td class="org-left">Psychological experiments</td>
</tr>


<tr>
<td class="org-left">Brain imaging</td>
</tr>


<tr>
<td class="org-left">Cognitive science</td>
</tr>


<tr>
<td class="org-left">Algorithms</td>
</tr>
</tbody>
</table>


<a id="orgd94e04f"></a>

### Thinking rationally ("laws of thought" approach)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Syllogistic reasoning</td>
</tr>


<tr>
<td class="org-left">Logic</td>
</tr>


<tr>
<td class="org-left">Expert systems</td>
</tr>


<tr>
<td class="org-left">Uncertainty</td>
</tr>


<tr>
<td class="org-left">Probability</td>
</tr>
</tbody>
</table>


<a id="org6c6ad54"></a>

### Acting rationally ("rational agent" approach)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Combination approach</td>
</tr>


<tr>
<td class="org-left">Constructivist</td>
</tr>


<tr>
<td class="org-left">Doing the right thing</td>
</tr>


<tr>
<td class="org-left">Standard model</td>
</tr>


<tr>
<td class="org-left">Control theory</td>
</tr>
</tbody>
</table>


<a id="orgd2566f1"></a>

## Major issues

![img](./img/issues.gif)

-   Bounded Rationality
-   Value alignment problem


<a id="org2060f26"></a>

## Bounded rationality

![img](./img/bakopoulos.png)

Image: [Bakopoulos, 1985](#org26c5438)

> AIMA: "For perfect rationality, the computational demands are just
> too high."

<div class="notes">
The article by [Bakopoulos (1985)](#org26c5438) helped to move IT from an arcane
discipline for technologists and nerds to a mainstream service
industry. To do this, Bakopoulos capitalized on the notion that
humans are not perfectly rational, that their rationality is
bounded by their humanity: "Data has no value unless put in the
context of the appropriate models, a process taxing the human
capacities to communicate, memorize and process information, and
thus leading to *bounded rationality*, which is a central concept
in organizational behavior theory."

I worked through this article a while back for a lecture I was
preparing, and found it remarkably difficult for such an old paper,
with a lot of connections in different directions - technology,
business, information theory, and philosophy.

Bakopoulos' result that information systems have no (or only
little) value without being properly integrated into business, and
that IT is useless if it does not 'speak" to people in ways that
they can understand and with results that they can measure, is
wonderfully relevant for the future development of AI, too.

</div>


<a id="org0c8c969"></a>

## Value alignment

![img](./img/mechanicalturk.png)

Image: [The Mechanical Turk](https://www.amazon.com/Turk-Famous-Eighteenth-Century-Chess-Playing-Machine/dp/B000HWZ28Q)

> AIMA: "The values or objectives put into the machine must be
> aligned with those of the human."

<div class="notes">
This kind of "alignment" sounds like an engineering task, but
actually it is a lot more complicated (or actually complex in a
technical sense): if rational agents are supposed to "do the right
thing", then their actions have to be not just logical, but
appropriate and moral. There is no algorithm for that - both
appropriateness (e.g. to a situation) and morality depend on the
circumstances. Take the example of Grace, the "ultra-lifelike
robotic nurse" from Hanson Robotics: she was designed for a certain
set of circumstances and both by, and for a particular set of moral
values. Will she do equally well in Japan and in Belgium, the
country with the "[world's most liberal euthanasia law](https://www.pbs.org/newshour/show/right-die-belgium-inside-worlds-liberal-euthanasia-laws)", and
therefore possibly a different approach to caring for the elderly?

The example of an 'unethical rational agent' chosen by AIMA, which
relates to the "Mechanical Turk", a chess machine that was operated
by a human hidden inside the machine, is admittedly a lot less
critical than when taking care of the sick and elderly is at
stake. However, the age of AI that dazzled us by beating chess
champions is long behind us, and the age of robots like Grace is
upon us!

</div>


<a id="orga4ff1bf"></a>

## Pros and cons

![img](./img/groupwork.gif)

-   Get together in groups of 2-3
-   Each group covers one approach
-   List pros and cons of your approach
-   Put your results [on the Kanban board](https://ideaboardz.com/for/AI%20approaches%20pros%20&amp;%20cons/4063343)


<a id="org664f955"></a>

## [Asimov's robot laws](https://en.wikipedia.org/wiki/Three_Laws_of_Robotics)

![img](./img/asimov.jpg)

Image: cover of "I, Robot" by Isaac Asimov (1940)


<a id="org6111bec"></a>

### Which approach fits these laws best?

1.  A robot may not injure a human being or, through inaction, allow
    a human being to come to harm.
2.  A robot must obey the orders given it by human beings except
    where such orders would conflict with the First Law.
3.  A robot must protect its own existence as long as such
    protection does not conflict with the First or Second Law.


<a id="org1e37919"></a>

# What's next?

![img](./img/river.gif)

-   Scientific foundations of AI
-   History of AI


<a id="org369e96e"></a>

# Any questions?

![img](./img/thankyou.gif)

[This presentation is available online.](https://github.com/birkenkrahe/ai482/tree/main/2_what_is_ai)


<a id="org6cbee69"></a>

# References

<a id="org26c5438"></a> Bakopoulos, J. Yannis, "Toward a More Precise
Concept of Information Technology" (1985). ICIS 1985 Proceedings. 4.
<http://aisel.aisnet.org/icis1985/4>

