# US Election Sentiment and Engagement Analysis via Reddit API

## Project Overview
This project builds an API data pipeline using the Reddit API to analyze public sentiment and engagement on posts related to the US election. By collecting data in real-time from trending election-related posts, this project leverages sentiment analysis and engagement metrics to provide insights into public opinion and discussions around key candidates.

## Features
- Data Collection: Accesses real-time Reddit posts from the /r/politics subreddit using the Reddit API, with a focus on posts related to the US election
- Data Preprocessing: Cleaned and tokenized post titles, removed stopwords, and stems keywords to prepare text for analysis, and also performed binary encoding for candidate label.
- Sentiment Analysis: Applies Natural Language Processing (NLP) techniques to analyze sentiment in post titles, quantifying public opinion on different candidates.
- Engagement Metrics: Collects upvote and downvote counts, scaling these metrics for further analysis.
- Data Visualization: Synthesizes sentiment and engagement scores into interpretable visualizations, illustrating public sentiment for each candidate.


## Results and Interpretation

| **Metric/Visualization**                 | **Description**                                                                                                    | **Interpretation**                                                                                                                                             |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Average Sentiment Score by Candidate** | A bar chart showing the mean sentiment score for each candidate, derived from post titles mentioning each candidate.| Positive scores indicate a favorable view among users, while negative scores suggest criticism or dissatisfaction. This helps gauge general public sentiment toward each candidate. |
| **Sentiment Distribution (Density Plot)**| Density plots for each candidate showing the spread of sentiment scores across posts.                               | Peaks in the density plot indicate where the majority of sentiment scores lie. Comparing peaks between candidates highlights who has more favorable (or unfavorable) sentiment. |
| **Sentiment Category Counts**            | Counts of positive and negative sentiment scores per candidate.                                                    | Higher counts of positive sentiment suggest broader public support, while higher negative counts may indicate controversy or criticism. Useful for understanding sentiment polarity. |
| **Engagement Metrics (Upvotes/Downvotes)** | Histograms or bar charts showing scaled upvote and downvote counts for posts about each candidate.                  | Higher engagement (upvotes) reflects the popularity or relevance of a candidate’s topic. Peaks in engagement can correlate with periods of heightened public interest. |
| **Combined Sentiment-Engagement Score**  | A synthesized score combining sentiment and engagement, calculated using exponential transformations.              | This metric balances sentiment with public engagement, allowing for a nuanced view of which candidates are viewed positively with high engagement. A higher score generally suggests favorable and engaging content. |


## Analysis of Results
Here’s a visual representation of the sentiment analysis results:

1. Average Exponential Sentiment by Candidate:
    * Kamala Harris has a positive average sentiment score, suggesting a generally favorable or supportive tone in the Reddit posts related to her.
    * In contrast, Donald Trump shows a negative average sentiment score, indicating a predominantly unfavorable or critical tone in posts mentioning him.
  
    ![Sentiment Analysis Result](images/avg_sentiment.png)

2. Sentiment Counts by Candidate:
    * Both candidates have a higher proportion of negative posts, but Trump has a significantly larger number of negative posts than positive ones.
    * Kamala Harris has a relatively more balanced distribution, with a greater share of positive posts compared to Trump.
    * This distribution implies that while both candidates face criticism, Trump receives a noticeably higher level of negative sentiment.
  
    ![Sentiment Count](images/count.png)

3. Density Plot of Exponential Sentiment by Candidate:
    * Kamala’s curve skews slightly toward the positive side, while Trump’s curve is more shifted toward the negative.
    * The overlap in the center suggests that there is some mixed sentiment for both candidates; however, the peaks indicate that Kamala tends to receive more positive posts, while Trump generally receives more negative posts.

    ![Sentiment Count](images/Density_plot.png)

4. Sentiment Distribution for Kamala Harris (Pie Chart):
    * Approximately 68.4% of the posts about her are negative, while 31.6% are positive.
    * Although she has more negative posts, the relatively high percentage of positive posts (compared to Trump) suggests a more balanced sentiment landscape for her.
  
    ![Piechart - Kamala Harris](images/piechart_kamala.png)

5. Sentiment Distribution for Donald Trump (Pie Chart):
    * About 87.5% of the posts about Trump are negative, with only 12.5% being positive.
    * This distribution indicates a highly critical sentiment toward Trump, with a very small proportion of supportive or favorable posts.
  
    ![Piechart - Trump](images/piechart_trump.png)

## Future Improvements
* Incorporate Additional Social Media Platforms

  Expanding the analysis beyond Reddit to include other platforms like Twitter, Facebook, or YouTube could provide a more comprehensive view of public sentiment on the election. This would allow us to validate results and spot trends across different social media audiences.

* Use Advanced Sentiment Analysis Techniques

  Currently, the project uses basic sentiment analysis with NLTK. Integrating more advanced natural language processing models like BERT, RoBERTa, or other transformer-based models could improve the accuracy of sentiment classification, especially for nuanced election-related discussions.

* Predictive Modeling with Machine Learning

  Implementing machine learning algorithms to identify correlations between sentiment, engagement metrics, and candidate support could improve the reliability of predictions. This could include training models to weigh sentiment and engagement factors to produce a forecast of candidate popularity or election outcomes.
