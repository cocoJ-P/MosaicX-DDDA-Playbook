# How2DDDA

> 🚀 **DDDA: Data-Driven Dimensional Analysis**
>
> 📐 From raw measurements to **optimal explicit functions in dimensionless form** — discover, evaluate, and refine the best local coordinate systems for describing physical manifolds.

This notebook is an interactive, hands-on walkthrough of **DDDA**, a lightweight yet extensible toolkit for building **data-driven dimensional analysis pipelines**.
It goes beyond simply computing Buckingham Π-groups: DDDA systematically searches variable combinations, evaluates **local solvability, sensitivity, and stability**, and selects the **optimal local coordinate system** in which the physical model’s manifold is expressed as a stable explicit function.

By combining **dimensional reduction** with **coordinate system optimization**, the workflow ensures that each explicit form — whether expressed in raw variables or dimensionless Π-groups — captures the physical phenomenon in its most robust, interpretable form.

---

📦 **What's inside?**

- 🔗 **Multi-source physical data integration** and preprocessing
- 📊 **Uncertainty quantification** across heterogeneous input sources
- ⚙️ **Automated Π-group discovery** via rank-reduction and null-space computation
- 🧭 **Local coordinate system search** with **solvability, sensitivity, and stability metrics**
- 🧩 **Phase-separated regime detection** and explicit function fitting
- 📚 Literature-backed insights with inline reasoning and discarded-path documentation

---

🧪 _Note: This is a research prototype — results and methods are evolving, and the work has not yet been formally published._

📁 All code and examples are shared to help researchers and engineers not only reproduce the results, but also understand the **decision logic** behind DDDA’s explicit-form selection, so they can adapt it to their own datasets and physical domains.

---

🔗 **Project Repository**:

