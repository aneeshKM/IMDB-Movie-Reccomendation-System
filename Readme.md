# IMDb Personalized Movie Recommendation System Using Hybrid Filtering Techniques

### CS-GY 6513 – Big Data Analysis  
**Team Members:**  
- Ashutosh Agrawal (`aa12398@nyu.edu`)
- Aniket Mane (`am14661@nyu.edu`)  
- Aneesh Mokashi (`akm9999@nyu.edu`)  

---

## 📌 Abstract
This project develops a scalable, personalized IMDb movie recommendation system using a **hybrid filtering approach**. We combine:
- **Collaborative Filtering (ALS)** based on user ratings
- **Content-Based Filtering** using TF-IDF and cosine similarity
- **Neural Collaborative Filtering (NCF)** for deep feature learning

All algorithms were implemented using **PySpark**, **Pandas**, and **TensorFlow**, with the goal of handling large datasets and enabling efficient, personalized, and dynamic movie suggestions.

---

## 🔍 Problem Statement
Users face difficulty navigating through a vast pool of movie options. IMDb provides rich metadata and user interaction data, but lacks real-time, personalized recommendation capabilities. We aim to address:
- Scalability
- Real-time updates
- Cold-start problem
- Dataset sparsity

---

## 🎯 Objectives
- Ingest and preprocess IMDb datasets (ratings, genres, actors, etc.)
- Build scalable distributed pipelines with **PySpark**
- Implement:
  - ALS-based collaborative filtering
  - TF-IDF + cosine similarity-based content filtering
  - Neural Collaborative Filtering (NCF) using TensorFlow
- Evaluate using metrics like **RMSE**, **confusion matrix**, **precision**, and **diversity**
- Address technological bottlenecks (e.g., Java heap errors, ID encoding)

---

## 🗃️ Dataset
IMDb public datasets (TSV format) used:
- `title.basics.tsv.gz`
- `title.ratings.tsv.gz`
- `title.akas.tsv.gz`
- `title.principals.tsv.gz`
- `name.basics.tsv.gz`

Download Link: [IMDb Datasets](https://datasets.imdbws.com/)

---

## ⚙️ Technologies & Tools
- **Languages:** Python, Scala, SQL
- **Data Processing:** PySpark, Pandas, Apache Spark
- **Storage:** (Initially planned) HDFS, MongoDB → used Pandas for simplicity
- **Machine Learning Libraries:** Spark MLlib, scikit-learn, TensorFlow
- **Visualization:** Matplotlib, Seaborn
- **(Optional)** Real-time: Apache Kafka, Spark Streaming (deferred for future work)

---

## 🧠 Algorithms Implemented
1. **Alternating Least Squares (ALS)**  
   Collaborative filtering based on user-item interaction matrix.

2. **Content-Based Filtering**  
   Used TF-IDF vectorization and cosine similarity over genres, descriptions, and cast.

3. **Neural Collaborative Filtering (NCF)**  
   Modeled complex non-linear user-item interactions with deep learning.

---

## 📊 Results
- Genre frequency plots
- Year-wise average rating trends
- Top-10 highest-rated movies
- Ratings distribution histogram
- Loss curve visualization
- Confusion matrix for classification performance

---

## 🧪 Evaluation Metrics
- **Root Mean Squared Error (RMSE)**
- **Confusion Matrix**
- **Precision/Recall**
- **Prediction diversity**

---

## 🛠️ Challenges & Fixes
| Challenge | Fix |
|----------|-----|
| Java Heap Space Error | Increased Spark memory allocation and repartitioned datasets |
| Non-numeric IDs in ALS | Used `StringIndexer` to map strings to numeric IDs |
| Window Function Slowness | Repartitioned data before applying window functions |
| ALS Fails on Sparse Data | Applied NCF for low-interaction cases |

---

## 🚀 Future Scope
- Add real-time recommendation updates using **Kafka + Spark Streaming**
- Address cold-start more robustly using metadata embeddings
- Develop a user-facing **web interface** with dashboards
- Apply **sentiment analysis** on user reviews for refined filtering

---

## 🔗 Project Repository
[GitHub Link](https://github.com/iamANIKETmane/BigDataProject)

---

## 🏁 Conclusion
The developed system efficiently integrates **collaborative**, **content-based**, and **neural** filtering techniques to produce accurate and diverse recommendations. It handles large-scale data using distributed PySpark pipelines and shows robust performance under sparsity. Future integration of streaming tools can enhance responsiveness and user experience.

