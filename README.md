# 📊 Amazon-EDA-Report
This project is an Exploratory Data Analysis (EDA) report created in Google Colab to understand the structure, quality, and insights from Amazon video content data. The analysis combines title metadata and credits (cast & crew) to uncover patterns related to content type, genre, country of production, and individual performance (actors/directors).

📁 Files Used
data_titles: Contains metadata for Amazon content, such as:

id, title, description

release_year, runtime, genres

production_countries, age_certification, tmdb_popularity, imdb_score, etc.

data_credits: Provides cast and crew information:

person_id, name, role (Actor/Director), id (for linking with data_titles)

These files were imported directly from Google Drive URLs using pandas.read_csv().

🔄 Data Preprocessing
✅ Cleaning Steps
Duplicates: Identified and removed from both datasets using duplicated() and drop_duplicates().

Missing Values:

Checked percentage of nulls using isnull().sum()/len(df).

Replaced missing values in numerical columns using mean or median.

Dropped columns like seasons and age_certification due to high null presence.

String to List Conversion: Converted genres and production_countries fields from stringified lists to actual Python lists using eval() safely inside a custom function.

📊 Visual Explorations & Insights
🔸 Content Type Distribution
A pie chart shows the proportion of Movies vs TV Shows on Amazon.

Bar plots visualize the number of titles released each year.

🔸 Genre & Country Analysis
Genres and production countries were exploded (one genre/country per row).

Top genres and countries were visualized using bar plots and heatmaps.

🔸 IMDb & TMDB Score Analysis
Average scores were calculated per genre, plotted side-by-side to compare IMDb vs TMDB ratings.

Scores were also grouped by 5-year bins of release_year to observe performance trends over time.

🔸 Bubble Chart: Genre vs Score over Time
Created interactive bubble plots to show:

How different genres performed over time.

Bubble size represents the number of titles.

Separate plots for Movies and TV Shows.

🔸 Heatmap: Top 15 Countries vs Top 15 Genres
Visualizes genre preferences across countries.

Helps understand which countries favor what kind of content.

👤 Cast & Crew Role Analysis
Merging Cast Data
Grouped and counted the number of actors and directors per title.

Merged this with the main data_titles to form df_titles_credits.

People Performance
Used explode() to create a row per person per role per title.

Merged with names using person_id.

Scatter Plot: IMDb Score vs Appearance Count
Created a Plotly scatter plot:

X-axis: number of titles a person appeared in

Y-axis: average IMDb score

Color by role (Actor/Director)

Size by IMDb score

Only included people with at least 3 appearances to ensure reliability

Box Plot: Number of Actors vs IMDb Score
Shows how the number of actors in a project impacts the IMDb score.

Outliers removed (only projects with ≤20 actors shown).

📌 What You’ll Learn from This Notebook
How Amazon content differs across countries and genres.

What kind of content performs well on IMDb and TMDB.

Which actors and directors have the strongest positive impact on ratings.

Trends in content creation over the years using grouping and visualization.

📚 Tools & Libraries Used
pandas, numpy: data handling

matplotlib, seaborn, plotly.express: visualization

eval, explode, groupby, merge: advanced data manipulation

✅ Conclusion
This Amazon-EDA-Report helps uncover:

High-performing genres and countries

Popular release periods

Influence of cast size and person-role dynamics on content quality

The notebook is rich in clean visualizations, well-handled missing data, and deep analysis of cast and crew effects — ideal for content strategy, recommendation systems, or market analysis.
