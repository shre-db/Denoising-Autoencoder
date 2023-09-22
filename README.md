# Denoising-Autoencoder

An autoencoder is a specific type of a neural network, which is mainly designed to encode the input into a compressed and meaningful representation, and then decode it back such that the reconstructed input is similar as possible to the original one.

Denoising autoencoders can be viewed either as a regularization option, or as a robust autoencoder which can be used for error correction. In these architectures, the input is distrupted by some noise (e.g., additive white Gaussian noise or erasures using Dropout) and the autoencoder is expected to reconstruct the clear version of the input.

![Denoising-Autoencoder]("images/Denoising-Autoencoder.png")

Two common noise options for disrupting inputs images are:
1. **Gaussian Noise**<br>
$\tilde x$ is  random variable, whose distribution is given by <br>$$C_{\sigma}(\tilde x|x) = \mathcal{N}(x, \sigma^2 \mathcal{I})$$
The variance parameter $\sigma$ sets the impact of the noise.
<br><br>
2. **Bernoulli Noise**<br>
$\tilde x$ is  random variable, whose distribution is given by <br>$$C_{p}(\tilde x|x) = \mathcal{\beta} \odot x, \hspace{3mm} \beta \sim Ber(p)$$
where $\odot$ denotes an element wise (Hadamard) product. The parameter $p$ sets the probability of a value in $x$ not being nullified.

