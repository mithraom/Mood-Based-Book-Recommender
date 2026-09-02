# Mood-Based Book Recommendation System

Independent research project building a mood-aware recommendation pipeline using NLP and sentiment analysis.

## Current Status
- Built a data collection pipeline over the UCSD Book Graph (Goodreads) academic dataset, currently scoped to the romance genre as a first pass
- Screened ~359,000 reviews, retained 20,000 (5.5%) via evidence-validated filters (minimum engagement/vote count, minimum review length)
- Thresholds validated against underlying data distributions rather than set arbitrarily
- Built a cleaning pipeline (spoiler-tag removal, whitespace/text normalization)
- Current phase: extracting mood/tone signal using sentence embeddings (sentence-transformers, all-MiniLM-L6-v2) paired with VADER for sentiment scoring

## Goal
Test whether mood-aware signals improve recommendation relevance over conventional preference-based baselines. Genre-general expansion planned once the single-genre pipeline is validated.

## Dataset
Sourced from UCSD Book Graph (Goodreads reviews), academic dataset. Not included in this repo due to licensing terms — contact for details.
