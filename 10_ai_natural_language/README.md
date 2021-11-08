
# Table of Contents

-   [UNDER CONSTRUCTION](#orge653a14)
-   [What will you learn?](#org9d18373)
-   [The nature of language](#org19f6922)
    -   [AI Sheds Light on How the Brain Processes Language](#orgf7c5cbc)
    -   [Can computers learn language? (2019)](#org1c155ea)
    -   [OpenAI codex: automatic coding](#org43859cc)
-   [Overview of NLP uses and tools](#org832a058)
    -   [Agent types](#orgdfae8dc)
    -   [Machine translation messing up](#orgd0b1217)
    -   [NLP methods summary](#orgb9b26a2)
-   [Zero to AI: AI for natural language](#orgea95059)
    -   [Measuring language complexity](#orgd345413)
    -   [NLP application scenarios](#org1253170)
-   [Questions for discussion](#org3c8bf7e)
-   [References](#orgdcf5d00)



<a id="orge653a14"></a>

# UNDER CONSTRUCTION

![img](./img/underconstruction.gif)


<a id="org9d18373"></a>

# What will you learn?

-   What is the nature of language?
-   What is Natural Language Processing (NLP)?
-   How is NLP success measured?
-   What is sentiment analysis?
-   How are chatbots designed?


<a id="org19f6922"></a>

# The nature of language


<a id="orgf7c5cbc"></a>

## [AI Sheds Light on How the Brain Processes Language](https://neurosciencenews.com/ai-language-processing-19536/)

> "One of the key computational features of predictive models such as
> GPT-3 is an element known as a forward one-way predictive
> transformer. This kind of transformer is able to make predictions
> of what is going to come next, based on previous sequences. A
> significant feature of this transformer is that it can make
> predictions based on a very long prior context (hundreds of words),
> not just the last few words.
> 
> Scientists have not found any brain circuits or learning mechanisms
> that correspond to this type of processing, Tenenbaum
> says. However, the new findings are consistent with hypotheses that
> have been previously proposed that prediction is one of the key
> functions in language processing, he says."

Source: [MIT, 2021](#org1b2c985).


<a id="org1c155ea"></a>

## Can computers learn language? (2019)

In 2019, my sister, who is a professor of linguistics at West
Chester U., asked me to talk to her students about NLP. This is when
I began to get interested in it. The [mindmap](https://github.com/birkenkrahe/ai482/blob/main/10_ai_natural_language/can_computers_learn_languages.xmind) and [lecture notes](https://github.com/birkenkrahe/ai482/blob/main/10_ai_natural_language/can_computers_learn_languages_notes.pdf) for
this talk are in GitHub, and here is a [screenshot](https://github.com/birkenkrahe/ai482/blob/main/10_ai_natural_language/can_computers_learn_languages.png)<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>.

This is also when I realized what a mess NLP was and how incomplete
our understanding of perhaps our most privileged ability, language,
stil is!

![img](./img/mess.jpg)


<a id="org43859cc"></a>

## OpenAI codex: automatic coding

**Assignment:** To get going, watch 5 minutes of this video (from [here](https://youtu.be/ISa10TrJK7w?t=115)
to [here](https://youtu.be/ISa10TrJK7w?t=367)) - recent coding successes with AI using natural language
([Neura Pod, 2021](#orgac8e789)).

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
> [&#x2026;<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup>]. It really accelerates me as a programmer, and takes
> away the boring stuff so I can focus on the fun ones."

I just got into the GitHub Copilot beta pilot for OpenAI Codex -
will report if I learn anything!<sup><a id="fnr.3" class="footref" href="#fn.3">3</a></sup>


<a id="org832a058"></a>

# Overview of NLP uses and tools

"What is NLP?" in 10 minutes. Video by [IBM Technology (2021](#org6bb3fa8)) - [via
YouTube](https://youtu.be/fLvJ8VdHLA0)


<a id="orgdfae8dc"></a>

## Agent types

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Use case<sup><a id="fnr.4" class="footref" href="#fn.4">4</a></sup></th>
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


<a id="orgd0b1217"></a>

## Machine translation messing up

![img](./img/mt1.png)

*Image: Google translate messing up.<sup><a id="fnr.5" class="footref" href="#fn.5">5</a></sup>*

This is even worse - `deepl` is often really good when it comes to
longer texts, but as a machine it is more on its own than Google
Translate.

![img](./img/mt2.png)
*Image: DeepL translate messing up.<sup><a id="fnr.5.100" class="footref" href="#fn.5">5</a></sup>*


<a id="orgb9b26a2"></a>

## NLP methods summary

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


<tr>
<td class="org-left">Named Entity Recognition</td>
<td class="org-left">Text labelling</td>
<td class="org-left">Label token <code>Arizona</code> as <code>US state</code></td>
</tr>
</tbody>
</table>

Result of stemming and lemmatization ([Manning et al, 2008](#org9a07b75)):

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

Resolving syntactic ambiguities using POS tags ([Godayal, 2018](#orgeb7b2e7)):

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

Named Entity Recognition (NER): labelling text data

![img](./img/ner.png)

-   Named Entity Recognition - [video](https://youtu.be/Ge-sXjgup6g) ([Datasaur, 2021a](#org83d6b62))
-   ML-assisted text labeling - video (Datasaur, 2021b)

Further reading: [Lee, 2020](#orgdd121a4).


<a id="orgea95059"></a>

# Zero to AI: AI for natural language

Image source: [Mauro/Valigi (2021)](#org67d10ac), chapter 5


<a id="orgd345413"></a>

## Measuring language complexity

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">METRIC</th>
<th scope="col" class="org-left">TARGET</th>
<th scope="col" class="org-left">ORIGIN</th>
<th scope="col" class="org-left">METAPHOR</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Width</td>
<td class="org-left">volume of the vocabulary</td>
<td class="org-left">domain diversity</td>
<td class="org-left">crown width</td>
</tr>


<tr>
<td class="org-left">Depth</td>
<td class="org-left">levels of understanding</td>
<td class="org-left">domain depth</td>
<td class="org-left">tree height</td>
</tr>


<tr>
<td class="org-left">Width x Depth</td>
<td class="org-left">complexity of patterns</td>
<td class="org-left">uses of language</td>
<td class="org-left">tree cover</td>
</tr>
</tbody>
</table>

![img](./img/nlp.png)

Greater area corresponds to greater "complexity"<sup><a id="fnr.6" class="footref" href="#fn.6">6</a></sup>.

![img](./img/nlp1.png)

*What is for example not captured with this measure?*<sup><a id="fnr.7" class="footref" href="#fn.7">7</a></sup>


<a id="org1253170"></a>

## NLP application scenarios

![img](./img/nlp2.png)


<a id="org3c8bf7e"></a>

# Questions for discussion

-   Which two metrics are used to measure NLP performance?
-   Why is sentiment analysis a classification problem?
-   What does OpenAI's GPT-2 model do?
-   How does BrokerBot differ from Eliza the therapist bot?


<a id="orgdcf5d00"></a>

# References

<a id="org1b2c985"></a> MIT (Oct 25, 2021). Artificial Intelligence Sheds Light on
How the Brain Processes Language [news]. [URL: neurosciencenews.com.](https://neurosciencenews.com/ai-language-processing-19536/)

<a id="org67d10ac"></a> Mauro/Valigi (2021). Zero to AI - a nontechnical,
hype-free guide to prospering in the AI era. Manning. [Online:
manning.com](https://www.manning.com/books/zero-to-ai).

<a id="orgac8e789"></a> Neura Pod - Neuralink (Oct 3, 2021). OpenAI&Neuralink
[video]:1:55-6:05. [Online: youtube.com.](https://youtu.be/ISa10TrJK7w)

<a id="org6bb3fa8"></a> IBM Technology/Martin Keen (Aug 11, 2021). What is NLP
(Natural Language Processing)? [video]. URL: [youtu.be/fLvJ8VdHLA0](https://youtu.be/fLvJ8VdHLA0)

<a id="org9a07b75"></a> Manning/Raghavan/Schuetze (2008). Introduction to
Information Retrieval. Cambridge Univ Press ([PDF](https://nlp.stanford.edu/IR-book/)). [URL:
nlp.stanford.edu.](https://nlp.stanford.edu/IR-book/)

<a id="orgeb7b2e7"></a> Godayal/Malhotra (June 8, 2018). An introduction to part of
speech tagging and the Hidden Markov Model [blog]. [URL:
freecodecamp.org](https://www.freecodecamp.org/news/an-introduction-to-part-of-speech-tagging-and-the-hidden-markov-model-953d45338f24/)

<a id="orgdd121a4"></a> Lee (Sep 3, 2020). Data Labeling for Natural Language
Processing: A Comprehensive Guide. [URL: medium.com/datasaur](https://medium.com/datasaur/data-labeling-for-natural-language-processing-a-comprehensive-guide-741343fea20e).

<a id="org83d6b62"></a> Datasaur (May 19, 2021). Datasaur Labeling
[video]. [URL: youtu.be/Ge-sXjgup6g](https://youtu.be/Ge-sXjgup6g)

<a id="org76f674c"></a> Datasaur (May 2, 2021). Datasaur.ai: ML-Assisted
Labeling [video]. [URL: youtu.be/Qsw7dhneBw4](https://youtu.be/Qsw7dhneBw4)

<a id="orgd893621"></a> Birkenkrahe (14 Nov 2021). Can Computers Learn Language?
Talk at West Chester U. [mindmap]. [URL: tinyurl.com](https://tinyurl.com/sn5hqh2)

<a id="org142ff62"></a> Dorner (1990). The logic of failure. In:
Phil. Trans.R. Soc. Lond. B 327:463-473 (1990).] [URL: gwern.net.](https://www.gwern.net/docs/existential-risk/1990-dorner.pdf)


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> There is a fair amount of posturing in the notes and in the
talk, because my sister asked me to impress her students.

<sup><a id="fn.2" href="#fnr.2">2</a></sup> Using the GPT-3 model.

<sup><a id="fn.3" href="#fnr.3">3</a></sup> "GitHub Copilot is an AI pair programmer which suggests line
completions and entire function bodies as you type. GitHub Copilot is
powered by the OpenAI Codex AI system, trained on public Internet text
and billions of lines of code." ([Source](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)). Alas, I do not use Visual
Code Studio - an editor from Microsoft (now it makes sense why GitHub,
also owned by Microsoft, partners with OpenAI Codex - more customers
for both their platforms and ultimately for their cloud business,
Azure).

<sup><a id="fn.4" href="#fnr.4">4</a></sup> We've used this term "use case" in class without definition. In
the Unified Modeling Language (UML), a use case diagram shows all the
different ways in which a user might interact with a system. The more
colloquial use means that we look at all the different ways, in which
a concept might be applied or used.

<sup><a id="fn.5" href="#fnr.5">5</a></sup> Actually, "Du kannst mich mal gerne haben" (German) means "Bite
me."  While "jemanden gerne haben" means "to like someone", the
operational part of the German sentence is "Du kannst mich mal", which
is correctly machine translated as "Bite me." But the last part is
inserted to soften it (typically used like this in the South of
Germany).

<sup><a id="fn.6" href="#fnr.6">6</a></sup> In quotes because this is an almost trivial notion of
complexity. Compare it with the complexity defined by [Dorner (1990)](#org142ff62) as
a function of dynamic variables.

<sup><a id="fn.7" href="#fnr.7">7</a></sup> Language ambiguities (overlaps). Different meaning as the result
of interaction (over time, space). Example: how language changes in
the course of a telephone conversation, a talk between lovers, or in
the course of a hostile company takeover or a conquest in war. More
generally, any features that cannot easily be captured with a feature
vector (e.g. because we don't even know what the variables are).
