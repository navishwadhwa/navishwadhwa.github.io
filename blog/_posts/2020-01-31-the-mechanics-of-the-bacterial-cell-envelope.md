---
layout: post
title: "The mechanics of the bacterial cell envelope"
description: ""
author: "Navish Wadhwa"
author_handle: navish
category: blog
published: true
theme: lab
tags: []
---
{% include JB/setup %}

 This post first appeared on the [blog of Biophysical Society][1]. This is part 1 of a 3-part series of blogs that I wrote about my favorite Biophysical Journal papers of 2019.

As we accelerate into the new year, it is natural and perhaps also useful to review what happened in the last one. 2019 saw the publication of a number of excellent papers, so I thought I would revisit three of my favorite Biophysical Journal papers from the year. This blog is the first of a three-part series in which I talk about these papers.

Now, you can imagine that this is an inherently subjective exercise and my favorite papers are unlikely to be the same set as anyone else’s. For one, I picked these papers because they contribute to my own field of interest – the biophysics of bacteria. A second factor that ties these papers together is that they all combine elegant experiments with simple theoretical models to learn something new. So, here is the first one.

### The mechanics of the bacterial cell envelope 
Wong, F., & Amir, A. (2019). Mechanics and Dynamics of Bacterial Cell Lysis. *Biophysical journal*, 116(12), 2378-2389.
[*link to article*][2]

One might erroneously consider prokaryotes to be the primitive cousins of their more advanced counterparts, the eukaryotes. However, this notion will quickly disappear when you look closer at the architecture and the properties of the cell envelope of bacteria. Unlike eukaryotes, which have a single lipid bilayer separating the inside of the cell from the outside, bacteria have a complex multilayered structure which, apart from forming a boundary, provides bacterial cells with their characteristic shapes. The bacterial cell envelope is like the exoskeleton of arthropods (think insects, crustaceans) – it is a rigid structure which gives shape and mechanical integrity to the organism.

It should be of no surprise then that mechanics plays a key role in the function of bacterial cell envelopes. Mechanical defects in the cell envelope can be lethal to bacteria because they lead the cell to bursting open in a process termed lysis. In fact, many antibiotics kill bacteria by targeting the synthesis or maintenance of the cell envelope, resulting in mechanical defects in the envelope. It is therefore of significant practical interest to study the mechanical properties of the bacterial cell envelopes and to develop simple mathematical models for them.

This is exactly what Wong and Amir do in their paper. They set out to model the cell envelope mechanics of the bacterium Escherichia coli. The cell envelope of *E. coli* consists of three layers - inner and outer membranes consisting largely of phospholipids, and a rigid peptidoglycan wall sandwiched in between the two membranes. Wong and Amir develop a continuum model for the cell envelope by approximating the peptidoglycan cell wall as an elastic cylindrical shell with given material properties and reference size (the length and radius it would have if it didn’t interact with anything else), and the inner and outer membranes as fluid membranes. The equilibrium conformation of such a structure can be calculated by minimizing the total free energy arising from the bending and stretching of each of the layers and the entropy of the solutes inside the cell.

As an experimental test of their modeling approach, Wong and Amir turned to the same antibiotics that I mentioned above. These antibiotics, called β-lactams, cause defects in the peptidoglycan layer, causing the cell membranes to bulge out of cell followed by a slow swelling and an eventual rupture of the bulge. The authors tweaked their model to include bulge formation in it and compared their analytical and computational results with experiments in which they exposed bacteria to β-lactams. For reasonable values of parameters, the model does a good job of capturing the experimental results for both healthy cells as well as cells with bulge due to β-lactam exposure. In addition, the work by Wong and Amir provides evidence that swelling of the bulge takes place due to enlargement of the defect through which the bulge formed in the first place.

The work by Wong and Amir advances our understanding of the mechanical nature of the bacterial cell envelope. Also, it is a demonstration of the power of simple models. Linear approximations are often as good as full-scale numerical solutions. Many would have considered an elastic shell model too simple to represent the bacterial cell envelope with all its intricate composition and spatiotemporal regulation. The results from this work prove otherwise. Remember the old adage, “If it works, it works”.
	
[1]: https://www.biophysics.org/blog/my-favorite-biophysical-journal-papers-of-2019-part-1
[2]: https://www.cell.com/biophysj/fulltext/S0006-3495(19)30412-6

