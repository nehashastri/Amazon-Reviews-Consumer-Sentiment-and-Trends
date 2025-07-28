# Amazon-Reviews-Consumer-Sentiment-and-Trends

## Project Overview

This project analyzes 2023 Amazon reviews in the **Clothing, Shoes & Jewelry** category to uncover:
- Emerging trends
- Key factors influencing review ratings
- Consumer sentiment and product issues

It combines **Big Data processing**, **Natural Language Processing**, and **Predictive Modeling** to generate actionable insights that support better business decision-making.

---

## Tools & Technologies
- **Big Data**: Apache Spark, Hadoop, YARN (multi-node cluster)
- **Cloud Platform**: Google Cloud Platform (GCP) Dataproc
- **Programming**: Python, PySpark
- **NLP**: TF-IDF, Logistic Regression, Topic Modeling (LDA), Sentiment Analysis
- **Visualization**: 3D clustering, exploratory plots

---

## Dataset

Two primary datasets were used:

### Review Dataset
- `rating`: Product rating (1–5)
- `title`: Title of the user review
- `text`: Full review text
- `timestamp`, `verified_purchase`, `helpful_vote`
- `asin`: Product ID, `user_id`: Reviewer ID

### Items Dataset
- `main_category`, `title`, `price`, `average_rating`
- `features`, `description`, `categories`
- `parent_asin`, `bought_together`

---

## NLP & Sentiment Analysis

- Built sentiment classifier using:
  - Tokenization
  - TF-IDF vectorization
  - Logistic Regression
- Achieved **ROC-AUC score of 79%**
- **Topic Modeling** (LDA):
  - Key themes: Fit, comfort, appearance, quality
  - Issues: Sizing problems, unmet expectations

---

## Predictive Modeling

- Built model to **predict review rating** from review text
- Used TF-IDF + Logistic Regression
- Overall accuracy: **69%**
- Challenge: Highly imbalanced dataset (63% were 5-star reviews)

| Rating | Precision | Recall | F1 Score |
|--------|-----------|--------|----------|
| 1      | 0.51      | 0.52   | 0.51     |
| 2      | 0.28      | 0.06   | 0.09     |
| 3      | 0.33      | 0.17   | 0.22     |
| 4      | 0.42      | 0.14   | 0.21     |
| 5      | 0.75      | 0.95   | 0.84     |

---

## Key Recommendations

- Improve **product quality** (especially in electronics & clothing)
- Strengthen **packaging & logistics**
- **Encourage verified reviews** via email prompts or small incentives
- Engage **prolific reviewers** through beta programs

---

## Future Work

- **Aspect-Based Sentiment Analysis**
- **Real-Time Monitoring** via streaming pipelines
- **Multimodal Feedback** (analyzing user-uploaded images/videos)
- **A/B Testing** for measuring impact of interventions
