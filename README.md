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

## Current phase
Prototype mood search (averaged review embeddings per book, cosine similarity to a mood query), compared against a TF-IDF keyword baseline. Investigating whether repeated results come from word matching.

## Dataset
UCSD Book Graph (Goodreads). Not included in this repo due to academic-use licensing.
