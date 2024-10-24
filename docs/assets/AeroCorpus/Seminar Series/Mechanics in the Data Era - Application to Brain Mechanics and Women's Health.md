---
layout: default
title: Mechanics in the Data Era - Application to Brain Mechanics and Women's Health
permalink: /Jerusalem
---

# "Mechanics in the Data Era - Application to Brain Mechanics and Women's Health"
Antoine Jérusalem - [Professor at the University of Oxford, St. Hughe's College](https://eng.ox.ac.uk/people/antoine-jerusalem/)

Materials science aims to understand and avoid limitations for a given application, design (or tune) new materials for such applications (or new applications), and optimize structural components from such materials for engineering applications. Computational mechanics uses mathematical tools to predict mechanical properties of materials. They are restricted to time scale (e.g. cannot simulate fatigue) and are limited by their determinism. We can measure the mechanical properties of materials many times at the relevant time / length scales using TEM, SEM, AFM, Instron, Confocal, XRT, EBSD, DMA, etc.. Real application measurements can provide direct information. They are intrinsically stochastic. However, they generally cannot be used to predict functional behavior. Machine learning can learn a  relationship between data and function in conjunction with mechanics.

Brain mechanics can be utilized as a predictive model for injuries or as a means to learn directed treatment techniques. How do we link an injurious head impact with a brain injury with limited information? We use a computational pipeline that integrates police data, mechanics, and machine learning to accomplish this. We use a multilayer perception (MLP) neural network - an ANN with many perceptional layers. We take in FE simulation with some BCs and output maximum stress, strain, pressure and other relevant characteristics to develop this MLP. Now we take in data from the police reports and output these relevant mechanical quantities. We use XGBoost on 53 real-world cases with metadata, and the inputs and outputs of the MLP to determine the probability of the skull fracture, loss of consciousness, and intercranial hemorrhaging. The results exceeded 79% in all metrics with skull fracture accuracy being 94%.

This framework can be applied to a range of problems. Metamaterial design is being worked on at Caltech. At Columbia, he is working with Prof. Kristen Myers to simulate the risk of injury during labor to mother and fetus. This is to determine what position of delivery is better for the fetus and mother (anterior vs. posterior). Our outputs are perineal tearing, labor difficulty, and apgar scores with potential to predict instruments used and epistiotomy.