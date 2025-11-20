# -Instagram-Data-Analysis
📊 Instagram Data Analysis

This project focuses on performing exploratory data analysis (EDA) on Instagram activity using multiple CSV files such as users, photos, likes, comments, tags, and photo-tag relationships.

The goal is to uncover patterns in user engagement, popular posts, trending tags, and overall platform activity.

📁 Dataset Files

The dataset contains the following files:

File Name	Description
users.csv	Information about Instagram users
photos.csv	Details about photos uploaded
likes.csv	Likes received on photos
comments.csv	Comments made by users
tags.csv	List of tags used
photo_tags.csv	Mapping between photos and tags
🎯 Objectives

This task includes:

✔️ Loading and cleaning data

✔️ Analyzing user activity

✔️ Studying engagement through likes & comments

✔️ Tag popularity analysis

✔️ Visualization of trends

🛠️ Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

🚀 How to Run the Analysis (Using Google Colab)

Create a new notebook in Google Colab

Upload all CSV files

Copy the code from this repository

Run all cells to view analysis and visualizations

📌 Code Overview
1. Importing Libraries & Loading Datasets
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

users = pd.read_csv("users.csv")
photos = pd.read_csv("photos.csv")
likes = pd.read_csv("likes.csv")
comments = pd.read_csv("comments.csv")
tags = pd.read_csv("tags.csv")
photo_tags = pd.read_csv("photo_tags.csv")

2. Basic Data Exploration
print(users.head())
print(photos.head())
print(likes.head())
print(comments.head())

3. Photos Uploaded per User
photos_per_user = photos['user_id'].value_counts()
plt.figure(figsize=(12,5))
photos_per_user.plot(kind='bar')
plt.title("Photos Uploaded per User")
plt.show()

4. Top 10 Most Liked Photos
likes_count = likes['photo_id'].value_counts().head(10)
likes_count.plot(kind='bar', figsize=(10,5))
plt.title("Top 10 Most Liked Photos")
plt.show()

5. Most Active Users by Comments
comments_per_user = comments['user_id'].value_counts().head(10)
comments_per_user.plot(kind='bar', figsize=(10,5))
plt.title("Top 10 Users by Comment Activity")
plt.show()

6. Most Frequently Used Tags
top_tags = photo_tags['tag_id'].value_counts().head(10)
top_tags.plot(kind='bar', figsize=(10,5))
plt.title("Top 10 Most Used Tags")
plt.show()

7. Engagement Analysis (Likes + Comments per Photo)
like_count = likes.groupby('photo_id').size()
comment_count = comments.groupby('photo_id').size()

engagement = (like_count + comment_count).sort_values(ascending=False).head(10)
engagement.plot(kind='bar', figsize=(10,5))
plt.title("Top 10 Photos by Engagement")
plt.show()

📊 Visual Output

The analysis generates:

Engagement metrics

Most liked photos

Most active commenters

User photo uploads

Tag usage trends

Distribution insights

📂 Project Structure
instagram-analysis/
│── README.md
│── instagram_analysis.ipynb
│── users.csv
│── photos.csv
│── likes.csv
│── comments.csv
│── tags.csv
│── photo_tags.csv
