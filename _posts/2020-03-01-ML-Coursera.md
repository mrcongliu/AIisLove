# Machine Learning



## 1. Introduction

**What is ML?**

Machine learning is the science of getting computers to learn, without being explicitly programmed.

**Why is ML so prevalent?**

- Grew out of work in AI
- New capability for computers

**Examples**: 

- Database mining

  ​	Large datasets from growth of automation/web.

  ​	E.g., Web click data, medical records, biology, engineering

- Applications can't program by hand

  ​	E.g., Autonomous helicopter, handwriting recognition, most of Natural Language Processing(NLP), Computer Vision.

- Self-customizing programs

  ​	E.g., Amazon, Netflix product recommendations

- Understanding human learning (brain, real AI).



### 1.1 What is Machine Learning?

#### 1.1.1 Definition

~ by **Arthur Samuel** (1959):  (An older, informal definition)

Machine Learning is the field of study that gives computers the ability to learn without being explicitly programmed. 

~ by **Tom Mitchell** (1998): (A more modern definition)

Well-posed Learning Problem is defined as follows: A computer program is said to learn from experience E with respect to some task T and some performance measure P, if its performance on T, as measured by P, improves with experience E.

E.g., Suppose your email program watches which emails you do or do not mark as spam, and based on that learns how to better filter spam. In this setting, the T, E, P are shown as follows:

- T: Classifying emails as spam or not spam.

- E: Watching you label emails as spam or not spam.

- P: The number (or fraction) of emails correctly classified as spam/not spam.

#### 1.1.2 Machine Learning algorithms

In general, any machine learning problem can be assigned to one of two broad classifications:

- Supervised learning
- Unsupervised learning

Others: Reinforcement learning, recommender systems.

#### 1.1.3 Practical advice for applying learning algorithms



### 1.2 Supervised Learning

If a data set comes with the correct output and we know the input and the output are somehow related, then we should use supervised learning.

Supervised learning problems are categorized into **regression** and **classification** problems. In a regression problem, we are trying to predict results within a continuous output, meaning that we are trying to map input variables to some continuous function. In a classification problem, we are trying to predict results in a distance output, meaning that we are trying to map input variables into discrete (*离散*) categories.

**Example 1**

Say you have collected a data of the size of houses  on real estate market and you want to predict their price. In this case, **house price is a function of size** and it is a continuous output. Therefore, this is a **regression problem**.

**Example 2**

Given a patient with a tumor, we have to predict whether the tumor is malignant or benign. This is a **classification problem**.



### 1.3 Unsupervised Learning

Unsupervised Learning allows us to approach problems with little or no idea what our results should look like. We can derive structure from data where we don't necessarily know the effect of the variables.

We can derive this structure by clustering the data based on relationships among the variables in the data.

With unsupervised learning there is no feedback based on the prediction results.

**Example**

Clustering: Take a collection of 1,000,000 different genes, and find a way to automatically group these genes into groups that are somehow similar or related by different variables, such as lifespan, location, roles and so on.

Non-clustering: The "Cocktail Party Algorithm", allows you to find structure in a chaotic environment. (i.e. identifying individual voices and music from a mesh of sounds at a cocktail party).



## 2. Model & Cost Function

### 2.1 What is Model?

To establish notation for future use, we'll use $x^{(i)}$ to denote the "input" variables (living area in this example), also called input features, and $y^







