- [https://github.com/cocoJ-P/MosaicPi](https://github.com/cocoJ-P/MosaicPi)
- [https://github.com/whoseboy/DDDA](https://github.com/whoseboy/DDDA)

---

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Build](https://github.com/<user>/owl-llm-cookbook/actions/workflows/ci.yml/badge.svg)](…)
[![MadeWith](https://img.shields.io/badge/Made%20with-Jupyter-blue)](…)
![Citations Tracked](https://img.shields.io/badge/references-traceable-blue)

---

## 📦 DDDA Integration

| Stage                                            | Description                                                                                                                         | Link     |
| ------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- | -------- |
| Variable & Physical Model Non-Dimensionalization | Define variables, construct or import the physical model, and apply reference-scale transformation to obtain its dimensionless form | [Open]() |
| Uncertainty Quantification                       | Estimate variance and confidence bounds across sources                                                                              | [Open]() |
| Pi Group Discovery                               | Automatically compute Pi groups using dimensional matrix                                                                            | [Open]() |
| Phase Detection                                  | Cluster or segment data based on dominant dimensionless groups                                                                      | [Open]() |

---

## 📦 Composite Algorithem

| Stage                | Description                                                    | Link     |
| -------------------- | -------------------------------------------------------------- | -------- |
| 隐函数显式化算法     | Estimate variance and confidence bounds across sources         | [Open]() |
| 光滑插值算法         | Automatically compute Pi groups using dimensional matrix       | [Open]() |
| Voronoi 空间赋权算法 | Cluster or segment data based on dominant dimensionless groups | [Open]() |

---

## 🧠 Techniques Used

|     | Method & Category                                                | Usage                                                                                                                                                                                       | Link                                                                                                                                                               |
| --- | ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1   | **Buckingham Pi Theorem & Dimensional Analysis**                 | Foundation for discovering dimensionless invariants (Π-groups) from physical variables and base units                                                                                       | [Open](https://github.com/cocoJ-P/How2DDDA/blob/main/notebooks/Techniques/Buckingham%20Pi%20Theorem%20%26%20Dimensional%20Analysis.ipynb)                          |
| 2   | **Linear Algebra: SVD, Eigenvalues & Eigenvectors**              | Used to estimate the rank of the dimensional matrix, identify null space, and analyze structural properties of dimensional systems                                                          | [Open]()                                                                                                                                                           |
| 3   | **Partial Derivatives & Physical Surface Morphology in Π-Space** | 计算无量纲数函数在 Π 空间的梯度与形貌特征，帮助理解变量之间的敏感性分布与几何结构                                                                                                           | [Open](https://github.com/cocoJ-P/How2DDDA/blob/main/notebooks/Techniques/Partial%20Derivatives%20in%20%CE%A0-Space%20and%20Physical%20Surface%20Morphology.ipynb) |
| 4   | **Mathematical Foundations for Explicitization**                 | 从隐函数的性质出发，进行扫描与可解性判定，通过稳定性与敏感性分析挑选最优显函数分组，并支持自动化组合策略                                                                                    | [Open](https://github.com/cocoJ-P/How2DDDA/blob/main/notebooks/Techniques/Implicit%20Function%20Theory.ipynb)                                                      |
| 4.1 | &emsp; ├─ Partitioning Strategy for Explicitization              | 在非线性隐函数曲面上，通过指标分布（det、cond、敏感性）进行空间分区，不同区域采用最优显式化分组；类比流形图册的局部坐标贴片方法                                                             | [Open]()                                                                                                                                                           |
| 4.2 | &emsp; ├─ Linear System Explicitization                          | 针对线性隐函数系统，利用常数雅可比矩阵进行一次性可解性与稳定性判定，无需区域化处理；适合在已知显式化关系或近似线性假设下的快速分析                                                          | [Open]()                                                                                                                                                           |
| 4.3 | &emsp; ├─ Nonlinear System Explicitization                       | 针对非线性系统，结合采样、指标计算与分区策略，避免奇异点与病态区域；支持局部拟合与多分组切换，实现全局稳定的显式化建模                                                                      | [Open]()                                                                                                                                                           |
| 4.4 | &emsp; └─ Data-Driven Jacobian Estimation (No Physics Model)     | 当缺乏显式物理模型时，从数据中估计 \(J\) / \(J_y\)：局部线性回归（邻域最小二乘）、扰动实验/有限差分、核回归/高斯过程导数、神经网络+自动微分、稀疏识别（SINDy/ SR3），并评估 det/cond/敏感性 | [Open]()                                                                                                                                                           |

## 🏃 Quickstart

```bash
git clone https://github.com/cocoJ-P/MosaicPi_101.git
cd MosaicPi_101
conda env create -f environment.yml  # or pip install -r requirements.txt
jupyter lab
```

---

## 📚 Reference System

This project uses a dual-layer reference system:

- [`references.bib`](./references.bib): Machine-readable BibTeX database of all sources.
- [`reference_explanation.md`](./reference_explanation.md): Human-readable explanations for each reference, including implementation context and usage notes.

🔎 We believe in **traceable and reproducible citations**: every reference in this project is either directly implemented, conceptually adapted, or compared with.

🧪 References are also reflected inside our [How2DDDA.ipynb](./notebooks/How2DDDA.ipynb) notebook with inline comments and links.

---

## 📝 quote

```bibtex
@misc{pang2025MosaicPi_101,
  author       = {Jiashun Pang},
  title        = {MosaicPi_101: A Hands-on Tutorial for MosaicPi},
  year         = {2025},
  url          = {https://github.com/cocoJ-P/MosaicPi_101},
  note         = {Accessed August 7, 2025}
}
```

---

## 🙏 Acknowledgement

This work acknowledges **DDDA (Data-Driven Dimensional Analysis)** as a precursor framework that laid the groundwork for data-driven approaches to dimensional analysis and explicit function selection. The development of MosaicPi was informed by the concepts and iterative practices established in DDDA, while extending them toward a more general framework for implicit–explicit partitioning, uncertainty propagation, and experiment-informed model refinement.

🔗 **DDDA Project Repository**: [https://github.com/whoseboy/DDDA](https://github.com/whoseboy/DDDA)

---
