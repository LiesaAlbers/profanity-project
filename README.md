# The Profanity Project: A Comparitive Study of Popular Rap and Pop Lyrics

## Project Overview
This research project studies the contextual application of profanity across different music genres, specifically comparing rap and pop. Our goal is to provide a nuanced perspective on language in popular music, potentially challenging or reaffirming stereotypes regarding the use of explicit language within rap.

## Research Question
- How does the sentiment and usage of profanity differ between rap and pop music lyrics, and does this support or challenge stereotypes about profanity in rap music?

## Methodology
**Data Source:** Apple Music's playlists, specifically "Top 100 2024: Shazam's Radio Chart" for hip-hop and pop genres:
- Hip-Hop: https://music.apple.com/be/playlist/top-100-2024-shazam-radio-chart-hip-hop/pl.745180bfbd374d56aa07d84c9420e5dc
- Pop: https://music.apple.com/nl/playlist/top-100-2024-shazam-radio-chart-pop/pl.bdb7c5da0c8c44479af4299a62c67b78?l=en-GB
**Analysis:** Comparative study of profanity usage and sentiment in rap (hip-hop) and pop lyrics.

## Project Structure
**1. Introduction & Background:** Introduces the topic by discussing previous research done on the use of profanity in rap lyrics, presents the aim of the research, and provides further relevent background.
**2. Tutorial:** Provides a guide through our process of collecting, managing, exploring, analysing, and visualising this study's data using Python.
**Active Learning Exercises:** Teaches viewers to manually calculate Cohen's Kappa using Python's `NumPy` package.

## Resulting Corpora
### Corpus Description
The Architects Lyrics Corpus is a collection of song lyrics from Architects' discography, 
spanning 10 full albums. It serves as a resource for anyone interested in analysing lyrical themes,
linguistic patterns, stylistic evolution over time, etc., of Architects' lyrics. 

### Text Selection Criteria
The corpus includes lyrics from all officially released studio albums by Architects as available on major streaming platforms, excluding:
- The album *For Those That Wish To Exist At Abbey Road* (2022),
  since this is a different rendition of the same songs on the original *For Those That Wish To Exist* (2021) album,
  which is already included in the corpus.
- Instrumental songs, bonus tracks, and deluxe edition songs.

### Data Collection process
Lyrics were collected per album from three different online lyric databases:
- [Dark Lyrics](http://www.darklyrics.com/a/architects.html ) for the first 8 albums.
- [Metal Kingdom](https://www.metalkingdom.net/album/architects-for-those-that-wish-to-exist-144830)
  for the second-to-latest album included in the corpus (*For Those That Wish To Exist*, 2021)
- [Rockalyrics](https://www.rockalyrics.com/m/565-6854/architects/the-classic-symptoms-of-a-broken-spirit-lyrics)
  for the latest album included in the corpus (*the classic symptoms of a broken spirit*, 2022)

### Cleaning and Preprocessing
Since the lyrics were retreived per album, the lyrics were processed so that each individual song lyric
is stored in its own separate text file. Additionally, extra lines in each file were replaced with spaces.


## Setup & Usage 
Run all cells in [code.ipynb](./code.ipynb)
Note that this notebook includes code to import and install any packages/libraries/modules that are used. Here is an overview of those packages/libraries/modules: 

**Packages:** `Selenium`, `webdriver-manager`, `pandas`, and `NumPy`
**Libraries:** `requests`, `BeautifulSoup`
**Modules:** `re`, `os`, `time`, `langdetect`, `pandas`, `Counter` , and `csv`


## File Formats
!!!!! profanity_list,
annotation_guidelines.pdf

### Notebook (.ipynb)
- The file `code.ipynb` contains the full project including all code used to realise the two corpora.
- The file `exercises(solutions).ipynb` contains the solutions to the active learning exercises in the `code.ipynb` file.
  
### Text files (.txt)
- The directory `lyrics` contains a directory for each genre (`hiphop` and `pop`) consisting of text files for the lyrics of each individual song, named in the format:
  `artist_songtitle.txt`

### CSV file (.csv)
- The file `pilot_profanity_lyrics_corpus.csv` contains a small portion (20 rows from each genre) of the full corpus used for a pilot annotation.
- The file `full_profanity_lyrics_corpus.csv` contains the full corpus.

    **Rows:** each row contains data on a song lyric.

    **Columns** (variables):

  | Header                 | Description |
  | ---------------------- | ----------- |
  | `Song_Title`           | The title of the song from which the lines containing profanity were extracted |
  | `Artist`               | The artist of the song from which the lines containing profanity were extracted |
  | `Genre`                | The genre the song belongs to |
  | `Profanity Lines`      | The lines containing profanity and context (before and after lines) the Profanity is CAPITALISED for easy identification during the annotation process |
  | `Sentiment Annotation` | The sentiment category the annotated profanity belongs to |
 

## Additional Information / Terms of Use
This corpus is provided for non-commercial, research purposes only. 
All rights to the lyrics belong to Architects and their publishers.

No explicit terms and conditions were stated on [poestories.com](https://poestories.com/poetry.php), nor was there a robots.txt file. 
This corpus is provided for non-commercial, research purposes only. All Rights Reserved.
MUSIC IS IN THE PUBLIC DOMAIN ???

