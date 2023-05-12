# EDA-Capstone-Project-on-Play-Store-App-Review-Analysis
### 📋 **Abstract**


 A few thousands of new applications are  uploaded on Google play store on regular basis. A large number of designers working freely on designing the apps and making them successful. It is important for a developer should be aware of the correct path for designing a sucessful app. Since the majority of Play Store apps are free, it is quite difficult to understand how in-app purchases, in-app advertisements, and memberships contribute to an app's success. In this way, rather of focusing on the amount of revenue generated, an application's success is typically determined by the number of installations it has received and the customer reviews it has received over time. The goal of this experiment is to provide information that will help engineers better understand client wants and, in turn, aid in the product's widespread adoption. We have made an effort to understand the connections between many characteristics, such as whether an application is free or paid, what kind of user feedback it has, and how well it is rated.


### 💾 **Project Files Description**

This Project includes 1 colab notebook, 1 technical documentation as well as 1 presentation:

**Input Files:**

**Play Store Data.csv** - It contains the basic details of the app like number of user reviews, ratings, etc.

**User Reviews.csv** - It contains the user reviews and its sentiment score for the respective app.
Data Source:

**Dataset** - Dataset taken from Almabetter

**Output:**
**Google Colab** - All the outputs are visible in the provided colab notebook.

📖 **Introduction:**
In the current environment, it is clear that mobile apps play a significant part in every person's life. A designer needs to be aware of whether they are moving in the right direction or not in the face of immense challenge from all around the world. The application designers may need to find out a way to maintain their current position in order to maintain this money and their position in the market. The dataset containing 10k  apps is accessible to study the android market. It can be looked at to analyse several categories, including family, communication, entertainment, tools, music, and cameras, among others. In this project, we look at the many data set characteristics that influence how well-liked an application is. We focused on to answer the questions like, what makes an app popular, what should be the price and size of the app, is there some trends in user sentiments.  The dataset has two CSV files for data analysis: Play Store Data User Reviews First, let's analyze the Play Store data. The Play Store data has 10841 rows and 13 columns.

**Dataset Information**

### **Play Store Data**

play store dataframe has 10841 rows and 13 columns. The 13 columns are identified as below:



*   **App** - It tells us about the name of the application.
*   **Category** - It gives the category to the app,like educational,sports,games etc.

*   **Rating** - It contains the average rating of the respective app received from its users.
*   **Reviews** - It shows us about the total number of users who have given a review for the application.

*   **Size** - It tells us about the size being occupied by the application on the mobile phone.

*  **Installs** - It tells us about the total number of installs/downloads for the application.
*   **Type** - It states whether an app is free to use or paid.

*  **Price** - It states the price payable to install the app. For free type apps, the price is zero.

*  **Content Rating** - It states whether or not an app is suitable for all age groups or not.

*   **Genres** - It tells us about the various other categories to which an application can belong.
*  **Last Updated** - It tells us about the when the application was updated.

*  **Current Ver** - It tells us about the current version of the application.

*  **Android Ver** - It tells us about the android version which can support the application on its platform.


### User Review dataset
user_reviews dataframe has 64295 rows and 5 columns. The 5 columns are identified as follows:

* **App:** Contains the name of the app with a short description (optional).
* **Translated_Review:** It contains the English translation of the review dropped by the user of the app.
* **Sentiment:** It gives the attitude/emotion of the writer. It can be ‘Positive’, ‘Negative’, or ‘Neutral’.
* **Sentiment_Polarity:** It gives the polarity of the review. Its range is [-1,1], where 1 means ‘Positive statement’ and -1 means a ‘Negative statement’.
* **Sentiment_Subjectivity:** This value gives how close a reviewers opinion is to the opinion of the general public. Its range is [0,1]. Higher the subjectivity, closer is the reviewers opinion to the opinion of the general public, and lower subjectivity indicates the review is more of a factual information.

### 📋 **Objectives**

Google Playstore is one of the top most apps market in the world and it is quite popular among millions of people.As apps store market is growing the demand of the developer is also growing. The playstore allows user to install different kinds apps as per  their interests and have access rate and  comment on the apps as per their experiences which called review.

To make a successful and engazing app developers should have knoledge of the users choices and prefernce of the featuers like apps size,it's price,android version,when it has last updated etc. 

Before developing the apps developers should have also knoledge of users sentiment of the others apps which have similar features with the future app.

Two datasets are provided to the anlysis of users choice and sentiment,one is the with  basic information of the apps and other one is about users review and sentiment of particular apps.Both datasets are need to examine in order to identify the important feauters that influence app engazement and success.

