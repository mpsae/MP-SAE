
# MP-SAE Synthetic Experiments

> ⚠️ **Credit**: The majority of this codebase is adapted from the original implementation by [Noa Nabeshima](https://github.com/noanabeshima/matryoshka-saes), accompanying the paper:
> **["Learning Multi-Level Features with Matryoshka Sparse Autoencoders"](https://arxiv.org/abs/2503.17547)**
> *Bart Bussmann, Noa Nabeshima, Adam Karvonen, Neel Nanda*

## 🧠 About This Project

This repository supports our NeurIPS 2025 submission:

> **From Flat to Hierarchical: Extracting Sparse Representations with Matching Pursuit**

In this work, we revisit the assumptions underlying conventional sparse autoencoders—such as global quasi-orthogonality—and propose **MP-SAE**, a novel architecture that encourages *conditional orthogonality* through a residual-guided, greedy inference process inspired by Matching Pursuit. To evaluate our model, we extend the synthetic benchmark introduced by Matryoshka SAEs and compare MP-SAE against several standard variants.

## 🧩 Synthetic Toy Hierarchy

We benchmark four SAE variants—Vanilla, BatchTopK, Matryoshka, and our proposed MP-SAE—on a two-level tree hierarchy of concepts. This setup builds upon the synthetic experiment from the Matryoshka SAE paper with the following key modifications:

* Ground-truth features are generated with explicit control over intra-level correlations.
* Children nodes are mutually exclusive (only one can be active at a time).

![Synthetic Hierarchy](figures/synthetic_tree.png)

## 📄 Acknowledgments

This project is heavily based on the original implementation by [Noa Nabeshima](https://github.com/noanabeshima/matryoshka-saes). We are grateful to the authors for releasing their code. If you use this codebase or build on it, please cite their original work:

```bibtex
@article{bussmann2024matryoshka,
  title={Learning Multi-Level Features with Matryoshka Sparse Autoencoders},
  author={Bussmann, Bart and Nabeshima, Noa and Karvonen, Adam and Nanda, Neel},
  year={2024}
}
```


