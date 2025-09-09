# FAS-MOEA: Multi-Objective Evolutionary Optimization for Accurate, Fair, and Serendipitous Recommendations

This repository contains the official implementation of the framework described in our **IPM submission**.  
We develop a **Fairness-Aware Serendipity-enhanced Multi-Objective Evolutionary Algorithm (FAS-MOEA)** for recommender systems, balancing **accuracy, fairness, and serendipity** simultaneously.

> **Note:** The provided notebook runs on a **small random subset** of the Amazon Electronics dataset for **demonstration and reproducibility**.  
> Absolute metric values are low due to subsampling. Please focus on **relative performance trends** compared to baselines.  
> Full dataset results, as reported in the paper, are significantly higher.

---

## Overview
- Implements a **multi-objective NSGA-II optimization** with custom operators (list-aware crossover, targeted mutation).  
- Evaluates **accuracy, fairness, and serendipity** objectives.  
- Uses **Amazon Electronics (SNAP)** dataset for benchmarking.  
- Includes standard recommendation metrics: Precision@K, Recall@K, nDCG@K, Diversity, Novelty, Explainability.  

---

## Requirements

Install required packages:

```bash
pip install pymoo==0.6.0 pandas tqdm scikit-learn matplotlib pyarrow
```

OR

Install dependencies with:

```bash
pip install -r requirements.txt
```

## Dataset

We use the Amazon Electronics dataset from SNAP:
- reviews_Electronics_5.json.gz → user-item interactions
- meta_Electronics.json.gz → metadata (categories, attributes, item popularity)

The notebook automatically downloads them if not already present.

For demonstration, we also use a small random subset (~2k users × 1k items) to ensure reproducibility and reasonable runtime.

> **Note:** Scores on the subset are much lower in absolute value than full dataset results.
> Reviewers should focus on relative trends and Pareto trade-offs.

## 
