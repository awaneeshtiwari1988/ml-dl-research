# ML/DL Research

Deep learning, NLP, and deep reinforcement learning projects — built to understand the mechanics, not just to call `.fit()`. Where it makes sense, I implement the core algorithm from scratch (NumPy, no autograd) before reaching for a framework, and I document what I learned from doing it that way.

This repo is under active construction as part of a structured MTech in AI & ML (BITS Pilani) plus independent study. Each project below will get its own subfolder with a self-contained README (problem, approach, results, and what I'd do differently).

---

## Planned projects (in build order)

- [ ] **Neural network from scratch** — MLP with forward/backward propagation in pure NumPy, no autograd. Benchmarked against a PyTorch equivalent for correctness.
- [ ] **CNN from scratch + transfer learning** — LeNet-style CNN from scratch on CIFAR-10/Fashion-MNIST, then fine-tuning a pretrained ResNet on a more interesting dataset.
- [ ] **Fine-tuned transformer + small RAG system** — Fine-tuning BERT/DistilBERT for text classification, then a lightweight retrieval-augmented generation pipeline over a domain-specific document set.
- [ ] **Deep RL agent (DQN/PPO)** — Trained on Gymnasium environments (CartPole → LunarLander → a harder Atari environment), with training curves and failure-mode analysis documented honestly.
- [ ] **Classical ML pipeline with proper experiment tracking** — Full EDA → feature engineering → model comparison → MLflow/W&B tracking → served via a simple API.

## Robotics + Multimodal AI (Sem 3 electives)

Robotics and Multimodal AI live here rather than in a separate repo — both are application areas that build directly on the Deep Learning and Deep RL work above, not separate technical disciplines. Keeping them in one place makes the connections between them visible instead of scattering related work across repos.

- [ ] **RL for robotic control** — a Deep RL agent (building on the DQN/PPO project above) applied to a robotics-flavored Gymnasium environment (e.g. a manipulation or continuous-control task), with sim-to-real considerations documented even if only simulated.
- [ ] **Multimodal representation learning** — a small CLIP-style joint embedding experiment: aligning image and text embeddings on a modest dataset, evaluated via cross-modal retrieval.
- [ ] **Vision-language-action demo (flagship for this pair)** — a scaled-down embodied-AI demo in the spirit of PaLM-E/RT-2: fusing a vision-language model's output with a simple control policy, even in a toy simulated environment. This is the project that visibly ties Robotics + Multimodal AI + Deep RL together.
- [ ] **(Stretch) Quantum-enhanced encoder swap** — once `quantum-ml` has a working VQC, swap one component of the vision-language-action demo for a quantum-enhanced encoder and benchmark against the classical version — the single project that touches all three portfolio lanes at once.

## Why from-scratch implementations

Being able to use `sklearn` or `torch.nn` doesn't tell you (or anyone reviewing this) whether you understand *why* something works. Each project here that says "from scratch" means the core math is implemented directly — backprop, gradient computation, the training loop — with a framework version alongside for comparison and validation.

## Status

🚧 Early build phase — first project (from-scratch MLP) in progress alongside coursework.

---

*Part of a three-lane portfolio — see [ml-systems-engineering](https://github.com/awaneeshtiwari1988/ml-systems-engineering) for production ML systems work, and [quantum-ml](https://github.com/awaneeshtiwari1988/quantum-ml) for quantum machine learning.*
