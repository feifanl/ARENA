# ARENA 3.0 AI Safety Curriculum (WIP)

My copy of the [ARENA AI Safety Curriculum](https://www.arena.education/curriculum) from [London Initiative for Safe AI (LISA)](https://www.safeai.org.uk/). ARENA is a structured curriculum that covers deep learning fundamentals, transformers, mechanistic interpretability, reinforcement learning, LLM evaluations, and other alignment topics such as emergent misalignment. This repo tracks my progress and key takeaways.

While self-studying ARENA, I have also replicated the seminal papers behind each section.

Huge shout out to LISA for making the curriculum public and doing so much for the AI safety space!

## Curriculum

### Chapter 0: Fundamentals

- [x] 0.0: Prereqs (PyTorch, einops, einsum)
- [x] 0.1: Ray tracing (vectorized geometry in PyTorch)
- [x] 0.2: Convolutional Neural Networks (CNNs) (build ResNet from scratch)
- [x] 0.3: Optimization (stochastic gradient descent, Adam, schedulers, hyperparam sweeps)
- [x] 0.4: Backpropagation (build autograd from scratch)
- [x] 0.5: VAEs and GANs

**Associated papers**:

- [x] **0.2 — CNNs / ResNet**: [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385) (He et al., 2015)
- [x] **0.3 — Optimization**: [Adam: A Method for Stochastic Optimization](https://arxiv.org/abs/1412.6980) (Kingma & Ba, 2014)
- [x] **0.5 — VAEs & GANs**: [Auto-Encoding Variational Bayes](https://arxiv.org/abs/1312.6114) (Kingma & Welling, 2013) · [Generative Adversarial Networks](https://arxiv.org/abs/1406.2661) (Goodfellow et al., 2014) · [DCGAN](https://arxiv.org/abs/1511.06434) (Radford et al., 2015)

### Chapter 1: Transformer Interpretability

- [x] 1.1: Transformer from scratch (GPT-style, attention, MLP, training)
- [x] 1.2: Intro to mech interp (TransformerLens, induction heads)
- [x] 1.3.1: Linear probes
- [x] 1.3.2: Function vectors and model steering
- [x] 1.3.3: Interpretability with sparse autoencoders (SAEs)
- [x] 1.3.4: Activation oracles
- [ ] 1.4.1: Indirect object identification (IOI) circuit
- [x] 1.4.2: SAE circuits
- [ ] 1.5.1: Balanced bracket classifier
- [x] 1.5.2: Grokking and modular arithmetic
- [x] 1.5.3: OthelloGPT
- [x] 1.5.4: Toy models of superposition and SAEs

**Associated papers**:

- [x] **1.1 — Transformer from scratch**: [Attention Is All You Need](https://arxiv.org/abs/1706.03762) (Vaswani et al., 2017)
- [x] **1.2 — Mech interp / induction heads**: [A Mathematical Framework for Transformer Circuits](https://transformer-circuits.pub/2021/framework/index.html) (Elhage et al., 2021) · [In-context Learning and Induction Heads](https://transformer-circuits.pub/2022/in-context-learning-and-induction-heads/index.html) (Olsson et al., 2022)
- [x] **1.3.2 — Function vectors & steering**: [Function Vectors in Large Language Models](https://arxiv.org/abs/2310.15213) (Todd et al., 2023) · [Activation Addition (Steering)](https://arxiv.org/abs/2308.10248) (Turner et al., 2023)
- [x] **1.3.3 / 1.5.4 — Superposition & SAEs**: [Toy Models of Superposition](https://transformer-circuits.pub/2022/toy_model/index.html) (Elhage et al., 2022) · [Towards Monosemanticity](https://transformer-circuits.pub/2023/monosemantic-features/index.html) (Bricken et al., 2023) · [Scaling Monosemanticity](https://transformer-circuits.pub/2024/scaling-monosemanticity/index.html) (Templeton et al., 2024)
- [x] **1.3.4 — Activation oracles**: [Activation Oracles: Training and Evaluating LLMs as General-Purpose Activation Explainers](https://arxiv.org/abs/2512.15674) (Karvonen et al., 2025)
- [ ] **1.4.1 — IOI circuit**: [Interpretability in the Wild: a Circuit for Indirect Object Identification in GPT-2 small](https://arxiv.org/abs/2211.00593) (Wang et al., 2022)
- [x] **1.4.2 — SAE circuits / transcoders**: [Sparse Feature Circuits](https://arxiv.org/abs/2403.19647) (Marks et al., 2024) · [Transcoders Find Interpretable LLM Feature Circuits](https://arxiv.org/abs/2406.11944) (Dunefsky et al., 2024)
- [x] **1.5.2 — Grokking & modular arithmetic**: [Progress Measures for Grokking via Mechanistic Interpretability](https://arxiv.org/abs/2301.05217) (Nanda et al., 2023) · [Grokking](https://arxiv.org/abs/2201.02177) (Power et al., 2022)
- [ ] **1.5.3 — OthelloGPT**: [Emergent World Representations](https://arxiv.org/abs/2210.13382) (Li et al., 2022) · [Othello-GPT Has a Linear Emergent World Representation](https://www.neelnanda.io/mechanistic-interpretability/othello) (Nanda, 2023)

### Chapter 2: Reinforcement Learning

- [ ] 2.1: Intro to RL (multi-armed bandits, tabular methods)
- [ ] 2.2: Deep Q-Network (DQN) and Vanilla policy gradient (VPG)
- [ ] 2.3: Proximal Policy Optimization (PPO)
- [ ] 2.4: Reinforcement learning from human feedback (RLHF)

**Associated papers**:

- [ ] **2.2 — DQN**: [Playing Atari with Deep Reinforcement Learning](https://arxiv.org/abs/1312.5602) (Mnih et al., 2013)
- [ ] **2.3 — PPO**: [Proximal Policy Optimization Algorithms](https://arxiv.org/abs/1707.06347) (Schulman et al., 2017)
- [ ] **2.4 — RLHF**: [Deep Reinforcement Learning from Human Preferences](https://arxiv.org/abs/1706.03741) (Christiano et al., 2017) · [Fine-Tuning Language Models from Human Preferences](https://arxiv.org/abs/1909.08593) (Ziegler et al., 2019)

### Chapter 3: LLM Evaluations

- [ ] 3.1: Intro to evals (capability + alignment evals)
- [ ] 3.2: Dataset generation
- [ ] 3.3: Running evals with Inspect (UK AISI framework)
- [ ] 3.4: LLM agents (tool use, agentic eval design)

**Associated papers**:

- [ ] **3.1 / 3.2 — Evals & dataset generation**: [Discovering Language Model Behaviors with Model-Written Evaluations](https://arxiv.org/abs/2212.09251) (Perez et al., 2022)
- [ ] **3.3 — Running evals with Inspect**: [Inspect](https://inspect.aisi.org.uk/) (UK AISI framework)

### Chapter 4: Alignment Science

- [ ] 4.1: Emergent misalignment
- [ ] 4.2: Science of misalignment
- [ ] 4.3: Interpreting reasoning models (interp on chain-of-thought reasoning models)
- [ ] 4.4: LLM Psychology & Persona Vectors
- [ ] 4.5: Investigator Agents (Petri, Bloom)

**Associated papers**:

- [ ] **4.1 — Emergent misalignment**: [Emergent Misalignment: Narrow Finetuning Can Produce Broadly Misaligned LLMs](https://arxiv.org/abs/2502.17424) (Betley et al., 2025)
- [ ] **4.4 — LLM psychology & persona vectors**: [Persona Vectors: Monitoring and Controlling Character Traits in Language Models](https://arxiv.org/abs/2507.21509) (Chen et al., 2025)
- [ ] **4.5 — Investigator agents**: [Petri: An Open-Source Auditing Tool to Accelerate AI Safety Research](https://www.anthropic.com/research/petri-open-source-auditing) (Anthropic, 2025)
