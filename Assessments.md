## Topic-1
# DATA MANIPULATION WITH PYTHON
#### 1. Consider the Pandas DataFrame df below. Filter it appropriately so that it outputs the shown results.

| |gh owner| language|      repo|  stars|
|-|--------|---------|----------|-------|
|0|  pandas-dev   python|    pandas|  17800|
|1|   tidyverse|        R|     dplyr|   2800|
|2|   tidyverse|        R|   ggplot2|   3500|
|3|      has2k1|   python|  plotnine|   1450|
```diff
+ print(df[df["stars"]==1450])
```

#### Expected output
| -|    repo| gh owner| language  |stars|
|--|-------|----------|-----------|-----|
|3 | plotnine|   has2k1|   python   |1450|

#### 2. Consider df below.

|--| x |  y|
|--|---|---|
|0 | 4 | 16|
|1 | 9 | 25|

```
print(df.apply(np.sqrt))
```

#### Expected Output
|- |   x|    y|
|--|----|-----|
|0 | 2.0 | 4.0|
|1  |3.0  5.0|

#### 3. Consider the Pandas DataFrame df below.
|-|     gh owner| language |     repo | stars|
|-----|-------|-----------|---------|-------|
|0 | pandas-dev |  python  |  pandas|  17800|
|1 |  tidyverse |       R  |   dplyr |  2800|
|2  | tidyverse |       R  | ggplot2 |  3500|
|3  |    has2k1  | python | plotnine |  1450|
```
print(df.loc[:,["gh owner"]])
```
#### Expected Output
|--  | gh owner|
|-----|---------|
|0 | pandas-dev|
|1 |  tidyverse|
|2 |  tidyverse|
|3 |     has2k1 |

4. Consider the Pandas DataFrame df. Explore its last five rows.
```
import pandas as pd
df = pd.read_csv(iris_csv)
print(df.tail())
```
#### Expected Output
|    SepalLength|  SepalWidth|  PetalLength|  PetalWidth  |          Name|
|---------------|------------|-------------|--------------|---------------|
|16    |      7.1     |    3.0   |       5.9     |    2.1 | Iris-virginica|
|17    |      6.3     |    2.9   |       5.6      |   1.8 | Iris-virginica|
|18    |      6.5     |    3.0   |       5.8     |    2.2 | Iris-virginica|
|19    |      7.6     |    3.0   |       6.6      |   2.1|  Iris-virginica|
|20    |      4.9     |    2.5   |       4.5      |   1.7|  Iris-virginica|

#### 5. Add the height column to the df DataFrame shown below.

| ----  |species    |name  |weight |
|-----|-----------|-------|------|
|0      | lion   |Sally     |121|
|1      |tiger   |Henry     |228|
|2       |lion    |Tony     |177|
|3      |tiger    |Lucy     |165|

```
height = [70, 100, 80, 85]
df['height'] = height 
print(df.head())
```
#### Expected Output
|-|  species|   name|  weight|  height|
|-|---------|-------|--------|--------|
|0|  lion|  Sally   |  121  |    70|
|1| tiger|  Henry  |   228   |  100|
|2|  lion |  Tony  |   177   |   80|
|3  | tiger |  Lucy   |  165   |   85|


#### 6. The wine DataFrame, whose first few rows are shown below, provides information on wine stocked by an online retailer, but is missing the year of the vintage. Add the year column to the data. The list of years has been created for you.

|-|type      |country   |price     |rating|
|----------------|----------|----------|--------|---------|
|style           |-|-|-|-|  
|alvarinho       |    white |  portugal|  18.99 |    4.2|
|blanc de blanc  |sparkling |    france |   NaN|     3.8|
|cabernet              |red|  argentina|  14.90|     4.0|
```
year = [2018, 2018, 2017, 2016, 2017, 2016, 2018, 2016, 2016]
wine['year'] = year
print(wine.head())
```
#### Expected Output
 |- |type   | country | price | rating | year|
 |-------------|--------|---------|--------|------|----|
|style         |-|-|-|-|-|
|alvarinho          | white  | portugal  |18.99  |   4.2 | 2018|
|blanc de blanc  |sparkling  |   france |   NaN   |  3.8 | 2018|
|cabernet        |      red  |argentina | 14.90   |  4.0 | 2017|
|gavi             |   white  |    italy  |13.56   |  NaN | 2016|
|malbec           |     red  |argentina | 19.04   |  4.2 | 2017|

#### 7. You have collected data on the age for each of 100 shoppers in your store. Calculate the mean age for the shoppers.
```
import numpy as np
mean_age = np.mean(age)
print(mean_age)
```
#### Expected Output
40.1

#### 8. The chess DataFrame contains information about the top female chess players around the world. Determine what fields exist in the dataset by printing the names of the columns.
```
print(chess.columns)
```
#### Expected Output
Index(['Fide id', 'Name', 'Federation', 'Gender', 'Year_of_birth', 'Title', 'Standard_Rating', 'Rapid_rating', 'Blitz_rating', 'Inactive_flag'], dtype='object')

#### 9. Which type of visualization should be used to show the number of students in each department at a university?

- [ ] Scatter plot
- [x] Bar chart
- [ ] Box plot
- [ ] Line plot

#### 10. Create a plot of the correlation matrix of the features contained in the wine Pandas DataFrame.
```
import matplotlib.pyplot as plt
import seaborn as sns
sns.heatmap(wine.corr())
plt.yticks(rotation=0)
plt.xticks(rotation=90)
plt.show()
```
Expected Output

