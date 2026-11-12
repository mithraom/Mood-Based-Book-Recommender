# Mood search prototype: observations (not yet validated)

- Dark/toxic query returned books readers describe in those terms (After, Beautiful Disaster, Fifty Shades).
- Slow burn arc and light/funny queries looked weak (low similarity scores, 0.29-0.45).
- Repeated books across queries: some expected (two dark queries), some possibly word matching on 'sweet' (title and review text). To be tested.
- Averaged review embeddings likely capture overall mood, not plot arc.
- TF-IDF keyword baseline comparison pending.
