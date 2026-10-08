---
layout: default
title: "Research"
permalink: /research
---
# Research
There remain some outstanding issues within the fluid surrogate modelling community that I aim to address through my work. For wide-scale industrial adoption of fluid mechanics surrogates for design and control, model architectures must be:

1. Trustworthy - violation of basic physical principles is an immediate disqualifier
2. Generalizable - cannot be limited to a narrow range of problems
3. Efficient - unlike language, CFD data is expensive to generate
4. Scalable - the same architecture must work across varying domain sizes

Only once all four of these traits are effectively synthesized in a single model architecture can surrogates be widely used alongside CFD as an efficient analysis tool of preliminary designs or as the plant within a control algorithm. Of course, they must also be very fast. The right combination of physical biases and scalability features will need to be decided upon for future foundation models. We also don't know how much data or how big a model we need for us to use these tools in a vast range of real world settings.

## RIKEN
Between my master's at Columbia and entering my PhD at the University of Washington, I worked in Tokyo at RIKEN Center for Computational Science, Japan's national supercomputing center. There I developed scalable methods for graph neural network (GNN) surrogate models for fluid dynamics. Like many other surrogate architectures, GNNs show better performance when you add physical inductive biases to align the learning task with real-world physical principles. In particular, GNNs are a more interpretable architecture for fluid surrogates due to the analogous relationship between message passing and spatiotemporal quantity transport. 

[![HIT GNN Comparison](/assets/kolmograph_compare_portrait.gif)](/assets/kolmograph_compare_portrait.gif)
Comparison of GNN models with and without physically principled architectural features.

[Undergraduate research →](/undergrad-research)
