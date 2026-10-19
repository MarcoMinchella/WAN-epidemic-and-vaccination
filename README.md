# World Airport Network: Structure, Epidemic Spreading and Vaccination Strategies



This project studies the World Airport Network (WAN), 3,933 airports linked by commercial flights, and asks how its topology shapes the spread of an epidemic and the effectiveness of different vaccination strategies. It was developed for the Network Science course of the MSc in ICT Engineering at the University of Padova.



## What this project does



**1. Network characterization.** Degree and strength distributions are fitted with the `powerlaw` package, and a truncated power law is preferred over a pure one in all four cases. Airport relevance is assessed with PageRank, betweenness and weighted out-degree. Assortativity shows two regimes: assortative at low degree and neutral at high degree. Community structure is analyzed with Louvain (\~30 communities, Q ≈ 0.77) and Infomap (\~151 communities). Their NMI of 0.787 reflects nesting of the partitions rather than disagreement. Robustness is evaluated under targeted attacks.



**2. Epidemic simulation.** A stochastic metapopulation SEIR model runs on the network, with R₀ ∈ {1.2, 1.9, 2.8} and eight seed airports: six hubs (ATL, IST, JFK, LAX, LHR, ORD) and two peripheral ones (PPG, UDJ).



**3. Vaccination strategies.** Seven strategies are compared against a no-vaccination baseline: Random, Degree, Degree + PageRank, Betweenness, Louvain bridges, Infomap bridges and Collective Influence.



## Main findings



- Epidemics seeded at hubs reach 100% outbreak probability under every strategy, so the choice of strategy only matters for peripheral seeds.

- Collective Influence delays the epidemic peak the most but is weak at geographic containment.

- Betweenness-based vaccination is dominated in cost-effectiveness by community-bridge strategies (Infomap, Louvain).



## Repository structure



- `notebooks/`: analysis and simulation notebooks

- `slides/`: presentation



## Reproducing the results



Python 3, with igraph, NetworkX, powerlaw, matplotlib and joblib. Install with `pip install -r requirements.txt` and run the notebooks in numerical order.



## References



Barrat et al. (2004); Clauset, Shalizi \& Newman (2009); Bucur \& Holme (2020); Morone \& Makse (2015); Matamalas et al. (2018).

