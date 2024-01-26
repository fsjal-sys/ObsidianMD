# Index
1. What is Data Mining?
2. Knowledge Discovery
3. Data Types
4. Mining Methods
5. Data Mining Disciplines
6. Data Mining Applications

<hr>

# What is Data Mining?
Data Mining, also known as _knowledge discovery from data_, is the discipline of identifying and formulating patterns from raw data. Vast amounts of raw data are generated constantly and rapidly on a daily basis, from things like web data, e-commerce, department/grocery transactions, bank transactions, social media, physical remote sensors, telescopic data, demographic statistics, weather and climate, etc. All of this raw data is generated for a reason but because of its sheer volume, it can initially appear as random information. Since there is a purpose behind this raw data, there is value in making an attempt to understand it. This can help us understand both the significance of this data and its usefulness for other applications.

### A Specific Example
An internet search engine receives hundreds of millions of search queries every day. Each query is a transaction where the user describes their information need. When a large number of these transactions are recorded, interesting patterns can be found which can be used to infer more meaning. _Google Flu Trends_ keeps track of queries concerned with flu activity, which it uses to measure the severity of a particular outbreak. This has been shown to estimate flu activity up to two weeks faster than traditional systems.

# Knowledge Discovery from Data (KDD) Process
As we have established, data mining is the discipline of finding patterns in raw data, which yields us valuable knowledge. The process of discovering this knowledge can be shown in an iterative set of steps.
1. Data Cleaning
	- The removal of noise and inconsistent data.
2. Data Integration
    - The combination of multiple data sources.
3. Data Selection
    - The selection of relevant data from the database.
4. Data Transformation
     - Data is transformed into forms which are appropriate for data mining.
5. Data Mining
     - The identification of patterns in the transformed data.
6. Pattern Evaluation
	- The evaluation of data patterns based on _interestingness measures.
7. Knowledge Presentation
	- The visualization of the knowledge obtained from the data mining process.

# Data Compositions
We can divide raw data into two fundamental types: **structured data** and **unstructured data**. 

**Structured data**: Data that is uniformed, structured in a table or record-like format. Structured data has a fixed set of attributes with a fixed set of value ranges and semantic meanings. Examples include _relational databases, data cubes, data matrices, and data warehouses_.
**Semi-structured data**: Data that contains a set value, a small set of heterogeneous typed values, or nested structures. 
**Unstructured data**: Data that takes no particular form. Unstructured data includes text data or multimedia data.

Data can be differentiated depending on its applications. As such, different data sets will require different data analysis methods. 
- **Sequence data**: Biological sequences will differ from shopping transaction sequences.
- **Time Series**: An ordered set of numerical values with equal time intervals.
- **Spatial, temporal, and spatiotemporal data**:
	- Spatial data follows a geometric space which can be represented by simple coordinates, points, lines, polygons, etc.
	- Temporal data follows a state in time.
	- Spatiotemporal data follows both a geometric space and a state in time.
- **Stored vs Streaming date**:
	- Stored data takes a finite form, stored in various kinds od large data repositories.
	- Streaming data takes a more dynamic form, which is constantly responding in real time. It poses challenges on effective data mining.
## Mining Various Kinds of Knowledge

1. Multidimensional Data Summarization
2. Mining Frequent Patterns, Associations, Correlations
3. Classification and Regression for Predictive Analysis
4. Cluster Analysis
5. Deep Learning
6. Outlier Analysis

### Multidimensional Data Summarization
With multidimensional data summarization, information undergoes integration and data warehouse construction. Data is cleaned, transformed, and integrated.