![129](https://user-images.githubusercontent.com/61821924/213892671-dc0cc806-597c-410e-be02-0866466c2432.svg)


#### 11. Which method is used to peek at the top of a DataFrame?
- [ ] .tail()
- [ ] .peek()
- [ ] .show()
- [x] .head()

#### 12. You have collected data on the age for each of 100 shoppers in your store. Calculate the standard deviation for the age of the shoppers.
```
import numpy as np
sd_age = np.std(age)
print(sd_age.round(2))
```
#### Expected Output
14.77

#### 13. Calculate the mean and median of the array x.
```
x = np.array([2.2, 0.9, 4.4, 6.7, 2.8, 3.2, 1.1, 3.5])
mean = np.mean(x)
median = np.median(x)
print('Mean:', mean, 'Median:', median)
```
#### Expected Output
Mean: 3.1 Median: 3.0

#### 14. Rank the figures in terms of the size of the Pearson correlation coefficients from smallest to largest.
![130](https://user-images.githubusercontent.com/61821924/213893645-5696d7c6-d6a5-4b1f-ac3e-52ed2e942a9c.png)

- [ ] Figure A < Figure B < Figure C < Figure D
- [x] Figure B < Figure D < Figure C < Figure A
- [ ] Figure A < Figure C < Figure D < Figure B
- [ ] Figure B < Figure C < Figure D < Figure A  

#### 15. Return the food DataFrame, previewed below, sorted by the index value item in descending order.

|-|energy  |protein  |carbohydrate|
|item | -|-|-| 
|----|------|----|---|
|waffles   |        200  |   4.29    |     35.71|
|tacos             |180    |10.94        | 23.44|
|tacos      |       180   | 10.94      |   23.44|
|lasagne    |       188   | 11.76      |   10.59|
|croissant  |       343   |  5.71       |  58.57|
|chicken salad|     110   |  5.00|      |    8.00|
```
print(food.sort_index(level = 'item', ascending = False))
```
#### Expected Output
|--------| energy  |protein  |carbohydrate|
|item |-------------|------- |------------| 
|---  |---|----|---|
|waffles   |        200  |   4.29    |     35.71|
|thai curry |       106   |  3.18      |   11.66|
|tacos      |       180   | 10.94      |   23.44|
|lasagne    |       188   | 11.76      |   10.59|
|croissant  |       343   |  5.71       |  58.57|
|chicken salad|     110   |  5.00|      |    8.00|


#### 16.  
```
sns.scatterplot(x = "age", y = "value", size = "mpg", data = valuation)
```
Output: It creates single graph scatter plot having different sizes 

#### 17. Set the column name as an index of the Pandas game DataFrame shown below
```
game = game.set_index('name')
print(game)
```
#### 18. Consider the Pandas DataFrames restaurant and location below, respectively. Combine their columns into a single DataFrame.
```
df = pd.concat([restaurant, location], axis = 1)
```
#### 19. To drop duplicates
```
wine_no_duplicates= wine.drop_duplicates()
``` 

#### 20. To reset index 
```
game = game.reset_index()
```

#### 21. 
```
import matplotlib.pyplot as plt
import seaborn as sns
sns.scatterplot(x = "age", y = "value", hue = "emissions", data = valuation)
plt.show()
```

#### 22. For descending order
```
print(food.sort_index(level = 'item', ascending = False))
```

#### 23. Adding new column
```
df['language'] = ['python', 'R', 'R', 'python']
print(df)
```
#### 24. To set index
```
chess = chess.set_index('Fide id')
print(chess.head())
```
#### 25. Your manager wants a list of the first names of all of her employees. Help her out by printing the index of the employee DataFrame shown below.
```
print(employee.index)
```
#### 26. The three columns in the stars DataFrame currently have very cumbersome names (Temperature (K), Luminosity(L/Lo), Radius(R/Ro)). Rename them using the provided list column_names.

```
import pandas as pd
column_names = [
  'temperature',
  'luminosity',
  'radius'
]
stars.columns = column_names
print(stars.head())
```
#### 27. 
```
import matplotlib.pyplot as plt
import seaborn as sns
sns.lineplot(x = 'day', y = 'order', data=df)
plt.xticks(rotation = 45)
plt.show()
```

#### 28. The chess DataFrame contains information about the top female chess players around the world. Determine what fields exist in the dataset by printing the names of the columns.

```
print(chess.columns)
```
#### 29. Stats function 
```
from scipy import stats
iqr_age = stats.iqr(age)
print(iqr_age)
```
#### 30. 
```
import pandas as pd
print(pd.DataFrame({
    "x": [1], 
    "y": [3],
}))
```
Expected Output
|---|x  |y|
|---|--|--|
|0  |1 | 3|

#### 31. Consider the Pandas DataFrame df below. Remove the column named "repo".

```
print(df.drop(columns="repo"))
```

Mean of values

#### 32. Consider df below.
|- |x  | y|
|--|---|---|
|0  |4|  16|
|1  |9 | 25|

```
print(df.apply(np.sqrt))
```

#### Expected Output
|---| x|    y |
|---|--|-------|
|0  |2.0|  4.0|
|1  |3.0|  5.0|

#### 33. You have been given the food data to analyse, it's already loaded for you and stored in a DataFrame. Before you get started you want to quickly see some summary statistics for each of the three columns in the data. Calculate and print these statistics.

```
print(food.describe())
```
#### 34. The food DataFrame contains nutritional information about six menu items from a restaurant. Print the row index of the data.

```
print(food.index)
```

#### 35. You are investigating the impact of age on the valuation of cars to better understand prices that should be offered to customers for second hand cars. You want to visualize both the individual distributions as well as the relationship between the two variables on a single graphic.

```
import matplotlib.pyplot as plt
import seaborn as sns
sns.jointplot(x = 'age', y = 'value', data = valuation)
plt.show()
```

#### 36. Return the Pandas DataFrame df shown below with the smallest salary value appearing first in the data frame.

```
result = df.sort_values('salary', ascending = True)
print(result)
```

#### 37. Subset the Pandas DataFrame df to return all rows with a weight greater than 175.

```
print(df[df['weight'] > 175])
```

#### 38. From the wine DataFrame, select the columns country and price.
```
subset_wine = wine[['country', 'price']]
print(subset_wine.head())
```

#### 39. Consider the Pandas DataFrame df below. Filter it appropriately so that it outputs the shown results.
```
print(df[df["stars"]==1450])
```

#### 40. The wine DataFrame, whose first few rows are shown below, provides information on wine stocked by an online retailer, but is missing the year of the vintage. Add the year column to the data. The list of years has been created for you.

```
year = [2018, 2018, 2017, 2016, 2017, 2016, 2018, 2016, 2016]
wine['year'] = year 
print(wine.head())
```

#### 41. Consider the Pandas DataFrame df below.

```
print(df.iloc[0:2])
```
The chess dataset contains information about the top female chess players around the world. Remove the redundant Gender column from the dataset.

```
chess.drop(columns="Gender", inplace=True)
print(chess.dtypes)
```

#### 42. You work for a second hand car sales company, and they want to know the relationship between the age and the value so that they can estimate the best price to sell their cars at. Create a plot to show the relationship, identifying the miles per gallon (mpg) by changing the size of each point. The valuation data is previewed below.
```
import matplotlib.pyplot as plt
import seaborn as sns
sns.scatterplot(x = "age", y = "value", size = "mpg", data = valuation)
plt.show()
```
#### 43. Create a pair plot of the song_metrics dataset.

```
import matplotlib.pyplot as plt
import seaborn as sns
sns.pairplot(song_metrics)
plt.show()
```


#### 44. Plot a boxplot of the pH variable in the wine DataFrame.

```
import matplotlib.pyplot as plt
import seaborn as sns
ax = sns.boxplot(wine['pH'])
plt.show()
```

#### 45. Add a legend to the distribution plot of avocado prices.

```
import matplotlib.pyplot as plt
import seaborn as sns
ax = sns.histplot(avocado.AveragePrice)
ax.axvline(x=1.75, label="Break Even", linestyle='--')
ax.legend()
plt.show()
```

## Topic-2
# STATISTICAL FUNDAMENTALS WITH PYTHON

#### 1. You want to compare the distribution of the arrival delays for two different airlines. In particular you want to see features of the data, so you have decided to create a boxplot. A sample of the arrivals data is shown below.

|  |   airline|   delay|
|--|----------|--------|
|0 |      A   |  20|
|1 |      B   |  63|
|2 |      B   |  28|
|3 |      B   |  25|
|4 |      A   |  20|

```diff
import matplotlib.pyplot as plt
import seaborn as sns
+ sns.boxplot(x= 'airline', y = 'delay' , data = arrivals ) 
plt.show()
```

#### Expected output

![131](https://user-images.githubusercontent.com/61821924/213913016-46a9d450-cee6-4d27-a5f7-f80cae4e6e12.svg)


#### 2. Create a pair plot of the song_metrics dataset.
```diff
import matplotlib.pyplot as plt
import seaborn as sns
+ sns.pairplot(data = song_metrics)
plt.show()
```
#### Expected Output

![132](https://user-images.githubusercontent.com/61821924/213913036-17da53c4-568b-4a1d-9ad2-f86564f64e04.svg)


#### 3. You have access to a lap_times DataFrame that contains the lap times for three different Formula 1 drivers across a number of races. The driver ids are stored in the column driverId, and the respective times are contained in the column seconds. Use a boxplot to compare the lap times of the different drivers.
```diff
import matplotlib.pyplot as plt
import seaborn as sns
ax = sns.boxplot(
+  	x = 'driverId', 
+  	y = 'seconds', 
+  	data=lap_times
	)
plt.show()
```
Expected Output

![133](https://user-images.githubusercontent.com/61821924/213913098-3ed1c684-7d26-42e0-b2a0-158e96339047.svg)

#### 4. Draw a sample of 20,000 numbers from a standard normal distribution. The random seed has been set for you.
```diff
import numpy as np
from scipy.stats import norm
+ sample = np.random.standard_normal(20000)
print(sample)
```
Expected Output
[ 0.49671415 -0.1382643   0.64768854 ...  0.37835397  1.71352973 -1.6199198 ]

#### 5. You have just arrived at a casino, and have decided to try out the roulette wheel. You know that the odds of winning any single number are approximately 3%, and yet you still decide to put your money on the number 21 for 10 separate spins. Generate a sample of the 10 fresh spins of the wheel. The random seed has been set for you.
```diff
import numpy as np
+ sample = np.random.choice(["Win", "Lose"], 10, p=(0.03, 0.97))
print(sample)
```
Expected Output
['Lose' 'Lose' 'Lose' 'Win' 'Lose' 'Lose' 'Lose' 'Lose' 'Lose' 'Lose']

#### 6. Consider the histogram of a data sample. Fit an empirical cumulative distribution function (ECDF) and calculate the cumulative probability of 40. The data sample is available in an array named x.

![134](https://user-images.githubusercontent.com/61821924/213913192-74f43598-7275-44b8-b228-e0eb20d4df32.png)
```diff
+ from statsmodels.distributions.empirical_distribution import ECDF
+ ecdf = ECDF(x)
print(ecdf(40))
```
Expected Output
0.645

#### 7. Using the DataFrame movies shown below, create a violin plot to compare the duration of movies by genre.

|   | genre| duration|
|---|------|---------|
|1 |Dramas  |     93|
|2 |Horror |      78|
|3 |Action |      80|
|4 |Dramas |     123|
|5 |Horror |      95|
|6 | Dramas|      119|
```diff
import matplotlib.pyplot as plt
import seaborn as sns
+ sns.violinplot(x='duration', y='genre', data=movies)
plt.show()
```
Expected Output

![135](https://user-images.githubusercontent.com/61821924/213913263-060e9e75-e826-46a2-bc2f-230c3df3d4a3.svg)

#### 8. For each of the next 50 visitors to your website you want to randomly assign them to either group A or B so that they see different versions of the page. There should be an even probability of being in each group. The random seed has been set for you.
```diff
import numpy as np
groups= ['A', 'B']
+ assignment= np.random.choice(groups, 50)
print(assignment)
```
Expected Output
['B' 'A' 'B' 'B' 'A' 'A' 'A' 'B' 'A' 'B' 'A' 'B' 'B' 'B' 'B' 'A' 'A' 'B'
 'B' 'A' 'B' 'A' 'A' 'B' 'A' 'A' 'A' 'B' 'B' 'B' 'A' 'A' 'A' 'A' 'A' 'A'
 'B' 'A' 'B' 'B' 'B' 'A' 'A' 'A' 'B' 'A' 'B' 'B' 'A' 'A']

#### 9. The results data contains the exam Score for a number of students. Create a boxplot of the values for the Score.

|   |    Score| Class |
|---|---------|-------|
|1  |     5.4 |    A  |
|2  |   13.0  |    B  |
|3  |     2.0 |    B  |
|4  |     1.4 |    A  |
|5  |    14.4 |    B  |
|6  |     3.3 |    B  |
```diff
import matplotlib.pyplot as plt
import seaborn as sns
+ sns.boxplot(x = "Score", data = results)
plt.show()
```
Expected Output

![136](https://user-images.githubusercontent.com/61821924/213913444-2209de4c-d6f3-4849-bb9e-f7f46e726305.svg)

#### 10. An eccentric chocolate factory owner has decided to conceal a limited number of special prizes, hidden under the wrapper, in his latest batch of chocolate bars. Perform a simulation of you purchasing three separate chocolate bars from a local store, sampling from the list chocolate. The random seed has been set for you.
```diff
import numpy as np
+ purchases = np.random.choice(chocolate, 3, replace=False)
print(purchases)
```
Expected Output
['Lose' 'Lose' 'Lose']

#### 11. You have conducted an experiment on your website and have measured the time spent on your site by two groups, group_a and group_b. Perform a suitable statistical test to test the hypothesis that the mean time on the site is different for the two groups.
```diff
from scipy import stats
+ test= stats.ttest_ind(group_a, group_b)
print(test.pvalue.round(3))
```
Expected Output
0.056

#### 12. Sample 100 values from a Poisson distribution, with a mean of 10. The random seed has been set for you.
```diff
import numpy as np
+ samples = np.random.poisson(10, 100)
print(samples)
```
Expected Output
[ 4  7 12 11 10  7 12 12 11 11  6 11 11  9  7  5 12 14 12 14 12  9 12 15
  7 16 17  7 13  9 11  5 15  9 14 18  3 22  7 14  9 10 10  7 14  9 16 10
  8  5  5 16 11 12 10 14  9  9 14 10  9  8  9  8  7  6 12 13  9  6 14  4
  7 12 16 12 12  9 12  9 10 12 17 16  8  5  5  8 11 11 11  7  8 11  8  4
  9  6 14  8]

#### 13. Draw a random sample from the professions data set. The random seed has been set for you.
```diff
import numpy as np
professions = ["doctor", 
               "nurse", 
               "product manager", 
               "marketing analyst", 
               "programmer"]
+ sample = np.random.choice(professions)
print(sample)
```
Expected Output
marketing analyst

#### 14. Ensure that results of your research, that involves simulation, are reproducible. The seed value has been provided in the object seed.
```diff
import numpy as np
seed = 121120
+ np.random.seed(seed)
print(np.random.poisson(5, 50))
```
Expected Output
[ 2  7  4  7  3  8  5  3 10  6  6  7  5  6  9  2  6  2  5  5  7  6  5  1
  8  3  6  5  2  4  3  3  3  5  9  4  8  4  4  5  3 10  4  7  3  3  7  1
  3  5]

#### 15. Create an array of 100 numbers sampled from a Poisson distribution were the observed interval is equal to 5. The random seed has been set for you.
```diff
import numpy as np
from scipy.stats import poisson
+ sample = np.random.poisson(5, 100)
print(sample)
```
Expected Output
[ 5  4  4  5  5  3  5  4  6  7  2  5  5  6  4  6  6  1  7  2 11  4  3  8
  3  3  5  8  3  2  5  3  8 10  3  2  5  7  6  6  2  4  9  7 11  8  3  2
  3  4  5  5  4  3  8  2  1  4  5  4  3  4  8  2  2  2  7  6  7  6  7  6
  4  2  3  4  7  4  3  2  6  3  5  9  6  6  9  4  9  2 10  6  9  4  1  6
  8  6  2  3]

## Topic-3
# STATISTICAL EXPERIMENTATION THEORY

1. You are a Data Scientist on a Marketing team. The team is analyzing whether changing the color of their campaign from red to green will increase click-through rates. What is an appropriate null hypothesis for this experiment?

- [x] There is no significant color between red and green color click-through rates 
- [x] There is significant color between red and green color click-through rates 
- [ ] Red will perform significantly better than green on click-through rates conversion
- [ ] Green will perform significantly better than red on click-through rates conversion

2. You conducted a telephone survey on an election candidate and after analyzing your data concluded that there is a 95% chance that she would capture between 26.5% and 33.5% of the vote given the margin of error of 3.5%. What can you say about the remaining 5% chance?

- [x] There is 2.5% chance that she will capture less than 26.5% and a 2.5% chance more than 33.5%
- [ ] there is 5% chance that a residual 5% voters will vote for the other candidate
- [ ] the distribution will have a standard devaition of 5% given the 95% confidence interval
- [ ] Given the confidence interval of 95%, there is a 5% chance that she will get 0 votes

3. As a credit risk analyst, you are conducting a test for a new customer scoring method using machine learning instead of traditional methods. You hypothesize that this new scoring metric will reduce losses at a 95% confidence level. You monitor this new scoring method using a 95% confidence level and have arrived at a p-value of 0.04. What can you say about the null hypothesis in this scenario?
- [ ] This is not enough statistical evidence to reject the null hypothesis
- [ ] the p-value is too small to be able to reject the null hypothesis
- [ ] the null hypothesis is not applicable and does not apply to this scenario
- [x] This is enough statistical evidence to reject the null hypothesis

4. You are a Data Scientist on a Marketing team. The team is analyzing whether changing the color of their campaign will increase or decrease click-through rates. What kind of hypothesis do you propose to solve the team's question?
- [ ] Null hypothesis test
- [x] Alternative hypothesis test
- [ ] Two-tailed hypothesis test
- [ ] One-tailed hypothesis test

5. You want to test the regrowth of hair in people who eat spinach on a daily basis vs. people who don't. You conduct an experiment and find that eating spinach daily has no effect on hair regrowth. What can you say about the null hypothesis?

- [ ] It can be rejected because spinach had no effect on hair regrowth
- [x] It cannot be rejected because hair regrowth was the same between the groups
- [ ]  It cannot be rejected because people who don't eat spanish had less hair loss
- [ ]  It can be rejected because eating spinach and hair loss are not correlated

6. Which test can show if a value is greater than another?

- [ ] Two-tailed
- [ ] Type I test
- [x] One-tailed
- [ ] Type II test

7. Which hypothesis testing method is best to use when two samples are not considered independent?
- [ ] Conjoint
- [ ] blocked
- [x] paired
- [ ] proportion

8. You conduct a survey to compare student study habits between two countries. Canada's data has a standard deviation of 10 and Mexico's has a standard deviation of 6. How can you describe the confidence interval for the Canadian students' study habits vs Mexican students'?
- [ ] Skewed
- [ ] Longer
- [x] Wider
- [ ] Narrower

9. You design an experiment to test engagement with a new product. The users exposed to the existing version of the product are called what?
- [x] control group
- [ ] historical group
- [ ] validation group

10. To measure the impact of a stimulus you divide you sample into two groups. What are these groups called?
- [ ] Test and validation
- [x] Test and control
- [ ] Test and training
- [ ] Test and treatment

11. As an analyst for a mutual fund, you would like to conduct an analysis to prove that your fund has performed 10% better than its benchmark last year. This example uses which type of hypothesis test?
- [ ] Uni-tailed test
- [ ] multi-tailed test
- [x] one-tailed test
- [ ] two-tailed test

12. You are using software to split web traffic between a test experience and control experience for a website. What is the name of the method used to avoid sampling bias?
- [ ] variation
- [ ] blocking
- [x] randomization

13. When testing the differences between two groups, groups A and B, in statistical experimentation, the null hypothesis proposes that:
- [ ] There is a significant difference between groups A and B
- [x] There is not a significant difference between groups A and B
- [ ] The difference in group A is larger than group B
- [ ] The difference in group B is larger than group A

14. How is a t-distribution different than a normal distribution?
- [ ] T-distributions are only used when the mean is greater than zero
- [x] A t-distributions has heavier tails and tends to have values farther from the mean
- [ ] A t-distribution is same as the normal distribution and has no difference in shape
- [ ] The standard deviation of a t-distribution is >1 while a normal distribution is < 1

15. Confidence intervals are commonly used in Statistics to help statistician understand their estimates. Which of the following statements below accurately describes a confidence interval?
- [ ] An interval in which the population mean is guranteed going to be found in repeated experiments
- [x] A range in which the true population mean is likely to be found with a certain probability.
- [ ] An interval in which we expect the p-value to be exactly 0.05
- [ ] A range in which we expect the p-value to fall into within a certain probability, given some observes data.

16. You work at a pharmaceutical company and are testing a new drug to reduce hair loss. You separate the group into two sections: one you will give the new drug and the other you will give a sugar pill. Which one did the control group receive?
- [ ] neither 
- [x] sugar pill
- [ ] new drug

17. What is the purpose of randomly assigning participants to control and test groups within experimental designs?
- [x] Randomaization helps to reduce bias in statistical research
- [ ] Randomization ensures that researchers can perform a t-test
- [ ] Randomization reduces variability across three or more studies

18. Suppose an analyst at your shoe company tells you that she ran a statistical test on expected sneaker sales. The test suggests customers will buy an average of 3 sneakers per person this year, with a margin of error of 1 sneaker. How do you explain to your stakeholder the results of this statistical finding?
- [x] We are 95% confident that the true population value lies between 2 and 4
- [ ] we are 5% confident that true sneaker sales will be exactly 3
- [ ] we are 5% confident that the true population value lies between 2 and 4
- [ ]  we are 95% confident that true sneaker sales will be exactly 3

19. As a Data Scientist in a Marketing team, you are asked to analyze the effect of changing the color of your campaign from red to green on the number of clicks the campaign receives. Which of the following represents the independent variable in this scenario?
- [ ] The campaign itself
- [ ] the number of clicks the campaign recieves
- [x] The color of the campaign
- [ ] The ddesign of the research

20. As a Data Scientist in a Marketing team, you are asked to analyze the effect of changing the color of your campaign from red to green on the number of clicks the campaign receives. Which of the following represents the dependent variable in this scenario?
- [ ] The campaign itself
- [x] the number of clicks the campaign recieves
- [ ] The color of the campaign
- [ ] The ddesign of the research

21. Which continuous probability distribution is characterized by being unimodal, symmetric, asymptotic to the x axis, with an equal mode, mean, and median?
- [x] Normal
- [ ] Uniform
- [ ] Exponential

22. As a Data Scientist at ABC corp., you are asked to explain to the Marketing Manager what a 95% confidence interval is. How should you describe a 95% confidence interval to the manager?
- [ ] If we run an experiment once, we can be 95% certain that the resulting value is accurate
- [x] In repeated experiments, we expect our test results to match results from the population 95% of the time.
- [ ] If we run an experiment twice, we expect our test results to be accurate within 95% of the previous experiment
- [ ] In repeated experiments, we can expect our test results to give the exact same number 95% of the time

##Topic-4
# DATA ANALYSIS IN SQL

#### 1. From the movie_budget table, return the first five rows where the title doesn't contain the character a only in lowercase.

```
SELECT *
FROM movie_budget
WHERE title NOT LIKE '%a%'
LIMIT 5;
```

#### 2. To calculate the average price for each category from the fruit_2022 table, ensure that the calculation only includes the prices using kg as the unit.
``` 
SELECT category, 
       AVG(price) AS avg_price
FROM fruit_2022
WHERE unit = 'kg'
GROUP BY category;
```

#### 3. From the movie_budget table, return the year with more than 3 movies in the table.
``` 
SELECT year, COUNT(*) AS n_of_movies
FROM movie_budget
GROUP BY year
HAVING COUNT(*) > 3;
```

#### 4. From the bike_stations table, convert the Station_ID column to INTEGER data type.
``` 
SELECT station_id,
SELECT Station_ID :: INT,
       Latitude,
       Longitude
FROM bike_stations;
```

#### 5. From the speaker table, return the number of speakers per year in descending order.
``` 
SELECT  EXTRACT(year FROM launch) AS year,
        COUNT(*) AS number_of_speakers
FROM speaker
GROUP BY year
ORDER BY number_of_speakers DESC;
```

#### 6. Based only on the preview shown, which column has missing values in the speaker table?
-- speaker
|   model                             | price |  launch     |  overall  |
|-------------------------------------|-------|-------------|-----------|
|   Bowers & Wilkins Formation Wedge  |  899  |  2019-06-01 |   160     |
|   Harman Kardon Citation 200        |  349  |  ''         |   147     |
|   Sonos Five                        |       |  2021-06-01 |    0 
Answer: Price column

#### 7. In the vendors table, some entries in the zip_code have 9 digits. Return a zip_code column that only contains the first 5 digits from the zip_code column.
``` 
SELECT vendor_name, 
      LEFT(zip_code,5) AS zip_code
FROM vendors;
```

#### 8. From the fruit_2022 table, you want to know which item in the vegetable category has an average price higher than 2.
```
SELECT item,
       AVG(price) AS avg_price
FROM fruit_2022
WHERE category = 'vegetable'
GROUP BY item
HAVING AVG(price) > 2;
```

#### 9. Add the rows from the movie_2010 table to movie_2000 but keep the duplicates.
```
SELECT *
FROM movie_2000
UNION ALL 
SELECT *
FROM movie_2010
ORDER BY year;
```

#### 10. Add the rows from the movie_2010 table to movie_2000 but remove the duplicates.
```
SELECT *
FROM movie_2000
UNION 
SELECT *
FROM movie_2010
ORDER BY year;
```

#### 11. For the vendors table, return the number of the rows without missing values in the vendor_state column. 
```
SELECT COUNT(*) 
FROM vendors
WHERE  vendor_state IS NOT NULL ;
```

#### 12.
```
SELECT item, 
    CASE WHEN energy > 300 THEN 'high'
    WHEN energy > 150 THEN 'medium'
    ELSE 'low' END AS calorie_rating
FROM food
ORDER BY item;
```

#### 13. The wine_region table gives a list of all wines offered by a restaurant. The pairing table lists the recommended food items for those wines. Return the style and price for all wines that have a pairing.
```
SELECT style, price
FROM wine_region
WHERE id IN(
	SELECT wine_id
	FROM pairing
)
ORDER BY price, style
LIMIT 5
```

#### 14. Extract the last two characters from the string sports.
```
SELECT RIGHT('sports', 2) AS sports_extract;
```
#### 15. Count the number of times each artist_id appears in the tracks table.
--tracks
| id     | name                | artist_id | release_date |
|--------|---------------------|-----------|--------------|
| 3qyX4g | Soon We'll Be Found | 5WUlDf    | 2004-10-03   |
| 04sN26 | Bored               | 6qqNVT    | 2017-03-30   |
| 4cCXPF | On Top Of The World | 53Xhwf    | 2021-04-09   |

```
SELECT artist_id, COUNT(*) AS artist_count
FROM tracks
GROUP BY artist_id
ORDER BY artist_count DESC, artist_id
LIMIT 5;
```

##### Expected Output

artist_id	artist_count
3meJIg	137
1dfeR4	33
3WrFJ7	19
4VMYDC	19
3Nrfpe	16


#### 16. The wine table gives information about wines stocked in an online wine retailer. Calculate the average rating of wines by type, return the data ordered by the average rating, from lowest to highest.
```
SELECT type, ROUND(AVG(rating), 2)
FROM wine
GROUP BY type
ORDER BY AVG(rating)
```

#### 17. The wine table gives information about wines from an online retailer. Use a common table expression to determine the highest count of bottles amongst all types.
```
WITH type_count AS (
	SELECT type, count(id) AS bottle_count
	FROM wine
	GROUP BY type
)
SELECT max(bottle_count) 
FROM type_count
```

18. Determine the average number of employees per manager using the employees table.
```
SELECT AVG(count_employees)
FROM (SELECT manager_id,
            Count(employee_id) AS count_employees
           FROM employees
           GROUP BY manager_id) AS employee_summary
```
19. Combine the words 'TV' and 'show' without spaces.
```
SELECT ('TV', 'show') AS new_word;
```

#### 20. Determine the total number of dance hits per artist (by artist_id). A song is considered a dance hit when dance_level > 75.

```
SELECT T.artist_id, COUNT(*) AS dance_hits
FROM tracks AS T
INNER JOIN features AS F
    ON T.id = F.song_id
WHERE F.dance_level > 75
GROUP BY T.artist_id
ORDER BY dance_hits DESC, artist_id
LIMIT 10;
```
##### Expected Output
artist_id	dance_hits
4q3ewB	3
1URnnh	2
1mcTU8	2
1r4hJ1	2
3Nrfpe	2
3TVXtA	2
3nFkdl	2
4VMYDC	2
06HL4z	1
0eDvMg	1


#### 21. The wine table, whose structure is shown below, contains information about a selection of wines offered by a restaurant. Calculate the minimum price for each type of wine and return the created field as min_price.
```
SELECT type, MIN(price) as min_price
FROM wine 
GROUP BY type
ORDER BY type
```

##### Expected Output
type	min_price
red	14.9
sparkling	
white	13.56


#### 22. Return the rows from the artists table where there are missing values for the nationality column.
```
SELECT *
FROM artists
WHERE nationality IS NULL
ORDER BY artist_id
LIMIT 10;
```

##### Expected Output:
artist_id	name	nationality	birth_date
4	Zainab Johnson		
5	Sammy Obeid		
6	Alie Ward		
10	Amir Wilson		
11	Ruby Ashbourne Serkis		
12	Thaddea Graham		
14	Elia Rumpt


#### 23. Return the id and style columns from the table wine where there are no missing values for the column price.

```
SELECT id, style
FROM wine
WHERE price IS NOT NULL
ORDER BY id;
```

#### Expected Output
id	style
21	gavi
31	alvarinho
48	cabernet
65	malbec
68	primitivo
69	riesling
76	valpolicella


#### 24. Which artists have popularity values of 98?

```
SELECT COUNT(*)
FROM artists
WHERE popularity = 98
```

##### Expected Output
count
3

#### 25. Return the values from all columns in the table artists where nationality is equal to 'Mexican'.
```
SELECT *
FROM artists
WHERE nationality = 'Mexican';
```

##### Expected Output
artist_id	name	nationality	birth_date
19	Cecilia Suárez	Mexican	1971-11-22
21	Verónica Castro

#### 26. Return the average of the popularity column in the tracks table.

```
SELECT ROUND(AVG(popularity) , 0) AS avg_popularity
FROM tracks;
```

##### Expected Output
avg_popularity
46

#### 27. You are analyzing nutritional information on food items on the menu of a restaurant. They want to know the average number of calories per 100g in items on their menu. Calories per 100g is contained in the energy column. You have calculated the average but you want to update your code to make it clear what the value shows, returning the column name as avg_calories.
```
SELECT AVG(energy) AS avg_calories
FROM food
```

##### Expected Output:
avg_calories
187.8333333333333333

#### 28. You have joined two tables, wine_region and pairing, to find wines that match food items. You now want to clean up your code so that you don't need to repeat the table names throughout. Shorten the table names to w and p.
```
SELECT w.style, p.item
FROM wine_region AS w
LEFT JOIN pairing AS p
	ON w.id = p.wine_id
ORDER BY style
```

##### Expected Output:
style	item
alvarinho	oysters
blanc de blanc	caviar
cabernet	lamb
gavi	
malbec	steak
pinot noir	salmon
primitivo	curry
riesling	roast duck
valpolicella	grilled vegetables

#### 29. Return the first_name of all employees in the employee table.

--employees
| employee_id | first_name | last_name |
|-------------|------------|-----------|
| 4430        | Betty      | Summers   |
| 6561        | Mary       | Hogan     |
| 8795        | Pearl      | Valdez    |
| 8808        | Molly      | Kramer    |
| 1036        | Hafza      | Hess      |

```
SELECT first_name
FROM employees
ORDER BY first_name
LIMIT 5;
```
##### Expected Output
first_name
Betty
Darren
Hafza
Hugo
Jack

#### 30. The food table gives nutritional information about various items served in a restaurant. Return the item, energy and protein columns ordered by protein so that high protein foods appear first.
```
SELECT item, energy, protein
FROM food
ORDER BY protein DESC
```

##### Expected Output
item	energy	protein
lasagne	188	11.76
tacos	180	10.94
croissant	343	5.71
chicken salad	110	5
waffles	200	4.29
thai curry	106	 3.18


#### 31. The wine table, whose structure is shown below, contains information about a selection of wines offered by a restaurant. How much would it cost to buy a single bottle of all of the wines on offer? The cost of a single bottle is given in the price column and there are no duplicates in the data.
```
SELECT SUM(price)
FROM wine
```

##### Expected Output:
sum
120.82


#### 32. Sort artists by the number of followers from the biggest to smallest using the artists table.

--artists
| id     | followers | name          | popularity |
|--------|-----------|---------------|------------|
| 1uNFoZ | 44606973  | Justin Bieber | 100        |
| 06HL4z | 38869193  | Taylor Swift  | 98         |
| 3TVXtA | 54416812  | Drake         | 98         |

```
SELECT name, followers
FROM artists 
ORDER BY followers DESC 
LIMIT 10;
```

##### Expected Output:
name	followers
Ed Sheeran	78900234
Ariana Grande	61301006
Drake	54416812
Justin Bieber	44606973
Eminem	43747833
Rihanna	42244011
Billie Eilish	41792604
Taylor Swift	38869193
Imagine Dragons	33665795
Queen	33483326


#### 33. The favorite shows of a small group of subscribers is recorded in the favorite table. The titles of the shows were not entered consistently. Convert all the values in the title column to lower case.

```
SELECT user_id,
       lower(title) AS title_lower
FROM favorite
ORDER BY user_id, title_lower
LIMIT 5;
```

##### Expected Output
user_id	title_lower
23	elite
23	money heist
43	stranger things
45	you
87	you


#### 20. Due to a database error, the column followers of the artists was incorrectly increased by 1000. Correct the mistake by subtracting 1000 from the followers column.

#### 21. For each vendor_name in the vendors table, ensure that only the first letter of each word is upper case e.g. DATACAMP would become Datacamp.

## Topic-5
# DATA-MANAGEMENT-IN-POSTGRESQL

#### 1. From the movie_budget table, return the first five rows where the title doesn't contain the character a only in lowercase.
-- movie_budget
|   Year  |   Title                  |   Budget       |
|---------|--------------------------|----------------|
|   1915  |   The Birth of a Nation  |   $110,000.00  |
|   1916  |   Intolerance            |   $489,653.00  |
|   1917  |   Cleopatra              |   $300,000.00  |
|   1918  |   Mickey                 |   $250,000.00  |
|   1919  |   The Miracle Man        |   $120,000.00  |
| ...     | ...                      | ...            |

Solution:
```
SELECT *
FROM movie_budget
WHERE title NOT LIKE '%a%'
LIMIT 5;
```

Expected Output:
|   Year  |   Title                  |   Budget       |
|---------|--------------------------|----------------|
|   1918  | Mickey	                | $250,000.00    |
|1925	|Ben-Hur|	$3,967,000.00|
|1927	|Wings	|$2,000,000.00|
|1928	|The Singing Fool|	$388,000.00|
|1929|	Sunny Side Up|	$600,000.00|


2.
Statement:
To calculate the average price for each category from the fruit_2022 table, ensure that the calculation only includes the prices using kg as the unit.

--fruit_2022
|   category   |   variety            |   price  |   unit  |
|--------------|----------------------|----------|---------|
|   fruit      |   bramleys_seedling  |   2.05   |   kg    |
|   fruit      |   coxs_orange_group  |   1.22   |   kg    |
| ...          | ...                  | ...      | ...     |
|   vegetable  |      savoy           |   0.51   |   head  |
| ...          | ...                  | ...      | ..      |

Solution:
```
SELECT category, 
       AVG(price) AS avg_price
FROM fruit_2022
WHERE unit = 'kg'
GROUP BY category;
```
Expected Output:

|category|	avg_price|
|--------|--------------|
|fruit|	1.2386075949367089|
|vegetable|	1.3434090909090909|


##### 3. Statement: From the vendors table, return the vendors in SEATTLE or AUSTIN city.

--vendors
|   vendor_name             |   vendor_city     |   vendor_state  |
|---------------------------|-------------------|-----------------|
|   CHONZIE INC             |   ASHEVILLE       |   NC            |
|   INREACH ONLINE CLE      |   AUSTIN          |   TX            |
|   HENDERSONVILLE JEEP CH  |   HENDERSONVILLE  |   NC            |
|   ....................... |   ............... |   ..      

Solution:
```
SELECT vendor_name,vendor_city,vendor_state
FROM vendors
WHERE vendor_city IN ('SEATTLE','AUSTIN');
```
Expected Output

vendor_name	vendor_city	vendor_state
INREACH ONLINE CLE	AUSTIN	TX
AMAZON CAPITAL SERVICES, INC.	SEATTLE	WA
SPEAKWRITE LLC	AUSTIN	TX
AMZN MKTP US	SEATTLE	WA


4.
Statement:
From the fruit_2022 table, return the rows with the top 3 highest prices.

-- fruit_2022
|   variety            |   date      |   price  |
|----------------------|-------------|----------|
|   bramleys_seedling  | 11-MAR-2022 |   2.05   |
|   coxs_orange_group  | 11-MAR-2022 |   1.22   |
|   egremont_russet    | 11-MAR-2022 |   1.14   |
|   braeburn           | 11-MAR-2022 |   1.05   |
|   gala               | 11-MAR-2022 |   1.03   |

Solution:
```
SELECT variety,date,price
FROM fruit_2022
ORDER BY price DESC
LIMIT 3;
```
Expected Output:
variety	date	price
bramleys_seedling	11-MAR-2022	2.05
coxs_orange_group	11-MAR-2022	1.22
egremont_russet	11-MAR-2022	1.14


##### 5. From the movie_budget table, return the year with more than 3 movies in the table.

-- movie_budget
|   year  |   title                  |   budget         |
|---------|--------------------------|------------------|
|   1915  |   The Birth of a Nation  |   $110,000.00    |
|   1916  |   Intolerance            |   $489,653.00    |
| ...     | ...                      | ...              |
|   1925  |   Ben-Hur                |   $3,967,000.00  |
| ...     | ...                      | ...              |

Solution:
```
SELECT year, COUNT(*) AS n_of_movies
FROM movie_budget
GROUP BY year
HAVING COUNT(*) > 3;
```

Expected Output:
year	n_of_movies
1933	4


##### 6. From the bike_stations table, convert the Station_ID column to INTEGER data type.

-- bike_stations
|   Station_ID  |   Latitude   |   Longitude    |
|---------------|--------------|----------------|
|   3045.0      |   34.028511  |   -118.25667   |
|   3046.0      |   34.05302   |   -118.247948  |
|   3055.0      |   34.044159  |   -118.251579  |

Solution:
```
SELECT Station_ID :: INT,
       Latitude,
       Longitude
FROM bike_stations;
```

Expected Output:
station_id	latitude	longitude
3045	34.028511	-118.25667
3046	34.05302	-118.247948
3055	34.044159	-118.251579


##### 7. From the speaker table, return the number of speakers per year in descending order.

-- speaker
|   model                             |   price  |   launch      |
|-------------------------------------|----------|---------------|
|   Bowers & Wilkins Formation Wedge  |   899    |   2019-06-01  |
|   Harman Kardon Citation 200        |   349    |   2020-09-01  |
|   Sonos Five                        |   499    |   2021-06-01  |
| ...                                 | ...      | ...           |

Solution:
```
SELECT  EXTRACT(year FROM launch) AS year,
        COUNT(*) AS number_of_speakers
FROM speaker
GROUP BY year
ORDER BY number_of_speakers DESC;
```
Expected Output:
year	number_of_speakers
2020	15
2021	12
2019	7
2018	6
2017	3
2022	1
2016	1


##### 8. Based only on the preview shown, which column has missing values in the speaker table?

-- speaker
|   model                             | price |  launch     |  overall  |
|-------------------------------------|-------|-------------|-----------|
|   Bowers & Wilkins Formation Wedge  |  899  |  2019-06-01 |   160     |
|   Harman Kardon Citation 200        |  349  |  ''         |   147     |
|   Sonos Five                        |       |  2021-06-01 |    0      |

Solution:
The model column
The price column ✔️
The launch column
The overall column


##### 9. In the vendors table, some entries in the zip_code have 9 digits. Return a zip_code column that only contains the first 5 digits from the zip_code column.

-- vendors
| vendor_name                               | zip_code   |
|-------------------------------------------|------------|
| CHONZIE INC                               | 28803      |
| VAUGHN & MELTON CONSULTING ENGINEERS,INC. | 28806-1721 |
| TEG LEASE FEE                             | 339073835  |

Solution:
```
SELECT vendor_name, 
      LEFT(zip_code,5) AS zip_code
FROM vendors;
```

Expected Output:
vendor_name	zip_code
CHONZIE INC	28803
VAUGHN & MELTON CONSULTING ENGINEERS,INC.	28806
TEG LEASE FEE	33907


##### 10. From the fruit_2022 table, you want to know which item in the vegetable category has an average price higher than 2.

--fruit_2022
|   category   |   item      |   variety            |   price  |
|--------------|-------------|----------------------|----------|
|   fruit      |   apples    |   bramleys_seedling  |   2.05   |
|   fruit      |   apples    |   coxs_orange_group  |   1.22   |
| ...          | ...         | ...                  | ...      |
|   vegetable  |   beetroot  |   beetroot           |   0.52   |
| ...          | ...         | ...                  | ..       |

Solution:
```diff
SELECT item,
       AVG(price) AS avg_price
FROM fruit_2022
+ WHERE category = 'vegetable'
GROUP BY item
HAVING AVG(price) > 2;
```

Expected Output:
item	avg_price
curly_kale	3.2700000000000000
pak_choi	3.3880000000000000
rhubarb	4.9107692307692308


##### 11. Add the rows from the movie_2010 table to movie_2000 but keep the duplicates.

-- movie_2000
| year    | title                    | budget       |
|---------|--------------------------|--------------|
|   2000  |   Mission: Impossible 2  |   125000000  |
|   2004  |   Shrek 2                |   150000000  |
|   2008  |   The Dark Knight        |   185000000  |
|   2010  |   Toy Story 3            |   200000000  |
-- movie_2010
|   year  |   title                            |   budget       |
|---------|------------------------------------|----------------|
|   2010  |   Toy Story 3                      |   200000000    |
|   2014  |   Transformers: Age of Extinction  |   210000000    |
|   2015  |   Star Wars: The Force Awakens     |   245000000    |
|   2016  |   Captain America: Civil War       |   250000000    |

Solution:
```
SELECT *
FROM movie_2000
UNION ALL 
SELECT *
FROM movie_2010
ORDER BY year;
```

Expected Output:
year	title	budget
2000	Mission: Impossible 2	125000000
2004	Shrek 2	150000000
2008	The Dark Knight	185000000
2010	Toy Story 3	200000000
2010	Toy Story 3	200000000
2014	Transformers: Age of Extinction	210000000
2015	Star Wars: The Force Awakens	245000000
2016	Captain America: Civil War	250000000


##### 12. Add the rows from the movie_2010 table to movie_2000 but remove the duplicates.

-- movie_2000
| year    | title                    | budget       |
|---------|--------------------------|--------------|
|   2000  |   Mission: Impossible 2  |   125000000  |
|   2004  |   Shrek 2                |   150000000  |
|   2008  |   The Dark Knight        |   185000000  |
|   2010  |   Toy Story 3            |   200000000  |
-- movie_2010
|   year  |   title                            |   budget       |
|---------|------------------------------------|----------------|
|   2010  |   Toy Story 3                      |   200000000    |
|   2014  |   Transformers: Age of Extinction  |   210000000    |
|   2015  |   Star Wars: The Force Awakens     |   245000000    |
|   2016  |   Captain America: Civil War       |   250000000    |

Solution:
``` 
SELECT *
FROM movie_2000
UNION 
SELECT *
FROM movie_2010
ORDER BY year;
```

Expected Output:
year	title	budget
2000	Mission: Impossible 2	125000000
2004	Shrek 2	150000000
2008	The Dark Knight	185000000
2010	Toy Story 3	200000000
2014	Transformers: Age of Extinction	210000000
2015	Star Wars: The Force Awakens	245000000
2016	Captain America: Civil War	250000000


##### 13. For the vendors table, return the number of the rows without missing values in the vendor_state column.

-- vendors
|   vendor_name       |   vendor_city  |   vendor_state  |
|---------------------|----------------|-----------------|
|   CHONZIE INC       |   ASHEVILLE    |   NC            |
| ...                 | ...            | ...             |
|   WEBSEDGE LIMITED  |   LONDON       |                 |
| ...                 | ...            | ...             |

Solution:
```
SELECT COUNT(*) 
FROM vendors
WHERE  vendor_state IS NOT NULL ;
```

Expected Output:
count
286


##### 14. Join the bike_trips table with bike but keep all the records from bike_trips no matter whether they have a match in bike.

-- bike_trips
| trip_ID | duration | bikeID |
|---------|----------|---------|
|     364 | 60       | 5000    |
|     365 | 900      | 2300    |
|     366 | 720      | 5002    |
-- bike
| bike_ID | last_date_in_use | color |
|---------|------------------|-------|
|    2300 |      2020-04-15  | blue  |
|    2350 |      2020-04-15  | green |
|    3000 |      2020-04-18  | green |

Solution:
```
SELECT Trip_ID, Duration, bikeID, last_date_in_use, color 
FROM bike_trips AS t
LEFT JOIN bike AS b
ON t.bikeID = b.bike_ID;
```

Expected Output
trip_id	duration	bikeid	last_date_in_use	color
365	900	2300	2020-04-15	blue
364	60	5000		
366	720	5002


##### 15. From the movie_budget table, return the movie title which only includes four letters. e.g. the movie Bean has four letters.

-- movie_budget
|   year  |   title                  |   budget         |
|---------|--------------------------|------------------|
|   1915  |   The Birth of a Nation  |   $110,000.00    |
|   1916  |   Intolerance            |   $489,653.00    |
| ...     | ...                      | ...              |
|   1925  |   Ben-Hur                |   $3,967,000.00  |
| ...     | ...                      | ...              |

Solution:
```
SELECT *
FROM movie_budget
WHERE title LIKE '____';
```

Expected Output:
year	title	budget
1975	Jaws	$9,000,000.00


## Topic-6
# MACHINE LEARNING FUNDAMENTALS IN PYTHON

#### 1. x_train and y_train are explanatory and response variables, respectively, used to fit a linear model, stored in the variable reg. Use reg to predict the value of the response variable y_test as a function of the explanatory variable x_test.

```diff
import numpy as np
import pandas as pd
from sklearn.linear_model import LinearRegression
reg = LinearRegression()
reg.fit(x_train, y_train)
- predictions = reg.predict(X_test)
+ predictions = reg.predict(x_test)
print(predictions)
```

#### Expected Output
[[22.]
 [24.]
 [26.]
 [28.]
 [30.]
 [32.]
 [34.]
 [36.]
 [38.]
 [40.]
 [42.]]
 
 #### 2. The following is a preview of the data df. One-hot encode the Animal variable.

|  |Age |  Animal | Weight|
|--|----|---------|-------|
|0 |  22|  dog    |   68.7|
|1 |  38|  cat    |   89.8|
|2 |  56|  cat    |   77.4|
|3 |  21|  dog    |   77.3| 
|4 |  43|  fish   |   82.8|

```
import pandas as pd
encoded = pd.get_dummies(df, columns=['Animal'])
print(encoded)
```

Expected Output
|   | Age|  Weight  |  Animal_cat | Animal_dog | Animal_fish|
|---|----|----------|-------------|------------|------------|
|0  | 22 |   68.7   |        0    |       1      |      0|
|1  | 38 |   89.8   |        1    |       0      |      0|
|2  | 56 |   77.4   |        1    |       0      |      0|
|3  | 21 |   77.3   |        0    |       1      |      0|
|4  | 43 |   82.8   |        0    |       0      |      1|

#### 3. Fit a Logistic Regression model to the binary data.

|x  | y  |
|---|----|
|0  |  0|
|1  |  1|
|2  |  0|
|3  |  0|
|...|...|

```
from sklearn.linear_model import LogisticRegression
model = LogisticRegression(random_state=1)
model.fit(x, y)
print(model.score(x, y))
```

## 4.  Calculate the mean of the array x, whose distribution is shown in the plot.

![137](https://user-images.githubusercontent.com/61821924/213921151-61761dd4-c1cb-4a12-90aa-ed547ab000d5.png)
```
import numpy as np
result = np.mean(x)
print(result)
```

#### Expected Output
0.01933205582232549
 
#### 5. Available in this session are the training (X_train, y_train) and test (X_test, y_test) sets. Fit a classification random forest model and then use the model to make predictions using the test data.

```diff
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score
model = RandomForestClassifier(n_estimators=300, max_depth=1, random_state=1)
model.fit(X_train, y_train)
- y_pred = model.predict(x_TEST)
+ y_pred = model.predict(X_test)
print(accuracy_score(y_test, y_pred))
```

Expected Output
0.9333333333333333 
 
#### 6. Available in your working session is the dataset scaled_samples. Instantiate a principal component analysis model object with 2 components, and fit the model to the scaled_samples object.
```
from sklearn.decomposition import PCA
pca = PCA(n_components=2)
pca.fit(scaled_samples)
pca_features = pca.transform(scaled_samples)
print(pca_features.shape)
```

#### Expected Output
(85, 2)
 
#### 7. You have created a k-means clustering model customer_model. The model groups customers into 5 classes. You now receive new data describing a set of 5 customers (X_new). Determine to which clusters they belong.
``` 
predictions = customer_model.predict(X_new)
print(predictions)
```
#### Expected Output
[1 3 4 4 3]
 
#### 8. A LogisticRegression model is fitted on the training data X_train and y_train, and stored in model. Use model and the X_test feature data to predict values for the response variable, and store it in y_pred. Then get the model score using X_test and y_test.
```
from sklearn.linear_model import LogisticRegression
model = LogisticRegression(random_state=1)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
score = model.score(X_test, y_test)
print(score)
```
#### Expected Output
0.9517543859649122 
 
 #### 9. Available in this session are the training data X_train and y_train for feature and target variables, respectively; as well as the testing data X_test and y_test for feature and target variables, respectively. Using sklearn, fit a classification decision tree model on X_train and y_train.
```
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import accuracy_score
model = DecisionTreeClassifier(max_depth=4, random_state=1)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
print(accuracy_score(y_test, y_pred))
```
#### Expected Output
0.9833333333333333
 
#### 10. A dataset has been prepared for you and split into test and training sets (X_train, X_test, y_train, y_test). Show the importance of each feature in the gradient boosting model that is fitted to the data
```diff
from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier(random_state=42)
model.fit(X_train, y_train)
+ importances = model.feature_importances_
+ feature_importances  = pd.Series(importances, wine_feat.columns)
print(feature_importances)
```
#### Expected Output
Alcohol       0.392
Malic.acid    0.266
Ash           0.110
Acl           0.231
dtype: float64 

#### 11. Using the original data, df, training (X_train, y_train) and test (X_test, y_test) sets have been created. Complete the code using the data sets in the appropriate places.
```diff
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error
lin_reg = LinearRegression()
+ lin_reg.fit(X_train,y_train)
+ predictions = lin_reg.predict(X_test)
+ print("Mean squared error: %.2f" % mean_squared_error(y_test, predictions))
```
#### Expected Output
Mean squared error: 8.47

#### 12. You are supplied with continuous variables in the NumPy arrays X and y. Build an appropriate model on the target array y using the features of X. Display the coefficient and intercept for the resulting model.
```diff
+ from sklearn.linear_model import LinearRegression
+ model = LinearRegression()
model.fit(X,y)
+ print("Regression coefficients: {}".format(model.coef_))
+ print("Regression intercept: {}".format(model.intercept_))
```
#### Expected Output
Regression coefficients: [[1.33333333]]
Regression intercept: [-1.0658141e-14]

#### 13. Determine if 50, 150 or 250 is the best value for the n_estimators hyperparameter of a random forest classifier.
```
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import GridSearchCV
model_params = {'n_estimators': [50, 150, 250]}
rf = RandomForestClassifier(random_state=42)
clf = GridSearchCV(rf, model_params, cv=5)
clf.fit(X_train, y_train)
print(clf.best_params_)
```
#### Expected Output
{'n_estimators': 150}

#### 14. Which of the following metrics would not be used when assessing the performance of a classification model?
- [ ] Area under the curve
- [ ] Precision
- [ ] Recall
- [x] Median absolute error

#### 15. You are supplied with a dataset assigned to the variable scaled_data. This dataset exhibits high dimensionality, you need to reduce it to 3 features.
```
from sklearn.decomposition import PCA
reducing_fn = PCA(n_components=3)
reducing_fn.fit(scaled_data)
reduced_ft = reducing_fn.transform(scaled_data)
print(reduced_ft.shape)
```
#### Expected Output
(85, 3)

#### 16. The scatterplot shows data for a sample of 14 biofuels. Fit a linear regression model and print the intercept and coefficient. x = iodine value (g), y = cetane number

![138](https://user-images.githubusercontent.com/61821924/213922409-03005484-06a6-45db-913f-b7348b911a73.png)
```
from sklearn.linear_model import LinearRegression
model = LinearRegression(fit_intercept=True)
model.fit(x, y)
print("Regression coefficients: {}".format(model.coef_))
print("Regression intercept: {}".format(model.intercept_))
```
#### Expected Output
Regression coefficients: [[-0.20938742]]
Regression intercept: [75.21243193]

#### 17. A LogisticRegression model is fitted on the training data X_train and y_train, and stored in model. Use model and the X_test feature data to predict values for the response variable, and store it in y_pred. Then get the model score using X_test and y_test.
```
from sklearn.linear_model import LogisticRegression
model = LogisticRegression(random_state=1)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
score = model.score(X_test, y_test)
print(score)
```
#### Expected Output
0.9517543859649122

#### 18. The Pandas DataFrame df is loaded on your working session. Using the scipy package, implement k-means clustering (with two centroids) on the columns x_scaled and y_scaled.
```
from scipy.cluster.vq import kmeans, vq
+ clusters = kmeans(
	df[['x_scaled', 'y_scaled']],
	2
)
print(clusters)
```
#### Expected Output
(array([[2.64462017, 2.17073744],
       [0.66058434, 0.15108795]]), 0.20140463751291524)

#### 19. x and y are Numpy arrays available in this session. Use them to fit a linear model, stored in the reg variable.
```
import numpy as np
import pandas as pd
from sklearn.linear_model import LinearRegression
reg = LinearRegression()
reg.fit(x, y)
print("Regression coefficients: {}".format(reg.coef_))
print("Regression intercept: {}".format(reg.intercept_))
```
#### Expected Output
Regression coefficients: [[2.]]
Regression intercept: [-1.77635684e-15]

#### 20. Overfitting means:
- [ ] We have built a model that will only perform well on previously unseen data.
- [x] We have built a model that will only perform well on the training data.
- [ ] We have spent a lot of the time building a model with no significant improvement
- [ ] We have built a model that will give reasonable results on any data.

#### 21. A medical researcher is looking to group species of bacteria based on their responsiveness to different antibiotics. What model should he use on his data?
 - [ ] Linear regression
 - [ ] Decision trees
 - [ ] Logistics regression
 - [ ] K-means clustering

#### 22. Are small or large residuals desired?
- [x] Residuals refer to the error values of a model and therefore smaller residuals are desirable
- [ ] Residuals refer to the error values of a model and therefore larger residuals are desirable
- [ ] Residuals refer to the error values of a model and therefore constant residuals are desirable
- [ ] The overall goal will determine whether small or large residuals are desired.

#### 23. A series of predicted values, y_pred, have been calculated from the fitted model, lin_reg. The data has been split into training and test sets. Choose the appropriate metric to assess the predictive performance.
```
from sklearn.linear_model import LinearRegression
from sklearn import metrics
lin_reg = LinearRegression()
lin_reg.fit(X_train,y_train)
y_pred = lin_reg.predict(X_test)
score = metrics.mean_squared_error(y_test, y_pred)
print(score)
```

#### Expected Output
8.474832262021076

#### 24. Calculate the mean of the array x, whose distribution is shown in the plot.

![139](https://user-images.githubusercontent.com/61821924/213922689-27d06940-7161-438e-874e-1550c3488ec2.png)
```
import numpy as np
result = np.mean(x)
print(result)
```

#### Expected Output
0.01933205582232549

#### 25. Which of the following best describes a decision tree?
- [ ] An algorithm that reduces the number of variables to a set of principal variables.
- [x] An algorithm with a sequence of if-else questions about the individual features used to infer the target variable
- [ ] An algorithm that describes a continuous response variable as a function of one or more predictor variables
- [ ] An algorithm that splits unlabled data into groups based on feature simalarities

#### 26. Available in this session are the training data X_train and y_train for feature and target variables, respectively; as well as the testing data X_test and y_test for feature and target variables, respectively. Using sklearn, fit a classification decision tree model on X_train and y_train.
```
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import accuracy_score
model = DecisionTreeClassifier(max_depth=4, random_state=1)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
print(accuracy_score(y_test, y_pred))
```
#### Expected Output
0.9833333333333333

#### 27. A simple linear regression model is fitted to data of a company's advertising budget and their sales. What is the relationship between a company's advertising budget and their sales as described by the regression model output below?

Regression coefficients: [[0.1]]
Regression intercept: [7]
Regression score: 0.9

- [ ] If the company increases their advertising budget by $1000, then there will be no change in sales.
- [ ] If the company increases their advertising budget by $1000, their sales will most likely decrease by $100.
- [x] If the company increases their advertising budget by $1000, their sales will most likely increase by $100.
- [ ] If the company increases their advertising budget by $1000, their sales will most likely increase by $70.

#### 28. Before we fit a model to our data we should consider centering and scaling the data so that:

- [ ] It's easier to interpret the model output because the variables are the same values
- [x] A feature does not have more influence on the model because of larger or smaller values
- [ ] We can remove outliers from the data because they will all be on the same range
- [ ] We can use both the original and scaled version of the variables in our model

#### 29. Which one of the following statements describes an unsupervised learning problem?

- [ ] A machine learning where we predict a caregorical variable as a function of both continuous and categorical variables
- [x] A machine learning where we seek to understand whether observations fit into distinct groups based on their similarities
- [ ] A machine learning problem where we fit a model a response variable as a function of a set of predictor variables
- [ ] A machine learning problems that deals with the importing and cleaning of a dataset, such that it is tidy

#### 30. Which of the following best describes linear regression?
- [ ] An algorithm that reduces the number of variables for data-modeling to a set of so-called principal variables
- [x] An algorithm that describes a continuous response variable as a funtion of one or more predictor variables
- [ ] An algorithm that describe a factor response variable as a function of one or more predictor variable
- [ ] An algorithm that splots data into groups based on feature similarities. 
