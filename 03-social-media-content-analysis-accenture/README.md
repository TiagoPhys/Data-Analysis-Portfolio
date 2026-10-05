# Content Popularity on a Social Media Platform

Notebook: [`content_popularity_analysis.ipynb`](content_popularity_analysis.ipynb). Client brief: [`brief/`](brief). Presentation: [`report/social-buzz-presentation.pdf`](report/social-buzz-presentation.pdf)

## Problem

Social Buzz receives more than 100,000 posts per day and asked for the 5 content categories with the highest total popularity. This is a case study from the Accenture virtual experience programme.

## Approach

1. Cleaned the three tables (content, reactions and reaction types), dropping unused columns and reactions without a type.
2. Standardised category labels. The raw data had 41 spellings for 16 categories, for example `animals`, `Animals` and `"animals"`.
3. Joined the tables following the client's data model and gave every reaction its score (from 0 to 75).
4. Ranked categories by total score, then looked at sentiment, content type and monthly activity.

## Results

![Popularity by category](images/category_popularity.png)

- Top 5 categories: Animals, Science, Healthy eating, Technology and Food.
- Food appears twice in the top 5 (Healthy eating and Food), and Cooking is 8th. Partnerships with food and healthy eating brands are a natural next step for the client.
- The average score per reaction is similar across categories, so the ranking depends mostly on how many reactions each category gets.
- Before the labels were standardised, Cooking was in the top 5 and Food was not. I recommended a fixed list of categories at upload.
