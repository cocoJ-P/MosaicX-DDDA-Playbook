# 📚 Reference Explanation

> This document explains how each cited reference is used within the DDDA project.

---

## [1] Buckingham, E. _On Physically Similar Systems; Illustrations of the Use of Dimensional Equations_, 1914. [`@PhysRev.4.345`](https://github.com/cocoJ-P/How2DDDA/blob/main/references.bib)

📌 **Purpose**: Formulated the **Buckingham-Π theorem**, proving that any physical law involving _n_ dimensional variables and _k_ base dimensions can be recast in terms of _n − k_ dimensionless Π groups. This work became the cornerstone of modern dimensional analysis.

✅ **Used in**: `notebooks/How2DDDA.ipynb` — _Section 2.1: build_dimension_matrix()_ and _Section 2.3: solve_null_space()_

🔍 **Key ideas reused**:

- Enforced the **principle of dimensional homogeneity**, asserting that physical equations must remain valid regardless of unit systems.
- Introduced a **systematic procedure for generating Π-groups** by:
  - Selecting _k_ repeating variables covering the base units,
  - Constructing invariant monomials for the remaining variables.
- Proved that **the number of independent Π-groups is n − k**, aligning with the nullity of the dimension matrix.
- Presented **classic examples** (ideal gas law, pipe flow, propeller thrust) showing how Π-groups unify experimental data.

⚠️ **Adaptation**:

- Replaced manual symbolic handling with a **linear algebra formulation**:
  - Construct the dimension matrix **D** (rows = units, cols = variables),
  - Solve `null(D)` using symbolic methods (`SymPy`) or numerical (`NumPy/SVD`),
  - Auto-detect repeating variables via matrix rank and QR decomposition,
  - Confirm equivalence with original Π-groups by comparing symbolic forms.

This allowed seamless integration of Buckingham’s reasoning into modern computational workflows for **data-driven dimensional analysis**.

---

## [2] Constantine, P. G. _Data-Driven Dimensional Analysis: Algorithms and Applications_, 2017. [`@constantine2017datadrivendimensionalanalysisalgorithms`](https://github.com/cocoJ-P/How2DDDA/blob/main/references.bib)

📌 **Purpose**: Provided inspiration for building a fully data-driven Pi-group discovery process, with emphasis on algorithmic tractability and matrix formulations.

✅ **Used in**: `notebooks/How2DDDA.ipynb`— _Section 3.2: compute_pi_groups()_

🔍 **Key ideas reused**:

- Treating the dimension matrix `D` as a linear system
- Identifying null space of `D` as the basis of invariants
- Emphasizing numerical conditioning and interpretability

⚠️ **Adaptation**: While the original talk used MATLAB-style demos, we reimplemented the method in NumPy and SymPy, focusing on symbolic reasoning.

---
