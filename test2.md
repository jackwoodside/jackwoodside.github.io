---
author:
- Jack Woodside (u6940872)
date: 21st of May, 2021
title: PHYS3101 Assignment 10
header-includes:
- \usepackage{physics}
---

# Question 1. {#question-1. .unnumbered}

Transform the following Hamiltonian into the momentum basis.
$$\begin{aligned}
        \hat{H} = \int \dd \vb{x}\hat{\psi}^{\dagger}(\vb{x}) \left(-\frac{\hbar^2}{2m}\nabla^2\right)\hat{\psi}(\vb{x}) + U \int \dd \vb{x}\hat{\psi}^{\dagger}(\vb{x})^2\hat{\psi}(\vb{x})^2\end{aligned}$$
We can represent the creation and annihilation operators by
$$\begin{aligned}
        \hat{\psi}^{\dagger}(\vb{x}) &= \int \dd \vb{p}\braket{\vb{p}}{\vb{x}} \hat{\tilde{\psi}}^{\dagger}(\vb{p}) \\
        \hat{\psi}(\vb{x}) &= \int \dd \vb{p}\braket{\vb{x}}{\vb{p}} \hat{\tilde{\psi}}(\vb{p}) \\\end{aligned}$$
where $$\begin{aligned}
        \braket{\vb{p}}{\vb{x}} &= \frac{1}{\sqrt{2\pi\hbar}^3}e^{-i\vb{p}\cdot\vb{x}/ \hbar} \\
        \braket{\vb{x}}{\vb{p}} &= \frac{1}{\sqrt{2\pi\hbar}^3}e^{i\vb{p}\cdot\vb{x}/ \hbar}.\end{aligned}$$
Considering just the kinetic energy term of the Hamiltonian, we get
$$\begin{aligned}
        \int \dd \vb{x}\hat{\psi}^{\dagger}(\vb{x})\left(-\frac{\hbar^2}{2m}\nabla^2\right)\hat{\psi}(\vb{x}) &= \frac{1}{(2\pi\hbar)^3}\int \dd \vb{x}\int \dd \vb{p}\int \dd \vb{q}e^{-i\vb{p}\cdot\vb{x}/ \hbar}\hat{\tilde{\psi}}^{\dagger}(\vb{p})\left(-\frac{\hbar^2}{2m}\nabla^2\right)e^{i\vb{q}\cdot\vb{x}/ \hbar}\hat{\tilde{\psi}}(\vb{q}) \\
                                                                                                                               &= \frac{1}{(2\pi\hbar)^3} \int \dd \vb{x}\int \dd \vb{p}\int \dd \vb{q}e^{i(\vb{q}- \vb{p})\cdot\vb{x}/ \hbar} \hat{\tilde{\psi}}^{\dagger}(\vb{p}) \frac{\vb{q}\cdot \vb{q}}{\hbar^2}\left(\frac{\hbar^2}{2m}\right) \hat{\tilde{\psi}}(\vb{q}).\end{aligned}$$
Then noting that $$\begin{aligned}
        \int \dd \vb{x}e^{i(\vb{q}- \vb{p}) / \hbar} &= (2\pi\hbar)^3\delta(\vb{q}- \vb{p}),\end{aligned}$$
this simplifies to $$\begin{aligned}
        \frac{1}{(2\pi\hbar)^3} \int \dd \vb{x}\int \dd \vb{p}\int \dd \vb{q}e^{i(\vb{q}- \vb{p})\cdot\vb{x}/ \hbar} \hat{\tilde{\psi}}^{\dagger}(\vb{p}) \frac{\vb{q}\cdot \vb{q}}{\hbar^2}\left(\frac{\hbar^2}{2m}\right) \hat{\tilde{\psi}}(\vb{q}) &=  \int \dd \vb{p}\int \dd \vb{q}\delta(\vb{q}- \vb{p}) \hat{\tilde{\psi}}^{\dagger}(\vb{p}) \frac{\vb{q}\cdot \vb{q}}{\hbar^2}\left(\frac{\hbar^2}{2m}\right) \hat{\tilde{\psi}}(\vb{q}) \\
                                                                                                                                                                                                                                         &= \int \dd \vb{p}\hat{\tilde{\psi}}(\vb{p}) \frac{\vb{p}\cdot \vb{p}}{2m}\hat{\tilde\psi}(\vb{p}).\end{aligned}$$

