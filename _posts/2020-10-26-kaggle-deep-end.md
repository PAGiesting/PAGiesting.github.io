---
layout: post
title: Jumping into Kaggle's Deep End
---

### They Don't Call It Deep Learning for Nothing

A fellow <a href="https://github.com/Oladotun">Metis alum</a> suggested that we enter a Kaggle competition. I've intended to do that for a long time, and this is certainly an <a href="https://www.kaggle.com/c/lish-moa/">interesting project</a> on the Method of Action of pharmeceuticals.

#### A Nickel of EDA

The input rows (one per experiment, presumably) are just labeled with a cryptic "sig_id" (presumably concealing proprietary drug chemistry...not something geochemists worry a whole lot about). The experiments are labeled to indicate whether they are experimental or control, the treatment time (24, 48, 72 hours), and a dosage flag (D1 or D2, not much help there).

The meat of the data consists of 772 columns of gene expression measurements (labeled g-0 to g-771) and 100 columns of cell viability measurements (c-0 to c-99... no clues there!). Whatever these measurements actually are, they have all been scaled from -10 to +10 (at most). If you're curious, I've plotted some distributions <a href="https://github.com/Oladotun/MoaKaggleCompetition/blob/main/pca-log-saga/moa-explore.ipynb">here</a>.

The targets are a list of 206 Methods of Action (hence the name!) that are labeled 0 or 1 for whether that treatment acted in that manner or not. For example, did the drug candidate act as a calcium channel blocker? A chelating agent? A cannabinoid receptor antagonist, perchance? I have just enough biochemical awareness to be curious what the differences are between agonists, antagonists, blockers, and inhibitors are. If it's anything like igneous petrology, the terms are used in a messy and blurry fashion, but maybe biochemists are more regimented?

I've poked further and done some preliminary modeling with logistic regression and naive Bayes, and hoooeeey, yeah, you need something stronger, *i.e.* deep learning / neural nets, to deal with this data. Plus I've got to get a solid handle on multilabel classification because, you know, 206 labels. But I'm going to hang it up for today because there's an info session about a physical science hackathon in half an hour. Exciting stuff!

--PAG

Blogging platform assembled by Jekyll, Poole, and Zach Miller of Metis.
