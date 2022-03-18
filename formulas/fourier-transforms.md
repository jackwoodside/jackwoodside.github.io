# Fourier Transforms

## Definition$$\require{physics}\newcommand{\F}{\mathcal{F}}\newcommand{\f}{\hat{f}}\newcommand{\g}{\hat{g}}$$

### Fourier Transform

$$\f(k) = \int_{-\infty}^\infty f(x)e^{-2\pi ikx} \dd x$$

### Inverse Fourier Transform

$$f(x) = \int_{-\infty}^\infty \f(k)e^{2\pi ikx} \dd k$$

$$f(-x) = \hat{\f}(x)$$

### Convolution

$$(f \ast g)(x) = \int_{-\infty}^\infty f(x-y)g(y) \dd y$$

## Properties

<center>
| $$f(x)$$       | $$\f(k)$$                |
|:------------------:|:--------------------------------------:|
| $$f'(x)$$      | $$2\pi ik\f(k)$$             |
| $$-2\pi ixf(x)$$   | $$\f'(k)$$                |
| $$f(x-a)$$      | $$e^{-2\pi iak}\f(k)$$          |
| $$e^{2\pi iax}f(x)$$ | $$\f(k-a)$$               |
| $$af(x) + bg(x)$$  | $$a\f(k) + b\g(k)$$           |
| $$f(ax)$$      | $$\frac{1}{a}\f\left(\frac{k}{a}\right)$$ |
| $$f(x)g(x)$$     | $$(\f \ast \g)(k)$$           |
| $$(f \ast g)(x)$$  | $$\f(k)\g(k)$$              |
</center>

## Common Transforms

<center>
|                | $$f(x)$$     | $$\f(k)$$                  |
|:--------------:|:---------------:|:------------------------------------------:|
| Delta Function | $$\delta(x)$$   |                      1                     |
|    Constant    |        1        | $$\delta(k)$$                |
|   Exponential  | $$e^{-a\abs{x}}$$ | $$\frac{2a}{a^2 + (2\pi k)^2}$$       |
|    Gaussian    | $$e^{-\pi x^2}$$ | $$e^{-\pi k^2}$$               |
|    Heaviside   | $$H(x)$$     | $$\frac{1}{2}\delta(k) + \frac{1}{2\pi ik}$$ |
|      Sign      | $$H(x) - H(-x)$$ | $$\frac{1}{\pi ik}$$             |
|     Square     | $$H(a-\abs{x})$$ | $$\frac{1}{\pi k}\sin(2\pi ka)$$       |
</center>

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>