Now considering the potential term, ignoring the constant out the front,
we have $$\begin{aligned}
        \int \dd \vb{x}\hat{\psi}^{\dagger}(\vb{x})^2\hat{\psi}(\vb{x})^2 &= \frac{1}{(2\pi\hbar)^6} \int \dd \vb{x}\int \dd \vb{p}\int \dd \vb{p}' \int \dd \vb{q}\int \dd \vb{q}' e^{i(\vb{q}+\vb{q}'-\vb{p}-\vb{p}')\cdot\vb{x}/ \hbar} \hat{\tilde\psi}^\dagger(\vb{p})\hat{\tilde\psi}^{\dagger}(\vb{p}')\hat{\tilde\psi}(\vb{q})\hat{\tilde\psi}(\vb{q}') \\
         &= \frac{1}{(2\pi\hbar)^3} \int \dd \vb{p}\int \dd \vb{p}' \int \dd \vb{q}\int \dd \vb{q}' \hat{\tilde\psi}^\dagger(\vb{p})\hat{\tilde\psi}^{\dagger}(\vb{p}')\hat{\tilde\psi}(\vb{q})\hat{\tilde\psi}(\vb{q}') \\
         &= \frac{1}{(2\pi\hbar)^3} \int \dd \vb{p}\int \dd \vb{p}' \int \dd \vb{q}\int \dd \vb{q}' \delta(\vb{q}+ \vb{q}'- \vb{p}- \vb{p}')\hat{\tilde\psi}^\dagger(\vb{p})\hat{\tilde\psi}^{\dagger}(\vb{p}')\hat{\tilde\psi}(\vb{q})\hat{\tilde\psi}(\vb{q}') \\
         &= \frac{1}{(2\pi\hbar)^3} \int \dd \vb{p}\int \dd \vb{q}\int \dd \vb{q}' \hat{\tilde\psi}^\dagger(\vb{p})\hat{\tilde\psi}^{\dagger}(\vb{q}+ \vb{q}' - \vb{p})\hat{\tilde\psi}(\vb{q})\hat{\tilde\psi}(\vb{q}').\end{aligned}$$
Overall, this gives the Hamiltonian in the momentum basis as
$$\begin{aligned}
        \hat{H} &= \int \dd \vb{p}\hat{\tilde\psi}(\vb{p}) \frac{\vb{p}\cdot \vb{p}}{2m}\hat{\tilde\psi}(\vb{p}) + \frac{U}{(2\pi\hbar)^3} \int \dd \vb{p}\int \dd \vb{q}\int \dd \vb{q}' \hat{\tilde\psi}^\dagger(\vb{p})\hat{\tilde\psi}^{\dagger}(\vb{q}+ \vb{q}' - \vb{p})\hat{\tilde\psi}(\vb{q})\hat{\tilde\psi}(\vb{q}').\end{aligned}$$

# Question 2. {#question-2. .unnumbered}

A system of bosons is in a single mode of a particular single-particle
basis. Furthermore, it is in a coherent state of that mode. Show that in
any other single particle basis, it is the tensor product of a coherent
state in each mode.\
\
We can represent the system by $$\begin{aligned}
        \ket{\psi} &= \ket{n,0,0,\ldots} \\
                   &= e^{-\abs{\alpha}^2 / 2} \sum_{n} \frac{\alpha^n}{\sqrt{n!}}\ket{n,0,0,\ldots}.\end{aligned}$$
But we can represent any state by applying creation operators repeatedly
to the vacuum, which is convenient since the vacuum is the same in any
basis. So then $$\begin{aligned}
        \ket{n_1,\ldots,n_j,\ldots} &= \prod_{j = 1}^{\infty} \frac{(\hat{a}_j^{\dagger})^{n_j}}{\sqrt{n_j!}}\ket{\{0\}}\end{aligned}$$
which gives us $$\begin{aligned}
        \ket{\psi}
        &= e^{-\abs{\alpha}^2 / 2} \sum_n \frac{\alpha^n}{\sqrt{n!}}\frac{(\hat{a}^{\dagger})^n}{\sqrt{n!}}\ket{\{0\}} \\
        &= e^{-\abs{\alpha}^2 / 2} \sum_n \frac{(\alpha \hat{a}^{\dagger})^n}{n!}\ket{\{0\}} \\
        &= e^{-\abs{\alpha}^2 / 2} e^{\alpha \hat{a}^{\dagger}} \ket{\{0\}}.\end{aligned}$$
We then want to express $\hat{a}^{\dagger}$ in an arbitrary single
particle basis. This is $$\begin{aligned}
        \hat{a}^{\dagger} &= \sum_i c_i \hat{b}_i^{\dagger},\end{aligned}$$
which means our state is $$\begin{aligned}
        \ket{\psi}
        &= e^{-\abs{\alpha}^2 / 2} \prod_{i} e^{\alpha c_i\hat{b}_i^{\dagger}} \ket{\{0\}} \\
        &= e^{-\abs{\alpha}^2 / 2} \prod_{i} e^{\abs{\alpha c_i}^2 / 2}\ket{\alpha_1, \alpha_2, \ldots}.\end{aligned}$$
When we take the product of the exponentials, the exponents will form a
sum. Considering that sum, we have $$\begin{aligned}
        \frac{\abs{\alpha}^2}{2}\sum_i \abs{c_i}^2 &= \frac{\abs{\alpha}^2}{2}\end{aligned}$$
since the probabilities $\abs{c_i}^2$ must add up to 1. Substituting
this back into our state, we get $$\begin{aligned}
        \ket{\psi} &= e^{-\abs{\alpha}^2 / 2} e^{\abs{\alpha}^2 / 2} \ket{\alpha_1, \alpha_2, \ldots} \\
        &= \ket{\alpha_1, \alpha_2, \ldots}\end{aligned}$$ which is the
tensor product of a coherent state in each mode.
