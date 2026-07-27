# Netflix Content Analysis 

Exploratory data analysis of Netflix's movie and TV show catalog, done with `pandas` and `numpy`.

I picked this dataset because streaming catalogs are a nice mix of dirty real-world data (missing countries, inconsistent duration formats, messy genre lists) and genuinely interesting questions — like which year Netflix added the most content, or who its most frequent collaborating directors are.

## What this notebook actually answers

- How much of the catalog is movies vs. TV shows?
- Which countries produce the most content on Netflix?
- How has the amount of content added per year changed over time?
- What are the most common genres?
- How is content distributed across age ratings (TV-MA, PG-13, etc.)?
- What's the average movie length, and which are the longest/shortest?
- Which directors have the most titles on the platform?

## A few things I ran into

- The `country` and `date_added` columns had a fair number of missing values — handled with a mix of filling and dropping, depending on the column.
- Genres are stored as comma-separated strings in a single column, so they needed to be split and exploded before counting individual genres properly (counting the raw combinations first gave misleading results).
- `duration` uses two completely different units depending on content type — minutes for movies, seasons for TV shows — so movie-length stats needed to be isolated and parsed as numbers first.

## Tools

Python, pandas, numpy, matplotlib

## Dataset

[Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows) (Kaggle)

## Running it

```bash
pip install pandas numpy matplotlib
jupyter notebook netflix-analysis.ipynb
```

Make sure `netflix_titles.csv` is in the same folder as the notebook.
