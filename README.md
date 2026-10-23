# music-engagement-mlp: Music Engagement Prediction (Spotify and YouTube)

Final project for CSAC 224 Machine Learning (BSCS-2A), Camarines Sur Polytechnic Colleges. A Multilayer Perceptron (MLP) built in Keras predicts a song's engagement score, which combines its YouTube views and Spotify streams. The inputs are the song's Spotify audio features, album type, duration and YouTube comment count.

The full paper is [`FP_Bacsain_BSCS2A.pdf`](FP_Bacsain_BSCS2A.pdf). All code and outputs are in [`FP_Bacsain_BSCS2A.ipynb`](FP_Bacsain_BSCS2A.ipynb).

## Dataset

[Spotify and YouTube dataset](https://www.kaggle.com/datasets/salvatorerastelli/spotify-and-youtube/data) from Kaggle, included as `Spotify_Youtube.csv`. It has 20,718 songs with Spotify audio features and stream counts, plus the matching YouTube video's views, likes and comments. Some rows are missing these values.

## Methodology

1. Fill missing values with the column mean (numbers) or the most frequent value (text), then min-max scale the numeric columns to 0 to 1.
2. Drop 11 columns that are IDs, URLs, text or the `Licensed` and `official_video` flags, and encode `Album_type` with `pd.factorize`.
3. Drop features with a correlation above 0.8. This removed `Likes`.
4. Build the target `Score = 0.8 × Views + 0.2 × Stream`, then remove `Views` and `Stream` from the inputs so the model cannot read the answer off them.
5. Split 80/20 at random (`random_state=42`): 16,574 training rows and 4,144 test rows, 13 input features.
6. Train a Keras `Sequential` MLP: 5 hidden Dense layers of 1000 ReLU units and 1 linear output (4,019,001 parameters). Adam with learning rate 0.001, mean squared error loss, 50 epochs.
7. Evaluate on the test rows with MSE, MAE, R² and explained variance. The trained model is saved as `my_model.h5`.

The test rows were also passed to Keras as `validation_data` during training, so the validation curves and the test metrics come from the same 4,144 rows.

## Results

On the 4,144 test songs the model reaches an R² of 0.584316 (notebook evaluation cell, report Table 1 on page 6).

| Metric | Value |
|---|---|
| MSE | 0.000570 |
| MAE | 0.011665 |
| R² | 0.584316 |
| Explained variance | 0.595103 |

The notebook ends with a command-line lookup: type a song name and it prints the actual and predicted score. Example outputs (report Table 4, page 9):

| Song | Actual score | Predicted score |
|---|---|---|
| Take on Me | 0.2354 | 0.1552 |
| In the End | 0.2326 | 0.1408 |
| Believer | 0.3746 | 0.1819 |
| Bad Guy | 0.2514 | 0.2176 |
| Shape of You | 0.7836 | 0.3510 |

Predictions tend to underestimate songs with high engagement (report section 4.5.1, page 9). The lookup searches the whole dataset, so some of these songs may have been in the training rows.

## How to Run

The notebook was run on Python 3.12.0. There is no requirements file; these are the packages it imports, plus Jupyter to open it:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn tensorflow jupyter
jupyter notebook FP_Bacsain_BSCS2A.ipynb
```

- **Train from scratch:** run the cells top to bottom. This trains for 50 epochs and replaces `my_model.h5`.
- **Use the included model:** run the code cell under the "Engagement Score Prediction" heading, then the command-line cell below it. Type a song name, or `exit` to quit.
