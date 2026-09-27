# ISCB-NLP-Course-2026

Material for the pre-conference course **"Clinical Text Mining under Real-World Constraints"**, held at ISCB-GMDS 2026.

Taught by Vittorio Torri and Francesca Ieva (MOX Lab, Politecnico di Milano)

The course introduces NLP methods for clinical text in settings where labelled data is scarce, moving from unsupervised exploration to weak supervision, interpretable models, and prompting with open-weight LLMs. Each part combines short theory with a hands-on notebook.

## Contents

| Notebook | Topic |
|---|---|
| [`notebooks/ex1_clustering_exercise.ipynb`](notebooks/ex1_clustering_exercise.ipynb) | Clustering short clinical texts with contextual embeddings, PCA and HDBSCAN, compared against an LDA baseline |
| [`notebooks/ex2_weak_supervision_classification.ipynb`](notebooks/ex2_weak_supervision_classification.ipynb) | Weak supervision: turning cluster-derived labels into training data for a Transformer classifier |
| [`notebooks/ex3_explainability.ipynb`](notebooks/ex3_explainability.ipynb) | Explainability: comparing SHAP (post-hoc) and Aug-Linear (an inherently interpretable n-gram + Transformer-embedding model) on the same classifier |
| [`notebooks/ex4_llm_prompting.ipynb`](notebooks/ex4_llm_prompting.ipynb) | Information extraction via zero-shot prompting with open-weight LLMs |

Each notebook opens directly in Google Colab via the badge at the top — no local setup required.

## Repository structure

```
.
├── notebooks/    # hands-on exercise notebooks (open in Colab via badge)
├── data/         # datasets used by the exercises
└── slides/       # course slides
```

## Data

`data/` contains the datasets used by the exercises:

- **Clinical notes** ([`NLP-FBK/dyspnea-clinical-notes`](https://huggingface.co/datasets/NLP-FBK/dyspnea-clinical-notes)): 2667 anonymized English emergency department notes. `dyspnea_notes_with_diagnoses.csv` already merges these notes with the diagnosis phrases extracted from them.
- **CRF Filling shared task data** ([`NLP-FBK/dyspnea-crf-development`](https://huggingface.co/datasets/NLP-FBK/dyspnea-crf-development) and [`NLP-FBK/dyspnea-valid-options`](https://huggingface.co/datasets/NLP-FBK/dyspnea-valid-options)): 80 English dev notes annotated with 134 structured fields each, used in EX4 (loaded directly from the Hub inside the notebook, not stored in this repo).
- **Cardiac/respiratory/neurological gold labels** (`dyspnea_real_labels.csv`): our own annotation of the notes above, used in EX2 and EX3 to check the weak labels against ground truth.

## Contact

Vittorio Torri — vittorio.torri@polimi.it
Francesca Ieva - francesca.ieva@polimi.it