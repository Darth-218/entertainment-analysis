# Entertainment & Culture Analysis

## Questions to Answer

- What factors most strongly predict box office success — budget, cast popularity, or IMDb ratings?
- Do movies released in summer perform better financially than those in winter?
- Is there a significant difference between critics’ and audience ratings across genres?

## Data Sources

- [TMDB](https://developer.themoviedb.org/docs/getting-started).
- [OMDb](https://www.omdbapi.com/)
- ~[IMDb](https://datasets.imdbws.com/)~.

## Data Features

#### Movie identifiers

- `movie_id` – TMDB unique identifier for the movie; used for joining TMDB API data.
- `title` – Movie title; useful for reference and scraping additional data.
- `imdb_id` – IMDb unique identifier; allows access to IMDb ratings, votes, and OMDb enrichment.
- `original_language` – Original language of the film; can control for international differences in revenue and ratings.

#### Financials

- `budget` – Production budget in USD; predictor of box office success.
- `revenue_worldwide` – Total global revenue; target variable for Q1 and Q2 analyses.
- `domestic_box_office` – US domestic revenue; helps measure seasonality effects and summer/winter performance.

#### Release information

- `release_date` – Date of release; used to derive season, day of week, and holiday indicators.
- `franchise` – Boolean indicating whether the movie is part of a franchise; controls for franchise effects on revenue.

#### Cast

- `cast_popularity_mean` – Average popularity of top-billed cast members; proxy for star power.
- `cast_popularity_max` – Maximum popularity among top-billed actors; captures influence of a single star.
- `director_popularity` – Popularity of the director; accounts for director-driven audience draw.

#### Ratings

- `imdb_rating` – IMDb audience rating (out of 10); measures audience reception.
- `imdb_votes` – Number of votes on IMDb; indicates reliability of the audience rating.
- `rotten_tomatoes_score` – Rotten Tomatoes critic score (percentage); used to compare critics vs audience perceptions.
- `metacritic_score` – Metacritic critic score (out of 100); alternative measure of critical reception.
- `mpaa_rating` – MPAA age rating (e.g., PG-13, R); controls for audience restrictions affecting revenue.

#### Film characteristics

- `runtime` – Movie length in minutes; can affect audience engagement and revenue potential.
- `genres` – List of genres; used for genre-level analyses, critic vs audience comparisons, and feature encoding.
- `awards_text` – Text listing awards and nominations; can be parsed for prestige or critical acclaim proxies.

## Data Cleaning

## Analysis Method

