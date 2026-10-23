# Graph Report - music-engagement-mlp  (2026-10-23)

## Corpus Check
- Large corpus: 500 files · ~680,437 words. Semantic extraction will be expensive (many Claude tokens). Consider running on a subfolder.

## Summary
- 22 nodes · 43 edges · 5 communities
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Music Engagement MLP Notebook
- Neural Network-Based Prediction of
- Composite Engagement Score (0.8*Views
- MLP Test Results (MSE
- Preprocessing: mean/mode imputation, Min-Max

## God Nodes (most connected - your core abstractions)
1. `Neural Network-Based Prediction of Online Music Content Engagement (MLP paper)` - 18 edges
2. `Music Engagement MLP Notebook (FP_Bacsain_BSCS2A.ipynb)` - 8 edges
3. `MLP Engagement Regressor (5x1000 ReLU, Adam lr=0.001, MSE, 50 epochs)` - 7 edges
4. `Preprocessing: mean/mode imputation, Min-Max scaling, Album_type factorization` - 7 edges
5. `MLP Test Results (MSE 0.000570, MAE 0.0117, R2 0.584)` - 5 edges
6. `Composite Engagement Score (0.8*Views + 0.2*Stream)` - 4 edges
7. `Spotify and YouTube Dataset (Kaggle, 20,718 tracks)` - 4 edges
8. `predict_song_score()` - 3 edges
9. `my_model.h5 (saved Keras MLP; paper calls it model.h5)` - 3 edges
10. `Collinearity Analysis (|r| > 0.8 dropped; Likes removed)` - 3 edges

## Surprising Connections (you probably didn't know these)
- `Music Engagement MLP Notebook (FP_Bacsain_BSCS2A.ipynb)` --references--> `Neural Network-Based Prediction of Online Music Content Engagement (MLP paper)`  [EXTRACTED]
  FP_Bacsain_BSCS2A.ipynb.md → FP_Bacsain_BSCS2A.pdf
- `Music Engagement MLP Notebook (FP_Bacsain_BSCS2A.ipynb)` --references--> `Collinearity Analysis (|r| > 0.8 dropped; Likes removed)`  [EXTRACTED]
  FP_Bacsain_BSCS2A.ipynb.md → FP_Bacsain_BSCS2A.pdf
- `Music Engagement MLP Notebook (FP_Bacsain_BSCS2A.ipynb)` --references--> `Preprocessing: mean/mode imputation, Min-Max scaling, Album_type factorization`  [EXTRACTED]
  FP_Bacsain_BSCS2A.ipynb.md → FP_Bacsain_BSCS2A.pdf
- `Music Engagement MLP Notebook (FP_Bacsain_BSCS2A.ipynb)` --references--> `MLP Test Results (MSE 0.000570, MAE 0.0117, R2 0.584)`  [EXTRACTED]
  FP_Bacsain_BSCS2A.ipynb.md → FP_Bacsain_BSCS2A.pdf
- `Music Engagement MLP Notebook (FP_Bacsain_BSCS2A.ipynb)` --references--> `Spotify and YouTube Dataset (Kaggle, 20,718 tracks)`  [EXTRACTED]
  FP_Bacsain_BSCS2A.ipynb.md → FP_Bacsain_BSCS2A.pdf

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Music engagement prediction pipeline (dataset -> preprocessing -> collinearity -> composite score -> MLP -> CLI)** — music_engagement_mlp_fp_bacsain_bscs2a_spotify_youtube_dataset, music_engagement_mlp_fp_bacsain_bscs2a_preprocessing, music_engagement_mlp_fp_bacsain_bscs2a_collinearity_analysis, music_engagement_mlp_fp_bacsain_bscs2a_composite_engagement_score, music_engagement_mlp_fp_bacsain_bscs2a_mlp_engagement_model, music_engagement_mlp_fp_bacsain_bscs2a_cli_prediction_interface [EXTRACTED 1.00]

## Communities (5 total, 0 thin omitted)

### Community 0 - "Music Engagement MLP Notebook"
Cohesion: 0.43
Nodes (7): Interactive CLI Engagement Prediction Interface, Music Engagement MLP Notebook (FP_Bacsain_BSCS2A.ipynb), my_model.h5 (saved Keras MLP; paper calls it model.h5), predict_song_score(), MLP Engagement Regressor (5x1000 ReLU, Adam lr=0.001, MSE, 50 epochs), Predicting the Popularity of Spotify Songs Using a Neural Network (Rusconi, 2024), Spotify and YouTube Dataset (Kaggle, 20,718 tracks)

### Community 1 - "Neural Network-Based Prediction of"
Cohesion: 0.40
Nodes (6): Neural Network-Based Prediction of Online Music Content Engagement (MLP paper), Hybrid Music Recommendation with Graph Neural Networks (Bevec et al., 2024), Collinearity Analysis (|r| > 0.8 dropped; Likes removed), Predicting Song Popularity via ML and Sentiment Analysis (Rompolas et al., 2024), Veritas AI: ML Models for Song Popularity Prediction on Spotify (Sardana, 2024; listed twice as [5] and [17]), Beyond Beats: A Recipe to Song Popularity? (Sebastian et al., 2024)

### Community 2 - "Composite Engagement Score (0.8*Views"
Cohesion: 0.67
Nodes (3): Composite Engagement Score (0.8*Views + 0.2*Stream), calculate_score(), How to Optimize Videos through YouTube Analytics Data (Patel, 2025)

### Community 3 - "MLP Test Results (MSE"
Cohesion: 0.67
Nodes (3): SpotHitPY: ML-Based Song Hit Prediction Using Spotify (Dimolitsas et al., 2023), MLP Test Results (MSE 0.000570, MAE 0.0117, R2 0.584), ML Approaches for Predicting Song Popularity: A Case Study (Velmuruga, 2023)

### Community 4 - "Preprocessing: mean/mode imputation, Min-Max"
Cohesion: 0.67
Nodes (3): Effect of Feature Selection on Music Popularity Classification (Khan et al., 2022), Preprocessing: mean/mode imputation, Min-Max scaling, Album_type factorization, Predicting Music Popularity Using Spotify and YouTube Features (Yee & Raheem, 2022)

## Knowledge Gaps
- **3 isolated node(s):** `Hybrid Music Recommendation with Graph Neural Networks (Bevec et al., 2024)`, `Predicting Song Popularity via ML and Sentiment Analysis (Rompolas et al., 2024)`, `Veritas AI: ML Models for Song Popularity Prediction on Spotify (Sardana, 2024; listed twice as [5] and [17])`
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 3 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Neural Network-Based Prediction of Online Music Content Engagement (MLP paper)` connect `Neural Network-Based Prediction of` to `Music Engagement MLP Notebook`, `Composite Engagement Score (0.8*Views`, `MLP Test Results (MSE`, `Preprocessing: mean/mode imputation, Min-Max`?**
  _High betweenness centrality (0.653) - this node is a cross-community bridge._
- **Why does `Music Engagement MLP Notebook (FP_Bacsain_BSCS2A.ipynb)` connect `Music Engagement MLP Notebook` to `Neural Network-Based Prediction of`, `Composite Engagement Score (0.8*Views`, `MLP Test Results (MSE`, `Preprocessing: mean/mode imputation, Min-Max`?**
  _High betweenness centrality (0.161) - this node is a cross-community bridge._
- **Why does `MLP Engagement Regressor (5x1000 ReLU, Adam lr=0.001, MSE, 50 epochs)` connect `Music Engagement MLP Notebook` to `Neural Network-Based Prediction of`, `Composite Engagement Score (0.8*Views`, `MLP Test Results (MSE`?**
  _High betweenness centrality (0.067) - this node is a cross-community bridge._
- **What connects `Hybrid Music Recommendation with Graph Neural Networks (Bevec et al., 2024)`, `Predicting Song Popularity via ML and Sentiment Analysis (Rompolas et al., 2024)`, `Veritas AI: ML Models for Song Popularity Prediction on Spotify (Sardana, 2024; listed twice as [5] and [17])` to the rest of the system?**
  _3 weakly-connected nodes found - possible documentation gaps or missing edges._