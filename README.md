# 👪 Users clustering and Topic modelling

![image](https://github.com/DooPhiLong/Users-clustering-and-Topic-modelling/assets/120476961/ebd426c9-4e0b-4ef4-bcdc-7ed210516f5c)


## 💼 Case study 

### Requirement
Recently, the number of text documents on the Internet has increased significantly and rapidly. The rapid development of mobile devices and Internet technology has encouraged users to search for information, communicate with friends and share their opinions and interests on social media such as Twitter. , Instagram, Facebook. The documents generated every day on social networks are huge and unstructured data. Short texts often lack context, which makes finding information in them difficult.

However, if we can intelligently mine and analyze these texts, they can provide valuable information about users' preferences and interests. This can help businesses gain a deeper understanding of their target audience and thereby optimize their business strategy for maximum benefits. In this work, I study the problem of how to cluster users according to their interests and make product recommendations, or create common development communities for each group based on the short documents they share. share on social networks. The results of this work can reveal valuable information for decision-making in future business activities of enterprises.

### Application
- Products recommendation .
- Building user communities.
- Understanding customer needs.
- etc..

## 📌 Crawl posts data from Facebook
I have crawled post data from the Facebook website using python with 2 libraries Request and BeautifulSoup.
  
716,649 posts from 302 famous personalities on social networking platforms. This research object represents a wide range of online communities, from people who love football, music, food to business issues, politics, ...

10 samples compiled of post by users: 

![image](https://github.com/DooPhiLong/Users-clustering-and-Topic-modelling/assets/120476961/eab8661e-e699-4334-a4f1-94d991209eb9)


## 📌 Performs user clustering and topic modeling

![image](https://github.com/DooPhiLong/Users-clustering-and-Topic-modelling/assets/120476961/4fe73242-05fa-43fa-8cd9-e5bdff5031b6)


1. Data cleaning

The data cleaning process is the first important step I take to prepare data for analysis. Data cleaning includes a series of steps such as removing duplicate data, handling missing values, standardizing data formatting, checking and correcting outliers, and cleaning data from characters. unwanted or special characters.

![image](https://github.com/DooPhiLong/Users-clustering-and-Topic-modelling/assets/120476961/b370e525-6b35-4660-ba45-f7a33fe40f7a)

2. Vecotr (word) embedding

The next important step is to convert the list of articles into Vector embeddings. This means I need to encode the semantic and syntactic information of each word or sentence in a vector space. Vector embedding is the numerical representation of each text object in a multidimensional vector space, where each dimension can represent a specific attribute of a word or sentence.

![image](https://github.com/DooPhiLong/Users-clustering-and-Topic-modelling/assets/120476961/ff377777-60c2-4365-a8de-cffdf79f547d)

In this study, I applied the Transfer learning method to inherit and reuse machine learning models in the field of natural language processing, specifically the three pre-trained models [E5-base](https://huggingface.co/intfloat/e5-base-v2), [E5-small](https://huggingface.co/intfloat/e5-small-v2), [E5-large](https://huggingface.co/intfloat/e5-large-v2) from Sentence transformers package.

3. Dimensionality reduction

After performing Vector embedding, we obtained very high-dimensional data, which made it difficult to perform clustering and visualization. To solve this problem, I will apply data dimensionality reduction methods, called Dimensionality reduction. I used Umap dimensionality reduction methods for this project because it usually worked well in clustering tasks.

4. Users clustering

User clustering is an important technique in data analysis that groups users into groups with similar characteristics or behaviors.
In processing text data from user posts on the social network Facebook, we often face a number of challenges, especially when there are no available labels to guide the model training process ( unsupervised data). In such a situation, using unsupervised clustering methods to group users is a suitable choice. We choose to apply the K-means unsupervised clustering method to perform user clustering.

5. Topic modeling

In the User Clustering section, we used the K-means method to group users based on posts on the social network Facebook. In this way, we created groups of users with similar characteristics and interests. Next, we analyzed the posts of users in the same cluster to identify the main topics that each user group is interested in using [LDA](https://www.geeksforgeeks.org/topic-modeling-using-latent-dirichlet-allocation-lda/) topic modeling, a non-invasive machine learning technique. Supervision helps analyze and identify themes in text data. In this way, we can better understand the content and preferences of each user group, thereby adjusting our engagement strategy and providing content more appropriately and effectively, based on specific characteristics. entity of each user group.

### Source code
[Click here](https://github.com/DooPhiLong/Users-clustering-and-Topic-modelling/blob/main/User%20clustering.ipynb)

## 📌 Product recommendation application

After grouping users into 7 clusters, and knowing the topics of interest of each user cluster, I proposed a few illustrative products corresponding to the topic of each cluster.

![image](https://github.com/DooPhiLong/Users-clustering-and-Topic-modelling/assets/120476961/f600b7cd-3867-4702-b5ab-a48bb46f12a2)

![image](https://github.com/DooPhiLong/Users-clustering-and-Topic-modelling/assets/120476961/7607c764-eb6a-4a47-989f-aa02f70d4d62)

![image](https://github.com/DooPhiLong/Users-clustering-and-Topic-modelling/assets/120476961/be86145e-b3b7-461e-871a-291ecd848988)

## 🔖 The project's goals have been achieved
- Analyze users' social media behavior and identify user clusters based on interest, activity, and interaction patterns on social media platforms.
- Identify common and different characteristics between user groups, including interests, needs, and desires when interacting on social networks.
- Propose strategies and approaches to reach specific user groups to optimize business performance and social media interactions, by promoting products and services that match needs and interests of each user group, building user communities with common interests to develop and promote product brands.
- Evaluate and recommend technological means and support tools to effectively collect and analyze data from social networks, to optimize the process of clustering users and applications in the enterprise.





