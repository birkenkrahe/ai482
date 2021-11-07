
# Table of Contents

-   [UNDER CONSTRUCTION](#org557d47b)
-   [The nature of language](#org58bd71d)
    -   [Artificial Intelligence Sheds Light on How the Brain Processes Language](#orgb131002)
-   [Entry example: Open AI Codex](#orgce6a2fc)
-   [What will you learn?](#org08e42be)
-   [Overview](#org372146e)
    -   [Agent types](#org10e6486)
    -   [Machine translation messing up](#org171607c)
    -   [NLP methods](#org2969498)
-   [Questions for discussion](#org96763a0)
-   [References](#org8173143)



<a id="org557d47b"></a>

# UNDER CONSTRUCTION

![img](./img/underconstruction.gif)


<a id="org58bd71d"></a>

# The nature of language


<a id="orgb131002"></a>

## Artificial Intelligence Sheds Light on How the Brain Processes Language

<https://neurosciencenews.com/ai-language-processing-19536/>


<a id="orgce6a2fc"></a>

# Entry example: Open AI Codex

**Assignment:** To get going, watch 5 minutes of this video (from [here](https://youtu.be/ISa10TrJK7w?t=115)
to [here](https://youtu.be/ISa10TrJK7w?t=367)) - recent coding successes with AI using natural language
([Neura Pod, 2021](#org0491ba9)).

The video reveals a particular (not uncommon) form of bias of what
AI can and should do for us. It is contained in this quote:

> "Programming is two things - one is: understand your problem. That
> includes talking to your users, thinking super hard about it,
> decomposing it in smaller pieces - these are the really cognitive
> aspects of building something. And then there's a second piece,
> which is: map a small functionality to code, whether it's an
> existing or an existing function, whether it's in your own codebase
> or out there in the world. And this second part is where the model
> really shines, like, I think it's better than I am at it, because it
> really has seen the whole universe of how people use code
> [&#x2026;<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>]. It really accelerates me as a programmer, and takes
> away the boring stuff so I can focus on the fun ones."

I just got into the GitHub Copilot beta pilot for OpenAI Codex -
will report if I learn anything!<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup>


<a id="org08e42be"></a>

# What will you learn?

-   What is Natural Language Processing (NLP)?
-   How is NLP success measured?
-   What is sentiment analysis?
-   How are chatbots designed?

Image source: [Mauro/Valigi (2021)](#org5d520c0), chapter 5


<a id="org372146e"></a>

# Overview

"What is NLP?" in 10 minutes. Video by [IBM Technology (2021](#org31a53db)) - [via
YouTube](https://youtu.be/fLvJ8VdHLA0)


<a id="org10e6486"></a>

## Agent types

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Use case<sup><a id="fnr.3" class="footref" href="#fn.3">3</a></sup></th>
<th scope="col" class="org-left"><a href="https://github.com/birkenkrahe/ai482/tree/main/8_machine_learning">Algorithm</a></th>
<th scope="col" class="org-left"><a href="https://github.com/birkenkrahe/ai482/tree/main/5_ai_agents">Agent type</a></th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Machine translation</td>
<td class="org-left">Deep learning</td>
<td class="org-left">Learning agent</td>
</tr>


<tr>
<td class="org-left">Virtual assistants (chatbots)</td>
<td class="org-left">Decision trees</td>
<td class="org-left">Utility-based</td>
</tr>


<tr>
<td class="org-left">Sentiment analysis</td>
<td class="org-left">Classification</td>
<td class="org-left">Model-based</td>
</tr>


<tr>
<td class="org-left">Spam detection</td>
<td class="org-left">Classification</td>
<td class="org-left">Goal-based</td>
</tr>
</tbody>
</table>

![img](./img/ibm.png)


<a id="org171607c"></a>

## Machine translation messing up

![img](./img/mt1.png)

*Image: Google translate messing up.<sup><a id="fnr.4" class="footref" href="#fn.4">4</a></sup>*

This is even worse - `deepl` is often really good when it comes to
longer texts, but as a machine it is more on its own than Google
Translate.

![img](./img/mt2.png)
*Image: DeepL translate messing up.<sup><a id="fnr.4.100" class="footref" href="#fn.4">4</a></sup>*


<a id="org2969498"></a>

## NLP methods

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">METHOD</th>
<th scope="col" class="org-left">DEFINITION</th>
<th scope="col" class="org-left">EXAMPLE</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Tokenization</td>
<td class="org-left">Breaking strings up</td>
<td class="org-left"><code>"the" "boy's" "cars" "are" "different" "colors"</code></td>
</tr>


<tr>
<td class="org-left">Stemming</td>
<td class="org-left">Identifying word stems</td>
<td class="org-left"><code>"car" "cars" "car's" "cars'"</code>: <code>car</code></td>
</tr>


<tr>
<td class="org-left">Lemmatization</td>
<td class="org-left">Morphological analysis</td>
<td class="org-left"><code>"am" "are "is"</code>: <code>be</code></td>
</tr>


<tr>
<td class="org-left">Part of speech tagging</td>
<td class="org-left">Syntactic analysis</td>
<td class="org-left"><code>Time flies like an arrow.</code></td>
</tr>
</tbody>
</table>

Result of stemming and lemmatization ([Manning et al, 2008](#org00c16ef)):

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">"the boy's cars are different colors"</td>
<td class="org-left"><code>the boy car be differ color</code></td>
</tr>
</tbody>
</table>

Resolving syntactic ambiguities using POS tags ([Godayal, 2018](#orgce20928)):

![img](./img/pos.jpeg)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Time flies like an arrow</td>
<td class="org-left">(1) Time is like an arrow, in that it passes fast</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">(2) "Time flies" (as in "fruit flies") like [to eat] an arrow</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">(3) You can time flies like you can time runners</td>
</tr>
</tbody>
</table>


<a id="org96763a0"></a>

# Questions for discussion

-   Which two metrics are used to measure NLP performance?
-   Why is sentiment analysis a classification problem?
-   What does OpenAI's GPT-2 model do?
-   How does BrokerBot differ from Eliza the therapist bot?


<a id="org8173143"></a>

# References

<a id="org5d520c0"></a> Mauro/Valigi (2021). Zero to AI - a nontechnical,
hype-free guide to prospering in the AI era. Manning. [Online:
manning.com](https://www.manning.com/books/zero-to-ai).

<a id="org0491ba9"></a> Neura Pod - Neuralink (Oct 3, 2021). OpenAI&Neuralink
[video]:1:55-6:05. [Online: youtube.com.](https://youtu.be/ISa10TrJK7w)

<a id="org31a53db"></a> IBM Technology/Martin Keen (Aug 11, 2021). What is NLP
(Natural Language Processing)? [video]. URL: [youtu.be/fLvJ8VdHLA0](https://youtu.be/fLvJ8VdHLA0)

<a id="org00c16ef"></a> Manning/Raghavan/Schuetze (2008). Introduction to
Information Retrieval. Cambridge Univ Press ([PDF](https://nlp.stanford.edu/IR-book/)). [URL:
nlp.stanford.edu.](https://nlp.stanford.edu/IR-book/)

<a id="orgce20928"></a> Godayal/Malhotra (June 8, 2018). An introduction to part of
speech tagging and the Hidden Markov Model [blog]. [URL:
freecodecamp.org](https://www.freecodecamp.org/news/an-introduction-to-part-of-speech-tagging-and-the-hidden-markov-model-953d45338f24/)


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> Using the GPT-3 model.

<sup><a id="fn.2" href="#fnr.2">2</a></sup> "GitHub Copilot is an AI pair programmer which suggests line
completions and entire function bodies as you type. GitHub Copilot is
powered by the OpenAI Codex AI system, trained on public Internet text
and billions of lines of code." ([Source](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)). Alas, I do not use Visual
Code Studio - an editor from Microsoft (now it makes sense why GitHub,
also owned by Microsoft, partners with OpenAI Codex - more customers
for both their platforms and ultimately for their cloud business,
Azure).

<sup><a id="fn.3" href="#fnr.3">3</a></sup> We've used this term "use case" in class without definition. In
the Unified Modeling Language (UML), a use case diagram shows all the
different ways in which a user might interact with a system. The more
colloquial use means that we look at all the different ways, in which
a concept might be applied or used.

<sup><a id="fn.4" href="#fnr.4">4</a></sup> Actually, "Du kannst mich mal gerne haben" (German) means "Bite
me."  While "jemanden gerne haben" means "to like someone", the
operational part of the German sentence is "Du kannst mich mal", which
is correctly machine translated as "Bite me." But the last part is
inserted to soften it (typically used like this in the South of
Germany).