### 📔 **What is Exploratory Data Analysis?**
Exploratory data analysis (EDA) is used by data scientists to analyze and investigate data sets for patterns, and anomalies (outliers), and form hypotheses based on our understanding of the dataset and summarize their main characteristics, often employing data visualization methods. It is an important step in any Data Analysis or Data Science project. It helps determine how best to manipulate data sources to get the answers you need.

EDA involves generating summary statistics for numerical data in the dataset and creating various graphical representations to understand the data better and make it more attractive and appealing.

The following are the various steps involved in the EDA process:

Problem Statement - We shall brainstorm and understand the given data set. We shall study the attributes present in it and try to do a philosophical analysis about their meaning and importance for this problem.

Hypothesis - Upon studying the attributes present in the data base, we shall develop some basic hypothesis on which we can work and play with the data to look for the varied results which we can get out of it.

Univariate Analysis - It is the simplest form of analyzing the data. In this we would initially pick up a single attribute and study it in and out. It doesn't deal with any sort of co-relation and it's major purpose is to describe. It takes data, summarizes that data and finds patterns in the data.

Bivariate Analysis - This analysis is related to cause and the relationship between the two attributes. We will try to understand the dependency of attributes on each other.

Multivariate Analysis - This is done when more than two variables have to be analyzed simultaneously.

Data Cleaning - We shall clean the dataset and handle the missing data, outliers and categorical variables.

Testing Hypothesis - We shall check if our data meets the assumptions required by most of the multivariate techniques.


### 📖 **Steps Involved**
After loading the dataset, we can start exploring. But before that, we need to check if the dataset is ready to perform multiple exploration operations. First, let's look at how the data is structured and organized.

**Data Cleaning**
Our dataset contains a large number of null values in the rating column, so we have dropped them. Some of the columns have a very few number of null values, so we replace the null values in these columns with the mode value of that particular column. Our data set also contain the duplicate rows for a single application. We also drop the duplicate rows because the rows contain the identical data. Also drop the rows, which have rating greater than 5.

**Data Transforming**
From the information of dataframe, we can see that all the columns except rating have the object data type but some of the columns like, reviews, size, installs and price have the numerical value. So, we have to transform them in proper data type and also remove the unwanted values from the numerical columns like ‘+’ and ‘,’ from installs and ‘$’ from price. In the size column we have some values in KB and some values in MB, so we transform all the values in MB.

**Exploratory Data Analysis**
After establishing a good sense of each feature, we proceeded with plotting a pairwise plot between all the quantitative variables to look for any evident patterns or relationships between the features. There is a high variance in the number of installs and in number of reviews. To overcome this problem, we take logarithmic values of installs and review columns before plotting.At first we have performed univariate analysis i.e analyse single feature itself and then find corelation of the features.

### 🛠 **Challenges Faced:***
Reading the dataset and comprehending the problem statement. Our major challenge was data cleaning.
* Handling the error, duplicate and NaN values in the dataset.
* 13.60% of reviews were NaN values, and even after merging both the dataframes, we could not infer much in order to fill them. Thus we had to drop them.
* User Reviews had 42% of NaN values, which could have been used for developing an understanding of the category wise sentiments, which would help us to fill 13.60% NaN values of the Reviews column.
* The merged data frame of both play store and user reviews, had only 816 common apps. This is just 10% of the cleaned data, we could have given more valuable analysis, if we had atleast 70% - 80% of the data available in the merged dataframes.

### 📋 **Conclusion:**

* Facebook is the most popular App in the playstore.

* Helix jumps is the most positive reviewd apps and angry birds classic is the most negative reviewd apps.

* When app has high positive and negative review the rating got high that means when it has updated it had overcome the negative subjectivity

* I am rich Premium is one of the highset paid app which have highest number of installation.

* around 3000 apps has not updated over few years,that means probably that number of are out of services

*  Paid apps are generally high rated than free apps in each category except parenting category.

* When the app size very high they are few numbered but installation number is high.


* The major challange of this project was data cleaning part. Around 15 percent data was missing from playstore data and  around 42 percent data missing from user reviews data.

* only 816 app has common between user review and playstore data. It is around 10 percent of the playstore app number.So data is in sufficient for analysis of merged data.

*   Current version, Last Update, Sentiment sujectivity should be analyzed for effect in rating and installation

*   The data journey of the app(installation,rating,review) over the year sholud have help to understand buisness more effectively. 

📚 References
* Geeksforgeeks
* W3schools
* Statology
* Analytics Vidya
* Towardsdatascience
* Python libraries documentation
* Stackoverflow

### 📜 **Feedback**
If you have any feedback, please reach out to us at sabitendumahapatra@gmail.com





