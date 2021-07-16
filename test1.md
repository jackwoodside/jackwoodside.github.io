# Question 3.
$$\require{physics}\newcommand{\x}{\vb{x}}$$

\(a\) In 1D, trying $$\vb{x}$$ and $$\vu{y}$$ and $$\curl{F}$$ and $$\x$$, all $$N$$ particles occupy the ground state of a harmonic
potential centred around $$x = 0$$. If we measured the number of particles
in the region $$-\infty < x < 0$$, what is the mean and variance of this
measurement?\
\
Initially, our state is $$\ket{\psi} = \ket{N,\{0\}}$$. The number
operator is given by $$\begin{aligned}
        \hat{N} &= \int \dd{x}\hat{\psi}^{\dagger}(x)\hat{\psi}(x)\end{aligned}$$
so the number of particles on the left is $$\begin{aligned}
         \hat{N}_l &= \int_{-\infty}^{0} \dd x \hat{\psi}^{\dagger}(x)\hat{\psi}(x).\end{aligned}$$
Since our state is in number notation, it would be easier if we convert
the above into this basis. We know that $$\begin{aligned}
        \hat{\psi}(x) &= \sum_{j} \phi_j(x)\hat{a}_j\end{aligned}$$ so
then the operator becomes $$\begin{aligned}
        \hat{N}_l &= \int_{-\infty}^{0} \dd x \sum_{ij} \phi_i^*(x)\phi_j(x)\hat{a}_i^{\dagger}\hat{a}_j.\end{aligned}$$
Then the mean of the measurement is $$\begin{aligned}
        \ev{\hat{N}_l} &= \ev{\hat{N}_l}{\psi} \\
                       &= \int_{-\infty}^{0} \dd x \sum_{ij} \phi_i^*(x)\phi_j(x)\bra{N,\{0\}}\hat{a}_i^{\dagger}\hat{a}_j\ket{N,\{0\}}.\end{aligned}$$
When the operators are applied forwards (or backwards) to states other
than the ground states, they will give zero. Therefore only the
$$i = j = 0$$ terms contribute, giving $$\begin{aligned}
        \ev{\hat{N}_l} &= \int_{-\infty}^{0} \abs{\phi_0(x)}^2 \sqrt{N} \sqrt{N} \\
                       &= N \int_{-\infty}^{0} \dd x \abs{\phi_0(x)}^2 \\
                       &= \frac{N}{2}.\end{aligned}$$ The variance is
