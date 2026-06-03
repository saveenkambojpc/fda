# User Behavior Analysis for Optimizing Engagement on Social Media Platforms

An advanced data analytics project focused on understanding, processing, and segmenting social media user behavior using unsupervised machine learning. This repository contains the workflows for cleaning raw platform telemetry, visualizing activity trends, and applying clustering algorithms to discover natural audience segments for personalized optimization strategies.

---

## 📌 Project Overview
Modern social media platforms generate vast amounts of behavioral data. To effectively maximize user retention and ad revenue, businesses must transition from broad, demographic-based targeting to data-driven behavioral segmentation. 

This project implements an end-to-end data science workflow using a dataset of **20,000 records** containing user profiles, content attributes, and explicit interaction metrics. By executing data preprocessing, statistical profiling, and comparative clustering modeling, the repository establishes an actionable structure to build specialized recommendation feeds, flag automated/bot profiles, and optimize marketing spend.

---

## 🛠️ Tech Stack & Dependencies
The codebase is built strictly in Python using standard data science libraries:
* **Data Manipulation:** `pandas`, `numpy`
* **Statistical Modeling & Unsupervised Learning:** `scikit-learn`, `scipy`
* **Data Visualization:** `matplotlib`, `seaborn`

---

## 📈 Pipeline Architecture & Features

### Phase 1: Robust Data Collection & Logging
The project ingests cross-sectional social media logs capturing multi-dimensional facets:
* **Demographics:** `user_age`, `user_gender`, `location`, `is_verified`, `account_creation_date`
* **Engagement Metrology:** `likes`, `comments`, `shares`, `engagement_rate`
* **Content Architecture:** `topic`, `post_content`, `content_length`, `hashtags`, `has_media`
* **Temporal & Network Context:** `post_date`, `device`, `language`, `followers_count`, `following_count`

### Phase 2: Structural Data Preprocessing & Cleaning
Raw platform telemetry often suffers from API transport anomalies and user profiling omissions. The cleaning suite isolates and addresses these anomalies:
* **Datetime Standardization:** Coerces irregular timestamp formats into linear temporal blocks via `pd.to_datetime` handling timezone drift.
* **Imputation Analytics:** Evaluates null rows. Applies localized **Median Imputation** for highly skewed numerical engagement indicators (`likes`) and sets a categorical fallback label (`'Unknown'`) for device properties.
* **Deduplication Suite:** Scans and eliminates mirrored vector instances generated during repetitive API callback processes.
* **Outlier Profiling:** Implements an Interquartile Range (IQR) analysis block to differentiate standard distributions from systemic distribution skews (such as hyper-viral organic content).

### Phase 3: Unsupervised Machine Learning Framework
Since platform profiles lack pre-existing class targets, this project positions audience discovery as an unsupervised clustering paradigm over traditional classification models. It implements, evaluates, and contrasts two primary approaches:

1.  **K-Means Centroid Clustering**
    * Scalable partitioning optimized via vector minimization across user engagement dimensions.
    * Segments the global user population into three clean, actionable interaction tiers.
2.  **Agglomerative Hierarchical Clustering**
    * Builds structural, distance-based linkage trees.
    * Implements a sample-reduction block to compute bottom-up topological relationships, rendered directly via dendrogram matrices.

---

## 📊 Benchmark Evaluation Metrics

Model performance was strictly benchmarked across computational processing velocities, linear sample scaling, and structural cluster cohesion:

| Evaluation Metric | K-Means Clustering | Hierarchical Clustering | Operational Takeaway |
| :--- | :---: | :---: | :--- |
| **Silhouette Cohesion Score** | **0.579** | 0.543 | K-Means yields tighter, significantly more distinct cluster boundaries. |
| **Baseline Processing Velocity** | **0.017 seconds** | 0.001 seconds | Hierarchical linkage shows high efficiency on compact micro-samples. |
| **Scalability Horizon (10k Rows)** | **0.0069 seconds** | 2.7518 seconds | K-Means processes large datasets with stable linear complexity $O(n)$. |
| **Systemic Outlier Resilience** | Absolute Assignment | Absolute Assignment | Both models assign out-of-bounds metrics into global vector limits. |

### Operational Audience Segments Identified:
* **Tier 1 (Low Interaction Base):** Passive consumer profiles tracking minimal explicit engagement signatures. Ideal for reactivation notifications.
* **Tier 2 (Moderate Core Community):** Regular user cohorts maintaining stable, proportional text and category interaction. Best suited for high-density native advertising.
* **Tier 3 (High-Velocity Amplifiers):** Verified accounts and creators holding heavy follower weights and dense interaction rates. Ideal for brand partnership strategies.

---

## 🚀 Key Operational Deliverables
By implementing these distinct algorithmic user matrices, a platform can natively power four strategic systems:
1.  **Contextual Hyper-Personalization:** Delivers automated algorithmic content loops aligned directly with behavioral historical profiles.
2.  **Ad-Campaign Optimization:** Segments demographic micro-groups, lifting campaign conversion and minimizing generic advertising waste.
3.  **Proactive Churn Mitigation:** Automatically flags downward velocity trends within the core segments to trigger defensive retention prompts.
4.  **Malicious Vector/Bot Interception:** Isolates clusters maintaining highly irregular or repetitive interaction signatures for security evaluations.

---

## 📜 Academic Reference & Citation
This framework was developed as part of an exhaustive research assignment for the **MSc Data Analytics** curriculum (Academic Year 2026).
* **Author:** Saveen Kamboj (Q1084614)
* **Affiliation:** University for the Creative Arts / Berlin School of Business & Innovation
* **Methodological References:** Core algorithmic principles adapted from *Han, Kamber and Pei (2022) - Data Mining: Concepts and Techniques* and *Tan, Steinbach and Kumar (2019) - Introduction to Data Mining*.
