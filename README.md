# 🎬 CineSpark: A Scalable Movie Recommender System using PySpark & Databricks

🚀 A full-fledged, distributed, and scalable **Movie Recommendation System** built with **Apache Spark (PySpark)** and **Databricks**, using the popular **MovieLens dataset**. This project demonstrates real-world data engineering, machine learning, and recommender system techniques on big data platforms.

---

## 📌 Table of Contents
- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Dataset](#dataset)
- [Pipeline Stages](#pipeline-stages)
- [Key Insights](#key-insights)
- [Recommendation Model](#recommendation-model)
- [Results](#results)
- [How to Run](#how-to-run)
- [Future Enhancements](#future-enhancements)

---

## 📖 Overview

**CineSpark** is a recommendation engine that analyzes user behavior and ratings to predict and recommend movies. It handles large-scale data using PySpark's distributed computing power and applies **collaborative filtering (ALS)** to provide **personalized movie suggestions**.

---

## 🛠️ Tech Stack

- **PySpark (Spark SQL, MLlib)**
- **Databricks (Notebooks)**
- **MovieLens Dataset (100k or 1M)**
- **Pandas / Matplotlib (for local visualizations)**


---

## 🎬 Dataset

- **Source**: [MovieLens](https://grouplens.org/datasets/movielens/)
- **Files Used**:
  - `movies.csv`: movieId, title, genres
  - `ratings.csv`: userId, movieId, rating, timestamp

---

## 🔄 Pipeline Stages

| Step | Description |
|------|-------------|
| **1. Data Ingestion** | Loaded datasets into PySpark DataFrames |
| **2. Data Cleaning & Transformation** | Parsed titles, extracted release year, split genres |
| **3. EDA & Visualization** | Analyzed popular genres, rating trends, user activity |
| **4. ALS Recommender Model** | Trained collaborative filtering model using Spark MLlib |
| **5. Evaluation** | Used RMSE metric to evaluate model performance |
| **6. Recommendations** | Generated Top-N movie recommendations per user |
| **7. Save & Export** | Stored results as Parquet/CSV and logged via MLflow |

---

## 📊 Key Insights

- 🎥 **Top-rated genres**: Drama, Comedy, Action
- 🔄 **Most active users**: High variance in user rating behavior
- 📈 **Rating volume peak**: ~1995–2000 (movie boom era)
- 🧠 **High rating density**: Older movies with cult followings

---

## 🤖 Recommendation Model

- **Algorithm**: Alternating Least Squares (ALS)
- **Parameters**:
  - `rank = 10`
  - `maxIter = 10`
  - `regParam = 0.1`
  - `coldStartStrategy = "drop"`

- **Evaluation**:  
  Achieved **RMSE = ~0.85** on test set — indicating good predictive power for unseen ratings.

---

## ✅ Results

Example output: **Top 5 recommendations for User 1**

| Movie Title | Predicted Rating |
|-------------|------------------|
| The Matrix (1999) | 4.87 |
| Toy Story (1995) | 4.76 |
| Pulp Fiction (1994) | 4.74 |
| Star Wars (1977) | 4.72 |
| Forrest Gump (1994) | 4.70 |

---

## 🧪 How to Run

### Option 1: On Databricks (Recommended)
1. Upload `movies.csv` and `ratings.csv` to DBFS
2. Clone this repo into your Databricks workspace
3. Run each notebook step-by-step:
   - `01_data_ingestion.ipynb`
   - `02_data_cleaning.ipynb`
   - `03_eda_visualization.ipynb`
   - `04_model_als_recommender.ipynb`
   - `05_save_wrapup.ipynb`
4. Use MLflow UI to track and compare model runs

---

## 🚀 Future Enhancements

- ✅ Add content-based filtering (title/genre embeddings)
- ✅ Integrate user demographics (age, gender) from extended datasets
- ✅ Deploy as an API using Flask + Spark job
- ✅ Stream real-time ratings using Apache Kafka + Structured Streaming

---

## 🙌 Author

**Baaja**  
M.Tech in Data Engineering | Amazon | Passionate about Big Data, ML & Cloud  
🌐 GitHub: [github.com/yourusername](https://github.com/yourusername)

---

## ⭐️ If you liked this project, don’t forget to **star the repo** and check out my other work!

