• Data Types
• Statics of Data
• Similarity and Distance Measures
• Data Quality, Data Cleaning and Data Integration
• Data Transformation
• Dimensionality Reduction

<hr>

## Introduction
The first step in the data mining process is *data pre-processing*, which involves the acquiring of *knowledge* from the raw data.

The specific characteristics that we search for during data pre-processing are the various *attribute types*:
1. **Nominal** attributes
2. **Binary** attributes
3. **Ordinal** attributes
4. **Numeric** attributes
From these attributes, we can obtain basic *statistical descriptions* or the measures of **central tendency**:
1. **Mean** (average value)
2. **Median** (middle value)
3. **Mode** (most common value)
These measures of **central tendency** provide us insight on the centre of distribution.

We can further analyse the data distribution's central tendency through *data visualisation*. If we visualise the data through graphs, we can make important observations regarding the **skewing** of the data or the **symmetric** characteristics of the data. We can identify **quantile plots** and develop **histograms** and **scatterplots**. These visualisation techniques can allow us to estimate missing values, smoothen noise values, spot outliers, and identify patterns and trends which may be useful to us.

Data visualisations also allow us to assess the **similarity** and **dissimilarity** between two *data objects*. These measures of **similarity/dissimilarity** are known as **proximities**. **Proximities** are the functions of the **distance** between the attribute values of two different data objects. 

Attribute Types --> Statistical Measures --> Central Tendency --> Dispersion of Data --> Data Visualisation --> Similarity/Dissimilarity

Terms: **[Nominal, Ordinal, Binary, Numeric], [Mean, Median, Mode], [Skew, Symmetry, Histogram, Scatterplot], [Similarity, Dissimilarity, Distance, Proximity]**

## Data Objects & Attribute Types
A data object can be described as having different *characteristics*. Characteristics that consist of different possible values are called *attributes*. Since there can be many different characteristics that describe an object, there are different *attribute types*. In data analysis, these attribute types are categorised as:
- Nominal Attributes
- Binary Attributes
- Ordinal Attributes
- Numeric Attributes
#### Nominal Attributes
- *Nominal* means "of names".
- A nominal attribute is an attribute where the possible values are different states of the object.
- Suppose there is a data object *Dog*. A dog can be of many different breeds, each having its own name or label. Thus a dog breed is *nominal* or "of names". The data object *Dog* would have a nominal attribute *Breed* which can have the nominal values of ['German Shepherd', 'Husky', 'Chihuahua', etc].
#### Binary Attributes
- *Binary* means "of two".
- A binary attribute is a type of nominal attribute where there are only two possible values.
- For the data object *Dog*, there can be a nominal attribute which describes the dog sex. A dog can only have two different sexes, *male* and *female*. These nominal values describe a particular state for the dog. Thus *Sex* is a binary attribute.
- Binary attributes can be either **symmetric** or **asymmetric** depending on the weight of each binary value. If both values are equal in weight, the binary attribute is **symmetric**. If one of the values weighs more than the other, the binary attribute is **asymmetric**.

#### Ordinal Attributes
- *Ordinal* means "of order".
- An ordinal attribute is an attribute whose possible values correspond to a meaningful order or ranking. 
- Suppose there is a data object *Drink*. A drink can come in several different sizes ranging from extra small to extra large. The attribute *Size* can consist of ['XS', 'S', 'M', 'L', 'XL']. These attribute values appear to follow a meaningful order, where 'XS' is smaller than 'S' which is smaller than 'M', and so on. Thus *Size* is an ordinal attribute.

#### Numeric Attributes
- *Numeric* means "of numbers".
- A numeric attribute is an attribute whose possible values are quantitative represented as either integers or real values.
- Suppose there is a data object *Exam*. The exam can have different possible scores represented as a percentage of a total. The possible values can be [0...100]. These values are all numeric, consisting of integers and real numbers. Thus the attribute *Score* would be a numeric attribute.
- Numeric attributes can either be **interval-scaled** or **ratio-scaled**. 
- **Interval-scaled**:
	- Measured on a scale of equal sized units.
	- Following an order and can be positive, negative, or 0.
	- Example: Temperature which can scale from a negative value to 0 to a positive value.
