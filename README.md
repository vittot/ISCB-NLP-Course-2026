# ISCB-NLP-Course-2026

Material for the pre-conference course **"Clinical Text Mining under Real-World Constraints"**, held at ISCB-GMDS 2026.

Taught by Vittorio Torri and Francesca Ieva (MOX Lab, Politecnico di Milano)

The course introduces NLP methods for clinical text in settings where labelled data is scarce, moving from unsupervised exploration to weak supervision, interpretable models, and prompting with open-weight LLMs. Each part combines short theory with a hands-on notebook.

## Contents

| Notebook | Topic |
|---|---|
| [`notebooks/ex1_clustering_exercise.ipynb`](notebooks/ex1_clustering_exercise.ipynb) | Clustering short clinical texts: contextual embeddings, PCA, HDBSCAN, and mapping clusters to clinical guidelines |
| [`notebooks/ex2_weak_supervision_classification.ipynb`](notebooks/ex2_weak_supervision_classification.ipynb) | Weak supervision: turning cluster-derived labels into training data for a Transformer classifier |
| [`notebooks/ex3_explainability.ipynb`](notebooks/ex3_explainability.ipynb) | Interpretable models with Aug-Linear (n-gram Transformer embeddings + linear model) |
| [`notebooks/ex4_llm_prompting.ipynb`](notebooks/ex4_llm_prompting.ipynb) | Information extraction via zero/few-shot prompting with open-weight LLMs |

Each notebook opens directly in Google Colab via the badge at the top — no local setup required.

## Repository structure

```
.
├── notebooks/    # hands-on exercise notebooks (open in Colab via badge)
├── data/         # datasets used by the exercises
└── slides/       # course slides
```

## Data

The `data/` folder contains only the (de-identified/derived) datasets needed to run the exercises. The original clinical notes underlying some exercises are not publicly shareable due to hospital data-sharing agreements.

## Contact

Vittorio Torri — vittorio.torri@polimi.it
Francesca Ieva - francesca.ieva@polimi.it