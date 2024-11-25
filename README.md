# portfolio-1-data_analysis-songs

![Project cover](/screenshots/cover.png)

## First portfolio project: Spotify songs insights
For this first portfolio project, my aim is to try to get a **first approach of insights** from a public dataset from [Kaggle](https://www.kaggle.com/): [30000 Spotify Songs](https://www.kaggle.com/datasets/joebeachcapital/30000-spotify-songs/data). The dataset is rich in songs attributes surrounding **a key performance measure: Popularity**.

The steps will be as follows:

1. **Data exploratory**: Read the csv file through a **jupyter notebook** to explore, validate and, in case is needed, clean the data to export it to Tableau and get some first findings.
2. **Data visualization**: The resulting csv file will be imported to **Tableau Public** to visualize the data trying to get to know the data enough to start to build some valuable insights.
3. **Insights description**: Returning to a new **jupyter notebook**, to get precise numbers about these insights discovered.
4. **Storytelling**: A straight-forward way to communicate these insights to stakeholders.

## 1. Data exploratory
Full jupyter notebook is included in current repository and also available online ready to run in Kaggle:
https://www.kaggle.com/code/gastnezequiellema/spotify-songs-data-exploratory

The purpose of this stage is to prepare data to be ready to be visualized. We need to validate and eventually clean the data

### Exploratory findings
- We’ve found several duplicated values for track_id. Duplicates are explained because of the participation of tracks in several playlists.
- I’ve decided to remove playlist data from this first approach as the cost of processing it presumably do not worth the insights value, at least for now.
- Dataset includes songs from 1957 to 2020 but 75% of them are from 2008 or newer.
- Data is consistent and it’s ready for visualization.

## 2. Data visualization

**A first set of interactive dashboards is available in Tableau Public:**

https://public.tableau.com/app/profile/gast.n.lema/viz/2020_30k_spotify_songs/Topartists?publish=yes

We will try to focus on insights based on **our key performance indicator: Track Popularity**. We will try to get the recipe for a popular song based on the attributes available so we will start by filter top 1000 most popular songs and see how attributes perform.

### Insights building

#### Tempo
![Loudness legend](/screenshots/loudness.png)
![Tempo distribution](/screenshots/tempo.png)

- Higher tempo songs tend to work better but outlier performant songs are in lower tempos: from 76 to 127 bpm

#### Duration
![Duration distribution](/screenshots/duration.png)

- Shorter songs tend to have more success but most of them start in around 150 seconds and last less than 300 seconds.
- Outlier most performant are between 159 and 246 seconds.

#### Danceability
![Danceability distribution](/screenshots/danceability.webp)

- Danceability is a key to success with outliers following that trend.

#### Energy
![Energy distribution](/screenshots/energy.webp)

- Most of top 1000 popular songs are high on energy but within that top, the trend is decresent, so to stand out, the energy must be lower than the average.
- Energy and loudness correlate very well.

### Overall insights
So trying to build this insights as a **recipe of a top hit in Spotify** we have these qualities:

- **Danceability is a must.**
- **Energy is optional and it can be a strategy to keep it low to stand out.**
- **We seek for a duration between 2.5 and 5 minutes.**
- **Let’s keep a low-mid tempo, between 91 and 127 bpm.**

## 3. Insights description
To **communicate well these insights to the business** we have to be **certain and precise with the numbers**. So we will get back to **jupyter notebooks** and build a new one to get the calculations ready. This notebook is available in this repository and also online in Kaggle.

https://www.kaggle.com/code/gastnezequiellema/spotify-songs-insights-calculation

## 4. Storytelling

To end this project we will present insights in a clear and straight forward manner, based on numbers from real data. A further stage could be building a presentation for stakeholders.

#### Danceability
- **Highly danceable tracks are 23.3% more likely to be successful compared to less danceable tracks. 12.2% of highly danceable tracks reach the top 10% in popularity.**
- Danceability progressively increases with popularity tiers. **Top 20% tracks have 3.4% higher danceability than bottom 20% tracks.**
- **Top 100 tracks have an average danceability of 70.3%**

#### Duration
- Among the **top 1000 tracks, 72.3% have a duration between 2.5-4.1 minutes. These tracks perform 106.3% better than the overall average.**

#### Tempo
- Among the **top 1000 tracks, 50.5% have a tempo between 91-127 BPM. These tracks perform 106.5% better than the overall average.**

#### Energy
- In top 1000 tracks, **energy shows a weak correlation of -0.142 with popularity**. The average energy is 65%.

### **Overall – Recipe**
- To craft a hit, aim for a track that **maximizes danceability**, ideally around 70%, as higher danceability significantly boosts the likelihood of success.
- **Keep the duration between 2.5 to 4.1 minutes** to align with top-performing tracks, and **set the tempo within the 91-127 BPM range** for optimal impact.
- While **energy levels should average around 65%, avoid overly high values**, as there is a slight negative correlation with popularity.

Balancing these elements can enhance a track’s chances of reaching the top charts.