- **Ratio-scaled**:
	- Measured with respect to a set zero-point.
	- Following an order and can be positive or 0. Values cannot be negative.
	- Example: The Kelvin scale does not go below 0.
### Discrete vs Continuous Attributes
Nominal, binary, ordinal, and numerical attribute types are distinct categorizations for attributes, but they are not mutually exclusive i.e. binary attribute can be nominal or numerical, or both. However, with **discrete** and **continuous** attributes, there cannot be an attribute that is both **discrete** and **continuous**.

**Discrete attributes**:
- A discrete attribute has a finite or countably infinite set of values which may or may not be represented as integers. 
- The attributes *Breed*, *Sex*, *Size*, consist of possible value sets that are of a finite size. This makes these attribute types **discrete**.
- The attribute *Score* can have a value anywhere between 0 and 100, which is infinite. However, the grades on an exam are calculated depending no the answers to each question. Each question consists of different *marks*. For example, question 1 on an exam can consist of 5 possible marks, question 2 can consist of 3 possible marks, etc. Although the score is represented as a percent, it is pegged to a countable set of integers i.e. marks. As a result, *Score* is still **discrete**.

**Continuous attributes**:
- A continuous attribute will have an infinite set of values which is not countable i.e. the set of values cannot be pegged to integers.
- The attribute *weight* would consist of values ranging from 0 to infinity. However, between 0 and 1, or 1 and 2, etc, there are an infinite number of values. Thus, *weight* is not countably infinite. *Weight* is a continuous attribute.

### Exam Question Example:
Identify the attribute types for the following attributes:
1. Time in terms of AM or PM.
	(a) Nominal, ordinal, interval-scaled, or ratio-scaled?
	 (b) Discrete or continuous?
2. The number of cylinders in an automobile engine.
	(a) Nominal, ordinal, interval-scaled, or ratio-scaled?
	(b) Discrete or continuous?

(1.a)
Given AM and PM, this attribute is **binary** and **nominal** as it contains two different states ['AM', 'PM'].
(1.b)
Given that there are only two different possible values, 'AM' and 'PM', then we can clearly see that there is a finite set of values. Therefore this attribute is **discrete**.
(2.a)
The number of cylinders in an automobile engine can be represented in a quantitative way i.e. a car has 1 cylinder, 2 cylinders, etc. So we can assume that this attribute is *numerical* which implies that it is either *ratio-scaled* or *interval scaled*. There cannot be a negative number of cylinders, so this cannot be *interval-scaled*. The number of cylinders must also follow a particular order i.e. an engine with 1 cylinder is less powerful than an engine with 2 cylinders, 2 cylinders is less powerful than 3 cylinders, etc. Therefore this attribute is **ordinal** and **ratio-scaled**.
(2.b)
There cannot be an infinite amount of cylinders, therefore the number of cylinders is *finite* and **discrete**.

## Statistical Measurements of Data
Statistical measurements for data will help us better understand the significance of the distribution of our data values. Three important statistical measures are:
1. Central Tendency
	1. The central tendency of a data distribution is its centre. The centre of a distribution is important because it represents where most of the data values are placed.
	2. The central tendency is measured through the mean, median, and mode of the data distribution.
2. Dispersion of Data
	1. The dispersion of data measures the data values with respect to their overall position in the distribution.
	2. Dispersion of data is measured through the range, quantiles, interquartile range, five-number summary, boxplots, variance, and standard deviation.
3. Graphical Representation of Data
	1. Graphical representations of data allow us to observe patterns of the distribution in detail.
	2. Common graphical representations include bar charts, pie chars, line graphs, quantile plots, quantile-quantile plots, histograms, and scatter plots.

#### Measuring Central Tendency
The main measurements for central tendency are the mean, median, and mode of a distribution.

