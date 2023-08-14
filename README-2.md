# STA380-Part-II
​
## Team
1. Karthick Vel
2. Manideep Telukuntla
3. Jahnavi Angati
4. Aneerudh Ravishankar
​
## Table of contents
1. [Introduction](#1-introduction)
2. [Questions](#2-questions)
3. [Overview](#3-overview)
4. [Data](#4-data)
​
## 1. Introduction 
In our "Introduction to Machine Learning" assignment, we have undertaken a comprehensive examination of the fundamental aspects of ML. This exploration spans the foundational principles of probability, advanced data wrangling techniques, the art of visual storytelling, methodologies in clustering and topic modeling, and the intricacies of neural networks. We invite you to delve into our repository for a detailed analysis and insights.
​
## 2. Questions
- Q1. Probability practice
- Q2. Wrangling the Billboard Top 100
- Q3. Visual story telling part 1: green buildings
- Q4. Visual story telling part 2: Capital Metro data
- Q5. Clustering and dimensionality reduction
- Q6. Market segmentation
- Q7. The Reuters Corpus
- Q8. Association rule mining
- Q9. Image classification with neural networks
​
## 3. Overview
### [Probability practice](https://github.com/kkarthick12/STA380-Part-II/blob/main/Q1-Probability.ipynb)
​
**Description:** 
- For our analysis, we employed the Rule of Total Probability to deduce the fraction of truthful clickers responding "yes" in a website survey scenario (Part A). Subsequently, we harnessed Bayes' Theorem to assess the likelihood of a disease presence given a positive test result, considering both the test's sensitivity and the disease's prevalence (Part B).
​
**Conclusions/Results:**
* The fraction of people who are truthful clickers answered yes is 71.43%
* The probability of someone having disease given that they tested positive is 19.89%
​
### [Wrangling the Billboard Top 100](https://github.com/kkarthick12/STA380-Part-II/blob/main/Q2-Data-Wrangling.md)
​
**Description**

The analysis involved wrangling and visualizing data from the Billboard Top 100 chart, encompassing every song since 1958 up to mid-2021. Three key aspects were explored:

    Identifying the top 10 most popular songs based on their presence on the chart.
    Analyzing the musical diversity over time by the number of unique songs each year.
    Finding 19 artists who have had at least 30 songs that were "ten-week hits."

**Results**

    Top 10 Popular Songs: Songs like "Radioactive" by Imagine Dragons and "Blinding Lights" by The Weeknd were identified among the top 10, with counts reflecting the number of weeks on the chart.
    Musical Diversity: A line graph revealed a peak in diversity in 1966, a decline until 2001, and a subsequent increase, portraying the variation in unique songs over time.
    Artists with Ten-Week Hits: A bar plot highlighted artists like Elton John and Madonna who have had significant ten-week hits, with Elton John leading the list.
    
### [Visual story telling part 1: green buildings](https://github.com/kkarthick12/STA380-Part-II/blob/main/Q3-Visual-Story-Telling-Green-Buildings.md)
​
**Description**

The analysis examines the economic impact of investing in green buildings in the commercial real estate sector in the United States. Using data from 7,894 commercial properties, including 685 green-certified buildings, the study aims to understand if investing in a green building would be financially beneficial for a specific real estate developer's project in Austin.

**Results**

The initial analysis suggested that green buildings would yield additional revenue and pay off in 7.7 years. However, a more detailed analysis, considering factors such as renovation, class of building quality, number of stories, and size of the floor, revealed that green buildings might actually be cheaper in rent by $3.5 per square foot compared to similar non-green buildings.

**Conclusion**

The comprehensive analysis challenged the initial recommendation to invest in green buildings. It concluded that the specific investment in a green building for the developer's project might not be economically advantageous. The study emphasizes the importance of considering various factors in decision-making and shows that the financial benefits of green buildings may not be as straightforward as initially believed.

### [Visual story telling part 2: Capital Metro data](https://github.com/kkarthick12/STA380-Part-II/blob/main/Q4-Visual-Story-Telling-Part-II-Capital-Metro-Data.md)
​
**Description**

The analysis investigates ridership patterns in Austin's Capital Metro bus network around the UT-Austin campus, focusing on variables like peak hours, weekdays vs. weekends, temperature effects, seasonal changes, and correlations between boarding and alighting.

**Results**

    Peak Hours: Boarding occurs mainly between 1500-1700, and alighting between 0800-0900 hours.
    Weekday vs. Weekend: Lower boarding and alighting during weekends.
    Temperature Effects: Peak ridership at 30-35°C, with trends corresponding to temperature changes.
    Seasonal Changes: An increase in boarding in October, possibly due to Halloween.
    Correlations: Different correlations between boarding and alighting were observed hourly, weekly, and monthly, reflecting various travel behaviors.

**Conclusion**

The study uncovers intricate patterns of bus ridership around UT-Austin, revealing insights into commuting habits, temperature preferences, and seasonal effects. The findings may contribute to optimizing transportation services in alignment with these observed trends, emphasizing the complexity of factors that influence urban transit usage.

### [Clustering and dimensionality reduction](https://github.com/kkarthick12/STA380-Part-II/blob/main/Q5-Clustering-and-dimensionality-reduction.md)
​
**Description**

The analysis applied Principal Component Analysis (PCA), t-Distributed Stochastic Neighbor Embedding (t-SNE), and K-Means Clustering on a dataset of 6500 vinho verde wines from northern Portugal to investigate if the chemical properties could distinguish between red/white wines and classify wines based on quality.

**Results**

    Red/White Differentiation:
        PCA achieved 98.16% accuracy.
        t-SNE achieved 86.14% accuracy.
    Quality Differentiation:
        PCA failed to effectively cluster wines based on quality.

**Conclusion**

PCA was the preferred technique, successfully distinguishing red from white wines but not effectively clustering wines by quality. The results highlight the ability to classify wines by color using chemical properties but reveal the complexity in predicting wine quality.

### [Market segmentation](https://github.com/kkarthick12/STA380-Part-II/blob/main/Q6-Market-Segmentation.md)
​
**Description**

The analysis of Twitter followers for a consumer brand, "NutrientH20," aimed to understand its audience and identify market segments. Using PCA, t-SNE, and K-Means clustering, seven distinct clusters were identified, representing different areas of interest.

**Results**

    Cluster 1: Social engagement (chatter, photos, travel).
    Cluster 2: Health-consciousness (nutrition, fitness).
    Cluster 3: College and gaming.
    Cluster 4: Home cooking and fashion.
    Cluster 5: Political activism.
    Cluster 6: Entertainment (TV, films).
    Cluster 7: Sports and religion.

**Conclusion**

The segmentation provides valuable insights for NutrientH20 to tailor its social media strategies, enhancing engagement with these specific market segments. By targeting these clusters, the brand can create more resonant and effective content.

### [The Reuters Corpus](https://github.com/kkarthick12/STA380-Part-II/blob/main/Q7-The%20Reuters%20Corpus.ipynb)
​
**Description:**
- For the Reuters C50 text corpus, we employed the LDA (Latent Dirichlet Allocation) model to perform topic modeling, identifying key themes across the corpus. Leveraging these discerned topics, we also designed a mini search engine that suggests authors based on user-input topics, enabling a targeted exploration of the dataset's content.
​
**Conclusions/Results:**
- Through LDA topic modeling, we discerned predominant themes in the Reuters C50 corpus, spanning U.S. business legalities, global financial trends, and geopolitical nuances, especially concerning China. This analysis paved the way for a tailored search system to connect users with authors specializing in their chosen topics.
​
### [Association rule mining](https://github.com/kkarthick12/STA380-Part-II/blob/main/Q8-Association-Rule-Mining.md)
​
**Description**

An analysis was conducted on a groceries dataset using Association Rule Mining and the Apriori algorithm to uncover patterns in buying behaviors.

**Results**

The analysis identified high-support items like bottled water and whole milk, specific interactions such as the strong association between alcoholic items, and moderately confident rules like the relationship between yogurt and whole milk.

**Conclusion**

The study provided insights into customer purchasing patterns, suggesting retail strategies like strategic placement of related items. It highlighted the value of Association Rule Mining in informing marketing and sales tactics, with a note of caution on high-lift rules based on fewer transactions.

### [Image classification with neural networks](https://github.com/kkarthick12/STA380-Part-II/blob/main/Q9%20-%20Image%20classification%20with%20neural%20networks.ipynb)
​
**Description**

The project involved building a neural network to classify satellite images into 11 land or land-use categories. Three different models were developed, including two custom CNN models and a ResNet-18 model.

**Results**

    Network 1: 80.93% Accuracy
    Network 2: 81.91% Accuracy
    ResNet-18: 88.78% Accuracy

The ResNet-18 model showed the highest accuracy but still faced challenges in distinguishing between certain similar categories.

**Conclusion**

The ResNet-18 model outperformed the custom models, achieving almost 89% accuracy. This success illustrates the benefits of using deep learning architectures like ResNet in image classification tasks. Future enhancements could focus on fine-tuning and additional data preprocessing to further improve accuracy.
## 4. Data
Created a seperate data directory to accommodate essential data files necessary for conducting the analysis.
