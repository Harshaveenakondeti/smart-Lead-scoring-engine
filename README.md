# smart-Lead-scoring-engine
Identifying potential leads for D2C startup

## Problem Statement

A **D2C startup** develops products using **cutting edge technologies** like **Web 3.0**. Over the past few months, the company has started multiple **marketing 
campaigns offline and digital** both. As a result, the users have started showing interest in the product on the website. These users with **intent to buy product**(s)
are generally known as **leads (Potential Customers)**.
Leads are captured in 2 ways - **Directly and Indirectly**. 

**Direct leads** are captured via forms embedded in the website while **indirect leads** are captured based on certain activity of a user on the platform such as
time spent on the website, number of user sessions, etc.

Now, the marketing & sales team wants to **identify the leads who are more likely to buy the product** so that the sales team can manage their bandwidth efficiently
by targeting these potential leads and increase the sales in a shorter span of time.

Now, as a **data scientist**, your task at hand is to **predict the propensity to buy a product** based on the user's past activities and user level information.

Here we have 2 datasets of train & test seperately, in which train has label of buy ,test doesnt have, we need to predict. we read data into pandas dataframe.
we did basic exploration of data by exploring shape,columns,missing values. Data munging done by converting data types of created at ,
signup date to timestamp. fill null values with respective mean & median respective of variable symmetric & skewed data. we examine trend of products purchased for 
signup date & created at. we can say it is decreasing from 2019 to 2021. so we need to focus on potential custumers or lead , to increase short term sales for next 3 
months. we need to predict who will likely to purchase products in next 3 months from their past data. we need to standardize data for machime learning.
As we dont have label for test, we used RF classsifier & calculate accuracy of train data. here train data splits into training & validating test.
This validating model used to predict label for test. Here we got accuracy of RF classifier is 92.35%, which is good model.
F1_score with micro average for buy label 1 is 0.92. we created buy label column in test dataframe.
we created new dataframe name buy_2 for label  values along with id saved into csv format.
