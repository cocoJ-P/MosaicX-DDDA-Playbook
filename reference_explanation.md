# 📚 Reference Explanation

> This document explains how each cited reference is used within the DDDA project.

---

## [1] Constantine, P. G. _Data-Driven Dimensional Analysis: Algorithms and Applications_, 2017. [`@constantine2017datadrivendimensionalanalysisalgorithms`](https://github.com/cocoJ-P/How2DDDA/blob/main/references.bib)

📌 **Purpose**: Provided inspiration for building a fully data-driven Pi-group discovery process, with emphasis on algorithmic tractability and matrix formulations.

✅ **Used in**: `notebooks/How2DDDA.ipynb`, Section 5: "Pi Discovery via Null Space"  
🔍 **Key ideas reused**:

- Treating the dimension matrix `D` as a linear system
- Identifying null space of `D` as the basis of invariants
- Emphasizing numerical conditioning and interpretability

⚠️ **Adaptation**: While the original talk used MATLAB-style demos, we reimplemented the method in NumPy and SymPy, focusing on symbolic reasoning.

---
