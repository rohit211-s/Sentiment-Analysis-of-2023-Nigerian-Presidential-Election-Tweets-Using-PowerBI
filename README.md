# Sentiment Analysis of 2023 Nigerian Presidential Election Tweets Using PowerBI
This project, titled "Public Sentiment Evaluation of Nigerian 2023 Presidential Election Tweets," leverages data analytics to explore public opinion regarding the candidates in the 2023 presidential election. Utilizing Twitter data, the study systematically captures and assesses the sentiment expressed toward each of the three primary presidential contenders in the aftermath of the election. The report offers a detailed perspective on post-election sentiments, providing valuable insights into the political atmosphere and public sentiment dynamics in Nigeria.

## About the Dataset

The dataset supporting this analysis was obtained from Kaggle, a leading data science and analytics platform, and serves as the backbone for the sentiment analysis of the 2023 Nigerian Presidential Election Tweets. The dataset facilitates a deep dive into public opinion surrounding the candidates and their election journey.

[Dataset Link](https://www.kaggle.com/datasets/gpreda/nigerian-presidential-election-2023-tweets)

### Key Columns in the Dataset

The dataset comprises several essential columns, each adding valuable information for a robust sentiment analysis on the 2023 Nigeria Presidential Election. These include:

1. **ID**: Unique identifier for each tweet.
2. **User Name**: The username associated with the tweet.
3. **User Location**: Location details provided by the user.
4. **User Description**: A brief description provided by the user.
5. **User Created**: The date when the user's account was created.
6. **User Followers**: Number of followers the user has.
7. **User Friends**: Number of friends or accounts the user follows.
8. **User Favorites**: Number of tweets the user has marked as favorites.
9. **User Verified**: Indicates whether the user's account is verified.
10. **Date**: The date and time when the tweet was posted.
11. **Text**: The content of the tweet itself.
12. **Hashtags**: Any hashtags included in the tweet.
13. **Source**: The source from which the tweet was posted (e.g., device or application).
14. **Retweets**: Number of times the tweet has been retweeted.
15. **Is Retweet**: A binary indicator of whether the tweet is a retweet or an original post.

Stored in CSV format, this dataset provides a comprehensive basis for analyzing the public’s sentiments on Twitter concerning the 2023 Nigerian presidential election. These columns are instrumental in extracting public sentiment insights and observing election-related public reactions.


## DATA CLEANING
### The Power Query Transformation Process:

The transformation process commenced within Power Query Editor, a robust tool within Microsoft Power BI. This environment provided an avenue to meticulously refine the dataset and mold it into a coherent structure for sentiment analysis. The following key steps were undertaken:   
**Data Source**

![Data Source](https://github.com/rohit211-s/Sentiment-Analysis-of-2023-Nigerian-Presidential-Election-Tweets-Using-PowerBI/blob/main/Picture/SOURCE.png)
**Promoting Headers**   
 A key step in the data cleaning process was the utilization of Power Query's built-in functionality to promote headers. By analyzing the first row of data, the Power Query Editor accurately identified column names, ensuring precision in subsequent transformations.
 
 ![Promoting Headers](https://github.com/rohit211-s/Sentiment-Analysis-of-2023-Nigerian-Presidential-Election-Tweets-Using-PowerBI/blob/main/Picture/SOURCE.png)
 In the course of dataset refinement, certain columns including "Date," "Content," "Location," and "Platform" were deliberately excluded from the dataset. This curation was undertaken to streamline the focus of the analysis and optimize the dataset for sentiment assessment and subsequent insights extraction.

 **Creating the Sentiment Score**   
 The dataset underwent a meticulous cleansing process through the utilization of the built-in "Clean" function applied to the  "Custom column", rendering the data primed for analysis. Subsequent to this preparation, the Text Analytics function from Azure Cognitive Service was harnessed to generate sentiment scores for each entry within the customized "Text" column. This approach facilitated the quantification of sentiment nuances, culminating in a comprehensive evaluation of the dataset's emotional undercurrents.
 ![Sentiment Score](https://github.com/rohit211-s/Sentiment-Analysis-of-2023-Nigerian-Presidential-Election-Tweets-Using-PowerBI/blob/main/Picture/score_sentiment.png)

 After calculating the sentiment scores using the Text Analytics tool, we organized the scores into clear categories using a conditional column. Sentiment scores above 0.5 were labeled as 'Positive', scores of 0.5 were marked as 'Neutral', and scores below 0.5 were categorized as 'Negative'. This straightforward approach added meaningful labels to the sentiment data, making it easier to grasp the emotional context behind each entry.
![conditional_column](https://github.com/rohit211-s/Sentiment-Analysis-of-2023-Nigerian-Presidential-Election-Tweets-Using-PowerBI/blob/main/Picture/conditional_sentiments.png)

![sentiment Column](https://github.com/rohit211-s/Sentiment-Analysis-of-2023-Nigerian-Presidential-Election-Tweets-Using-PowerBI/blob/main/Picture/sentiment_column_table.png)

**Key Phrase Extraction**   
AI capabilities were utilized to extract key phrases from the text column, unveiling significant phrases within the tweets.

![step 1](https://github.com/rohit211-s/Sentiment-Analysis-of-2023-Nigerian-Presidential-Election-Tweets-Using-PowerBI/blob/main/Picture/extract_key_phrase_step.png)

![Step 2](https://github.com/rohit211-s/Sentiment-Analysis-of-2023-Nigerian-Presidential-Election-Tweets-Using-PowerBI/blob/main/Picture/extract_key_phrase.png)

## Data Analysis and Visualization
![sentiment reach](https://github.com/rohit211-s/Sentiment-Analysis-of-2023-Nigerian-Presidential-Election-Tweets-Using-PowerBI/blob/main/Picture/sentiment_by_reach.png)

This report presents a thorough sentiment analysis of tweets originating from Nigerian users on the subject of the election. Upon meticulous examination, the dataset encompassed a total of 48,239 tweets. Delving into the sentiment distribution, it was revealed that Negative sentiments prevailed, constituting the highest count at 17,622. Following closely, Neutral sentiments accounted for 16,686, while Positive sentiments were recorded at 13,935.

The prominence of Negative sentiments, standing at 36.53% of the total sentiment count, bears particular significance. This insight offers valuable perspective into the prevailing sentiments expressed by Nigerian Twitter users concerning the election. This analysis not only sheds light on the emotional tones shaping the discourse but also provides a deeper understanding of the diverse viewpoints prevalent within the Twitter landscape surrounding this significant event. Such insights stand to enrich the comprehension of the public sentiment dynamics pertinent to the Nigerian election on the Twitter platform.

**Sentiment Score Trend**   
![Score Trend](https://github.com/rohit211-s/Sentiment-Analysis-of-2023-Nigerian-Presidential-Election-Tweets-Using-PowerBI/blob/main/Picture/sent_score_trend.png)

In the realm of tweets discussing the Nigerian election, the sentiment analysis reveals interesting insights. Among these tweets, those with a Positive sentiment score, indicating optimism or approval, stood out with the highest Sum of Score sentiment at 12,605.89. This was remarkably higher, by 812.87%, compared to tweets carrying a Negative sentiment, which registered the lowest Sum of Score sentiment at 1,380.90.

To put it simply, Positive tweets held the strongest sway, making up 56.45% of the overall sentiment analysis. This suggests that a significant portion of the tweeted opinions about the Nigerian election carried a positive tone, reflecting favorable views or hopeful perspectives. In contrast, tweets with Negative sentiment were fewer in number, hinting at a lower level of critical or unfavorable sentiments.

It's worth noting that Neutral tweets, with a Sum of Score sentiment at 8,343, presented a balanced stance, neither overly positive nor negative. This analysis provides a window into how people expressed their feelings and opinions about the Nigerian election on social media, with Positive sentiments leading the discourse.

**Key Phrase Analysis**
![Key Entities Bar](https://github.com/rohit211-s/Sentiment-Analysis-of-2023-Nigerian-Presidential-Election-Tweets-Using-PowerBI/blob/main/Picture/sent_entities.png)

The sentiment analysis of key phrases within Nigerian election-related tweets yields valuable insights. Among the sentiments, Positive emerged with the highest aggregate Sum of Score sentiment, totaling 12,605.89. This was closely trailed by Neutral with 8,343, and Negative with 1,380.90.

Further delving into the key phrases, the term "INEC" emerged as a noteworthy contributor, constituting 1.20% of the overall Sum of Score sentiment. This highlights the significance of this term in shaping sentiments within the discourse.

Additionally, when evaluating average Sum of Score sentiment, Positive sentiments exhibited the highest average at 1.40, followed by Neutral at 0.81, and Negative at 0.13. This nuanced analysis provides a comprehensive understanding of sentiment dynamics surrounding key phrases related to the Nigerian election, revealing the prevailing tones and emphasizing the impact of specific terms on sentiment expression.

**Word Cloud**
![Word Cloud](https://github.com/rohit211-s/Sentiment-Analysis-of-2023-Nigerian-Presidential-Election-Tweets-Using-PowerBI/blob/main/Picture/word_cloud.png)

The visual representation of a word cloud presents an augmented perspective on the key phrases that have surfaced within discussions surrounding the Nigerian election. This amalgamation of phrases serves to deepen our comprehension of the ongoing discourse, offering a more intricate insight.

Prominent among the array of phrases are "Election," "BVAS," "amp," "IREV," "God," and "president," each contributing a distinct facet to the broader sentiment landscape. Notably, the term "Election" stands as a pivotal centerpiece, mirroring its central significance within these discussions. Furthermore, phrases such as "BVAS" and "IREV" illuminate specific entities or concepts of relevance embedded within the election narrative.

The sentiment nuances find further resonance through the term "God," amplifying the emotional depth intertwined with the discourse. Additionally, the presence of "president" underscores the substantial weight accorded to leadership elements.

These interwoven key phrases serve as threads, intricately woven into the fabric of sentiment expression. Collectively, they offer an enlightening portrayal of the sentiments, themes, and focal points that converge to shape the ongoing conversations surrounding the Nigerian election. The word cloud thus presents a visually immersive gateway to delve into the multifaceted dimensions of sentiment and discourse.

## CONCLUSION

In conclusion, the sentiment analysis of Nigerian election-related tweets has yielded invaluable insights into the prevailing emotional currents within this digital discourse. The prominence of Negative sentiments, alongside the noteworthy presence of key phrases such as "INEC", "Election," "BVAS," "amp," "IREV," "God," and "president," collectively paints a multifaceted portrait of the sentiment landscape. The dominance of Positive sentiments in the Sum of Score sentiment, coupled with the nuanced sentiment breakdown and the exploration of sentiment trends, enriches our comprehension of public sentiment dynamics. This analysis underscores the diverse viewpoints, emotions, and thematic concentrations that converge to shape discussions around the Nigerian election on social media.

**Neutral Stance and Impartiality:** It is essential to emphasize that this analysis maintains an impartial stance, devoid of any political affiliation or propagandistic intent. The goal of this analysis is solely to offer an objective exploration of sentiment patterns and key themes surrounding the Nigerian election tweets. The absence of partisan influence underscores the analytical integrity of this study, ensuring its dedication to unbiased insights. This analysis is a neutral endeavor that seeks to contribute a factual and balanced perspective, devoid of any agenda, to the discourse surrounding the Nigerian election on Twitter.
### REPORT
![Cover Image](https://github.com/rohit211-s/Sentiment-Analysis-of-2023-Nigerian-Presidential-Election-Tweets-Using-PowerBI/blob/main/Picture/cover_image_sentim_pb.png)






