---

# YTS Movie Dataset

This repository contains a dataset collected from the movie piracy site [YTS](https://yts.mx) via a custom-built [web crawler](https://github.com/Sevinda-Herath/yts_data_crawler). It includes data on 12,149 unique movie entries, aggregated from two separate crawler runs over a span of four days.

## File Format
- **Format:** CSV (Comma-Separated Values)
- **Encoding:** UTF-8
  
## Web Crawler
**Repo** - [YTS_Data_Crawler](https://github.com/Sevinda-Herath/yts_data_crawler)

## Repo File Structure

### Original Datasets
The data was collected in two separate runs:
1. **Original_Dataset_1.csv** – 12,047 movie entries
2. **Original_Dataset_2.csv** – 12,041 movie entries

After deduplication, the final dataset contains 12,149 unique entries.

### Processed Data
The two original datasets were merged, and duplicates were removed, resulting in the following processed dataset:
- **Combined_Dataset.csv** – 12,149 unique movie entries

This combined dataset is ready for analysis, machine learning, or any other data-driven movie-related projects.

### Additional Files
1. **Jupyter.ipynb** – A Jupyter notebook demonstrating the process of creating the combined dataset using Pandas.
2. **PowerBI.pbix** – A more processed version of the combined dataset created in Microsoft Fabric. (Note: I couldn't figure out how to export this to CSV in MS OneLake. If anyone knows how, please reach out!)

---

## Dataset Description

### Columns in Original Datasets
- **key:** Unique identifier for each movie entry
- **Genres:** Genre(s) of the movie
- **IMDb_Rating:** IMDb rating of the movie
- **IMDb_Votes:** Number of votes on IMDb
- **Movie_Director:** Director(s) of the movie
- **Movie_Title:** Title of the movie
- **Released_Year:** Year the movie was released
- **Runtime:** Duration in minutes
- **Seeds:** Number of available seeds for the movie
- **URL:** Link to the movie page on YTS
- **Uploaded_Time:** Date and time the movie was uploaded
- **Uploader:** Username of the uploader
- **YTS_Likes:** Number of likes the movie received on YTS

### Columns in Processed Dataset
- **Title:** Movie title
- **Director:** Director(s) of the movie
- **Year:** Release year
- **Duration:** Duration (e.g., "1hr 36min")
- **IMDb Rating:** IMDb rating
- **Votes:** Number of IMDb votes
- **Metascore:** Metascore rating from Metacritic
- **Uploader:** Username of the uploader
- **Upload Date:** Date the movie was uploaded
- **URL:** Link to the movie page on YTS
- **Genres:** List of associated genres

#### Genre Indicators
Binary columns indicate the presence (1) or absence (0) of specific genres:
- Action, Adventure, Animation, Biography, Comedy, Crime, Documentary, Drama, Family, Fantasy, Film-Noir, Game-Show, History, Horror, Music, Musical, Mystery, News, Reality-TV, Romance, Sci-Fi, Sport, Talk-Show, Thriller, War, Western

---

## Possible Uses of This Dataset
- Analyzing movie genre trends over time
- Building recommendation systems based on genres and ratings
- Performing sentiment analysis on reviews (when combined with review data)
- Exploring relationships between directors, genres, and ratings


---

## License
This project is licensed under the MIT License. 

---

Feel free to adjust the placeholders and the sample code section according to your needs!