##### Mean
The **mean** is the most common and effective measurement of the central tendency. The mean shows us the average of each data value.

Suppose we have an attribute $X$ for the *Salary* of a data object *Employee*. Let $x_1, x_2, ..., x_N$ be a set of $N$ values or *observations* of $X$. We can calculate the **mean** $\bar{x}$ with the following formula:

$$\bar{x} = {{\sum_{i=1}^{N}x_i} \over N} = {{x_1+x_2+...+x_N}\over{N}}$$
The **mean** $\bar{x}$ is essentially the sum of all data values divided by the absolute value of all of the data values.

**_Example_**:
Salary $X$ is represented by the set $[30, 36, 47, 50, 52, 52, 56, 60, 70, 70, 110]$ where each integer represents the salary by each thousand.
To calculate the mean $\bar{x}$, we will use the formula $\bar{x} = { \sum_{i=1}^{N}{x_i} \over {N}}$.
$$\sum_{i=1}^{N}{x_i} = 30 + 26 + 47 + 50 + 52 + 52 + 56 + 60 + 70 + 110 = 696$$
$$N = 12$$
$$\bar{x} = { \sum_{i=1}^{N}{x_i} \over {N}} = {696 \over 12} = 58$$Therefore, the mean salary is $58,000. 😏

Although the mean is often the most useful measure for describing a dataset overall, it is not necessarily always the most useful for describing the **central tendency**. This is due to the sensitivity of the mean - any extreme values will easily throw off the value of the mean. To offset the effects of these outlier values, we can trim these values off to determine the **trimmed mean**. The **trimmed mean** is the mean value obtained from excluding the high and low extreme values.

##### Median
Not all data distributions are symmetric. Most real world data distributions are asymmetric, which means that they are skewed in either a positive or negative direction. If we are to measure the **central tendency**, then simply calculating the mean will not yield us the best information when the distribution is skewed. It is far better to calculate the **median**. The **median** is the middle value of the distribution when the set of values is **ordinal** i.e. the middle value when each value in the data set is ordered from least to greatest. When a data set contains an _odd_ number of values, then the median is simply the single middle value in the ordinal set. When a data set contains an *even* number of values, then the median is the average of the two middle values in the ordinal set.

***Example***:
In a small data set, the median can be easily determined. We will determine the median from the previous set of salaries.
$[30, 36, 47, 50, 52, 52, 56, 60, 63, 70, 70, 110]$ 

Since each value in the data set is already ordered, we can see that the middle values are $52$ and $56$. The median would be the average of these two values: $$median = {{52+56}\over{2}} = 108 \div 2 = 54$$
Let's remove $110$ from this data set, now we have the data set $[30, 36, 47, 50, 52, 52, 56, 60, 63, 70, 70]$. This data set has an *odd* number of values, so the median is the single middle value in this ordinal set, $median = 52$. 😏

A lot of data sets contain a large amount of data values. If we were to calculate the median of a data set with hundreds of values, then ordering every value and looking for the middle values would be a very tedious process. Instead, large data sets are often grouped by frequencies.

***Example***:

| Age | Frequency |
| ---- | ---- |
| $1 - 5$ | $200$ |
| $6 - 15$ | $450$ |
| $16 - 20$ | $300$ |
| $21 - 50$ | $1500$ |
| $51 - 80$ | $700$ |
| $81 - 110$ | $44$ |
In this data set, we have more than one thousand total values. 200 of these values are between 1 and 5, 450 are between 6 and 15, 300 are between 16 and 20, etc.

To calculate the median from this table of grouped data values, we can use the following formula: $$median = L_1 + ({{N \over 2} - (\sum{freq})_1 \over {freq_{median}}})width$$
$L_1$ represents the lower boundary of the median interval.
$N$ represents the number of values in the entire data set.
$(\sum{freq})_1$ represents the sum of the frequencies of all of the intervals that are lower than the median interval.
$freq_{median}$ represents the frequency of the median interval.
$width$ represents the width of the median interval.

