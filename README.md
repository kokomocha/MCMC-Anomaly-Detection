# Markov Chain Monte Carlo for designing Anomaly Detection Models 

## This Repository
<figure style="text-align: center;">
    <img height="350" src="https://www.akcp.com/wp-content/uploads/2021/05/6sigmafm_blog-1.png" alt="Hot Spot CFD" 
      title="Hot Spot CFD" style="margin-right: 10px;" />
</figure>

**This repository contains the 3 Reference Papers used to design and propose Anomaly detection models for Data Center Cooling Systems in 2020-2021. This approach had 
also been a pre-cursor to exploring a Reinforcement Learning Model.**

A Data Center has to maintain fixed range of temperatures, typically 18-22 deg celcius for optimal functioning of servers. Also, maximizing Energy Efficency 
is still considered a great challenge despite tracking and predicting server loads, DC aisle temperatures and Airflows. This stems due the unsolved Physics
problem of Sequential Hot air-Cold air interactions at macro-scale which lead to formation of localized "Hot Spots".

In the specific Cooling Audit case, Markov Chain Monte Carlo was used to predict sequential Markov Processes influencing Hot Spot Creation for the Cooling Layout 
and Operational Machines scenarios. Based on sensor data, probaabilities were inferred from priors to check against posterior probabalities of ideal scenaries to 
tag the state as an anomaly.
</br>

## What is MCMC?
<figure style="text-align: center;">
    <img height="300" src="https://upload.wikimedia.org/wikipedia/commons/d/de/Flowchart-of-Metropolis-Hastings-M-H-algorithm-for-the-parameter-estimation-using-the.png" 
      alt="Metropolis-Hastings demo" title="Metropolis-Hastings demo" style="margin-right: 10px;" />
</figure>

A Markov chain is a sequence of random states where the probability of moving to the next state depends only on the current state (the Markov property). Monte Carlo 
methods use repeated random sampling to approximate numerical results, such as integrals. MCMC combines this approach with the structure of a Markov chain to sample 
from the target distribution effectively and explore the target distribution iteratively. Markov Chain Monte Carlo (MCMC) is a class of algorithms used to sample from 
complex probability distributions, particularly when direct sampling is computationally infeasible. It is widely used in Bayesian statistics, machine learning, and 
computational physics to estimate properties of distributions and solve problems involving high-dimensional or analytically intractable spaces. These algorithms 
iteratively generate samples by proposing a new state based on the current state and deciding whether to accept or reject the proposed state based on a criterion that 
ensures convergence to the target distribution.

## Use of MCMC in Anomaly Detection
In anomaly detection, MCMC can be used to model and infer the probability distributions of normal behavior in a system. By sampling from a learned model of the system’s 
typical state, MCMC helps estimate the likelihood of observed data points. Low-probability regions identified through the sampling process are flagged as anomalies. 
This approach is particularly effective in complex systems where normal behavior cannot be defined through simple thresholds or fixed rules, such as in financial 
transactions, network traffic, or sensor data. MCMC-based anomaly detection is robust to noise and adaptable to dynamic environments, as it leverages probabilistic 
reasoning to handle uncertainty and variability.
