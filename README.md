# 🎬 EDA of Amazon Prime Movies & TV Shows

## **📘 Project Overview**

This project performs an **Exploratory Data Analysis (EDA)** on the *Amazon Prime Video* dataset to uncover meaningful insights about the platform’s content — including trends in genres, ratings, countries, and popularity over time.

The analysis aims to:

* Understand the **distribution of content** across movies and TV shows.
* Explore **temporal trends** in content release and audience preferences.
* Identify **top-performing genres, countries, and creators** based on IMDb and TMDB scores.
* Provide **data-driven insights** that could guide strategic decisions in content planning and acquisition.

---

## **🛠️ Technologies Used**

* **Programming Language:** Python
* **Environment:** Jupyter Notebook (`EDA_of_Amazon_Prime_Movies_&_TV_Shows.ipynb`)
* **Libraries & Tools:**

  * **Data Manipulation:** pandas, numpy
  * **Visualization:** matplotlib, seaborn, plotly
  * **Data Cleaning & Preprocessing:** pandas, regex, datetime
  * **Statistical Analysis:** scipy (if used for correlations or distributions)

---

## **📂 Project Structure**

```
EDA_of_Amazon_Prime_Movies_&_TV_Shows/
│
├── EDA_of_Amazon_Prime_Movies_&_TV_Shows.ipynb  # Main Jupyter notebook for EDA
│
├── visuals/
│   ├── chart1_content_type.png
│   ├── chart2_yearly_trend.png
│   ├── chart3_country_wise.png
│   ├── chart4_genre_ratings.png
│   ├── chart5_tmdb_popularity.png
│   ├── chart6_imdb_genre_trend.png
│   ├── chart7_genre_country_heatmap.png
│   └── chart8_cast_crew_scores.png
│
├── README.md                    # Project documentation
```

### **Key Components**

* **Notebook (`.ipynb`)** — Contains the entire workflow: data loading, cleaning, EDA, and visualization.
* **Data folder** — Holds all CSV files used for analysis.
* **Visuals folder** — Stores exported plots and charts for presentation.
* **README.md** — Provides project overview, structure, and insights.

---

👉 [Click to Watch Video](https://drive.google.com/file/d/1nL4__REdGlDcS-TeDAumjOjKon-aLsGK/view?usp=sharing)


---

## **📊 Insights from Charts**

1. Movies dominate the platform (≈86%), while TV Shows form only 14%.
2. There was a sharp rise in content after 2010, peaking around 2020.
3. USA leads by a wide margin in production, followed by India and the UK.
4. IMDb top genres are Documentary, History, and Reality, while TMDB top genres are Animation, Reality, and History.
5. Shows generally have higher TMDB scores than movies; popularity surged significantly after 2015, driven by movies.
6. Recent years show more content in Drama, Comedy, and Action; older genres like History and War had higher ratings but fewer titles; TV shows often outperform movies in IMDb ratings.
7. US dominates across most genres; India and UK are strong in Drama and Romance; Japan stands out for Animation; France for Documentary.
8. Few actors/directors with limited work have exceptional IMDb scores, while high-volume contributors maintain moderate but consistent scores.

