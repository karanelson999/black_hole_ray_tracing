# Black Hole Ray Tracing

Numerical ray-tracing code for studying critical photon dynamics in Kerr and non-separable spacetimes.

This repository contains the numerical framework developed as part of my M.S. thesis, *Toward the Study of Photon Dynamics in Non-Separable Spacetimes*. The code integrates null geodesics using a Hamiltonian formulation and uses backward ray tracing and bisection methods to identify critical photon trajectories and black hole critical curves.

## Notebooks

### `Data_Generation.ipynb`
Main numerical ray-tracing framework. Includes:
- Hamiltonian equations of motion integrated using DOP853
- Kerr and quasi-Kerr metric implementations
- Backward ray tracing from the observer
- Plunge/escape classification
- Bisection searches for critical trajectories
- Multiple image-plane sampling methods
- Trajectory and critical-curve data generation

### `Critical_Curves.ipynb`
Analysis and visualization of numerical black hole critical curves, including comparison with analytic Kerr results.

### `Dynamical_Plots.ipynb`
Analysis and visualization of the dynamics of near-critical photon trajectories, including radial and polar motion.

## Usage Notes

The notebooks currently contain local file paths corresponding to the directory structure used during development. Users running the code on another machine will need to update the data and output directory paths near the beginning of the relevant notebooks to match their local directory structure.

The notebooks are intended to be configured for different numerical runs by changing parameters such as the spacetime metric, spin, observer inclination, image-plane sampling method, and sampling values. Relevant parameters and options are identified explicitly within the notebooks, with comments indicating where settings should be changed. Some filenames, parameter choices, and analysis settings therefore reflect the particular datasets or tests used during development and should be adjusted as needed for different runs.

## Current Status

The Kerr implementation and associated dynamical plots are the primary validated components of the current code.

The quasi-Kerr implementation is under active development. In particular, the treatment of the inner radial cutoff and related trajectory classification is currently being updated. The dynamical plotting routines are therefore presently intended for Kerr data, while the quasi-Kerr framework continues to be developed and validated.
