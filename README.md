# 🏎️ Formula 1 Driver Performance Clustering

Welcome to a project where Formula 1 meets machine learning.  
Instead of looking at just podiums, wins, or championship points, this project asks:

## ❓ What if we grouped F1 drivers by their **full race-day performance profile**?

Using **unsupervised learning**, this project explores hidden patterns in historical Formula 1 data and clusters drivers based on how they actually perform across races.


## 📌 What This Project Does

This project analyzes Formula 1 race-day data to discover **natural groupings of drivers** based on performance traits like:

- 🟢 Grid position
- 🏁 Final position
- ⏱️ Total race time
- ⚡ Fastest lap and average lap time
- 🔧 Pit stop count and duration
- 🎯 Qualifying performance (Q1, Q2, Q3)
- 💯 Race points

Rather than predicting an outcome, this project focuses on **finding patterns** that may not be obvious from standings alone.


## 📂 Dataset

The data comes from a **Kaggle Formula One dataset** covering **every Grand Prix from 1950 to 2024**.

### It includes:
- Driver records
- Race results
- Lap-level data
- Pit stop behavior
- Qualifying results
- Final standings

This gives a much richer view of race-day performance than simply checking who finished first.


## 🛠️ Tech Stack

- **Python** 🐍
- **Jupyter Notebook**
- **Data preprocessing + feature engineering**
- **Dimensionality reduction**
- **Clustering analysis**
- **Data visualization**


## 🧠 Methods Used

This project combines several unsupervised learning techniques:

### 1. 🧹 Data Preparation
Real-world F1 data contains missing values, so preprocessing was an important first step.

### 2. 🩹 Matrix Completion with SoftImpute
Missing values were filled using **SoftImpute**, which applies low-rank SVD iteratively.  
This helped preserve important rows instead of dropping incomplete data.

### 3. 📉 PCA (Principal Component Analysis)
PCA was used to reduce the number of features and make the data easier to visualize and cluster.

### 4. 🔢 SVD (Singular Value Decomposition)
SVD was used to understand variance distribution, project the data into lower dimensions, and support missing-value handling.

### 5. 🎯 K-Means Clustering
K-Means was applied to the PCA-transformed dataset to group similar driver-race performance profiles.

### 6. 🌳 Hierarchical Clustering
Hierarchical clustering was used alongside K-Means to better understand how clusters relate to one another.

### 7. 📏 Cluster Evaluation
The project used:
- **Elbow Method**
- **Silhouette Score**
to help determine the best number of clusters.


## 📊 Results

Here’s the main takeaway:

- ✅ The analysis found that **4 clusters** best captured the diversity of race-day driver performance
- ✅ The **elbow plot leveled off around k = 4**
- ✅ The **silhouette score also supported k = 4**
- ✅ A **3D PCA scatter plot** showed reasonable separation between clusters

In simple terms:  
different drivers and race performances naturally fall into distinct performance groups and unsupervised learning helps reveal them.


## 🚦 Why This Matters

In Formula 1, performance is more than just “win or lose.”

A driver can:
- qualify well but race poorly
- recover positions after a weak start
- gain advantage through consistency
- lose time through pit strategy
- perform differently depending on race conditions

This project shows that machine learning can capture those deeper patterns and turn them into meaningful performance clusters.


## 🎯 Project Goal

The goal of this project is to show that **unsupervised learning can uncover hidden structure in Formula 1 race-day data** and provide a more complete way to understand driver performance.


## 🚀 Possible Future Improvements

- Add interactive visualizations
- Compare clusters across eras
- Profile cluster characteristics more deeply
- Explore t-SNE or UMAP for visualization
- Build dashboards for driver cluster exploration


## 🎯 Note from the Author:

As someone who enjoys Formula 1 🏎️, data science 📊, machine learning 🤖, and sports analytics 📈, this project brings all of those interests together in one place.
Because sometimes, the most interesting thing in racing isn’t just **who won** - it’s **how they raced**.
