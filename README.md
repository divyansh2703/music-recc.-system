# Song Recommendation from Lyrics with a Streamlit Interface

A content based recommendation prototype that compares song lyrics and displays suggested songs through Streamlit. The notebook prepares text features and a similarity matrix; the application uses the selected song to return five recommendations with album artwork retrieved through Spotify.

## The question

Which songs have similar lyric content to a selected song, and how can the results be presented interactively?

## Tools and methods

Python, pandas, NLTK, scikit learn, Streamlit, Spotipy, Recommendation systems.

## Work in this repository

1. Preprocessed song lyrics with tokenisation and stemming.
2. Built TF IDF features and cosine similarity scores.
3. Created a song selector and five recommendation display in Streamlit.
4. Added album artwork lookup through the Spotify client library.

## Evidence and scope

| Measure | Recorded value |
| --- | --- |
| Recommendations requested by the interface | 5 |

## Repository guide

| File or folder | Purpose |
| --- | --- |
| [Model Training.ipynb](https://github.com/divyansh2703/music-recc.-system/blob/main/Model%20Training.ipynb) | Text preprocessing and similarity generation |
| [app.py](https://github.com/divyansh2703/music-recc.-system/blob/main/app.py) | Streamlit interface |
| [df.pkl](https://github.com/divyansh2703/music-recc.-system/blob/main/df.pkl) | Committed song table artifact |

## Getting started

Obtain the lyric source identified as `spotify_millsongdata.csv` in the notebook and replace its absolute input path. Prepare dependencies for pandas, NLTK, scikit learn, Streamlit and Spotipy. Configure your own Spotify application credentials locally.

Run the notebook to generate `df.pkl` and `similer.pkl`; the latter filename matches the application spelling and is not present in the reviewed tree. Do not substitute the empty `similarity` file. Once the required trusted artifacts exist:

```bash
streamlit run app.py
```

## Current limitations

1. The committed application cannot complete its recommendation workflow without the missing similarity artifact.
2. The method compares lyric content. It does not learn an individual listening history or demonstrate collaborative filtering.
3. No recommendation relevance benchmark or user engagement lift is measured.
4. The existing application embeds credential configuration in code; replace that configuration with private local settings before reuse.

## Next steps

1. Publish a reproducible artifact generation workflow and move credentials to local configuration.
2. Evaluate recommendation relevance on an explicit benchmark.

## Authors and reuse

Divyansh Doshi.

Documentation reviewed against the public repository on 7 September 2026. Counts are taken from the named saved artifacts or directly inspected CSVs; this review did not rerun model training or validate a complete deployment. No source code licence was found in the reviewed project tree. Data and third party material may have separate terms.
