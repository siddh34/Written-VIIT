# DSML

## Unit 4 Supervised learning

Q1. Supervised learning vs unsupervised learning

![sl vs unls](./images/sl%20vs%20unsl.jpg "Title")

Q2. Solve using navies bayes (Red domestic SUV) stolen or not

![navies bayes](./images/navies%20bayes%20question.jpg "Title")

(Total must be total numbers of yes or no as denominator. Do not consider freq of  original column values  total)

    P(Red|Yes) = 3/5
    P(Red|No) = 2/5

    P(Yes) = 5/10
    P(No) = 5/10

    P(domestic|Yes) = 2/5
    P(domestic|No) = 3/5

    P(SUV|Yes) = 1/5
    P(SUV|No) = 3/5

    probability of stolen = 3/5 * 5/10 *  2/5 * 1/5 = 0036

    probability of not stolen = 2/5 * 5/10 * 3/5 * 3/5 = 0.072

    By comparision car is not stolen

Q3. Decide root node using gini / entropy

![gini entropy](./images/gini%20entropy%20example.jpg "Title")

![gini entropy 1](./images/gini%201.jpg "Title")

![gini entropy 2](./images/gini%202.jpg "Title")

![gini entropy 3](./images/gini%203.jpg "Title")

![gini entropy 3](./images/gini%204.jpg "Title")

    Gini(spicy) = 0.439
    Gini(Cuisine) = 0.367 
    Gini(Packed) = 0.428
    Gini(Meal type) = 0.342

    As gini values measures impurity so we need the lowest gini value for root which is gini(Meal type)

![gini entropy 3](./images/gini%20root.jpg "Title")

Q4. Difference between gini and entropy

| Gini | Entropy |
| -----| -------|
| Gini measure frequency at which a label can be mislabelled | Entropy is a measure of information that indicates the disorder of the features with the target |
| ![gini diff ](./images/gini%20form.jpg "Title") | ![entropy diff ](./images/entropy%20form.jpg "Title") |
| Faster calculation| Slow calculation |
| Less complex | More complex |
| We finally see weighted sum of gini value of features | We finally see information gain|
| Smaller gini values decides the root | Greater Information Gain decides the root|

## Unit 5 Model evaluation

Q1. Calculate precision, recall, accuracy and error

![Matrix](./images/confusion%20matrix.jpg "Title")

    ▪ Precision = TP / (TP + FP) = (173 / (173 + 46)) = 0.78995
    ▪ Recall = (TP / (TP + FN)) = (173 / (173 + 2)) = 0.988571
    ▪ Accuracy = (TP + TN) / (TP + TN + FN + FP) = 0.994533
    ▪ Error = 1 – 0.99 = 0.01

Q2. List methods to evaluate classifiers

    1. Holdout method
        a. Training set (e.g., 2/3) for model construction
        b. Training set (e.g., 2/3) for model construction
        c. Then these are evaluated multiple times to get the best
    2. Cross-validation
        a. Randomly partition the data into k mutually exclusive subsets, each approximately equal size
        b. For certain iteration certain subsets are for traning and certain are for testing they both do changes continuously while getting the best results
    3.Bootstrap method
        a. Works well with small data sets
        b. Training set are changed by replacing the values within them with the testing set values. Then overall accuracy is calculated

Q3. Explain N-fold cross validation

    1. Instead of a single test-training split, split data into N equal-sized parts

![N cross fold](./images/n%20cross%20flod.jpg "Title")

    2. Accuracy on each test is calculated
    3. Difference between accuracies are calculated of different models are calculated
    4. Where there is difference less and accuracy is values are more thats the best split
    5. See the table below

![N cross fold](./images/acc%20differnce.jpg "Title")

## Unit 6 Visualization

Q1. What are best practices for Data Visualization?

    1. Most important is to identify your audience
    2. Select the target graph
    3. Label your chart effectively
    4. Emphasize the important points effectively
    5. Make use of color 
    6. Ensure graph is readable

Q2. What are the types of visualization? Also write any 4/5 graph and mention there use.

    1. Exploration, which helps find a story the data is telling you
    2. Explanation, which tells a story to an audience

    Graphs ->

    a. Bar Charts (Used in comparison)
    b. Scatter Plots (Used in clustering and to see variation)
    c. Pie and Donut Charts (Used for plotting numerical proportions)
    d. Box plot (For outliers identification purposes)

Q3. Use of data visualization in medical applications

    1. Today's healthcare systems collect and track huge amount of information around the clock
    2. Modern data visualization tools in healthcare convert complex data into user-friendly visuals that are easy to understand for its people like doctors, patients, or government officers
    3. Dashboards combine several interactive reports and are the most common visualization tool used by healthcare organizations
    4. They can be built into existing software together with data analysis functionality or be a part of reporting software tailored to the organization's specific needs
    5. There are three main types of dashboards
        a. Operational for displaying real-time data
        b. Strategic for showing patterns and trends over time
        c. Analytical for more advanced analytics
    6. BBC website showing recent statistics on COVID-19 cases.

Q4. Pivot table and pivot charts

    1. Large data analysis is done using PivotTables
    2. PivotTable complements the manner the data is collated, related, summarized and mentioned
    3. We just have to import the required data to excel and 
    excel will automatically recreates the relationships between the features
    4.After Data is represented, we can explore it via the filters which we can apply from the side bar
    5. We can also use the pivot chart option to see the desired chart on our data
    6. In excel pivot charts also work on non pivot table data
