# Restaurant Success
Family Grill House (FGH) is a major franchise restaurant chain with over a thousand locations. The company allows franchise operators to suggest new locations and helps them get the restaurants open and running.
A large number of new FGH restaurants struggle to become profitable and have to be closed down. The franchise is looking to utilize the data of current resturants to improve the success rate with new locations.

## Objective
- Identify which factors are most important in determining the profitability of a new location.
- Predict whether the third year profits are positive with 75% accuracy.

## Dataset
The dataset contains information about existing FGH restaurants. 
- location :- Discrete. Unique identifier for the restaurant.
- year_3_profit :- Nominal. 1 if profitable after 3 years, 0 otherwise.
- local_pop :- Discrete. Population within 30 minutes of travel to the restaurant. Any positive integer.
- competitors :- Discrete. Number of competitor restaurants within 2 kilometers. Any positive integer.
- nearest_fgh :- Continuous. Distance in kilometers to the nearest other Family Grill House location. Any positive value.
- hours :- Ordinal. One of "Regular", "Extended", or "24 hours".
- highway :- Discrete. Travel time in minutes to the nearest highway. Should be at least 1 minute.
- drivethru :- Ordinal. Whether the location has a drive-through order and collection service ("Yes" or "No").


## Summary of Approach to Solution
1. Data Validation was perfomed to check the sanity of data and get basic information. Missing values and data inconsistency were addressed using appropiate Imputing techniques.

2. EDA was performed to get an exhaustive understanding of the dataset that revealed few key points as follows:

   a) About 83% of restaurants are profitable "hinting class imbalance" in the dataset.

   b) More than 90% of the restaurants do not have any competitors within 2kms radius.

4. Label Encoding and Ordinal Encoding were done to convert catgeorical columns to numerical. Outliers were treated with suitable methods in order to minimize the effect on model's performance.

5. Transformation and Scaling such as PowerTransform, StandardScaler were used to create data values suitable for ML algorithms.

6. **SMOTE technique** was introduced to address the problem of class imbalance and improve model's ability to predict output.

7. This is a **Classification problem** since the requirement is to predict whether a new location will be profitable/not.

8. Logistic Regression, Support Vector Classifier, Random Forest Classifier models were developed.

9. KPI : Accuracy and Precision were compared among the 3 models and RF classifier outperformed the other 2 by achieving better Cross-Validation score, precision and 79% accuracy.

10. The top 3 features of importance from the model:

    a) **Local Population**
   
    b) **Travel time from nearest Highway**
   
    c) **Distance to the nearest neighbouring FGH restaurant**.
   
Analysis was done to draw inference on how the key features affect the profitability of a restaurant.




## Business Recommendation
Use **Random Forest Classifier** model to predict profitability of a new restaurant after 3 years. The model needs to be finetuned at regular intervals and when the data is updated to get the most optimal performance.

Below are the suggestions to business:

**1. Focus on locations with larger local population.**

The franchise should consider opening new restaurants in areas with **high population density**, generally more than 157.5k that is within a 30 minute travel time. This is because the average local population of profitable restaurants were observed to be higher than not-profitable locations.

**2. Proximity to other FGH restaurant**

The proximity of the Profitable restaurants to the **nearest other FGH is close**. The mean distance was 7.6 km. It suggests that opening new FGH locations near existing ones might positively impact the profitability.

**3. Explore regions with limited competitors**

Restaurants with **no competitors** within 2kms are **thriving and profitable**. Location of new restaurants could be planned this way, so that the FGH franchise could be the **first in business** at such locations which leads to larger customer acquisition/base.
The franchise also must look upon **improving business** at locations that are not profitable even though there are no competitors, evaluate and address the pain points of such locations in order to make them profitable.

**4. Locations 15mins+ from highway**

Contradictory to the general expectation, FGH restaurants that are far from the highways are profitable. So, the franchise can consider opening **new locations that are atleast 15 mins from the highway** and at locations where there is limited competition.

**5. Franchise to decide on Drive-Through and Service Hours**

The service hours was **not a prominent factor** in determining the profitability. All 3 types were **performing equally good** and due to missing values, the result was a bit inconclusive. The drive-thru distibution against profitability was almost equal. Since, the **operational costs** based on the type of service hours is **unavailable**, we can recommend the **franchise to take the call** while setting up restaurant in new locations based on the local regulations.
