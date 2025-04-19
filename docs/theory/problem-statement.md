---
title: What problem are we trying to solve?
sidebar_label: Problem statement
---

We want to calculate the electronic structure of real materials and their
physical properties by *ab-initio* method. A material is composed of atoms,
while atoms themselves consist of electrons, protons, and neutrons. The dynamics
of macroscopic particles such as electrons are governed by the laws of quantum
mechanics. Quantum particles are described by the wave function.

$$
\lambda \cdot p = h
$$

where $h$ is the Plank constant. There are four fundamental forces of nature:
electromagnetic, strong nuclear, weak nuclear, and gravitational influencing the
influencing the dynamics of any particle. However, when it comes to
understanding the behavior of materials, we only need to consider the
electromagnetic force. The Wavefunction of an electron in a potential filed
$(V)$ is calculated by solving the Schrödinger equation:

$$
-\frac{\hbar^2}{2m} \nabla^2 \Psi(\textbf{r}, t) + V(\textbf{r}, t) = i\hbar
\frac{\partial\Psi(\textbf{r}, t)}{\partial t}
$$

Fortunately, in most practical purposes, the potential field is not a function
of time $(t)$, or even if it is a function of time, they changes relatively
slowly compared to the dynamics we are interested in. For example, the electrons
inside a material are subjected to the Coulomb field of the nucleus. The nucleus
is heavy and their motion is much slower than the motion of the electrons. In
such situation, we can separate out the spatial and temporal parts of the wave
function:

$$
\Psi(\textbf{r}, t) = \psi(\textbf{r}) f(t)
$$

That reduces our task to solving only time independent Schrödinger equation:

$$
\left[-\frac{\hbar^2 \nabla^2}{2m} + v(\textbf{r})\right] \psi(\textbf{r}) =
\epsilon \psi(\textbf{r})
$$

Once we have the wavefunction, we can calculate the observables by taking the
expectation values.

$$
\braket{\psi_i | \psi_j} = \delta_{ij}
$$

$$
\braket{\psi_i | \hat{\mathcal{H}} | \psi_i} = \epsilon_i
$$

However, the challenge is to solve the Schrödinger equation as a real physical
system is consists of a large number of atoms. The Schrödinger equation becomes
coupled many-body equation.

$$
\left[-\frac{\hbar}{2m} \sum_{i=1}^N \nabla_i^2 + \sum_{i=1}^NV(\textbf{r}_i)
+ \sum_{i=1}^N \sum_{j<i}U(\textbf{r}_i, \textbf{r}_j)\right]\psi(\textbf{r}_1,
\textbf{r}_2, ..., \textbf{r}_N) = E\psi(\textbf{r}_1, \textbf{r}_2, ...,
\textbf{r}_N)
$$

With today's available computing power, it is far from feasible to solve the
actual electronic wavefunction of a condensed matter system, where $N$ is of the
order of $10^{23}$.
