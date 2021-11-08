
# Table of Contents

-   [UNDER CONSTRUCTION](#org54812a9)
-   [What will you learn?](#org8cf2a11)
-   [The nature of language](#org3aef56b)
    -   [Can computers learn language? (2019)](#orgdc53526)
    -   [OpenAI codex: automatic coding](#org14c026f)
-   [Overview of NLP uses and tools](#org208582a)
    -   [Agent types](#org63104eb)
    -   [Machine translation messing up](#orgff198ec)
    -   [NLP methods summary](#org4d2ef40)
-   [Zero to AI: AI for natural language](#orgd113cc7)
    -   [Measuring language complexity](#org5adc6c2)
    -   [NLP application scenarios](#org1b63a08)
    -   [Sentiment analysis and autonomous spam detection](#org7dd7f40)
    -   [Text classification and document search and retrieval](#org9a5bd41)
    -   [Natural conversation and transformer models](#orgf46bae9)
        -   [Insight generation with Viable](#orgfc0605d)
        -   [AI Sheds Light on How the Brain Processes Language](#org5ee1b54)
    -   [Case study: Translated](#orgb9aa16f)
-   [Questions for discussion](#org9023f09)
-   [References](#org09e3e1a)



<a id="org54812a9"></a>

# UNDER CONSTRUCTION

![img](./img/underconstruction.gif)


<a id="org8cf2a11"></a>

# What will you learn?

-   What is the nature of language?
-   What is Natural Language Processing (NLP)?
-   What are some NLP tools?
-   How is NLP success measured?
-   Different current NLP application scenarios


<a id="org3aef56b"></a>

# The nature of language


<a id="orgdc53526"></a>

## Can computers learn language? (2019)

In 2019, my sister, who is a professor of linguistics at West
Chester U., asked me to talk to her students about NLP. This is
when I began to get interested in it. The [mindmap](https://github.com/birkenkrahe/ai482/blob/main/10_ai_natural_language/can_computers_learn_languages.xmind) and [lecture notes](https://github.com/birkenkrahe/ai482/blob/main/10_ai_natural_language/can_computers_learn_languages_notes.pdf)
for this talk are in GitHub, and here is a [large screenshot](https://github.com/birkenkrahe/ai482/blob/main/10_ai_natural_language/can_computers_learn_languages.png) for
download<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>.

This is also when I realized what a mess NLP was and how incomplete
our understanding of perhaps our most privileged ability, language,
stil is!

![img](./img/mess.jpg)


<a id="org14c026f"></a>

## OpenAI codex: automatic coding

**Assignment:** To get going, watch 5 minutes of this video (from [here](https://youtu.be/ISa10TrJK7w?t=115)
to [here](https://youtu.be/ISa10TrJK7w?t=367)) - recent coding successes with AI using natural language
([Neura Pod, 2021](#orgbe6b486)).

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


<a id="org208582a"></a>

# Overview of NLP uses and tools

"What is NLP?" in 10 minutes. Video by [IBM Technology (2021](#orgedbc58f)) - [via
YouTube](https://youtu.be/fLvJ8VdHLA0)


<a id="org63104eb"></a>

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


<a id="orgff198ec"></a>

## Machine translation messing up

![img](./img/mt1.png)

*Image: Google translate messing up.<sup><a id="fnr.5" class="footref" href="#fn.5">5</a></sup>*

This is even worse - `deepl` is often really good when it comes to
longer texts, but as a machine it is more on its own than Google
Translate.

![img](./img/mt2.png)
*Image: DeepL translate messing up.<sup><a id="fnr.5.100" class="footref" href="#fn.5">5</a></sup>*


<a id="org4d2ef40"></a>

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

Result of stemming and lemmatization ([Manning et al, 2008](#orgcd389b3)):

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

Resolving syntactic ambiguities using POS tags ([Godayal, 2018](#org34d2d10)):

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

-   Named Entity Recognition - [video](https://youtu.be/Ge-sXjgup6g) ([Datasaur, 2021a](#org35c8e4f))
-   ML-assisted text labeling - video (Datasaur, 2021b)

Further reading: [Lee, 2020](#orgb2574a3).


<a id="orgd113cc7"></a>

# Zero to AI: AI for natural language

Image source: [Mauro/Valigi (2021)](#orgf3a81ae), chapter 5

For this lecture, I have merely extracted what I think are the most
interesting features of this chapter. Overall, it gives a fair
impression of the state of the art without getting bogged down in
technical detail (true to the expected non-technical business
audience).


<a id="org5adc6c2"></a>

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

Two application examples:

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Application</th>
<th scope="col" class="org-left">Depth</th>
<th scope="col" class="org-left">Width</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Sentiment analysis on tweets</td>
<td class="org-left">low: positive or negative review label</td>
<td class="org-left">high: many different subjects</td>
</tr>


<tr>
<td class="org-left">Classifying customer support tickets</td>
<td class="org-left">high: many different support types</td>
<td class="org-left">low: all tasks in one domain</td>
</tr>
</tbody>
</table>


<a id="org1b63a08"></a>

## NLP application scenarios

![img](./img/nlp2.png)

This is a bit of a downer but not surprising: the application of
machine "intelligence" is a function of our understanding of an
entity. In the case of natural (i.e. human) language, this
understanding is not forthcoming:

> "In the last 40 years, there has been an explosion of research on
> [the] problem [of language evolution] as well as a sense that
> considerable progress has been made. We argue instead that the
> richness of ideas is accompanied by a poverty of evidence, with
> essentially no explanation of how and why our linguistic
> computations and representations evolved." ([Hauser et al, 2014](#org83ea95b)).

However, notice advances with rational agents despite our inability
to understand, or define, human intelligence (which is an even
larger canvas than language).

Also, understanding of the "evolution of language" is not the same
as understanding of language. Another possibility is here that our
understanding of evolution as a concept (or theory) is incomplete
or erroneous. Cp. [Wolfe (2016)](#org148eed4) for some heretic thoughts on the
matter.


<a id="org7dd7f40"></a>

## Sentiment analysis and autonomous spam detection

-   Classification problems
-   Statistical method: naive Bayes<sup><a id="fnr.8" class="footref" href="#fn.8">8</a></sup>
-   "Learning by experience beats hand-coded rules"

![img](./img/sentiment.png)


<a id="org9a5bd41"></a>

## Text classification and document search and retrieval


<a id="orgf46bae9"></a>

## Natural conversation and transformer models

-   GPT-3 powers fast apps like [`viable`](#orgf8e3a87) ([1 min video](https://askviable.com/))
-   GPT-3 does not really understand what it's saying
-   GPT-3 can get stuck on a loop or produce gibberish
-   Probabilistic reasoning is not the same as understanding


<a id="orgfc0605d"></a>

### Insight generation with Viable

> Using GPT-3, Viable identifies themes, emotions, and sentiment
> from surveys, help desk tickets, live chat logs, reviews, and
> more. It then pulls insights from this aggregated feedback and
> provides a summary in seconds.
> 
> For example, if asked, “What’s frustrating our customers about the
> checkout experience?”, Viable might provide the insight:
> “Customers are frustrated with the checkout flow because it takes
> too long to load. They also want a way to edit their address in
> checkout and save multiple payment methods.” (Source: [OpenAI](#org645ffb5))

![img](./img/viable.png)

Image: Viable sample feedback summary. Source: [OpenAI](#org645ffb5).


<a id="org5ee1b54"></a>

### [AI Sheds Light on How the Brain Processes Language](https://neurosciencenews.com/ai-language-processing-19536/)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">MIT team analyzed different language models (incl. GPT-3<sup><a id="fnr.9" class="footref" href="#fn.9">9</a></sup>)</td>
</tr>


<tr>
<td class="org-left">"Best-performing next-word prediction models activity patterns resemble those seen in the human brain."</td>
</tr>


<tr>
<td class="org-left">"We found that the models that predict the neural responses well also tend to best predict human behavior responses, in the form of reading times. And then both of these are explained by the model performance on next-word prediction. This triangle really connects everything together."</td>
</tr>
</tbody>
</table>

![img](./img/mit.png)

> "One of the key computational features of predictive models such
> as GPT-3 is an element known as a forward one-way predictive
> transformer. This kind of transformer is able to make predictions
> of what is going to come next, based on previous sequences. A
> significant feature of this transformer is that it can make
> predictions based on a very long prior context (hundreds of
> words), not just the last few words.
> 
> Scientists have not found any brain circuits or learning
> mechanisms that correspond to this type of processing, Tenenbaum
> says. However, the new findings are consistent with hypotheses
> that have been previously proposed that prediction is one of the
> key functions in language processing, he says."

Source: [MIT, 2021](#org9fe74f4).


<a id="orgb9aa16f"></a>

## Case study: Translated


<a id="org9023f09"></a>

# Questions for discussion

-   Which two metrics are used to measure NLP performance?
-   Why is sentiment analysis a classification problem?
-   What does OpenAI's GPT-2 model do?
-   How does BrokerBot differ from Eliza the therapist bot?


<a id="org09e3e1a"></a>

# References

<a id="org9fe74f4"></a> MIT (Oct 25, 2021). Artificial Intelligence Sheds Light on
How the Brain Processes Language [news]. [URL: neurosciencenews.com.](https://neurosciencenews.com/ai-language-processing-19536/)

<a id="orgf3a81ae"></a> Mauro/Valigi (2021). Zero to AI - a nontechnical,
hype-free guide to prospering in the AI era. Manning. [Online:
manning.com](https://www.manning.com/books/zero-to-ai).

<a id="orgbe6b486"></a> Neura Pod - Neuralink (Oct 3, 2021). OpenAI&Neuralink
[video]:1:55-6:05. [Online: youtube.com.](https://youtu.be/ISa10TrJK7w)

<a id="orgedbc58f"></a> IBM Technology/Martin Keen (Aug 11, 2021). What is NLP
(Natural Language Processing)? [video]. URL: [youtu.be/fLvJ8VdHLA0](https://youtu.be/fLvJ8VdHLA0)

<a id="orgcd389b3"></a> Manning/Raghavan/Schuetze (2008). Introduction to
Information Retrieval. Cambridge Univ Press ([PDF](https://nlp.stanford.edu/IR-book/)). [URL:
nlp.stanford.edu.](https://nlp.stanford.edu/IR-book/)

<a id="org34d2d10"></a> Godayal/Malhotra (June 8, 2018). An introduction to part of
speech tagging and the Hidden Markov Model [blog]. [URL:
freecodecamp.org](https://www.freecodecamp.org/news/an-introduction-to-part-of-speech-tagging-and-the-hidden-markov-model-953d45338f24/)

<a id="orgb2574a3"></a> Lee (Sep 3, 2020). Data Labeling for Natural Language
Processing: A Comprehensive Guide. [URL: medium.com/datasaur](https://medium.com/datasaur/data-labeling-for-natural-language-processing-a-comprehensive-guide-741343fea20e).

<a id="org35c8e4f"></a> Datasaur (May 19, 2021). Datasaur Labeling
[video]. [URL: youtu.be/Ge-sXjgup6g](https://youtu.be/Ge-sXjgup6g)

<a id="orgddeae6c"></a> Datasaur (May 2, 2021). Datasaur.ai: ML-Assisted
Labeling [video]. [URL: youtu.be/Qsw7dhneBw4](https://youtu.be/Qsw7dhneBw4)

<a id="org079cccf"></a> Birkenkrahe (14 Nov 2021). Can Computers Learn Language?
Talk at West Chester U. [mindmap]. [URL: tinyurl.com](https://tinyurl.com/sn5hqh2)

<a id="org7aae621"></a> Dorner (1990). The logic of failure. In:
Phil. Trans.R. Soc. Lond. B 327:463-473 (1990).] [URL: gwern.net.](https://www.gwern.net/docs/existential-risk/1990-dorner.pdf)

<a id="org83ea95b"></a> Hauser et al (2014). The mystery of language
evolution. Front.Psychol. 7
May 2014. <https://doi.org/10.3389/fpsyg.2014.00401>

<a id="org148eed4"></a> Wolfe (2016). The Kingdom of Speech. Little, Brown and
Company. [URL: wikipedia.org.](https://en.wikipedia.org/wiki/The_Kingdom_of_Speech)

<a id="org517710a"></a> Luis Serrano (Feb 10, 2019). Naive Bayes classifier: A
friendly approach. [URL: youtu.be/Q8l0Vip5YUw](https://youtu.be/Q8l0Vip5YUw)

<a id="org0dfafc1"></a> Serrano (2021). Grokking Machine
Learning. Manning. [URL: bit.ly/grokkingML](https://www.manning.com/books/grokking-machine-learning)

<a id="org96a937f"></a> Graham (Aug 2002). A Plan for Spam [Blog]. [URL:
paulgraham.com](http://www.paulgraham.com/spam.html)

<a id="org645ffb5"></a> openai.com (March 25, 2021). GPT-3 Powers the Next
Generation of Apps [blog]. URL: [openai.com](https://openai.com/blog/gpt-3-apps/)

<a id="orgf8e3a87"></a> askviable.com (2021). It used to take hours to find
insights in customer feedback.  Now it takes seconds [website]. URL:
askviable.com.


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
complexity. Compare it with the complexity defined by [Dorner (1990)](#org7aae621) as
a function of dynamic variables.

<sup><a id="fn.7" href="#fnr.7">7</a></sup> Language ambiguities (overlaps). Different meaning as the result
of interaction (over time, space). Example: how language changes in
the course of a telephone conversation, a talk between lovers, or in
the course of a hostile company takeover or a conquest in war. More
generally, any features that cannot easily be captured with a feature
vector (e.g. because we don't even know what the variables are).

<sup><a id="fn.8" href="#fnr.8">8</a></sup> Here is an [excellent video](https://youtu.be/Q8l0Vip5YUw) ([Serrano, 2019](#org517710a)) explaining this
important statistical theorem about conditional probabilities. The
creator of the video has also just (Oct 21) published a well reviewed
book on machine learning (Serrano, 2021). You should also read the
original article by Paul Graham on spam detection ([2002](#org96a937f)).

<sup><a id="fn.9" href="#fnr.9">9</a></sup> "Generative Pre-trained Transformer 3" created by OpenAI
([2021](#org645ffb5)).
