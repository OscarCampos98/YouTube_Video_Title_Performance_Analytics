# YouTube Title Performance Analytics

Exploratory analysis of how **title wording** relates to **video performance signals** using
Bag-of-Words features and lightweight models (Binary/Multinomial Naive Bayes, Linear Regression).

## Repo Map
- `BagOfWords_YoutubeData_.ipynb` — text prep + EDA + baseline NB
- `BagOfWords_YoutubeData_MultinomialNB.ipynb` — multinomial NB experiment
- `RegressionModel_in_YoutubeData.ipynb` — regression on engagement metrics
- `SENG550_Group13_Final Project Report.pdf` — full write-up

## Data
- **US YouTube dataset** (daily trending snapshots; columns include title, tags, views, likes, dislikes, etc.).
- Typical cleaning: lowercase, punctuation removal, stopword filtering, tokenization; `CountVectorizer`/Bag-of-Words.

## Questions
1) Do specific **title tokens/phrases** correlate with higher engagement?
2) Can simple models predict **engagement** from title text alone?

## Methods
- **Features:** Bag-of-Words; (optionally) n-grams, min_df, and stopword lists.
- **Models:** Binary NB, Multinomial NB (classification); Linear Regression (regression).
- **Evaluation:** (fill in once copied from the PDF)
  - Classification: accuracy / F1 on hold-out
  - Regression: RMSE / R² on hold-out

## Results (from report)
- Key tokens associated with higher/lower performance (top 10 with log-odds or coefficients).
- Headline metrics for each model (copy from PDF tables).
- Short takeaway on **title wording** vs. performance.

## Reproduce
> Colab-friendly; Python 3.x

1) Open notebook(s) in Colab.
2) Run the setup cell to install dependencies.
3) Execute cells top-to-bottom.

## Notes & Limits
- Text-only features; ignores thumbnails, channel effects, and recency.
- Dataset skew (trending set) may inflate apparent predictability.
- Future work: TF-IDF, regularized linear models, and neural baselines (e.g., DistilBERT).

## Authors
Group project (SENG 550): Isaiah Lemieux, Gian Adug, Oscar Campos, Tien Dat Johny Do.