The median is the middle value. If we obtain the total number of observations $N$ and divide this cumulative amount by 2, then this would give us the middlemost observation. This middlemost observations would be where the median falls on.

| Age | Frequency | $N$ |
| ---- | ---- | ---- |
| $1 - 5$ | $200$ | $200$ |
| $6 - 15$ | $450$ | $650$ |
| $16 - 20$ | $300$ | $950$ |
| $21 - 50$ | $1500$ | $2450$ |
| $51 - 80$ | $700$ | $3150$ |
| $81 - 110$ | $44$ | $3194$ |

$N = \sum{(frequency)} = 200 + 450 + 300 + 1500 + 700 + 44 = 3194$
$N/2 = 3194/2 = 1597$ therefore the median is the $1597_{th}$ observation.

If the median is the $1597_{th}$ observation, then the median interval would have to be that which contains the $1597_{th}$ observation. If we refer back to the table, we can see that the value $N = 2450$ is at the age range 21 - 50 and $2450 > 1597$. Likewise, the age range below that is 16 - 20 where $N = 950$ and $950 < 1597$. So we can reasonably assume that the observation which the median falls on is in the age range of 21 - 50, therefore the median interval is 21 - 50. 

Since the median interval is 21 - 50, then the lower boundary of the median interval $L_{1} = 21$. Recall that 16 - 20 is the interval right before the median interval where $N = 950$, therefore the sum of the frequencies of all intervals that are lower than the median interval i.e. $(\sum{freq})_{1} = 950$. The median frequency is 21 - 50 and if we refer to the chart we can easily see that $freq_{median} = 1500$. Finally, the width of the median interval $width$ would be the difference between the median interval's upper boundary and the upper boundary of the interval below it i.e. $width = 50 - 20 = 30$ since the upper boundary of the median interval $21 - 50$ is $50$ and the upper boundary of that below the median interval $16 - 20$ is $20$.

Altogether we have isolated the values:
$L_{1} = 21$
$N/2 = 1597$
$(\sum{freq})_{1} = 950$
$freq_{median} = 1500$
$width = 30$

We can plug these values into the median formula to obtain the median:
$median = L_{1} + ({{N/2} - (\sum{freq})_1\over freq_{median}})width$ 
$= 21 + ({1594 - 950 \over 1500})30$ 
$= 30.94$
Therefore the median is $30.94$ years.

##### Mode
Another way of measuring the central tendency is through the **mode** of the data distribution. The **mode** represents the value which occurs the most within a data distribution. Modes can be *qualitative* or *quantitative* and there can be more than one mode. A data distribution with a single mode is *unimodal* whereas a distribution with two modes is *bimodal*, a distribution with three modes is *trimodal*, and so on.

When a data distribution is *skewed* or *asymmetric*, there is an empirical formula which can help us isolate the mean, median, and mode given that we know at least two of those values.
$$mean - mode = 3 \times (mean - median)$$
##### Symmetric and Skewed Data Distributions
We can determine the symmetry of a unimodal data distribution if we know understand the **central tendency** of the data distribution. We can use the mean, median, and mode values of the central tendency to understand the central tendency. 

![[symmetric.png]]
The above data distribution is clearly symmetric. From basic observation, the mean, median, and mode will all fall on the same point. So if we are calculating the mean, median, and mode of a data distribution and we find that they are all equal, we can conclude that the data distribution is **symmetric**.

![[positive.png]]
For positively skewed distributions, the mean is greater than the median the mode is less than the median. It should follow that if we calculate the mean, median, and mode and we find that mean > median and median > mode, the distribution is **positively skewed**.

![[negative.png]]
Likewise for negative skewed distributions, the mode is greater than the median and the mean is less than the median. It should follow that if we calculate the mean, median, and mode and we find that mode > median and median > mean, the distribution is **negatively skewed**.

