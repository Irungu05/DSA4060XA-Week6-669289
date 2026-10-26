# DSA 4060XA - Week 6 Guided Evaluation Lab

## Student Information
* **Name:** ANGELA IRUNGU
* **Student ID:** 669289

## Lab Objective
To evaluate and compare Popularity Baseline, Content-Based Filtering, and Item-Based Collaborative Filtering models on explicit rating predictions (MAE/RMSE) and Top-N recommendation quality (Precision@3, Recall@3, NDCG@3, Coverage, Novelty, Diversity).

## Dataset Summary
* **Source Files:** `DSA4060_Week6_Movies.csv` (36 titles) & `DSA4060_Week6_Ratings.csv` (440 ratings across 40 users)
* **Train/Test Split:** Leave-Last-Out per user (400 train, 40 test interactions)

## Experimental Results
* **Best Model for Rating Prediction (MAE/RMSE):** Content-Based Filtering (MAE: 0.6031, RMSE: 0.6991)
* **Best Model for Top-3 Ranking (Precision/NDCG):** Content-Based Filtering (Precision@3: 0.2222, NDCG@3: 0.4881)
* **Coverage, Novelty, and Diversity Findings:**
  * *Popularity Baseline:* Lowest coverage (16.7%) and novelty (1.8092).
  * *Content-Based:* High precision and recall with strong catalog coverage (80.6%).
  * *Item-Based CF:* Maximum catalogue coverage (100%) and highest novelty (2.5779).

## Business Scenario Recommendation
* **Selected Model:** Item-Based Collaborative Filtering
* **Rationale:** Delivers 100% catalogue coverage and the highest novelty score (2.5779), ensuring non-blockbuster movies are exposed to users.

## Evaluation Limitations
1. **Leave-One-Out Evaluation Variance:** Holding out only 1 item per user creates high metric variance.
2. **Offline vs. Online Gap:** Offline metrics fail to capture real-time user discovery or satisfaction.
3. **Cold-Start Problem:** Cold users and items cannot be effectively evaluated without interaction history.
