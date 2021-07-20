# Vector Calculus

## Coordinate System Conversion$$\require{physics}\newcommand{\x}{\vu{x}}\newcommand{\y}{\vu{y}}\newcommand{\z}{\vu{z}}\newcommand{\r}{\vu{r}}\newcommand{\s}{\vu{s}}\newcommand{\l}{\vb{l}}\newcommand{\v}{\vb{v}}\newcommand{\f}{\hat{\boldsymbol{\phi}}}\newcommand{\q}{\hat{\boldsymbol{\theta}}}$$

### Spherical

$$x = r\sin\theta\cos\phi$$

$$y = r\sin\theta\sin\phi$$

$$z = r\cos\theta$$

$$\x = \sin\theta\cos\phi\r + \cos\theta\cos\phi\q - \sin\phi\f$$

$$\y = \sin\theta\sin\phi\r + \cos\theta\sin\phi\q + \cos\phi\f$$

$$\z = \cos\theta\r - \sin\theta\q$$

$$r = \sqrt{x^2 + y^2 + z^2}$$

$$\theta = \tan^{-1}\left(\sqrt{x^2 + y^2}/z\right)$$

$$\phi = \tan^{-1}(y/x)$$

$$\r = \sin\theta\cos\phi\x + \sin\theta\sin\phi\y + \cos\theta\z$$

$$\q = \cos\theta\cos\phi\x + \cos\theta\sin\phi\y - \sin\theta\z$$

$$\f = -\sin\phi\x + \cos\phi\y$$

### Cylindrical

$$x = s\cos\phi$$

$$y = s\sin\phi$$

$$\x = \cos\phi\s - \sin\phi\f$$

$$\y = \sin\phi\s + \cos\phi\f$$

$$s = \sqrt{x^2 + y^2}$$

$$\phi = \tan^{-1}(y/x)$$

$$\s = \cos\phi\x + \sin\phi\y$$

$$\f = -\sin\phi\x + \cos\phi\y$$

## Derivatives

### Cartesian

$$\dd\l = \dd x \x + \dd y \y + \dd z \z \qquad \dd \tau = \dd x \dd y \dd z$$

$$\grad{f} = \pdv{f}{x}\x + \pdv{f}{y}\y + \pdv{f}{z}\z$$

$$\div{\v} = \pdv{v_x}{x} + \pdv{v_y}{y} + \pdv{v_z}{z}$$

$$\curl{\v} = \left(\pdv{v_z}{y} - \pdv{v_y}{z}\right)\x + \left(\pdv{v_x}{z} - \pdv{v_z}{x}\right)\y + \left(\pdv{v_y}{x} - \pdv{v_x}{y}\right)\z$$

$$\grad^2f = \pdv[2]{f}{x} + \pdv[2]{f}{y} + \pdv[2]{f}{z}$$

### Spherical

### Cylindrical

## Identities

## Theorems

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>
