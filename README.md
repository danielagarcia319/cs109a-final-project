# CS109A Final Project

Ilona Demler, Daniela Garcia, Kayla Manning, Saul Soto

## Project Description

What makes a playlist popular?

Can we quantify what makes a playlist popular? Is there something inherent about the qualities of the songs or the behavior of the listeners? This project aims to predict the popularity of playlists by using public data and the Spotify API in order to determine what might make someone's playlist "popular". In this case, popularity would be measured by the followers of the playlist, with predictors being a variety of playlist and song characteristics including the length of the playlist, duration of the songs, the "energy level"/"dancability" of each song, the popularity of artists, the listen time, etc. Will you be able to determine the next hit playlist?

Motivated students may find it appropriate to use the Spotify API to gather more information.

## Contents

- Project Guidelines
- Data Descriptions (click for [sliced](https://drive.google.com/drive/folders/1v9VchFigNE4bWx8jpaLzMrUlzH9zCQu9?usp=sharing) and [joined](https://drive.google.com/file/d/11kJ_E_K5ekkaN5SuYU5sjKqgR8uSMuxA/view?usp=sharing) raw data) 
- Data Processing Jupyter Notebooks (`json_to_csv.ipynb` and `join_data.ipynb`)
- Milestone 2 Jupyter Notebook and PDF Report (`Milestone_2.ipynb` and `CS109a_Final_Project_Milestone_2.pdf`)
- Milestone 3 Jupyter Notebook and PDF Report (`Milestone_3.ipynb` and `CS109a_Final_Project_Milestone_3.pdf`)

## Data

### Data Description

This project will utilize the [Million Playlist Dataset](https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge/dataset_files), which consists of a sample of 1 million public playlists from over 4 billion public playlists on Spotify. Consisting of over 2 million unique tracks from nearly 300,000 artists, the dataset contains public playlists created by Spotify users between January 2010 and October 2017. 

The dataset, sourced from [AIcrowd](https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge), contains the following columns:

- `pid` - integer - playlist id - the MPD ID of this playlist. This is an integer between 0 and 999,999.
- `name` - string - the name of the playlist
- `description` - optional string - if present, the description given to the playlist. Note that user-provided playlist descriptions are a relatively new feature of Spotify, so most playlists do not have descriptions.
- `modified_at` - seconds - timestamp (in seconds since the epoch) when this playlist was last updated. Times are rounded to midnight GMT of the date when the playlist was last updated.
- `num_artists` - the total number of unique artists for the tracks in the playlist.
- `num_albums` - the number of unique albums for the tracks in the playlist
- `num_tracks` - the number of tracks in the playlist
- `num_followers` - the number of followers this playlist had at the time the MPD was created. (Note that the follower count does not include the playlist creator)
- `num_edits` - the number of separate editing sessions. Tracks added in a two-hour window are considered to be added in a single editing session.
- `duration_ms` - the total duration of all the tracks in the playlist (in milliseconds)
- `collaborative` - boolean - if true, the playlist is a collaborative playlist. Multiple users may contribute tracks to a collaborative playlist.
- `tracks` - an array of information about each track in the playlist. Each element in the array is a dictionary with the following fields:
    - `track_name` - the name of the track
    - `track_uri` - the Spotify URI of the track
    - `album_name` - the name of the track’s album
    - `album_uri` - the Spotify URI of the album
    - `artist_name` - the name of the track’s primary artist
    - `artist_uri` - the Spotify URI of the track’s primary artist
    - `duration_ms` - the duration of the track in milliseconds
    - `pos` - the position of the track in the playlist (zero-based)

Playlists are sampled with randomization and anonymized to protect user privacy. The playlists are manually filtered to maximize quality and to remove offensive content, and some playlists have fictitious tracks added as noise. Therefore, the playlists in this dataset are not representative of the overall population of playlists on Spotify. 

- Data [Site](https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge)
- Data [Download](https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge/dataset_files)

## Overleaf

- Milestone 2 [Overleaf Template](https://www.overleaf.com/3316578227zhhjypgtmjqq)
- Milestone 3 [Overleaf Template](https://www.overleaf.com/5297315935qprcpnwcryck)
