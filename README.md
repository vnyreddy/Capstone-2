### Movie recommendation system

by Vinay Reddy Maligireddy

#### Executive summary
The business has an online streaming platform that wants to increase user engagement with the platform and retain user subscriptions. Since there are many streaming platforms in the market it is important for business growth. Also, within this streaming platform, there are thousands of content to choose from, and there is a high chance that users can miss likable content, On the other hand, the business also runs ads between videos and it is important to show more ads to get revenue.

The goal of the business is to create a recommendation system, that can recommend movies to the users that are most likely interested, and help users to find rind right content by recommending, also increasing business revenue.

#### Rationale
There are various factors and practical considerations that are motivating to research this question.

User Satisfaction:
The movie recommendation system aims to enhance user satisfaction by providing personalized and relevant recommendations. This research will help to improve the accuracy and effectiveness of those systems, leading to a better user experience.

Information Overload: 
There is a vast amount of movie collection, users often might not find the right content, a recommendation system helps users discover movies that suit their preferences, and saves time and effort in the selection process.

Business Impact:
In streaming platforms, effective recommendation systems can have a significant impact on user engagement, and retention, which brings more revenue to the business.

Personalization:
Users have diverse tastes, and one set of movie selections will not fit all, and it will not be effective. So research in movie recommendation systems focuses on developing personalized models that consider individual preferences.

#### Research Question
Can we accurately recommend movies that can bring more user engagement?

#### Data Sources
The data used to solve this problem is collected from the website called grouplens(https://grouplens.org/datasets/movielens/), GroupLens research has collected movie ratings from the MovieLens website, the data collected thousands of movies from many users in various points of the time. The dataset describes the 5-star ratings and free-text tagging activity from MovieRlens. The users who participated in this survey were selected randomly, and all the selected users had rated at least 20 movies.

Citation: F. Maxwell Harper and Joseph A. Konstan. 2015. The MovieLens Datasets: History and Context. ACM Transactions on Interactive Intelligent Systems (TiiS) 5, 4: 19:1–19:19. https://doi.org/10.1145/2827872

#### Methodology
There are various tools and techniques available to model this problem. 
- Some of the tools are Jupyter Notebook, python, and Pandas. 
- Seaborn, plotly, and Matplot are used for data visualization.
- Sklearn, and surprise libararis for modeling
- Used techniques such as Collaborative filtering, and Contentbase filtering models

Here is the step-by-step process

* First, the data is gathered from the above-mentioned source as CSV files, then read and create data frames that can be used for modeling.
* Then performed data analysis, and visualized the distribution rating per user and movie, as well as the distribution of genres. And checked the data quality, fortunately, the data is clean.

  ![Screen Shot 2023-12-14 at 8 46 46 PM](https://github.com/vnyreddy/Capstone-2/assets/18583217/f6ffdb49-298d-41bb-9de5-d806a01ecba1)

  ![Screen Shot 2023-12-14 at 8 47 04 PM](https://github.com/vnyreddy/Capstone-2/assets/18583217/869cdf4c-d003-4b86-b1a6-4bf0d21a5b27)

  ![Screen Shot 2023-12-14 at 8 47 21 PM](https://github.com/vnyreddy/Capstone-2/assets/18583217/1f2da8b3-f34d-4c17-9f34-eb7277b8b12a)

* Prepared data using Surprise library, and split data into test set and train set.
Performed collaborative filtering models
* Created and trained a simple baseline model to use it as a point of comparison for more complex models.
* Then created and trained more complex models such as SlopeOne, Singular Value Decomposition(SVD), and KNNBase.
* Performed GridSearchCV for optimizing the SVD hyperparameter tuning, to improve the performance of the model.
* Lastly, performed k-fold cross-validation of the models using metrics such as Root Mean Square Error(RMSE), Mean Square Error(MSE), and Fit time.

  ![Screen Shot 2023-12-14 at 8 45 58 PM](https://github.com/vnyreddy/Capstone-2/assets/18583217/1746066f-651b-4dad-b044-24c1e858e1e8)


MSE and RMSE are metrics for evaluating the accuracy of a predictive model. It measures the average magnitude of the error between predicted values and actual values. The fit time is used to evaluate the performance of the model by the time it took to run the model.

After comparing all the models, such as Baseline, SlopOne, KNNBasic, and SVD, the SVD with hyperperameter tuning seems to be the best choice since it has a low mean square error and root mean squared error, also less fit time.


#### Results
After the analysis of comparing all the models at this stage, the Singular Value Decomposition(SVD) seems to be the best choice to accurately recommend movies, since it has low mean square error, root mean squared error, and also less fit time. This can accurately recommend movies.

#### Next steps
The next steps are to improve the model performance and accuracy by hyperparameter tuning with the help of GridSearchCV.

The MovieLens dataset doesn't have explicit tags for each movie, and the dataset is not structured in a way that supports effective content-based recommendation using tags, so need more data collection for tags, and then re-model for effective results.

#### Outline of project

- https://github.com/vnyreddy/Capstone-2/blob/master/MovieRecommendation.ipynb


##### Contact and Further Information
