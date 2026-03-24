
# MP-SAE

This repository accompanies the NeurIPS 2025 paper:
<div align="center">

### **From Flat to Hierarchical: Extracting Sparse Representations with Matching Pursuit**

**Valérie Costa · Thomas Fel · Ekdeep Singh Lubana · Bahareh Tolooshams · Demba E. Ba**

[OpenReview](https://openreview.net/forum?id=Ll5miDx8KB) · [NeurIPS](https://neurips.cc/virtual/2025/loc/san-diego/poster/118531)

</div>

```bibtex
@inproceedings{
costa2025from,
title={From Flat to Hierarchical: Extracting Sparse Representations with Matching Pursuit},
author={Val{\'e}rie Costa and Thomas Fel and Ekdeep Singh Lubana and Bahareh Tolooshams and Demba E. Ba},
booktitle={The Thirty-ninth Annual Conference on Neural Information Processing Systems},
year={2025},
url={https://openreview.net/forum?id=Ll5miDx8KB}
}
````

> ⚠️ **Credit**: The majority of this codebase is adapted from the original implementation by [Noa Nabeshima](https://github.com/noanabeshima/matryoshka-saes), accompanying the paper:
> **["Learning Multi-Level Features with Matryoshka Sparse Autoencoders"](https://arxiv.org/abs/2503.17547)**
> *Bart Bussmann, Noa Nabeshima, Adam Karvonen, Neel Nanda*

## 🧠 About This Project

In this work, we revisit the assumptions underlying conventional sparse autoencoders—such as global quasi-orthogonality—and propose **MP-SAE**, a novel architecture that encourages *conditional orthogonality* through a residual-guided, greedy inference process inspired by Matching Pursuit.

To evaluate our model, we extend the synthetic benchmark introduced by Matryoshka SAEs and compare MP-SAE against several standard variants.


## 🔗 Related Implementations

An implementation of **MP-SAE** is also available in the excellent [**overcomplete SAE library**](https://github.com/KempnerInstitute/overcomplete), developed by co-author Thomas Fel:

* [https://github.com/KempnerInstitute/overcomplete/blob/main/overcomplete/sae/mp_sae.py](https://github.com/KempnerInstitute/overcomplete/blob/main/overcomplete/sae/mp_sae.py)

The large-scale vision experiments presented in our paper were conducted using this library. We recommend checking it out for additional implementations and perspectives on sparse autoencoders.

## 🧩 Synthetic Toy Hierarchy

We benchmark four SAE variants—Vanilla, BatchTopK, Matryoshka, and our proposed MP-SAE—on a two-level tree hierarchy of concepts. This setup builds upon the synthetic experiment from the Matryoshka SAE paper with the following key modifications:

* Ground-truth features are generated with explicit control over intra-level correlations.
* Children nodes are mutually exclusive (only one can be active at a time).
* We introduce variance in the code activations so that parent and child activation strengths are not perfectly correlated.

![Synthetic Hierarchy](synthetic_tree.png)


## 📄 Citation

If you use this codebase, please cite both our work and the original Matryoshka SAE paper:

### Matching Pursuit Sparse Autoencoders (this work)

```bibtex
@inproceedings{
costa2025from,
title={From Flat to Hierarchical: Extracting Sparse Representations with Matching Pursuit},
author={Val{\'e}rie Costa and Thomas Fel and Ekdeep Singh Lubana and Bahareh Tolooshams and Demba E. Ba},
booktitle={The Thirty-ninth Annual Conference on Neural Information Processing Systems},
year={2025},
url={https://openreview.net/forum?id=Ll5miDx8KB}
}
```

### Matryoshka Sparse Autoencoders

```bibtex
@inproceedings{
bussmann2025learning,
title={Learning Multi-Level Features with Matryoshka Sparse Autoencoders},
author={Bart Bussmann and Noa Nabeshima and Adam Karvonen and Neel Nanda},
booktitle={Forty-second International Conference on Machine Learning},
year={2025},
url={https://openreview.net/forum?id=m25T5rAy43}
}
```
