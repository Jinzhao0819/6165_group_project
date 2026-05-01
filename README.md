# DSBA 6165 Group Project

This repository contains the end-to-end workflow for a DSBA 6165 group project on Amazon Sports reviews, including data retrieval, preprocessing, modeling, clustering, and error analysis.

## Project Scope

The project is organized around three research questions:

- `RQ1`: How does a classical baseline (`TF-IDF + Logistic Regression`) compare with `DistilBERT` for sentiment classification?
- `RQ2`: How can product reviews be grouped using clustering (including BERT-based embeddings) to generate marketing insights?
- `RQ3`: What linguistic patterns are associated with DistilBERT misclassification of neutral (3-star) reviews?

## Repository Structure

- `01_Data_Retrieval_and_Merging.ipynb`: builds merged review datasets and creates balanced/random samples.
- `02_EDA_and_Text_Preprocessing-random.ipynb`: EDA and preprocessing pipeline for random dataset.
- `03_EDA_and_Text_Preprocessing-balanced.ipynb`: EDA and preprocessing pipeline for balanced dataset.
- `RQ1_Comparison_TFIDF_LR_vs_DistilBERT.ipynb`: RQ1 modeling and comparison.
- `04_RQ2_Product_Clustering_and_Modeling.ipynb`: RQ2 clustering workflow and baseline summary outputs.
- `RQ3_DistilBERT_Error_Analysis_ChiSquare.ipynb`: RQ3 misclassification and linguistic pattern analysis.
- `Dataset/`: cleaned datasets, sampled subsets, and clustering outputs used by notebooks.

## Key Data Files

Main files in `Dataset/` include:

- `sports_balanced_50k.csv`
- `sports_random_50k_final.csv`
- `sampled_5k_pos_5k_neg.csv`
- `cleaned_amazon_balanced_reviews.csv`
- `cleaned_amazon_random_reviews.csv`
- `bert_clustering_k3_results.csv`
- `bert_clustering_marketing_insights.csv`
- `clustering_baseline_summary_*.csv`

## Recommended Execution Order

1. Run `01_Data_Retrieval_and_Merging.ipynb`
2. Run preprocessing notebook(s):
   - `02_EDA_and_Text_Preprocessing-random.ipynb`
   - `03_EDA_and_Text_Preprocessing-balanced.ipynb`
3. Run task-specific analysis:
   - `RQ1_Comparison_TFIDF_LR_vs_DistilBERT.ipynb`
   - `04_RQ2_Product_Clustering_and_Modeling.ipynb`
   - `RQ3_DistilBERT_Error_Analysis_ChiSquare.ipynb`

## Environment Notes

- Python 3.10+ is recommended.
- Several notebooks are compatible with both local Jupyter and Google Colab.
- Some notebook cells reference Google Drive paths; update paths for local execution if needed.

## Reproducibility Tips

- Keep dataset filenames unchanged unless you also update the notebook paths.
- Run notebooks in order to ensure intermediate files are generated before downstream analysis.
- If results differ slightly, verify random seeds and train/validation/test split settings in each notebook.
