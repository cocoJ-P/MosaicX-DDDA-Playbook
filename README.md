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

🧪 *Note: This is a research prototype and the work has not yet been formally published.*

📁 All code and examples are shared to help researchers and engineers understand the reasoning behind DDDA — and to make it easy to try on your own data.

🔗 **Project Repository**: [https://github.com/whoseboy/DDDA](https://github.com/whoseboy/DDDA)

---
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Build](https://github.com/<user>/owl-llm-cookbook/actions/workflows/ci.yml/badge.svg)](…)
[![MadeWith](https://img.shields.io/badge/Made%20with-Jupyter-blue)](…)

---

## 📦 DDDA Pipeline

| Stage | Description |  Link |
|-------|-------------| ------|
| Data Integration | Load raw quantities and units from CSV, JSON, or measurement logs | [Open]() |
| Uncertainty Quantification | Estimate variance and confidence bounds across sources | [Open]() |
| Pi Group Discovery | Automatically compute Pi groups using dimensional matrix | [Open]() |
| Phase Detection | Cluster or segment data based on dominant dimensionless groups | [Open]() |

---
## 🧠 Techniques Used
| Method | Usage | Link |
|--------|-------|------|
| Null space solver | For discovering dimensional invariants (Π-groups) | [Open]() |
| SVD | Estimate rank and reduce noise in dimensional matrices | [Open]() |
| Sparse regression (e.g. LASSO) | Optional post-selection of relevant invariants | [Open]() |
| Symbolic algebra (SymPy) | For expressing Pi groups in interpretable form | [Open]() |

---
## 🏃 Quickstart

```bash
git clone https://github.com/cocoJ-P/How2DDDA.git
cd How2DDDA
conda env create -f environment.yml  # or pip install -r requirements.txt
jupyter lab
```

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
