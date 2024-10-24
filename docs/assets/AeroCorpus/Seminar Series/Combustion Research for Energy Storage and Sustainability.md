---
layout: default
title: Combustion Research for Energy Storage and Sustainability
permalink: /Deng
---
# Combustion Research for Energy Storage and Sustainability

Presenter: Sili Deng - [Associate Professor at MIT](https://web.mit.edu/~silideng/www/)

70% of greenhouse gas emissions come from fossil fuel combustion. Replacing these fossil fuels with sustainable fuel sources can drastically reduce greenhouse gas emissions. The essential question is how to balance efficiency, environmental impact, and practicality. The United States is responsible for one sixth of global energy consumption. Fossil fuel mix remains at ~80% of US energy consumption. However, there has been a shift from coal to natural gas. Energy conversion via combustion is roughly 85%. We need infrastructure to harvest and store renewable energy and multi-tier approaches for sustainability.

Deng's research group has three main arms.
*  Scientific Machine Learning for Chemical Kinetic Models
* Flame-assisted synthesis
* Alternative fuels (e.g. Carbon-zero fuels, H2, NH3)

### Energy Material Production
There is great demand for lithium-ion (LI) batteries in the future. The cathode material is critical in determining battery cost and performance. Multi-component metal oxides are the most widely used cathode materials e.g. Lithium-Nickel-Cobalt-Manganese (NCM) cathode materials. The cathode is the single largest cost component in a lithium-ion battery.

The components of a LI battery come in solution and are formed in precursor production. This is time consuming and cannot be integrated with a continuous production cycle. The production of the LI battery itself is also time consuming and expensive. We can solve this issue via combustion. Combustion occurs in three stages:

1. Precursors
2. Flame (Reactor)
3. Solid Particles (Products)

We have a setup whereby we dissolve metal salts in water, precipitate salts, and a cold flow burner for fast material decomposition into the relevant materials. This allows for continuous production in seconds and integrable with existing production. A significant amount of nanoscale lithium particles are noticed on the particle surface. We add urea to the precursors to reduce the calcination and heat treatment time from one day to 40 minutes. This yields comparable performance in capacity and retention of the battery (100 cycles) to the alternative method.

A single droplet experiment was conducted. Urea was deposited as a droplet and its diameter was measured over time. The shape of the droplet was observed to obey the $d^2$ law. Next, we do some numerical modelling and see that the solutes precipitate in the order $\text{Mn} \rightarrow \text{Ni} \rightarrow \text{Co} \rightarrow \text{Mn}$. We also want to control morphology.

In summary, this is an efficient way of yielding high-performance cathode materials with controllable morphology and reduced synthesis time. There is great potential in commercialization and we want to understand more of the fundamental physics.

### Battery Safety
The TSA wants you to check your batteries because of the thermal runaway process. We want to understand the kinetics and develop strategies to mitigate this issue. We observe the thermal runaway capability of a material (i.e. thermal stability) using differential scanning calorimetry (DSC). We measure the heat flow vs. temperature and observe peaks (exothermic reactions). Each peak is assumed to be a different reaction under a single global reaction. The challenges are that types of data (DSC and ARC for battery cells) are limited and we don't have detailed kinetic knowledge to model these reactions. We develop scientific machine learning models for large-scale optimization using physical laws.

Mathematically you can express the law of mass action into the neural network (NN) 

$$R = k[A]^{V_A}[A]^{V_B} = \exp(\ln k + v_A \ln[A] + v_B \ln[B]$$

to yield the reaction orders, rate constant, and stoichiometric coefficients. We also embed the Arrhenius Law. The number of hidden nodes is the number of reactions. Computing the loss with respect to 

$$\frac{d \text{ Species}}{dt}$$

gives us a PINN. We embed physics to compensate for data unavailability. *How do you do uncertainty quantification? This is a feed-forward NN. Is this a Bayesian NN or just a Bayesian approach with MCMC (Slide 41). Previously it was HMC and now they use stochastic gradient descent over many models.* Kinetics in the literature have large uncertainties which need to be reconciled in cell-level modeling. We can simulate thermal runaways using combustion reaction neural networks. 