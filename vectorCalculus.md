
# Vector Calculus $$\require{physics}$$

## Coordinate System Conversion

### Spherical

$$x = r\sin\theta\cos\phi$$

$$y = r\sin\theta\sin\phi$$

$$z = r\cos\theta$$

$$\x = \sin\theta\cos\phi\r + \cos\theta\cos\phi\mathbf{\hat{\boldsymbol{\theta}}} - \sin\phi\mathbf{\hat{\boldsymbol{\phi}}}$$

$$\y = \sin\theta\sin\phi\r + \cos\theta\sin\phi\mathbf{\hat{\boldsymbol{\theta}}} + \cos\phi\mathbf{\hat{\boldsymbol{\phi}}}$$

$$\z = \cos\theta\r - \sin\theta\mathbf{\hat{\boldsymbol{\theta}}}$$

$$r = \sqrt{x^2 + y^2 + z^2}$$

$$\theta = \tan^{-1}\left(\sqrt{x^2 + y^2}/z\right)$$

$$\phi = \tan^{-1}(y/x)$$

$$\r = \sin\theta\cos\phi\x + \sin\theta\sin\phi\y + \cos\theta\z$$

$$\mathbf{\hat{\boldsymbol{\theta}}} = \cos\theta\cos\phi\x + \cos\theta\sin\phi\y - \sin\theta\z$$

$$\mathbf{\hat{\boldsymbol{\phi}}} = -\sin\phi\x + \cos\phi\y$$

### Cylindrical

$$x = s\cos\phi$$

$$y = s\sin\phi$$

$$\x = \cos\phi\s - \sin\phi\mathbf{\hat{\boldsymbol{\phi}}}$$

$$\y = \sin\phi\s + \cos\phi\mathbf{\hat{\boldsymbol{\phi}}}$$

$$s = \sqrt{x^2 + y^2}$$

$$\phi = \tan^{-1}(y/x)$$

$$\s = \cos\phi\x + \sin\phi\y$$

$$\mathbf{\hat{\boldsymbol{\phi}}} = -\sin\phi\x + \cos\phi\y$$

## Derivatives

## Identities

## Theorems

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>
<script>
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [['$','$'], ['\\(','\\)']],
      processEscapes: true
    }
    TeX: {
      Macros: {
        x: "{\vu{x}}"
        y: "{\vu{y}}"
        z: "{\vu{z}}"
        r: "{\vu{r}}"
        s: "{\vu{s}}"
      }
    }
  });
</script>
