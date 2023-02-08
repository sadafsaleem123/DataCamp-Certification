# 1. 
```
import unittest

class TestSampleMethod(unittest.TestCase):

    def test_sum(self):
          self.assertEqual(sum(2,2), 4)
```

- The code **import unittest** at the top of the file imports the unittest module, which provides a framework for writing and running tests.
- The code **class TestSampleMethod(unittest.TestCase):** defines a new class **TestSampleMethod** that inherits from unittest.TestCase. This makes TestSampleMethod a test case, which allows us to run tests and make assertions about the behavior of the code we are testing.
- The code **def test_sum(self):** defines a method **test_sum** inside TestSampleMethod. This method is a test case and will be executed as part of the test suite.
- The line **self.assertEqual(sum(2,2), 4)** is the actual test. It uses the assertEqual method of the TestCase class to make an assertion about the expected behavior of the sum method. 
- The **assertEqual** method takes two arguments and checks if they are equal. In this case, it checks if sum(2,2) returns 4. If the assertion passes, the test is considered to have passed. If the assertion fails, the test is considered to have failed and an error will be reported.

In data science, unit tests are used to verify that individual pieces of code, such as functions or methods, are working correctly. Unit tests ensure that changes to the code, such as bug fixes or updates, do not break existing functionality.


# 2. 
```
from sklearn.datasets import make_blobs
```
- It imports the **make_blobs** function from the **sklearn.datasets** module in the scikit-learn library. 
- **make_blobs** is a function that generates clusters of random data points for use in machine learning. It creates blobs of points that are randomly distributed around a central point, which can then be used to test and train clustering algorithms. In simple terms, it's used to create fake data for testing purposes.

# 3.

```
from sklearn.cluster import KMeans
```
- **from sklearn.cluster import KMeans** is a Python code that imports the **KMeans** class from the **sklearn.cluster** module in the **scikit-learn** library. 
- The KMeans class is a popular implementation of the k-means clustering algorithm. 
- Clustering is a machine learning technique used to divide a set of objects into groups (clusters) based on the similarity between the objects. 
- The k-means algorithm is a specific type of clustering that partitions the data into k clusters, where k is a user-defined number. The algorithm iteratively finds the k cluster centers and assigns each data point to the nearest cluster center, until the cluster centers no longer change.


# 4.
```
import matplotlib.pyplot as plt
```
- **matplotlib** is a data visualization library in Python that provides functions for creating static, animated, and interactive visualizations in Python. 
- The **pyplot** module provides a convenient interface for plotting data and creating charts and graphs. With pyplot, you can plot data, create histograms, bar charts, line graphs, scatter plots, and more. 
- By importing the module as **plt**, you can use its functions with a short and convenient alias (e.g., plt.plot() instead of matplotlib.pyplot.plot()).

# 5.
```
import seaborn as sns
```
- **seaborn** is a data visualization library based on matplotlib that provides a high-level interface for creating attractive and informative statistical graphics. 
- It has built-in support for plotting a variety of statistical models and visualizations, including histograms, violin plots, box plots, scatter plots, heatmaps, and more. 
- The seaborn library is widely used for data exploration and visualization in the field of data science and machine learning.


## Question? 
### Why we use seaborn library when we have matplotlib for data visualization?
- matplotlib and seaborn are both powerful libraries for data visualization in Python, but seaborn is built on top of matplotlib and offers several additional features and benefits:
- seaborn has a more visually appealing default style for its plots, with little to no additional effort.
- seaborn has a built-in support for statistical visualizations, making it easier to explore and visualize complex datasets.
- Easy to use interface: seaborn has a high-level interface for plotting, which can save you time and effort compared to using matplotlib directly. 
- Built-in color palettes: seaborn provides a wide range of color palettes for creating visually appealing visualizations.

In summary, seaborn is a convenient and powerful tool for data visualization in Python, especially for exploring and visualizing statistical data. It's often used in addition to matplotlib to create more visually appealing and informative visualizations.


# 6.
```
import pandas as pd
```


# 7.
```
import statsmodels.api as sm
```


# 8.
```
from sklearn import linear_model
```


# 9.
```
import statsmodels.formula.api as smf
```


# 10.
```
import requests
url = 'https://jsonplaceholder.typicode.com/posts/1'
response = requests.get(url)
data = response. json()
print(data)
```
