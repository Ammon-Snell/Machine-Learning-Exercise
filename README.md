# Stakeholder Problem
Our automotive company is releasing a new vehicle to the market soon and is wanting to maximize profits by targeting the marketing and advertising to the individuals who are the most likely to purchase the vehicle.
Previous data analysis demonstrates that individuals who make over $50000 a year were significantly more likely to purchase previous models of the same car.
We will be looking at various features of individuals to see if we can predict whether or not they fit into our target demographic.

# Data
The data that is used for this analysis comes from kaggle and contains over 48000 entries representing individual adults. The features in the dataset include features like age, who employs
the individual, their educational level as both objects and ordinal encoded columns, marital status, hours worked per week and capital gains and losses. It also includes race gender and occupation.

# Insights
![download](https://user-images.githubusercontent.com/120761360/225144803-7e59327a-1104-4318-af5f-d257d81d4eee.png)

We can see that the general trend for hours worked per week increases the higher the educational level increases. However we can 
also see that the hours worked per week begins to decrease once the education level hits 9 or freshman year. This helps demonstrate
why hours worked per week may not tell the full picture.


![download](https://user-images.githubusercontent.com/120761360/225146756-dcb395d5-82b2-4ff3-b209-16ae38cb7d08.png)

With this chart, we can see how the green dots, indicating our target, occupy the educatinal levels of 9 and above primarily.

# Model
Our tuned KNN model using PCA performed the best out of the models implemented. The total accuracy for the model was .83
while our precision, recall and f-1 scores were .86, .93 and .89 respectively the .93 recall score in particular indicates
a good score as we can be 93% sure that those individuals who make $50k or less will be predicted as such. This will be useful 
since it means we can be assured that those we're marketing to fall in our demographic.

However, the main drawback to our model is the recall score for individuals making over $50k a year being .53. This means that
while we can be confident our model is correct when predicting someoe making over $50000, it is only predicting that outcome correctly
half the time.

This model will be useful for weeding out individuals who are less likely to purchase the product. It might be useful to implement
as a cost effective model until more data can be used to develop a more accurate and comprehensive model.

Another possibility would be to replace age with work experience in current career.
