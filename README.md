# 🎬 Letterboxd Movie Dataset: EDA and Hybrid Recommender Systems
## Repository Name: Letterboxd-Movies-EDA-Systems

### 📋 Table of Contents

1.  Project Overview
2.  Dataset Source
3.  Methodology and Workflow
4.  Key Insights (EDA Results)
5.  Developed Recommendation Systems
6.  Technologies Used

---

### 1. Project Overview

This project focuses on performing in-depth Exploratory Data Analysis (EDA) and developing three distinct movie recommendation systems using the comprehensive Letterboxd Movie Dataset from Kaggle. The main objective was to engineer a robust **Weighted Content-Based Hybrid Recommender System** capable of delivering highly relevant and nuanced film suggestions.

### 2. Dataset Source

* **Dataset Name:** Letterboxd Movies Dataset
* **Source:** Kaggle
* **Link:** [Insert the Original Kaggle Dataset Link Here]
* **Record Count:** 16,246 movie entries
* **Features:** 28 columns (including Genres, Runtime, Country, Year, etc.)

### 3. Methodology and Workflow

The project followed a standard Data Science workflow:

#### A. Data Cleaning and Preprocessing
* Missing values were identified using `df.info()`.
* Missing categorical features (e.g., `primary_genre`, `country`) were imputed with **"Unknown"**.
* Numerical features (e.g., `runtime`) were imputed using the **Median** value.

#### B. Exploratory Data Analysis (EDA)
* **Univariate:** Visualized the distribution of top genres (e.g., Comedy, Romance) and runtime (Median Runtime: [Insert Your Found Median Runtime] min).
* **Temporal:** Analyzed film production trends over time and visualized genre popularity across decades (Heatmap).
* **Bivariate:** Examined the relationship between `primary_genre` and `runtime` using Box Plots.

#### C. Modeling: Three Recommendation Systems Developed
All systems rely on similarity calculations, either through **Cosine Similarity** or **Distance Metrics**.

### 4. Developed Recommendation Systems

| System Type | Focus | Technique | Goal |
| :--- | :--- | :--- | :--- |
| **1. Simple Category-Based** | `primary_genre` or `decade_category` | Filtering & Ranking by Year | Provides a baseline list of the most recent/top films within a specified category. |
| **2. Genre-Only Content-Based** | Solely `genres` | TF-IDF & Cosine Similarity | Recommends films with matching genre tags (narrow recommendations). |
| **3. Weighted Hybrid Content (Core Focus)** | `genres`, `country`, `language`, `decade_category` | **Weighted TF-IDF & Cosine Similarity** | Combines features with weights to recommend films similar in genre, geography, and time period (highest relevance). |

### 5. Key Insights

* **Dominant Genre:** The dataset is heavily skewed towards [State the most dominant genre] (e.g., Comedy).
* **Runtime Trends:** The comparison between **Classic** and Non-Classic films revealed [State your finding about runtime difference].
* **Hybrid Superiority:** The Weighted Hybrid System provided demonstrably richer recommendations by identifying films with shared [Mention a secondary feature like "country" or "decade"] similarities that the Genre-Only model missed.

### 6. Technologies Used

* `Python`
* `Jupyter Notebook`
* `Pandas` (Data Manipulation)
* `NumPy` (Numerical Operations)
* `Matplotlib` / `Seaborn` (Visualization)
* `Scikit-learn (sklearn)` (TF-IDF, Cosine Similarity)
* `Git` / `GitHub` (Version Control & Hosting)
