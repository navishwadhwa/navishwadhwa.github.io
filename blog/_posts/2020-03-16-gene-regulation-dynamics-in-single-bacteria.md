---
layout: post
title: "Gene regulation dynamics in single bacterial cells"
description: ""
author: "Navish Wadhwa"
author_handle: navish
category: blog
published: true
theme: lab
tags: []
---
{% include JB/setup %}

This post first appeared on the [blog of Biophysical Society][1]. This was part 2 of a 3-part series of blogs that I wrote about my favorite Biophysical Journal papers of 2019. You can read part 1 [here][3]. 

### Gene regulation dynamics in single bacterial cells
Uphoff, S. (2019). A quantitative model explains single-cell dynamics of the adaptive response in Escherichia coli. *Biophysical journal*, 117(6), 1156-1165.
[*link to article*][2]

Every living organism has three core missions in life – eat, survive, and reproduce. All these missions require the organism to interact with its environment at some level. The organism must continuously collect information from the environment – about resources, threats, mates – and respond in real time. The right response, be it timing, magnitude, or type, is critical for the organism’s success.

Very often, especially for unicellular organisms like bacteria, the response comes in the form of gene expression. The cell constantly monitors its internal state as well as the external environment. For example, in the presence of a new food source, the cell can turn on genes that allow it to consume the new food source. Similarly, if the cell senses a threat, say a chemical that causes DNA damage, it turns on genes that neutralize the threat and/or undo the damage.

While the big picture for gene expression is relatively easy to grasp, the real-world cases are often much more complicated. The expression of specific genes is often controlled by several competing factors, each of which in turn interacts with several different genes and proteins. This results in a complex web of interactions, often making it very challenging to understand and model the expression of single genes. Moreover, gene expression in itself isn’t sufficient for the cell to mount a response to a change in the environment. The transcribed RNA, in most cases, must be translated into a protein that carries out the function that forms the response. These complexities mean that in practice, it is not that likely to find a cellular process that can be described by only a few interacting parts in a way that is easily understood.

It is for this reason that it was a great pleasure to read the paper by Uphoff, which reports a simple model for the response of Escherichia coli to the DNA modifying methylation agent methyl methane-sulfonate (MMS). Indiscriminate alkylation of DNA has several negative effects, including problems associated with transcription, replication, as well as mutations. Bacteria must therefore react as soon as DNA methylation is detected. E. coli reacts through a protein called Ada, which repairs DNA methylation by transferring the methyl groups on to itself. The beauty of this response is that methylated Ada then activates its own transcription, leading to a positive feedback loop that increases the levels of Ada in the cell in the presence of methylation agents.

Uphoff wrote down a simple model for this process. The cell produces Ada at a small basal rate, which gets methylated in the presence of a methylation agent like MMS and activates the transcription of the Ada gene. Methylated Ada (meAda) can be inactivated (inAda) by proteolysis or other mechanisms and both Ada and meAda get diluted as the cell grows and divides. That’s it. The model can be written down as three coupled differential equations, one each for Ada, meAda, and inAda. Solving these equations for a given amount of MMS (which determines the rate of methylation of Ada to meAda) gives the total amount of Ada in the cell as a function of time, as well as the three individual species.

What’s even more remarkable is how well the model works. A single set of parameters obtained by fitting the steady state Ada response to varying MMS concentrations reproduced the whole family of response curves, including their time dependence. Even more instructive are the stochastic simulations of how single cells respond to MMS exposure. The noisy, seemingly random responses of individual cell in the simulations average out to produce the same clean curve produced by the coupled equations. This, to me, is a great demonstration of the power of differential equations even in cases when they are representing inherently stochastic processes.

The model also allowed Uphoff to rationalize a seemingly puzzling observation. Experiments had shown that even in the presence of high amounts of MMS, a subpopulation of cells did not show any response or had a long delay in the response. The solution to this puzzle might already be evident to many readers. Since the basal level of Ada production is small, many cells have no Ada molecules to initiate a response to DNA methylation. This subpopulation of cells simply must wait for the synthesis of the first Ada molecule, with the waiting times distributed exponentially as in a Poisson process. Uphoff confirmed this by comparing his simulations with the experimental observations of response times delay. 

Finally, this work is also a great reminder of bacteria as a powerful model to study biology. Being “simpler” than their eukaryotic relatives, bacteria are a treasure trove of fundamental cellular processes that can be quantified and understood with mathematical precision. This gives us scientists a rare opportunity to truly and deeply understand the building blocks of life.

[1]: https://www.biophysics.org/blog/my-favorite-biophysical-journal-papers-of-2019-part-2
[2]: https://www.sciencedirect.com/science/article/pii/S0006349519306940
[3]: /blog/the-mechanics-of-the-bacterial-cell-envelope