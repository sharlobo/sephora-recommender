# Sephora Recommender

Note: GitHub may not render the notebook preview due to Colab widget metadata. Please download and run the notebook locally or in Colab.

This repository contains the code for a personalized skincare and makeup recommendation system built using natural language processing and retrieval-based methods. The system matches user queries to Sephora products by leveraging semantic similarity over customer review text, followed by a light explanation layer.

## Project Overview

The goal of this project is to explore whether unstructured review language can be used to power meaningful product recommendations without relying heavily on manually curated attributes. The system embeds user queries and review documents into a shared semantic space, retrieves the most relevant reviews, aggregates them at the product level, and ranks products using a hybrid scoring function.

A constrained large language model (LLM) is used only to generate short, explanations for the final ranked products. The LLM does not influence retrieval or ranking decisions.

## Data Preprocessing

Data preprocessing was performed in earlier exploratory notebooks during development. These steps include cleaning raw product and review files, merging datasets by product_id, and constructing review-level text documents.

The final notebook (`sephora_new.ipynb`) assumes the use of these cleaned CSV outputs and focuses on embedding generation, retrieval, ranking, and evaluation.

## Dataset

This project uses the **Sephora Products and Skincare Reviews** dataset from Kaggle (March 2023 scrape).

Due to licensing restrictions, the dataset is **not included** in this repository.

Download the dataset here:  
https://www.kaggle.com/datasets/nadyinky/sephora-products-and-skincare-reviews

After downloading, place the cleaned CSV files in a local `data/` directory before running the notebook.

## Code Structure

- `sephora_new.ipynb`  
  Main notebook containing data preprocessing, embedding generation, FAISS retrieval, product ranking, evaluation, and example recommendations.

## Running the Code

1. Install dependencies:
   ```bash
   pip install pandas numpy sentence-transformers faiss-cpu gradio openai tqdm
   ```
2. Open the notebook
3. Run all cells top to bottom 
