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