given by
$$\ev{\sigma_{\hat{N_l}}} = \ev{\hat{N}_l^2} - \ev{\hat{N}_l}^2$$. We
already have the second term, so we just need to calculate the first
term. Then $$\begin{aligned}
        \ev{\hat{N}_l^2} &= \ev{\hat{N}_l\hat{N}_l}{\psi} \\
                         &= \int_{-\infty}^{0} \int_{-\infty}^{0} \dd x \dd x' \sum_{ijkl} \phi_i^*(x)\phi_j(x)\phi_k^*(x')\phi_l(x')\bra{N,\{0\}}\hat{a}_i^{\dagger}\hat{a}_j\hat{a}_k^{\dagger}\hat{a}_l\ket{N,\{0\}} \\
                         &= \int_{-\infty}^{0} \int_{-\infty}^{0} \dd x \dd x' \sum_{ijkl} \phi_i^*(x)\phi_j(x)\phi_k^*(x')\phi_l(x')\bra{N,\{0\}}\hat{a}_i^{\dagger}(\hat{a}_k^{\dagger}\hat{a}_j + \delta_{jk})\hat{a}_l\ket{N,\{0\}}.\end{aligned}$$
Expanding that out will give two terms, which we can consider
separately. For the first term, we get $$\begin{aligned}
        \int_{-\infty}^{0} \int_{-\infty}^{0} \dd x \dd x' \sum_{ijkl} \phi_i^*(x)\phi_j(x)\phi_k^*(x')\phi_l(x')\bra{N,\{0\}}\hat{a}_i^{\dagger}\hat{a}_k^{\dagger}\hat{a}_j\hat{a}_l\ket{N,\{0\}} &= \int_{-\infty}^{0} \int_{-\infty}^{0} \dd x \dd x' \abs{\phi_0(x)}^{2}\abs{\phi_0(x')}^2 \sqrt{N}^2\sqrt{N-1}^2 \\
                                                                                                                                                                                                                                          &= \frac{N(N-1)}{2 \cdot 2} = \frac{N(N-1)}{4}.\end{aligned}$$
For the second term, we get $$\begin{aligned}
        &\int_{-\infty}^{0} \int_{-\infty}^{0} \dd x \dd x' \sum_{ijkl} \phi_i^*(x)\phi_j(x)\phi_k^*(x')\phi_l(x')\bra{N,\{0\}}\hat{a}_i^{\dagger}\delta_{jk}\hat{a}_l\ket{N,\{0\}} \\
        &= \sum_j\int_{-\infty}^{0} \int_{-\infty}^{0} \dd x \dd x' \phi_0^*(x)\phi_j(x)\phi_j^*(x')\phi_0(x')N \\
        &= N \int_{-\infty}^{0} \int_{-\infty}^{0} \dd x \dd x' \delta(x-x')\phi_0^*(x)\phi_0(x') \\
        &= N \int_{-\infty}^{0} \dd x \abs{\phi_0(x)}^2 \\
        &= \frac{N}{2}.\end{aligned}$$ Overall, the variance is
$$\begin{aligned}
        \ev{\sigma_{\hat{N}_l}} &= \frac{N(N-1)}{4} + \frac{N}{2} - \frac{N^2}{4} \\
        &= \frac{N}{4}.\end{aligned}$$ (b) Generalise your result for a
measurement of the number of particles in any region $$x_1$$-$$x_2$$.
Express your answer in terms of the quantity $$\begin{aligned}
        F = \int_{x_1}^{x_2} \abs{\phi_0(x)}^2 \dd x,\end{aligned}$$
where $$\phi_0(x)$$ is a single-particle ground-state position-space
wavefunction of the harmonic potential.\
\
We can denote the number of particles in this region $$x_1$$-$$x_2$$ by
$$\begin{aligned}
        \hat{N}_x &= \int_{x_1}^{x_2} \dd x \sum_{ij} \phi_i^*(x)\phi_j(x)\hat{a}_i^{\dagger}\hat{a}_j.\end{aligned}$$
The only difference between this and our earlier operator $$\hat{N}_l$$ is
the integration bounds. This means that apart from the integral, the
same simplifications from (a) also work for this new operator. Therefore
the mean of the measurement is $$\begin{aligned}
        \ev{\hat{N}_x} &= N \int_{x_1}^{x_2} \abs{\phi_0}^2 \\
        &= FN.\end{aligned}$$ Similarly, we can calculate the variance
by first finding the two terms from $$\ev{\hat{N}_x^2}$$. The first term
is $$\begin{aligned}
        N(N-1) \int_{x_1}^{x_2}\int_{x_1}^{x_2}\dd x \dd x' \abs{\phi_0(x)}^2 \abs{\phi_0(x')}^2 &= F^2N(N-1)\end{aligned}$$
and the second term is $$\begin{aligned}
        N \int_{x_1}^{x_2} \int_{x_1}^{x_2} \dd x \dd x' \delta(x-x')\phi_0^*(x)\phi_0(x') &= N\int_{x_1}^{x_2} \dd x \abs{\phi_0(x)}^2 \\
        &= FN.\end{aligned}$$ Overall, the variance is $$\begin{aligned}
        \ev{\sigma_{\hat{N}_x}} &= F^2N(N-1) + FN - F^2N^2 \\
                                &= N(F-F^2).\end{aligned}$$
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
