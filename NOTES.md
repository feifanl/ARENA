# ARENA Notes

## Chapter 0
### 0.0
- Python: Learned some interesting things such as dir(object), __slots__, and pprint
- Einops: b h w c mean batch height width color
- Einops: Collapse dimensions using () e.g. "b h w c" -> "b (h w c)"
- Broadcasting: two tensors in elementwise operation can be of diff sizes, broadcasting prepends dummy dims (size 1) until both have same n_dims, then can copy within a dim if its size 1 until the corresponding dim on the other tensor is of the same size
  - The dimension needs to be 1 to be copied
  - Goes from right to left
- Learned basic applications of einops and torch tensor methods for ML like softmax and cross-entropy loss
- Learned einsum

### 0.1
- Manipulating tensors is quite annoying lol
- intersect_rays_1d was pretty challenging
- "s.t." means such that
- Assertions are important and I should learn to use them 

### 0.2
- I might not actually like coding and may instead just think of it as a means to an end
- This section really boring to me -- writing code and reimplementing functions just isn't exciting
- Will skip to 0.3

### 0.3
- Not that interesting either
- Momentum is interesting; coding the optimizers themselves isn't as much
  - I find the concepts fascinating

### 0.4
- Backprop is simple, and implementing it is boring

### 0.5
- This stuff is much more fun, maybe its because we abstract away a lot of things like optimizers and aren't fiddling around with tensor manipulation
- It is difficult for autoencoders to generate content
  - An approach to generation could be sampling randomly from latent space and decoding
  - But if autoencoder has close to lossless compression, it's likely overfitted and may not have fully coherent latent space
- Variational autoencoders use regularisation to make autoencoders capable of generative capabilities
- Encoders act as data compression, decoders reconstruct initial space
  - Want to find best encoder/decoder pair that minimizes loss on compression and loss on reconstruction
- VAEs enforce regularization by making encoders encode a distribution over latent space rather than a single point
  - The decoder then samples from that distribution, and the error from the deconstruction is backpropagated through the network
  - Since the distribution is enforced to be normal, this is a form of regularization and also prevents overfitting (distribution, and decoder samples randomly)
  - Regularisation happens using a regularisation term that is expressed as the KL divergence between a standard Gaussian and the encoder's returned distribution
    - To prevent model from cheating by creating distributions with low variance or with high mean variance, we regularize the mean to be close to 0 and the covariance matrix to avoid narrow distributions
- GANs work by training a generator and a discriminator: the generator learns to generate better and better outputs to fool the discriminator and the discriminator tries to classify outputs as real or fake
  - There is a problem of convergence: the discriminator gives feedback to the generator (backpropagation, gradients calculated for generator BUT weights are not updated for discriminator (creates a moving target for generator to optimize against)), but as the generator gets better, the discriminator gets less accurate
    - This leads to worse feedback as the generator starts training against junk results