#### Measuring the Dispersion of Data
Aside from measuring the central tendency, the dispersion of a data set is another way of understanding the data distribution. The dispersion is the overall spread of the data values in the data distribution. There are many different measurements which are used to understand the dispersion of a data set. 
##### Dispersion of Symmetric Distributions
![[quartiles.png]]
A data distribution can be partitioned into smaller subsets. These smaller subsets are called *quantiles*. Usually distributions are divided into four *quantiles*, each quantile being a **quartile**.
The quartiles each represent the spread of the data within specific regions of the overall distribution. When we divide a distribution into four quartiles, we yield three important values regarding the middle of the distribution:
- The first quartile, **Q1** or the 25th percentile.
- The second quartile, **Q2**, 50th percentile, or the **median**.
- The third quartile, **Q3** or the 75th percentile.
From these quartiles, we can derive the **inter-quartile range** which will describe the dispersion of the centre of the data distribution. The **inter-quartile range (IQR)** also helps us identify potential **outliers** using the $1.5\times IQR$ rule. 

We can obtain the IQR from subtracting Q1 from the Q3 i.e. $IQR = Q3 - Q1$.

If a value falls too far outside of the IQR, then we can assume that value is an outlier. The $1.5\times IQR$ rule is a measurement for determining if a value falls too far outside of the IQR:
- If a value is $1.5\times IQR$ greater than Q3, it is an outlier.
- If a value $1.5\times IQR$ less than Q1, it is an outlier.
##### Dispersion of Asymmetric or Skewed Distributions
When a distribution is skewed, the quartiles will not give an accurate portrayal of the overall dispersion of the data. Instead, the **five-number summary** adds more information to give a clearer representation. The **five-number summary** consists of:
- The Minimum value.
- Q1 or the 25th percentile.
- Q2, the 50th percentile, or the median.
- Q3, or the 75th percentile.
- The Maximum value.
With the addition of the Minimum and Maximum values, we can get a better sense for how far off the IQR is from the two tails of the distribution, which will take in for account the skewing of the data distribution.

**Boxplots** are the graphical representations of the five-number summary. If we have several attributes which their own data distributions, representing them as boxplots on one boxplot chart will allow u to easily compare the dispersion of data of each attribute. ![[boxplot.png]]
- The two whiskers protruding from the boxes represent the Maximum and the Minimum values.
- The top and bottom of the boxes represent Q3 and Q1.
- The middle of each box represents Q2 or the median.
- Outliers are plotted as individual points on the chart.

##### Variance & Standard Deviation
The **variance** and **standard distribution** give us information about the position of the data values with respect to the other data values. The **variance** gives us a measure of how far the data values tend to be from the mean of the distribution; The **standard distribution** gives us a measure of how far the data values tend to be from each other.

The variance can be calculated using the following formula: $$\sigma^{2} = ({1\over N} \sum^{N}_{i=1}x_{i}^{2}) - \bar{x}^{2}$$
- $N$ is the number of observations within that data set.
- $\sum^{N}_{i=1}{x^{2}_{i}}$ is the sum of the squared values of all of the observations.
- $\bar{x}^{2}$ is the squared value of the mean of the data set.
The standard deviation $\sigma$ is simply the square root of the variance: $$\sigma = \sqrt{\sigma^{2}}$$
*Example*:
Suppose we have a data set:
$[20, 26, 47, 50, 52, 52, 56, 60, 63, 70, 70, 110]$
$\sigma^{2} = ({1\over N}\sum^{N}_{i=1}{x_{i}^{2}}) - {\bar{x}^{2}} \approx$ 379.17
$\sigma = \sqrt{sigma^{2}} \approx \sqrt{379.17} \approx 19.47$
Therefore the variance of this data set is approximately $379.17$ and the standard deviation of this data set is approximately $19.47$.

##### Correlation Analysis
**Correlation** and **covariance** are both measures for assessing how much two particular attributes change together. 

In order to determine if two attributes are correlated, we can utilize the **chi-square test** which follows a formula:
$\chi^{2} = \sum^{n}_{i=1}{{(Observed_{i}-Expected_{i})^{2}}\over Expected_{i}}$ 
- 