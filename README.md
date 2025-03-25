# Handson 8 Report

## Overview
This report analyzes social media posts using Apache Spark. We explored trending hashtags, user engagement by age, how sentiment affects engagement, and who the most influential verified users are.

---

## Steps

###  Running Locally

- Checked Python:
```bash
python3 --version 
``` 

- Installed PySpark 
```bash 
pip install pyspark
``` 
- Checked Spark:
```bash 
spark-submit --version
``` 

- I completed the TODOs in each task and then ran the following:

### Task 1
``` bash 
spark-submit src/task1_hashtag_trends.py
``` 

### Task 2
``` bash 
spark-submit src/task2_engagement_by_age.py
``` 

### Task 3
``` bash 
spark-submit src/task3_sentiment_vs_engagement.py
``` 

### Task 4
``` bash 
spark-submit src/task4_top_verified_users.py
``` 
- I verified that the output of each script was saved correctly to the outputs/ folder and matched the assignment requirements.


# Findings 

### Task 1: Hashtag Trends
1. goal: Find out which hashtags are used the most.
- What I Did: 
   - Split the Hashtags column into individual tags.

   - Counted how often each hashtag appeared.

   - Sorted and took the top 10.

2. results 
- Tags like #AI and #mood are very popular.

### Task 2: Engagement by Age Group 
1. goal: See which age group interacts (likes/retweets) the most.

- What I Did: 
   - Joined posts with user data using UserID.

   - Grouped by AgeGroup.

   - Calculated average likes and retweets.

2. results 
- Teens had the highest engagement.
- Adults followed next, and seniors had the least.

### Task 3: Sentiment vs Engagement
1. Check if happy or angry posts get more attention.

- What I Did: 
   - Grouped posts as Positive (> 0.3), Neutral (-0.3 to 0.3), or Negative (< -0.3).

   - Calculated average likes and retweets for each group.

2. results 
- Neutral posts had the highest engagement.
- Positive posts did okay.
- Negative posts got the least attention..

### Task 4: Top Verified Users by Reach
1. Find the verified users with the most reach.

- What I Did: 
   - Filtered for verified users only.

   - Calculated reach by summing likes and retweets.

   - Grouped by user and sorted to get the top 5.

2. results 
- Top users like @designer_dan and @social_queen had the highest audience reach.
- Verified users play a key role in spreading content.
