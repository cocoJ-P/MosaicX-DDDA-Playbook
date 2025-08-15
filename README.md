# How2DDDA

> 🚀 **DDDA: Data-Driven Dimensional Analysis**
>
> 📐 From raw data to interpretable dimensional insight — integrate, quantify, reduce, and explain.

This notebook is a hands-on walkthrough of **DDDA**, a lightweight yet extensible toolkit for building dimensional analysis pipelines from data. It aims to **automate the discovery of Buckingham Π-groups**, quantify uncertainty, and reveal **phase-separated dimensional regimes** through real datasets.

DDDA 项目的交互式 notebook，不仅演示从多源聚合物理数据到自动 Pi 组发现和不确定性分析的全过程，还记录了关键设计决策、探索思路与被放弃的方法。

📦 **What's inside?**

- 🔗 **Data integration** for physical quantities
- 📊 **Uncertainty quantification** across input sources
- ⚙️ **Automated Π-group computation** using rank-reduction and null space logic
- 🧭 **Dimensional phase detection** and interpretation
- 📚 Literature-backed insights with inline explanations

🧪 _Note: This is a research prototype and the work has not yet been formally published._

📁 All code and examples are shared to help researchers and engineers understand the reasoning behind DDDA — and to make it easy to try on your own data.

🔗 **Project Repository**: [https://github.com/whoseboy/DDDA](https://github.com/whoseboy/DDDA)

---

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Build](https://github.com/<user>/owl-llm-cookbook/actions/workflows/ci.yml/badge.svg)](…)
[![MadeWith](https://img.shields.io/badge/Made%20with-Jupyter-blue)](…)
![Citations Tracked](https://img.shields.io/badge/references-traceable-blue)

---

## 📦 DDDA Integration

| Stage                                | Description                                                       | Link     |
| ------------------------------------ | ----------------------------------------------------------------- | -------- |
| Data Integration & Dimensionlization | Load raw quantities and units from CSV, JSON, or measurement logs | [Open]() |
| Uncertainty Quantification           | Estimate variance and confidence bounds across sources            | [Open]() |
| Pi Group Discovery                   | Automatically compute Pi groups using dimensional matrix          | [Open]() |
| Phase Detection                      | Cluster or segment data based on dominant dimensionless groups    | [Open]() |

---

## 📦 Composite Algorithem

| Stage                | Description                                                    | Link     |
| -------------------- | -------------------------------------------------------------- | -------- |
| 隐函数显式化算法     | Estimate variance and confidence bounds across sources         | [Open]() |
| 光滑插值算法         | Automatically compute Pi groups using dimensional matrix       | [Open]() |
| Voronoi 空间赋权算法 | Cluster or segment data based on dominant dimensionless groups | [Open]() |

---

## 🧠 Techniques Used

| Method & Category                                                | Usage                                                                                                                                                 | Link                                                                                                                                                               |
| ---------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Mathematical Foundations for Explicitization**                 | 建立从隐函数到显函数的数学框架，包括变量分组、雅可比矩阵、可解性（可逆性）、稳定性（条件数）、敏感性等核心指标的定义与计算方法                        | [Open]()                                                                                                                                                           |
| **Buckingham Pi Theorem & Dimensional Analysis**                 | Foundation for discovering dimensionless invariants (Π-groups) from physical variables and base units                                                 | [Open](https://github.com/cocoJ-P/How2DDDA/blob/main/notebooks/Techniques/Buckingham%20Pi%20Theorem%20%26%20Dimensional%20Analysis.ipynb)                          |
| **Linear Algebra: SVD, Eigenvalues & Eigenvectors**              | Used to estimate the rank of the dimensional matrix, identify null space, and analyze structural properties of dimensional systems                    | [Open]()                                                                                                                                                           |
| **Partial Derivatives & Physical Surface Morphology in Π-Space** | 计算无量纲数函数在 Π 空间的梯度与形貌特征，帮助理解变量之间的敏感性分布与几何结构                                                                     | [Open](https://github.com/cocoJ-P/How2DDDA/blob/main/notebooks/Techniques/Partial%20Derivatives%20in%20%CE%A0-Space%20and%20Physical%20Surface%20Morphology.ipynb) |
| **Implicit Function Theory (Parent)**                            | 从隐函数的性质出发，进行扫描与可解性判定，通过稳定性与敏感性分析挑选最优显函数分组，并支持自动化组合策略                                              | [Open](https://github.com/cocoJ-P/How2DDDA/blob/main/notebooks/Techniques/Implicit%20Function%20Theory.ipynb)                                                      |
| &emsp; ├─ **Partitioning Strategy for Explicitization**          | 在非线性隐函数曲面上，通过指标分布（det、cond、敏感性）进行空间分区，不同区域采用最优显式化分组，以提升可解性与稳定性；类比流形图册的局部坐标贴片方法 | [Open]()                                                                                                                                                           |
| &emsp; ├─ **Linear System Explicitization**                      | 针对线性隐函数系统，直接利用常数雅可比矩阵进行一次性可解性与稳定性判定，无需区域化处理；适合在已知显式化关系或近似线性假设下的快速分析                | [Open]()                                                                                                                                                           |
| &emsp; └─ **Nonlinear System Explicitization**                   | 针对非线性系统，结合采样、指标计算与分区策略，避免奇异点与病态区域；支持局部拟合与多分组切换，实现全局稳定的显式化建模                                | [Open]()                                                                                                                                                           |

## 🏃 Quickstart

```bash
git clone https://github.com/cocoJ-P/How2DDDA.git
cd How2DDDA
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
@misc{pang2025how2ddda,
  author       = {Jiashun Pang},
  title        = {How2DDDA: A Hands-on Tutorial for Data-Driven Dimensional Analysis},
  year         = {2025},
  url          = {https://github.com/cocoJ-P/How2DDDA},
  note         = {Accessed August 7, 2025}
}
```
