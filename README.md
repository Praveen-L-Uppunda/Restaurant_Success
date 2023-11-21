# Restaurant_Success
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
