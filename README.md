# Recommendation System

## Problem Statement
### What does the topic cover?
A **recommendation system** is a subclass of information filtering system that seeks to predict the "rating" or "preference" a user would give to an item. [Wikipedia](https://en.wikipedia.org/wiki/Recommender_system)

### Why it is important?
Because it has been so deeply incorporated into our daily life, through digital devices and different platforms all over the Internet. On the Internet, where the information is too much, or the number of choices is overwhelming, the recommendation system comes to help us filter and optimize our choices based on our personal interests.

## Applications
### What are applications of the topic?
Recommendation systems are used in a variety of areas, with commonly recognized examples taking the form of playlist generators for video and music services, product recommenders for online stores, or content recommenders for social media platforms and open web content recommenders. [Wikipedia](https://en.wikipedia.org/wiki/Recommender_system)

### What is the societal significance of the research?

There are both positive and negative social impact of advanced recommendation system from my perspective.

On the one hand, recommendation system is making our life more convenient, with less information to look up before making decisions. On the other hand, recommendation system in media platforms is exploiting people's addiction to eye-catching content online, causing attention distraction and time waste.


## Area of focus

There are two areas of focus on recommendation system applications in my mind:

The first is online video platforms, e.g., Bilibili (similar to YouTube) because it is always recommending highly similar videos from my personal experience.

The second is product recommendations for online stores, e.g., Amazon.com to find out what else a buyer need after he bought something instead of urging him to buy similar things again.

## Literature Review

### Abstract

In this literature review on the Recommendation System, we introduce the background of the Recommendation System's presence, followed by different approaches to realize the Recommendation System, then to review on ways the Recommendation System is put into applications in different mainstream online platforms.

### Introduction

As the size of data increases exponentially nowadays, the huge amount of data cannot be managed efficiently by the common database management systems. The datasets in the form of semi-structured data and unstructured data like image, audio, video, JSON documents and search patterns etc. cannot be stored and handled by traditional databases, so the concept of Big Data came into the picture. The Big Data is described by 3 V's (Volume, Velocity and Variety). Volume is described as the quantity of information produced by individuals or organizations. Velocity is defined as the rate at which data is generated. Variety is represented as various sort of information extracted from various sources.[[1]](#1)

Due to the huge, dynamic and unstructured nature of web data, the Recommendation System have become one of the most convenient way to find relevant information within a short time.[[2]](#2) Recommender systems usually make use of either or both collaborative filtering and content-based filtering (also known as the personality-based approach). Collaborative filtering approaches build a model from a user's past behavior (items previously purchased or selected and/or numerical ratings given to those items) as well as similar decisions made by other users. This model is then used to predict items (or ratings for items) that the user may have an interest in. Content-based filtering approaches utilize a series of discrete, pre-tagged characteristics of an item in order to recommend additional items with similar properties. Current recommender systems typically combine one or more approaches into a hybrid system.[[3]](#3)

### Approaches

In this section we present three most common ways of building the Recommendation System, collaborative filtering, content-based filtering and hybrid recommendation system.

#### Collaborative filtering

Collaborative filtering is based on the assumption that people who agreed in the past will agree in the future, and that they will like similar kinds of items as they liked in the past. The system work by collecting user remark in the form of ratings for items in a given field and exploiting similarities in rating actions amongst several users in determining how to recommend an item. Collaborative filtering systems recommend an item to a user based on opinions of other users.[[4]](#4)

A key advantage of the collaborative filtering approach is that it does not rely on machine analyzable content and therefore it is capable of accurately recommending complex items such as movies without requiring an "understanding" of the item itself. Many algorithms have been used in measuring user similarity or item similarity in recommender systems.

However, collaborative filtering approaches often suffer from three problems: cold start, scalability, and sparsity.

- **Cold start**: For a new user or item, there isn't enough data to make accurate recommendations. 
- **Scalability**: In many of the environments in which these systems make recommendations, there are millions of users and products. Thus, a large amount of computation power is often necessary to calculate recommendations.
- **Sparsity**: The number of items sold on major e-commerce sites is extremely large. The most active users will only have rated a small subset of the overall database. Thus, even the most popular items have very few ratings.

#### Content-based filtering

Another common approach when designing recommender systems is content-based filtering. Content-based filtering methods are based on a description of the item and a profile of the user's preferences. These methods are best suited to situations where there is known data on an item (name, location, description, etc.), but not on the user. Content-based recommenders treat recommendation as a user-specific classification problem and learn a classifier for the user's likes and dislikes based on an item's features.

In this system, keywords are used to describe the items and a user profile is built to indicate the type of item this user likes. In other words, these algorithms try to recommend items that are similar to those that a user liked in the past, or is examining in the present. It does not rely on a user sign-in mechanism to generate this often temporary profile. In particular, various candidate items are compared with items previously rated by the user and the best-matching items are recommended.

A key issue with content-based filtering is whether the system is able to learn user preferences from users' actions regarding one content source and use them across other content types. When the system is limited to recommending content of the same type as the user is already using, the value from the recommendation system is significantly less than when other content types from other services can be recommended.

#### Hybrid Recommendation System

Traditional recommender system techniques such as collaborative filtering (CF), content-based, and knowledge-based filtering,  each have unique strengths and limitations. For example, CF suffers from cold start, scalability and sparsity problems, while content-based approaches suffer from narrowness and require descriptions. However, a hybrid approach can use one approach to make predictions where the other fails, resulting in a more robust recommender System.

### Applications

In this section we present Recommendation Systems' applications on different platforms: Amazon.com, Netflix and YouTube to explore their methods and find potential ways to improve them.

#### Amazon.com

Amazon.com launched item-based collaborative filtering in 1998, enabling recommendations at a previously unseen scale for millions of customers and a catalog of millions of items. Since the algorithm is published in IEEE Internet Computing in 2003, it has seen widespread use across the Web, including YouTube, Netflix, and many others.[[5]](#5) The algorithm has been updated and improved since then.

#### Netflix

There are typically about 40 rows on each Netflix homepage (depending on the capabilities of the device), and up to 75 videos per row; these numbers vary somewhat across devices because of hardware and user experience considerations. The videos in a given row typically come from a single algorithm. Genre rows  are driven by their personalized video ranker (PVR) algorithm. As its name suggests, this algorithm orders the entire catalog of videos (or subsets selected by genre or other filtering) for each member profile in a personalized way. The resulting ordering is used to select the order of the videos in genre and other rows, and is the reason why the same genre row shown to different members often has completely different videos.

They also have a Top N video ranker that produces the recommendations in the Top Picks row. The goal of this algorithm is to find the best few personalized recommendations in the entire catalog for each member, that is, focusing only on the head of the ranking, a freedom that PVR does not have because it gets used to rank arbitrary subsets of the catalog.

Each of the algorithms in their recommender system relies on statistical and machine learning techniques. This includes both supervised (classification, regression) and unsupervised approaches (dimensionality reduction through clustering or compression, e.g., through topic models).[[6]](#6)

#### YouTube

There are many aspects of the YouTube site that make recommending interesting and personally relevant videos to users a unique challenge: Videos as they are uploaded by users often have no or very poor metadata. The video corpus size is roughly on the same order of magnitude as the number of active users. Furthermore, videos on YouTube are mostly short form (under 10 minutes in length). User interactions are thus relatively short and noisy. Compare this to user interactions with movie rental or purchase sites such as Netflix or Amazon where renting a movie or purchasing an item are very clear declarations of intent. In addition, many of the interesting videos on YouTube have a short life cycle going from upload to viral in the order of days requiring constant freshness of recommendation.

The overall design of the YouTube recommendation system is guided by the goals and challenges outlined above: they want recommendations to be reasonably recent and fresh, as well as diverse and relevant to the user’s recent actions. In addition, it’s important that users understand why a video was recommended to them.

The set of recommended videos videos is generated by using a user’s personal activity (watched, favorited, liked videos) as seeds and expanding the set of videos by traversing a co-visitation based graph of videos. The set of videos is then ranked using a variety of signals for relevance and diversity.[[7]](#7)

### Conclusion

In this literature review we start with the needs to have the Recommendation System present for the new era of Big Data, then explain three main ways, collaborative filtering and content-based filtering or both, to build a recommendation system. Afterwards we investigate how recommendation systems are put into practice, firstly in Amazon.com where it is shown to the industry, then Netflix and YouTube have adapted this algorithm to meet their own user scenarios and development demands.

### References

<a id="1">[1]</a>. Das, Debashis, Laxman Sahoo, and Sujoy Datta. "A survey on recommendation system." *International Journal of Computer Applications* 160.7 (2017).

<a id="2">[2]</a>. Singhal, Ayush, Pradeep Sinha, and Rakesh Pant. "Use of deep learning in modern recommendation system: A summary of recent works." *arXiv preprint arXiv:1712.07525* (2017).

<a id='3'>[3]</a>. Recommender system. (2019, April). In *Wikipedia*. https://en.wikipedia.org/wiki/Recommender_system.

<a id="1">[4]</a>. Bhatt, Bhumika, J. Patel Premal, and Hetal Gaudani. "A Review Paper on Machine Learning Based Recommendation System 1." (2014).

<a id="5">[5]</a>. Smith, Brent, and Greg Linden. "Two decades of recommender systems at Amazon. com." *Ieee internet computing* 21.3 (2017): 12-18.

<a id="6">[6]</a>. Gomez-Uribe, Carlos A., and Neil Hunt. "The netflix recommender system: Algorithms, business value, and innovation." *ACM Transactions on Management Information Systems (TMIS)* 6.4 (2015): 1-19.

<a id="7">[7]</a>. Davidson, James, et al. "The YouTube video recommendation system." *Proceedings of the fourth ACM conference on Recommender systems*. 2010.

## Open Source Research

[microsoft/recommenders: Best Practices on Recommendation Systems](https://github.com/microsoft/recommenders)

## Duplicate the results

To be updated