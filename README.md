# Random Forests and Gradient Boosting to Predict Housing Prices

### **Summary and Problem Definition**

Estimating real estate prices has widespread benefit and application for those who can do so.  Given data on the Boston housing market, our goal is to produce accurate and reproducible predictions for median home prices in the city. A preliminary analysis investigated four approaches: linear, ridge, lasso, and elastic net regressions. Here, we will add two methods, random forests and gradient boosting. Their results and scalability will be analyzed.

### **Methods**

A defined project structure alleviates many concerns regarding the validity of the work being done. This project follows a typical end-to-end machine learning (ML) pipeline with 7 key steps. First the big picture is observed, then the data is procured, insights and perspective are found during data discovery, the data is prepared for ML models, models are selected and trained, fine-tuned, and finally the solution is presented. These steps will be condensed into the next four sections.

#### *Research Design*

The data we are examining is well-defined and contains no null values. It is simple to work with and preprocessing is minimal. Data quality is essential to research design. Many models lose applicability as data quality is compromised, assessing what we have is a crucial first step. From there, a multitude of regression models are employed and the best two are tested further.

#### *Measurement*

Assessing the quality of our models is key to creating reproducible, scalable results. The k-fold method randomly divides the dataset into groups where one is the validation set and the others are used to fit the model and is repeated for consistency. For each fold, our regression models are assessed with root mean squared error (RMSE) and the coefficient of determination (R2). Afterwards the averages are calculated across all folds and displayed.

#### *Statistical Methods*

The accuracy of each model is tested through two factors: the R2 statistic and the root mean-squared error. R2 is calculated as the total sum of squares – the residual sum of squares divided by the total sum of squares, acting as a proportion of fit. RMSE is the square root of the variance of the residuals. It shows how close predictions are to the actual values.

#### *Traditional and Machine Learning Methods*

Two approaches to modeling are assessed: random forest regression and gradient boosted regression. A random forest uses a tree-based prediction model that is similar to bagging. The key difference occurs at each split of the tree. At each level of the tree, a subset of predictors can be chosen. This helps limit reliance on a single predictor, known as decorrelating the tree. We test subset variations to find the best random forest method. Conversely, the gradient boosted regression creates multiple trees that rely on the information of previous trees. 

### **Overview of Programming Methods**

First the data is preprocessed in the same fashion as our earlier efforts. Notable changes include a scalar transformation and a train, test split. 20 possible models are assessed, and the best two methods are compared. Before doing this, data is divided into training and test sets using a train_test_split procedure, with RMSE and R2 values calculated for each fold. Then we reassess the two best regressions with the repeated k-fold method randomly dividing the dataset into groups where one is the validation set and the others are used to fit the model. Ultimately, averaged RMSE and R2 results are displayed. Feature importance differences are visualized for the six-feature random forest and gradient boost regressions. 

### **Results and Recommendations**

The six-feature random forest and gradient boost regressions produce positive results. The random forest regression yields a RMSE of 0.35 and R2 of 0.87. The gradient boost regression yields a RMSE of 0.33 and R2 of 0.89. These scores are obtained from a 5-fold design repeated three times. Our preliminary analysis using ridge and linear regressions is well replaced by either method. Feature importance tends to be more extreme for gradient boost methods. If new data is expected to alter results, then a random forest regression is the better choice. Otherwise, both answers are viable.
