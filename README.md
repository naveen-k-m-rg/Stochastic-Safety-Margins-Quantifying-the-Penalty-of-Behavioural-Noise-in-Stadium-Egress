# Stochastic Safety Margins in Stadium Egress

This repository contains the computational work for my BEng Individual Project at the University of Bath. The project investigates how behavioural variability affects crowd movement through a stadium exit bottleneck.

Rather than treating pedestrians as identical, perfectly predictable agents, the model introduces stochasticity into their movement. It uses this to explore how small variations in behaviour can affect congestion, clogging and total egress time.

## What the code does

The notebooks implement an agent-based, Active-Langevin-style crowd simulation. A group of 50 agents moves from a wide stadium opening through a funnel and narrow vomitory/corridor exit. Each time step combines:

- a driving force towards the exit;
- wall-boundary forces;
- directional social repulsion and damping between agents; and
- a configurable stochastic noise term representing behavioural variation.

The model records agent positions, velocities and bottleneck occupancy. It then calculates metrics including total egress time, individual exit times and peak queue density. The notebooks also generate comparison plots and a speed-coloured animation to visualise free flow, slowing and jammed conditions.

## Repository contents

- `diss final.ipynb` - the final simulation notebook, including metrics, plots and animation.
- `diss section 4.3.ipynb` - a batch experiment that varies the diffusion/noise coefficient and reports its effect on total egress time.

## Running the notebooks

The work was developed in Python with Jupyter Notebook. The main dependencies are:

```text
numpy
matplotlib
IPython
```

Open a notebook in Jupyter and run the cells in order. The primary scenario settings are near the top of each notebook:

- `D_val` controls the behavioural-noise/diffusion level;
- `vomitory_width` controls the bottleneck width; and
- `n_agents` sets the number of simulated pedestrians.

Simulation runs are stochastic, so results will vary between runs unless a random seed is set.

## Dissertation availability

The dissertation itself is not included in this repository while permission for its public release is being considered. This repository is intended to share the modelling and analysis code only, not the full written submission or supplementary material.

## Author

Naveen Kumar Muthukumaran  
BEng Individual Project, University of Bath

