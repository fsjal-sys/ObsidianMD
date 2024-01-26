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

Example:
*Salary* $X$ is represented by the set $[30, 26, 47, 50, 52, 52, 56, 60, 70, 70, 110]$ where each integer represents the salary by each thousand.
To calculate the mean $\bar{x}$, we will use the formula $\bar{x} = { \sum_{i=1}^{N}{x_i} \over {N}}$
$$\sum_{i=1}^{N}{x_i} = 30 + 26 + 47 + 50 + 52 + 52 + 56 + 60 + 70 + 110 = 696$$
$$N = 12$$
$$\bar{x} = { \sum_{i=1}^{N}{x_i} \over {N}} = {696 \over 12} = 58$$Therefore, the mean salary is $58,000.

