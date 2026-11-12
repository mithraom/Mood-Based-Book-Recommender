# Mood-Based Book Recommendation System

Independent research project on mood-aware book recommendation using NLP on Goodreads reviews (UCSD Book Graph, romance genre).

## Results so far
| Test | Result |
|---|---|
| Ridge regression, star rating from VADER score | R2 = 0.072 (5-fold CV) |
| Ridge regression, star rating from sentence embeddings | R2 = 0.289 (5-fold CV) |

Embeddings explain about 4x more rating variance than VADER on 20,000 reviews.

## Data coverage
20,000 engagement-filtered reviews cover 13,429 books (median 1 review per book). Only 400 books have 5+ reviews, so the mood search prototype is limited to those.

## Mood search evaluation (400 books, precision@10)
Shelf tags (a book counts if at least 20 readers shelved it under the tag) were used as independent labels, with 3 label-style queries per mood fixed before running.

| Mood | Books with tag | Random | Embeddings | Keyword (TF-IDF) |
|---|---|---|---|---|
| dark-romance | 56 | 0.14 | 0.43 | 0.67 |
| dark | 112 | 0.28 | 0.80 | 0.90 |
| funny | 98 | 0.24 | 0.50 | 0.73 |
| angst | 132 | 0.33 | 0.53 | 0.53 |
| enemies-to-lovers | 38 | 0.10 | 0.27 | 0.30 |

Both methods beat random on every mood, but the keyword baseline matched or beat embeddings on these label-style queries (the query words appear in the reviews themselves). Caveats: 400 books, 3 queries per mood, noisy reader-made labels.

## Current phase
Testing label-free queries (paraphrased moods that avoid the tag words), review-level retrieval and hybrid keyword+embedding ranking, then scaling to a larger catalog.

## Dataset
UCSD Book Graph (Goodreads). Not included in this repo due to academic-use licensing.
