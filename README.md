# Leveraging Machine Learning and Text Analytics for Mental Health Classification in Reddit Posts


DATA SOURCE

https://www.kaggle.com/datasets/neelghoshal/reddit-mental-health-data

PROBLEM STATEMENT

This project aims to harness mental health-related posts on Reddit and develop a classifier that accurately assigns them into five categories: Stress, Depression, Bipolar Disorder, Personality Disorder, and Anxiety. This is particularly important because a growing number of individuals, especially younger populations, use online platforms to discuss and seek support for their mental health struggles. By analyzing the way people express their emotions and struggles through texts, this model aims to better understand the unique characteristics of each post and provide meaningful insights into mental health patterns.
Furthermore, this project has the potential to make a real difference in people’s lives. It can help mental health applications and online forums identify individuals who may need support and guide them to the right resources. Social media platforms can use it to promote safe and supportive online spaces, directing users to professional help when needed. Additionally, governments, universities, and healthcare providers can leverage these insights to create more targeted mental health awareness campaigns, ensuring that support reaches those who need it most.

METHODOLOGY

To develop an accurate classification model, we structured our approach into three key phases:
1. Data Collection & Preprocessing:
- Used a Kaggle dataset containing Reddit discussions from mental health-related subreddits. 
- Cleaned the text by removing stopwords, special characters, and redundant elements through lemmatization. 
2. Exploratory Analysis:
- Compared between two text processing techniques Bag of Words (BOW) and TF-IDF and identified TF-IDF better at capturing meaningful words. 
- Latent Dirichlet Allocation (LDA) was used to identify recurring topics within each mental health category.
- Sentiment Analysis was applied using VADER technique to evaluate whether posts promote positive, negative, or neutral emotions.
3. Feature Engineering & Model Selection:
- Utilized LDA, TF-IDF vectorization, and BERT embeddings to extract meaningful textual features.
- Four machine learning models were tested: Naïve Bayes, Support Vector Machines (SVM), Random Forest, and KNN, followed by hyperparameter tuning with Grid Search to optimize performance.
4. Evaluation: Accuracy, Precision, Recall, and F1-score were used to ensure balanced classification performance. 
5. Validation & Suicide Risk Analysis: Research suggests that depression and bipolar disorder are more associated with suicidal ideation and attempts than anxiety, stress, and personal disorder. To validate our model, we utilized an external dataset that classified 500 Reddit posts based on suicidality. This dataset includes anonymized posts labeled using the Columbia Suicide Severity Rating Scale (C-SSRS). Our aim was to determine whether our model could accurately classify most suicide-related posts as being associated with bipolar disorder or depression rather than stress, anxiety, or personal disorder.
  
RESULTS DISCUSSION 

The Support Vector Machine (SVM) model achieved an overall accuracy of 79%, with recall rates above 75% across all categories: Stress (76%), Depression (77%), Bipolar Disorder (79%), Personality Disorder (82%), and Anxiety (80%), showing its effectiveness in mental health classification.

After applying our model to the external suicidality dataset, it classified 224 out of 500 posts as depression and 114 as bipolar disorder. These were the most frequently predicted categories, aligning with existing research on the prevalence of these conditions in suicidal posts and reinforcing the reliability of our model’s classification. These findings demonstrate the potential of machine learning driven mental health tools in early detection and intervention.

SOCIETAL IMPACT

This model can be a valuable tool for public and private sector initiatives focused on mental health intervention.
- Government agencies, crisis helplines, and nonprofits can use it to prioritize intervention efforts, particularly for individuals discussing depression and bipolar disorder online.
- Social media platforms like Reddit could integrate the model to flag high-risk posts and direct users to hotlines, therapy options, or crisis support services.
- Universities and student wellness centers could implement this model to monitor mental health trends among students. For example, at McGill University, the Student Wellness Hub could integrate the model into an AI-powered chatbot to provide students with:
- Personalized self-help resources 
  - Direct access to mental health professionals when necessary
  - Crisis intervention support for high-risk case

### Refer to Notebook for more details. 
