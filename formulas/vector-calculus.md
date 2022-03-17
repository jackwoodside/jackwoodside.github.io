# Vector Calculus

## Coordinate System Conversion$$\require{physics}\newcommand{\x}{\vu{x}}\newcommand{\y}{\vu{y}}\newcommand{\z}{\vu{z}}\newcommand{\r}{\vu{r}}\newcommand{\s}{\vu{s}}\newcommand{\l}{\vb{l}}\newcommand{\v}{\vb{v}}\newcommand{\f}{\hat{\boldsymbol{\phi}}}\newcommand{\q}{\hat{\boldsymbol{\theta}}}\newcommand{\A}{\vb{A}}\newcommand{\B}{\vb{B}}\newcommand{\C}{\vb{C}}\newcommand{\a}{\vb{a}}\newcommand{\b}{\vb{b}}$$

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

$$\divergence{\v} = \pdv{v_x}{x} + \pdv{v_y}{y} + \pdv{v_z}{z}$$

$$\curl{\v} = \left(\pdv{v_z}{y} - \pdv{v_y}{z}\right)\x + \left(\pdv{v_x}{z} - \pdv{v_z}{x}\right)\y + \left(\pdv{v_y}{x} - \pdv{v_x}{y}\right)\z$$

$$\grad^2f = \pdv[2]{f}{x} + \pdv[2]{f}{y} + \pdv[2]{f}{z}$$

### Spherical

$$\dd\l = \dd r \r + r \dd \theta \q + r\sin\theta \dd \phi \f \qquad \dd \tau = r^2\sin\theta \dd r \dd \theta \dd \phi$$

$$\grad{f} = \pdv{f}{r}\r + \frac{1}{r}\pdv{f}{\theta}\q + \frac{1}{r\sin\theta}\pdv{f}{\phi}\f$$

$$\divergence{\v} = \frac{1}{r^2}\pdv{r}(r^2v_r) + \frac{1}{r\sin\theta}\pdv{\theta}(\sin\theta v_\theta) + \frac{1}{r\sin\theta}\pdv{v_\phi}{\phi}$$

$$\curl{\v} = \frac{1}{r\sin\theta}\left(\pdv{\theta}(\sin\theta v_\phi) - \pdv{v_\theta}{\phi}\right)\r + \frac{1}{r}\left(\frac{1}{\sin\theta}\pdv{v_r}{\phi} - \pdv{r}(rv_\phi)\right)\q + \frac{1}{r}\left(\pdv{r}(rv_\theta) - \pdv{v_r}{\theta}\right)\f$$

$$\grad^2f = \frac{1}{r^2}\pdv{r}\left(r^2\pdv{f}{r}\right) + \frac{1}{r^2\sin\theta}\pdv{\theta}\left(\sin\theta\pdv{f}{\theta}\right) + \frac{1}{r^2\sin^2\theta}\pdv[2]{f}{\phi}$$

### Cylindrical

$$\dd\l = \dd s \s + s \dd \phi \f + \dd z \z \qquad \dd \tau = s \dd s \dd \phi \dd z$$

$$\grad{f} = \pdv{f}{s}\s + \frac{1}{s}\pdv{f}{\phi}\f + \pdv{f}{z}\z$$

$$\divergence{\v} = \frac{1}{s}\pdv{s}(sv_s) + \frac{1}{s}\pdv{v_\phi}{\phi} + \pdv{v_z}{z}$$

$$\curl{\v} = \left(\frac{1}{s}\pdv{v_z}{\phi} - \pdv{v_\phi}{z}\right)\s + \left(\pdv{v_s}{z} - \pdv{v_z}{s}\right)\f + \frac{1}{s}\left(\pdv{s}(sv_\phi) - \pdv{v_s}{\phi}\right)\z$$

$$\grad^2f = \frac{1}{s}\pdv{s}\left(s\pdv{f}{s}\right) + \frac{1}{s^2}\pdv[2]{f}{\phi} + \pdv[2]{f}{z}$$

## Identities

### Triple Products

$$\A \cdot (\B \times \C) = \B \cdot (\C \times A) = \C \cdot (\A \times \B)$$

$$\A \times (\B \times \C) = \B(\A \cdot \C) - \C(\A \cdot \B)$$

### Product Rules

$$\grad(fg) = f(\grad g) + g(\grad f)$$

$$\grad(\A \cdot \B) = \A \times (\curl{\B}) + \B \times (\curl{\A}) + (A \cdot \grad)\B + (\B \cdot \grad)\A$$

$$\divergence{(f\A)} = f(\divergence{\A}) + \A \cdot (\grad f)$$

$$\divergence{(\A \times \B)} = \B \cdot (\curl{\A}) - \A \cdot (\curl{\B})$$

$$\curl{(f\A)} = f(\curl{\A}) - A \times (\grad f)$$

$$\curl{(\A \times \B)} = (\B \cdot \grad)\A - (\A \cdot \grad)\B + \A(\divergence{\B}) - \B(\divergence{\A})$$

### Second Derivatives

$$\divergence{(\curl{\A})} = 0$$

$$\curl{(\grad f)} = 0$$

$$\curl{(\curl{\A})} = \grad(\divergence{\A}) - \grad^2\A$$

## Theorems

### Gradient Theorem

$$\int_\a^\b (\grad f) \cdot \dd\l = f(\b) - f(\a)$$

### Stokes' Theorem

$$\int (\curl{\A}) \cdot \dd\a = \oint \A \cdot \dd\l$$

### Divergence Theorem

$$\int (\divergence{\A}) \dd\tau = \oint \A \cdot \dd\a$$

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>
