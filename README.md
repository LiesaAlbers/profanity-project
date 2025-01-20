# The Profanity Project: A Comparitive Study of Popular Rap and Pop Lyrics

## Project Overview
This research project studies the contextual application of profanity across different music genres, specifically comparing rap and pop. Our goal is to provide a nuanced perspective on language in popular music, potentially challenging or reaffirming stereotypes regarding the use of explicit language within rap.

## Research Question
- How does the sentiment and usage of profanity differ between rap and pop music lyrics, and does this support or challenge stereotypes about profanity in rap music?

## Methodology
**Data Source:** Apple Music's playlists, specifically *Top 100 2024: Shazam's Radio Chart* for hip-hop and pop genres:
- Hip-Hop: https://music.apple.com/be/playlist/top-100-2024-shazam-radio-chart-hip-hop/pl.745180bfbd374d56aa07d84c9420e5dc
- Pop: https://music.apple.com/nl/playlist/top-100-2024-shazam-radio-chart-pop/pl.bdb7c5da0c8c44479af4299a62c67b78?l=en-GB
  
**Analysis:** Comparative study of profanity usage and sentiment in rap (hip-hop) and pop lyrics.

## Project Structure
- **1. Introduction & Background:**\
  Introduces the topic by discussing previous research done on the use of profanity in rap lyrics, presents the aim of the research, and provides further relevent background information.
- **2. Tutorial:**\
  Provides a guide through our process of collecting, managing, exploring, analysing, and visualising this study's data using Python.
- **3. Active Learning Exercises:**\
  Teaches viewers to manually calculate Cohen's Kappa using Python's `NumPy` package.

## Setup & Usage 
Run all cells in [code.ipynb](./code.ipynb).

Note that this notebook includes all code to import and install any packages/libraries/modules that are used. Regardless, here is an overview: 

**Packages:** `Selenium`, `webdriver-manager`, `pandas`, and `NumPy` \
**Libraries:** `requests`, `BeautifulSoup` \
**Modules:** `re`, `os`, `time`, `langdetect`, `pandas`, `Counter` , and `csv`

## Corpus
### Description 
The `full_profanity_lyrics_corpus.csv` is a collection of song lyric lines that contain profanity. The lyrics were web scraped from the online lyric database [AZLyrics](https://www.azlyrics.com/) and were preprocessed by converting them to lowercase, removing punctuation, and empty lines. The songs were selected based on Apple music's *Top 100 2024: Shazam's Radio Chart* for hip-hop and pop genres. The corpus serves as a resource for anyone interested in further analysing the use of profanity, patterns, etc., of popular music from these two genres. 

## File Formats

### PDF files (.pdf)
- The [annotation_guidelines.pdf](./annotation_guidelines.pdf) file contains the guidelines used for the sentiment annotation proces, including definitions and examples.

### Notebooks (.ipynb)
- The file [code.ipynb](./code.ipynb) contains the full project including all code used to realise the corpus.
- The file [exercises(solutions).ipynb](./exercises(solutions).ipynb) contains the solutions to the active learning exercises in the [code.ipynb](./code.ipynb) file.
  
### Text files (.txt)
- The directory `lyrics` contains a directory for each genre (`hiphop` and `pop`) consisting of text files for the lyrics of each individual song, named in the format:
  `artist_songtitle.txt`
- The [profanity_list](./profanity_list) file contains a curated collection of common swear words used to extract the profanities from the web scraped lyrics. The list is sourced from this [GitHub Gist](https://gist.github.com/ryanlewis/a37739d710ccdb4b406d) by Ryan Lewis.

### CSV files (.csv)
- The file [pilot_profanity_lyrics_corpus.csv](./pilot_profanity_lyrics_corpus.csv) contains a small section (20 rows from each genre) of the full corpus used for a pilot annotation.
- The file [full_profanity_lyrics_corpus.csv](./full_profanity_lyrics_corpus.csv) contains the full corpus (726 rows x 5 columns).

    **Rows:** each row contains data on a song lyric.

    **Columns**:

  | Header                 | Description |
  | ---------------------- | ----------- |
  | `Song_Title`           | The title of the song from which the lines containing profanity were extracted |
  | `Artist`               | The artist of the song from which the lines containing profanity were extracted |
  | `Genre`                | The genre the song belongs to |
  | `Profanity Lines`      | The line containing profanity and its context (lines before and after). The profanity is CAPITALISED for easy identification during the annotation process |
  | `Sentiment Annotation` | The sentiment category the annotated profanity belongs to |
 

## Terms of Use
This corpus is provided for non-commercial, research purposes only. All rights to the lyrics belong to the copyright owners, their agents, and representatives.
