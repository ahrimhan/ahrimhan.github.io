---
permalink: /dsmlproject/
title: "Data Science and Machine Learning"
author_profile: true
---

# Data Science and Machine Learning

I completed the bootcamp of the Springboard Data Science Career Track specialized in deep learning. Throughout the course for 11 months, I have mastered the skills in Python, SQL, data analysis, data visualization, hypothesis testing, and machine learning.

---
## Springboard Capstone Projects

I completed on the two in-depth capstone projects.

## **[Capstone Project 1: Prediction of Scores for Public Schools in California](https://github.com/ahrimhan/data-science-project/tree/master/project1)**

### Documention
1. [Final Report](https://github.com/ahrimhan/data-science-project/blob/master/project1/reports/capstone1_final_report.pdf)
2. [Presentation](https://github.com/ahrimhan/data-science-project/blob/master/project1/reports/capstone1_presentation.pdf)

### Jupyter Notebooks
1. [Data Wrangling](https://github.com/ahrimhan/data-science-project/blob/master/project1/data_wrangling.ipynb)
2. [Data Visualization](https://github.com/ahrimhan/data-science-project/blob/master/project1/data_visualization.ipynb)
3. [Exploratory Data Analysis](https://github.com/ahrimhan/data-science-project/blob/master/project1/exploratory_data_analysis.ipynb)
4. [Machine Learning](https://github.com/ahrimhan/data-science-project/blob/master/project1/machine_learning.ipynb)


**We have analyzed the California Assessment of Student Performance and Progress (CAASPP) score data (California Department of Education) and house prices (Zillow research data) to help predict and find the inferior groups of schools that indeed need help.**

In the data visualization and exploratory data analysis, we plotted the various kinds of graphs interactive stacked bars using Plotly library and gained the insights on exceeded scores and inferior scores regarding to gender, ethnicity, english-language fluency, economic status, disability status, and parent educations.
We also performed correlation analysis, univariate selection, and feature importance methods to find the strong indicators affecting lower scores.

In the modeling, we used the supervised machine learning  algorithms including the regression and classification to build predictive models.
The regression algorithm predicts the percentage of students who do not meet the standard.
The classification algorithm predicts if the schools "need help" (1) or "do not need help" (0).
We set the "need help" schools that has more than "80\% of the standard not met" students (312 out of 8,786 schools).
We tried various machine learning techniques to pick the one which performs best.
For regression, out of 5 different models, we obtained the best regression model using the random forest regressor with 10 folds cross validation
with the accuracy of RMSE 10.77, MAE 7.69, and R<sup>2</sup> 0.68.
For classification, we tried to solve the class imbalanced problems using the Stratified K-fold cross validation and the weighted evaluation metrics to reflect the mass of the classes. In addition, we scaled the training data and significantly improved the accuracy of the K-Nearest Neighbor algorithm.
As a result, we obtained the best classification model using the random forest classifier based on grid search cross validation with the accuracy 0.97 and AUC 0.98.

Based on these results, we identified the top and bottom schools and found the important features determining those schools.
We recommended some strategies
that effectively increase the achievements for scores.


## **[Capstone Project 2: Sentiment Analysis of Movie Reviews using a Deep Learning Convolutional Neural Network](https://github.com/ahrimhan/data-science-project/tree/master/project2)**


### Documention
1. [Final Report](https://github.com/ahrimhan/data-science-project/blob/master/project2/reports/capstone2_final_report.pdf)
2. [Presentation](https://github.com/ahrimhan/data-science-project/blob/master/project2/reports/capstone2_presentation.pdf)

### Jupyter Notebooks
1. [Vocabulary Dictionary](https://github.com/ahrimhan/data-science-project/blob/master/project2/vocab.ipynb)
2. [Cleaning Documents](https://github.com/ahrimhan/data-science-project/blob/master/project2/cleaning_document.ipynb)
3. [Building and Training Deep Learning Models](https://github.com/ahrimhan/data-science-project/blob/master/project2/deep_learning_CNN.ipynb)


**Problem Statment.** Sentiment analysis (or opinion mining) is the task of identifying and classifying
the sentiment expressed in a piece of text as being positive or negative. Given a bunch of text, sentiment
analysis classifies peoples opinions, appraisals, attitudes, and emotions toward products, issues,
and topics. The sentiment analysis has a wide range of applications in industry from forecasting market
movements based on sentiment expressed in news and blogs, identifying customer satisfaction and dissatisfaction
from their reviews and social media posts. It also forms the basis for other applications like recommender systems.

In recent years, there has been a remarkable performance improvement to Natural Language Processing
(NLP) problems by applying deep learning neural networks.
Therefore, in this project, **I build deep learning models using various parameters to classify the positive and negative movie reviews using the Convolutional Neural Nework.** I compare models and observe the parameters affecting the performance in accuracy.

**Expected Beneficiaries.** Automated and accurate sentiment analysis techniques can be used to detect
fake reviews, news, or blogs and are becoming more and more important due to the huge impact on the
business markets. We provide the potential beneficiaries of this work.

* Businesses can find consumer opinions and emotions about their products and services.
* E-commerce companies, such as Amazon and Yelp, can identify fake reviews. There are cases when the results are not consistent from the actual looks and the sentiment analysis (automated
analysis). For example, if majority reviews are positive, but the sentiment analysis determines
that reviews should not be positive. Then the administrators should inspect the reviews manually
if those are fake or not. Fake reviews are not only damaging both competing companies and
customers, but they also lead to reduced trust in e-commerce companies and lower sales.
* Potential customers also can know the opinions and emotions of existing users. Customers also
can use the system based on the sentiment analysis and check if the reviews are reliable and
trustable before they make the decisions on buying products or services.

**Approach.** We prepare the movie review text data for classification with deep learning methods. We
obtain the large data set of the movie reviews. We clean the documents of text reviews by
removing punctuations, stopwords, stemming and removing non-frequent words to prevent a model from
overfitting. In this pre-processing of documents, we use the more sophisticated methods in the NLTK
python package. To build a deep learning Convolutional Neural Network (CNN) model, we basically use the sequential
model of Keras.

1. First, the Embedding layer is located. There are two ways of setting the embedding layer: using the pre-trained word embedding or training new embedding from scratch. For a pre-trained word embedding, we use the GloVe (Global Vectors for Word Representation) embeddings.
2. Second, a series of convolution 1D Neural Network and pooling layers are added according to typical CNN for text analysis. Then, after flattening layer, fully connected Dense layers are added.
Since this is a binary classification problem, we use the Sigmoid function as an activation function for the final Dense layer. To prevent overfitting, we add Dropouts to deactivate neurons randomly, which forces the network to learn a more balanced representation.
3. Finally, we make the different deep learning models by adjusting the parameters and will find the best accurate model. We later will investigate the features affecting the accuracy.  

**Results.** In the paper, the performance of machine learning models are in range of 67.42% to 88.89%. The model performed best in the cross validated Support Vector Machine (SVM) when concatenated with bag of words representation. In this project, we generate the preliminary results, and the best accuracy of our deep learning models based on CNN is 90.14%.


---
## Springboard Courses

The list of working files contain results performed during the Springboard data science career track course.

### Data Wrangling
* [JSON based mini-project (Jupyter Notebook format)](https://github.com/ahrimhan/springboard-course/blob/master/data-wrangling/data_wrangling_json/sliderule_dsi_json_exercise.ipynb)
* [SQL case study](https://github.com/ahrimhan/springboard-course/blob/master/data-wrangling/SQL/1520094343_sql_project.sql)
* [API based mini-project](https://github.com/ahrimhan/springboard-course/blob/master/data-wrangling/API/api_data_wrangling_mini_project.ipynb)

### Exploratory Data Analysis - Inferential Statistics
* [Mini-project on human body temperature dataset](https://github.com/ahrimhan/springboard-course/blob/master/exploratory-data-analysis/EDA_human_temperature/sliderule_dsi_inferential_statistics_exercise_1.ipynb)
* [Mini-project on racial discrimination dataset](https://github.com/ahrimhan/springboard-course/blob/master/exploratory-data-analysis/EDA_racial_discrimination/EDA_racial_discrimination.ipynb)
* [Mini-project on hospital readmissions dataset](https://github.com/ahrimhan/springboard-course/blob/master/exploratory-data-analysis/EDA_hospital_readmit/sliderule_dsi_inferential_statistics_exercise_3.ipynb)

### Machine Learning
* [Linear Regression using Boston housing data set](https://github.com/ahrimhan/springboard-course/blob/master/machine-learning/linear_regression/Mini_Project_Linear_Regression.ipynb)
* [Heights and weights using Logistic Regression](https://github.com/ahrimhan/springboard-course/blob/master/machine-learning/logistic_regression/Mini_Project_Logistic_Regression.ipynb)
* [Predictive movie ratings from reviews using naive bayes](https://github.com/ahrimhan/springboard-course/blob/master/machine-learning/naive_bayes/Mini_Project_Naive_Bayes.ipynb)
* [Customer segmentation using clustering](https://github.com/ahrimhan/springboard-course/blob/master/machine-learning/clustering/Mini_Project_Clustering.ipynb)

### Spark
* [Spark Mini-Project: Databricks edition](https://github.com/ahrimhan/springboard-course/blob/master/spark_Databricks/Spark_DF_SQL_ML_Exercise.ipynb)

### Take-home Challenges
* [Relax Inc.: Important features identifying Adopted Users](https://github.com/ahrimhan/springboard-course/blob/master/take-home-challenge/relax_challenge/)
* [Ultimate Technologies Inc.](https://github.com/ahrimhan/springboard-course/blob/master/take-home-challenge/ultimate_challenge/)

### Job Findings
* [Experience in attending data science meetup](https://docs.google.com/document/d/1M00SeNrBVVslh6UT4vONdnGYAg8D-yP3nDtM7VJIdgM/edit?usp=sharing)

---

The tool, techniques, libraries used for completing courses and projects can be summarized as follows.

#### Data Wrangling and Exploratory Data Analysis
- Pandas library
- Numpy library
- Scipy library

#### Data Visualization
- Matplotlib library
- Pyplot library
- Seaborn library
- Plotly (interactive stacked bars)

#### Machine Learning
- Scikit-learn library

#### Communication
- Jupyter Notebook
- Markdown

#### IDE
- Visual Studio Code


#### Deep Learning and Natural Language Processing
- Keras, Tensorflow
- [`nltk`](http://www.nltk.org/)
- Word Embeddings ([GloVe](https://nlp.stanford.edu/projects/glove/))

#### Machine Learning Methods
- Regression (Linear Regression, Random Forest Regressor, Gradient Boosting Regressor)
- Classification (Logistic Regression, Decision Tree, Random Forest Classifier, and k-Nearest Neighbors Classifier)


<!--[`spaCy`](https://spacy.io/), [`pattern`](http://www.clips.ua.ac.be/pattern)-->
