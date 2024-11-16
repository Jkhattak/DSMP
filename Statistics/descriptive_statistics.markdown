# Statistics 

Statistics is a branch of mathematics that invovles `collecting, analysing, interpreting, and presenting data`. It provides `tools and methods` to understand and make sense of large amounts of data and to `draw conclusion` and `make decision based on the data`. 


## Type of Statistics

<div style="text-align: center;">

```mermaid 
graph TD
  Statistics --> Descriptive
  Statistics --> Inferential
  Descriptive --> MeasuresOfCentralTendency
  Descriptive --> MeasuresOfDispersion
  Inferential --> HypothesisTesting
  Inferential --> RegressionAnalysis


```
</div>


## Descriptive Statistics 

Descriptive Statistics is a branch of statistics that focuses on summarizing and organizing data in a meaningful way. It provides simple summaries about the sample and the measures. This can include measures of central tendency (such as mean, median, and mode) and measures of dispersion (such as range, variance, and standard deviation). Descriptive statistics help in understanding the basic features of the data, offering a quick overview without drawing conclusions or making predictions about the data.

## Infrential Statistics 


- Inferential Statistics is a branch of statistics that allows us to make predictions or inferences about a population based on data collected from a sample. It involves using probability theory to estimate population parameters, test hypotheses, and make decisions or predictions. Inferential statistics go beyond merely describing the data and help determine relationships, assess the reliability of estimates, and draw conclusions that extend beyond the data set at hand. 
  - Examples include hypothesis testing, confidence intervals, regression analysis, and ANOVA.

---

## Population and Sample are fundamental concepts in statistics:

- <b> Population </b>: Refers to the entire group of individuals, items, or data that you want to study or draw conclusions about. It includes all possible observations that can be made. 
  - For example, if you're studying the average height of all adults in a country, the population would consist of every adult in that country.

- <b> Sample </b>: A subset of the population that is selected for the actual study or analysis. A sample is used when it is impractical or impossible to study the whole population. 
  - For example, instead of measuring the height of every adult in a country, you might select a sample of 1,000 adults to estimate the average height.
### Things to be careful about which creating samples
  - Sample size
  - Random
  - Representative

---
## Types of Data

<div style="text-align: center;">

```mermaid
graph TD
    A[Types of data] --> B[Categorical or qualitative data]
    A --> C[Numerical or quantitative data]
    B --> D[Nominal data]
    B --> G[Ordinal data]
    C --> E[Discrete data]
    C --> F[Continous data]
```
</div>

- `Types of Data:` Data can be broadly classified into different types based on the characteristics of what is being measured or observed. These types help in selecting appropriate statistical methods for analysis.

- `Categorical or Qualitative Data:` This type of data represents characteristics or attributes that can be used to group or categorize objects but cannot be measured or counted numerically. Examples include gender, religion, and color.

- `Numerical or Quantitative Data:` This type of data represents values or observations that can be measured or counted and expressed numerically. Examples include height, age, and income.

- `Nominal Data:` A subcategory of categorical data, nominal data consists of labels or names used to identify or classify objects, but the order of these labels is not meaningful. Examples include eye color (blue, brown, green) and type of cuisine (Italian, Chinese, Mexican).

- `Ordinal Data:` Another subcategory of categorical data, ordinal data represents categories that have a meaningful order or ranking but the differences between the ranks are not quantifiable. Examples include rankings (1st, 2nd, 3rd) and satisfaction levels (satisfied, neutral, dissatisfied).

- `Discrete Data:` A subcategory of numerical data, discrete data represents countable values or numbers that can only take specific values. There are gaps between these values, such as the number of students in a class or the number of cars in a parking lot.

- `Continuous Data:` Another subcategory of numerical data, continuous data represents values that can take any value within a given range, and there are no gaps between the values. Examples include height, weight, and temperature. Continuous data can be measured to any level of precision, depending on the measurement tool.

---

## Measure of Central Tendency 

A measure of central tendency is a statistical measure that represents a typical or central value for a dataset. it provides a summary of the data by identifying a single value that is most representative of the dataset as whole. 

<div style="text-align: center;">

```mermaid
graph TD    

    A[Measure of central tendency] --> B[Mean]
    A[Measure of Central Tendency] --> C[Median]
    A[Measure of Central Tendency] --> D[Mode]

```
</div>
- `Mean:` The average of all values in a dataset, calculated by adding up all the values and dividing by the total number of values. The mean is sensitive to outliers, which can skew the result. 
  - For example, the mean of 2, 3, and 4 is (2+3+4)/3 = 3.

- `Median:` The middle value of a dataset when it is ordered from least to greatest. If there is an even number of values, the median is the average of the two middle numbers. The median is less affected by outliers and is often used when the data distribution is skewed. 
  - For example, the median of 2, 3, and 10 is 3.

- `Mode:` The value that appears most frequently in a dataset. A dataset may have one mode, more than one mode, or no mode at all if no value repeats. It is best use in categorical dataset.
  - For example, in the dataset 1, 2, 2, 3, the mode is 2.

---
### Population Mean vs. Sample Mean

The **Population Mean** and **Sample Mean** are two ways of calculating the average, but they differ in terms of the dataset used:

1. **Population Mean**:
   - The population mean (denoted by the Greek letter μ) is the average of all values in an entire population.
   - It is calculated by adding up all the values in the population and dividing by the total number of values in the population.
   - **Formula**:  
     $$\mu = \frac{\sum X}{N}$$  
     where:
     - $\sum X$ = Sum of all values in the population
     - $N$ = Total number of values in the population
   - Since it includes every data point in the population, it gives a complete picture but is often impractical to calculate when the population size is very large.

2. **Sample Mean**:
   - The sample mean (denoted by $\bar{x}$) is the average of all values in a sample, which is a subset of the population.
   - It is calculated by adding up all the values in the sample and dividing by the total number of values in the sample.
   - **Formula**:  
     $$\bar{x} = \frac{\sum x}{n}$$  
     where:
     - $\sum x$ = Sum of all values in the sample
     - $n$ = Total number of values in the sample
   - The sample mean is used to estimate the population mean and is more practical to calculate, but it may not be as accurate as the population mean, depending on the sample's representativeness.

**Key Difference**: The population mean is the average of all data points in a population, while the sample mean is the average of a subset of the population and serves as an estimate of the population mean.

**Caution**: It is prone to outliers so always be careful when using mean to describe a dataset. 

---
## Weighted Mean

The **Weighted Mean** is an average that takes into account the relative importance or frequency of some values in a dataset. Unlike the regular mean, where all values are given equal weight, the weighted mean assigns different weights to different values based on their significance or frequency.


### Formula
$$
\text{Weighted Mean} = \frac{\sum (w_i \times x_i)}{\sum w_i}
$$
where:
- $x_i$ = Each individual value
- $w_i$ = The weight assigned to each value
- $\sum$ = The summation symbol, indicating that we sum over all values

### Example
Imagine you have three test scores: 85, 90, and 95, with weights of 1, 2, and 3, respectively, representing the importance of each test. The weighted mean would be calculated as:

$$
\text{Weighted Mean} = \frac{(85 \times 1) + (90 \times 2) + (95 \times 3)}{1 + 2 + 3} = \frac{85 + 180 + 285}{6} = \frac{550}{6} \approx 91.67
$$

### Use Cases
The weighted mean is particularly useful when:
- Different data points have different levels of importance.
- The dataset includes categories or groups that need to be given varying significance.

Examples include calculating a student’s grade point average (where courses have different credit hours) or computing an average cost when different quantities are purchased at different prices.

---

## Trimmed Mean

The **Trimmed Mean** is a measure of central tendency calculated by  `removing a certain percentage of the smallest and largest values from a dataset` and then taking the mean of the remaining values. It helps reduce the effect of outliers.

### Numerical Example
Consider the following dataset:


Suppose we want to calculate a 20% trimmed mean. This means removing 20% of the values from both the lower and upper ends of the dataset.

  - **Sort the Data** (if not already sorted):
    - `10, 15, 20, 25, 30, 35, 100`
  -  **Remove 20% from Both Ends**:
     - Since there are 7 values, 20% of 7 is 1.4, which we round to 1.
     - Remove the smallest and largest value: 10 and 100.
     - Remaining values: `15, 20, 25, 30, 35`

  - **Calculate the Mean of the Remaining Values**:
$$ \text{Mean} = \frac{15 + 20 + 25 + 30 + 35}{5} = \frac{125}{5} = 25 $$

### Result
The 20% trimmed mean of the dataset is **25**.

### Note
- The percentage of trimming should be chosen based on the nature of the data and how much you want to reduce the impact of outliers.

---

### Measure of Dispersion

**Measures of dispersion** are statistical tools used to describe the spread or variability of a dataset. They help to understand how much the data points differ from the mean or each other, providing insights into the distribution of the data. The most common measures of dispersion include:

1. **Range**: 
   - The difference between the largest and smallest values in a dataset.
   - **Formula**:  
     $$ \text{Range} = \text{Maximum Value} - \text{Minimum Value} $$
   - Example: If the smallest value is 10 and the largest is 50, the range is $50 - 10 = 40$.
   - **Cautious**: Range is prone to outliers

2. **Variance**:
   - A measure of how far each data point in the dataset is from the mean, calculated as the average of the squared differences from the mean.
   - It is proportional to the spread of the dataset. If a dataset has a large spread, it will also have a large variance. 
   - **Formula for Population Variance** ($\sigma^2$):  
     $$ \sigma^2 = \frac{\sum (X_i - \mu)^2}{N} $$
   - **Formula for Sample Variance** ($s^2$):  
     $$ s^2 = \frac{\sum (X_i - \bar{X})^2}{n - 1} $$
   - Where:
     - $X_i$ = Each individual data point
     - $\mu$ = Population mean
     - $\bar{X}$ = Sample mean
     - $N$ = Total number of data points in the population
     - $n$ = Total number of data points in the sample

3. **Standard Deviation**:
   - The square root of the variance, providing a measure of the average distance of each data point from the mean.
   - **Formula**:  
     $$ \text{Standard Deviation} = \sqrt{\text{Variance}} $$
   - It is expressed in the same units as the data, making it easier to interpret.

4. **Interquartile Range (IQR)**:
   - The difference between the 75th percentile (Q3) and the 25th percentile (Q1) of the dataset, showing the range within which the middle 50% of the data falls.
   - **Formula**:  
     $$ \text{IQR} = Q3 - Q1 $$
   - Useful for identifying the spread of the central portion of a dataset, especially when dealing with outliers.

5. **Mean Absolute Deviation (MAD)**:
   - The average of the absolute differences between each data point and the mean.
   - **Formula**:  
     $$ \text{MAD} = \frac{\sum |X_i - \mu|}{N} $$
   - Where:
     - $|X_i - \mu|$ = Absolute difference between each data point and the mean
     - $N$ = Total number of data points

### Importance
- **Understanding Variability**: Measures of dispersion give an understanding of the variability within a dataset, which helps to make informed decisions.
- **Data Comparison**: They are useful for comparing the spread of different datasets.
- **Identifying Outliers**: Measures like the IQR can help identify outliers in the data.

These measures complement central tendency metrics, providing a more comprehensive understanding of the data distribution.

---

### Standard Deviation

**Standard Deviation** is a measure of dispersion that indicates how spread out the values in a dataset are around the mean. It is calculated as the square root of the variance and is expressed in the same units as the data, making it a useful and interpretable statistic.

### Equation
For a population:
$$
\sigma = \sqrt{\frac{\sum (X_i - \mu)^2}{N}}
$$

For a sample:
$$
s = \sqrt{\frac{\sum (X_i - \bar{X})^2}{n - 1}}
$$

where:
- $\sigma$ = Population standard deviation
- $s$ = Sample standard deviation
- $X_i$ = Each individual data point
- $\mu$ = Population mean
- $\bar{X}$ = Sample mean
- $N$ = Total number of data points in the population
- $n$ = Total number of data points in the sample

### Pros of Using Standard Deviation
1. **Gives a Clear Measure of Variability**:
   - Standard deviation provides a quantifiable measure of how much the values in a dataset vary or deviate from the mean. This helps in understanding the data distribution and assessing the consistency of the data.

2. **Useful for Normally Distributed Data**:
   - When data follows a normal distribution, standard deviation becomes a very powerful tool, as it allows you to make precise inferences about the data, such as using the empirical rule (68-95-99.7 rule).

### Cautions When Using Standard Deviation
1. **Sensitive to Outliers**:
   - Standard deviation can be greatly affected by outliers or extreme values in the dataset. A few extreme values can inflate the standard deviation, giving a misleading impression of variability.

2. **Not Suitable for Skewed Distributions**:
   - For datasets with a highly skewed distribution or when the data does not follow a normal distribution, the standard deviation might not accurately represent the variability, and other measures like the interquartile range (IQR) may be more appropriate.

---

### Coefficient of Variation (CV)

The **Coefficient of Variation (CV)** is a standardized measure of dispersion that indicates the ratio of the standard deviation to the mean. It is often expressed as a percentage and is useful for comparing the degree of variation between datasets with different units or means.

### Equation
$$
\text{CV} = \frac{\sigma}{\mu} \times 100
$$

where:
- $\sigma$ = Standard deviation
- $\mu$ = Mean of the dataset

### Interpretation
- A **higher CV** indicates greater variability relative to the mean.
- A **lower CV** suggests less variability relative to the mean.

### Pros of Using Coefficient of Variation
1. **Unitless Measure**:
   - The CV is dimensionless, making it ideal for comparing variability across datasets that have different units or scales.

2. **Relative Comparison**:
   - CV allows for easy comparison of the relative variability between datasets, even when the means differ significantly.

### Cautions When Using Coefficient of Variation
1. **Not Suitable for Data with a Mean Close to Zero**:
   - When the mean is close to zero, the CV can become extremely large or misleading, as the ratio amplifies small variations in the mean.

2. **Assumes a Positive Mean**:
   - CV is typically used for data with a positive mean, and it is not useful for datasets with negative or zero means.

---

## Bivariate Analysis 

```mermaid
graph TD
  A[Bivariate Analysis] --> B[Continuous vs Continuous]
  A --> C[Continuous vs Categorical]
  A --> D[Categorical vs Categorical]
  
  B --> E[Scatter Plot]
  B --> F[Correlation Coefficient]
  B --> G[Regression Analysis]

  C --> H[Box Plot]
  C --> I[Violin Plot]
  C --> J[ANOVA]

  D --> K[Contingency Table]
  D --> L[Chi-Square Test]
  D --> M[Stacked Bar Chart]
```


---
## Working with Categorical Tables

### 1. Categorical Frequency Distribution Table

**Definition**: A frequency distribution table for categorical data lists each category and the number of occurrences (frequency) in the dataset.

**Example Table**:
| Category       | Frequency |
|----------------|-----------|
| Apples         | 30        |
| Bananas        | 25        |
| Oranges        | 20        |
| Grapes         | 15        |

**Types of Graphs**:
- **Bar Chart**: Shows the frequency of each category using bars.
- **Pie Chart**: Displays the proportion of each category in a circular chart.
- **Pareto Chart**: A bar chart that shows frequencies in descending order and includes a line for cumulative frequency.

---

### 2. Relative Frequency Distribution Table

**Definition**: A relative frequency table shows the proportion or percentage of the total number of observations that fall into each category.

**Example Table**:
| Category       | Frequency | Relative Frequency |
|----------------|-----------|--------------------|
| Apples         | 30        | 0.30 (30%)         |
| Bananas        | 25        | 0.25 (25%)         |
| Oranges        | 20        | 0.20 (20%)         |
| Grapes         | 15        | 0.15 (15%)         |

**Calculation**:  
$$
\text{Relative Frequency} = \frac{\text{Frequency of the Category}}{\text{Total Frequency}}
$$

**Types of Graphs**:
- **Bar Chart**: Can be modified to show proportions instead of raw frequencies.
- **Pie Chart**: Effective for visualizing relative frequencies.
- **Stacked Bar Chart**: Used for comparing proportions across multiple groups.

---

### 3. Cumulative Frequency Distribution Table

**Definition**: A cumulative frequency table shows the sum of frequencies for all categories up to and including the current category. It helps in understanding how frequencies accumulate over categories.

**Example Table**:
| Category       | Frequency | Cumulative Frequency |
|----------------|-----------|----------------------|
| Apples         | 30        | 30                   |
| Bananas        | 25        | 55                   |
| Oranges        | 20        | 75                   |
| Grapes         | 15        | 90                   |

**Calculation**:  
- Cumulative frequency is the sum of the frequency of the current category and all previous frequencies.

**Types of Graphs**:
- **Cumulative Frequency Graph (Ogive)**: A line graph that shows the cumulative frequency distribution.
- **Step Chart**: An alternative way to represent cumulative frequencies.

---

### Summary of Graph Types
1. **Categorical Frequency Distribution**:
   - Bar Chart
   - Pie Chart
   - Pareto Chart

2. **Relative Frequency Distribution**:
   - Bar Chart (for proportions)
   - Pie Chart
   - Stacked Bar Chart

3. **Cumulative Frequency Distribution**:
   - Cumulative Frequency Graph (Ogive)
   - Step Chart

---

## Numerical Frequency Distribution Table

**Definition**: A frequency distribution table for numerical data organizes the data into intervals (bins) and shows the number of data points that fall within each interval. It helps to understand how the data is distributed across the range.

**Example Table**:
Consider a dataset representing the ages of 30 individuals:


We can create a frequency distribution table with age intervals of 10 years:

| Age Interval | Frequency |
|--------------|-----------|
| 20 - 29      | 3         |
| 30 - 39      | 3         |
| 40 - 49      | 3         |
| 50 - 59      | 3         |
| 60 - 69      | 3         |
| 70 - 79      | 3         |
| 80 - 89      | 3         |
| 90 - 99      | 3         |

---

### Histogram

**Definition**: A **Histogram** is a graphical representation of a frequency distribution for numerical data. It uses adjacent bars to show the frequency of data points in each interval, where the height of each bar represents the frequency.

### Shapes of Histograms

1. **Bell-Shaped (Normal Distribution)**:
   - Symmetrical with a single peak at the center.
   - Most data points cluster around the mean.
   - **Example**: Heights of individuals in a large population.

2. **Uniform Distribution**:
   - All intervals have approximately the same frequency.
   - Data points are evenly distributed across the range.
   - **Example**: Rolling a fair six-sided die multiple times.

3. **Bimodal Distribution**:
   - Two distinct peaks.
   - Indicates the presence of two different groups within the data.
   - **Example**: Test scores from two different classes.

4. **Skewed Right (Positively Skewed)**:
   - Tail extends to the right.
   - Most data points are concentrated on the left.
   - **Example**: Income distribution in many economies.

5. **Skewed Left (Negatively Skewed)**:
   - Tail extends to the left.
   - Most data points are concentrated on the right.
   - **Example**: Age at retirement in a population.

6. **Multimodal Distribution**:
   - More than two peaks.
   - Indicates multiple groups or modes within the data.
   - **Example**: Test scores from students of different proficiency levels.

### Visual Examples

Below are visual representations of different histogram shapes:

- **Bell-Shaped Histogram**:
- 
  ![Bell-Shaped Histogram](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fvt-vtwa-assets.varsitytutors.com%2Fvt-vtwa%2Fuploads%2Fproblem_question_image%2Fimage%2F23829%2FNormal.png&f=1&nofb=1&ipt=21e5ed89e41bfee2619556ead73e1262aa94e3078c69d6d7ec480ac8d4edd6ad&ipo=images)

- **Uniform Histogram**:
- 
  ![Uniform Histogram](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi1.wp.com%2Fwww.mathbootcamps.com%2Fwp-content%2Fuploads%2Funiform-histogram.jpg%3Fresize%3D576%252C384&f=1&nofb=1&ipt=f1e03b15fdea3ac12a7814a006f78c497d356dd02db53dc4db9ea45e61cfaf08&ipo=images)

- **Bimodal Histogram**:
- 
  ![Bimodal Histogram](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi0.wp.com%2Fstatisticsbyjim.com%2Fwp-content%2Fuploads%2F2022%2F03%2FBimodal_histogram.png%3Fresize%3D576%252C384%26ssl%3D1&f=1&nofb=1&ipt=3c468409477b9d7fd5affb5a39de2bf6a8fc74457194db58944e8d9364510ee5&ipo=images)

- **Skewed Right Histogram**:
- 
  ![Skewed Right Histogram](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fassets-global.website-files.com%2F621e95f9ac30687a56e4297e%2F64adcace377905a651ca4910_V2_1681696383676_ac795440-2535-4d6f-b94b-cf447b166ae4_HIGH_RES.png&f=1&nofb=1&ipt=bceb5465f30bdc3a5261830bab0e80f8c01fd303fa611004814991cf6517af36&ipo=images)

- **Skewed Left Histogram**:
- 
  ![Skewed Left Histogram](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fassets-global.website-files.com%2F621e95f9ac30687a56e4297e%2F64adca5b377905a651c9e574_V2_1681696470397_c24a2161-6502-420e-bd18-c8a3837f3651_HIGH_RES.png&f=1&nofb=1&ipt=b856d4309d8cbae03c355d1e1567c87f8eb13e559ca89eeaacadec2d4d9945e4&ipo=images)

- **Multimodal Histogram**:
- 
  ![Multimodal Histogram](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fstatisticsbyjim.com%2Fwp-content%2Fuploads%2F2019%2F02%2Fmultimodal_histogram.png&f=1&nofb=1&ipt=b42da3eabc8b9d83f3e506c2366274b3a022ef74af92918eaac59953fc6c30e1&ipo=images)

### Notes
- **Histogram Shapes**: Understanding the shape of a histogram is crucial for interpreting the underlying data distribution.
- **Graph Types**: The shape of a histogram can provide insights into the data's characteristics, such as whether it is normally distributed, skewed, or contains multiple peaks.

---

## Bivariate Analysis: Categorical vs. Categorical 

```mermaid
graph TD
  A[Bivariate Analysis] --> B[Categorical vs Categorical]
  
  B --> C[Contingency Table]
  B --> D[Chi-Square Test]
  B --> E[Stacked Bar Chart]
  B --> F[Clustered Bar Chart]

```


**Categorical vs. Categorical:** This refers to analyzing the relationship between two categorical variables to understand how they are associated or distributed relative to each other.

  - ` Contingency Table:` A table that displays the frequency distribution of two categorical variables and helps identify possible relationships.
  - ` Chi-Square Test:` A statistical test used to determine if there is a significant association between the two categorical variables.
  - ` Stacked Bar Chart:` A visual representation where bars are divided into segments to show the distribution of one categorical variable across the levels of another.
  -  `Clustered Bar Chart:` Another type of bar chart that groups bars of different categories side-by-side to compare frequencies or proportions.

---

## Bivariate Analysis: Numerical vs. Numerical Diagram 

```mermaid
graph TD
  A[Bivariate Analysis] --> B[Numerical vs Numerical]
  
  B --> C[Scatter Plot]
  B --> D[Correlation Analysis]
  B --> E[Regression Analysis]
  B --> F[Line Graph]

```

**`Numerical vs. Numerical:`** This type of bivariate analysis explores the relationship between two numerical variables.

  - ` Scatter Plot:` A graph that shows individual data points plotted in a two-dimensional space, allowing you to visualize any potential correlation or pattern between the variables.
  - ` Correlation Analysis:` A statistical method used to measure the strength and direction of the relationship between two numerical variables. The correlation coefficient (r) ranges from -1 to 1.
  - ` Regression Analysis:` A technique used to model and analyze the relationship between the independent (predictor) variable and the dependent (response) variable, often used for prediction.
  - ` Line Graph:` Useful for visualizing the relationship between two numerical variables over time or a continuous range, especially when one variable is dependent on the other.

---

## Bivariate Analysis: Categorical vs. Numerical Diagram 

```mermaid
graph TD
  A[Bivariate Analysis] --> B[Categorical vs Numerical]
  
  B --> C[Box Plot]
  B --> D[Violin Plot]
  B --> E[Bar Chart with Means]
  B --> F[ANOVA]

```

**`Categorical vs. Numerical:`** This type of bivariate analysis examines the relationship between a categorical variable and a numerical variable.

  -  `Box Plot:` A graphical representation that shows the distribution of the numerical variable across the different categories. It displays the median, quartiles, and potential outliers for each category.
  -  `Violin Plot:` Similar to a box plot but also includes a density plot, providing more information about the distribution of the numerical variable within each category.
  -  `Bar Chart with Means:` A bar chart that displays the mean value of the numerical variable for each category, often used to compare averages across groups.
  -  `ANOVA (Analysis of Variance):` A statistical test used to determine if there are significant differences in the means of the numerical variable across multiple categories.

# Quantiles and Percentiles

## **Quantiles**
Quantiles are points that divide a dataset into equal-sized, consecutive intervals. They are used to understand the distribution of data.

### **Key Points**
- Quantiles divide data into **`q` equal parts**.
- Common quantiles include:
  - **Quartiles**: Divide data into 4 parts (25% intervals).
  - **Deciles**: Divide data into 10 parts (10% intervals).
  - **Percentiles**: Divide data into 100 parts (1% intervals).
- Quantiles help identify the spread and skewness of the data.

### **Quartiles**
Quartiles are a specific case of quantiles dividing the dataset into four equal parts:
1. **Q1 (First Quartile)**: The value below which 25% of the data falls.
2. **Q2 (Second Quartile or Median)**: The value below which 50% of the data falls.
3. **Q3 (Third Quartile)**: The value below which 75% of the data falls.

### Things to remember while calculating these measures:
- Data should be sorted from `low to high`
- You are basically finding the `location of an observation` 
- They are `not actual values in the data` 
- All other tiles can be easily derived from `Percentile`

#### **Formula to Find a Quartile**
$$ Q_k = \text{Value at position } \frac{k \times (n + 1)}{4} $$
- \( k \): The quartile number (1, 2, or 3).
- \( n \): Total number of data points.

---

## **Percentiles**
Percentiles are a type of quantile that divide the dataset into 100 parts, each representing 1% of the distribution.

A **percentile** is a statistical measure that represents the percentage of observations in a dataset that fall below a particular value. For example, the **75th percentile** is the value below which **75%** of the observations in the dataset fall.

### **Key Points**
- **Pth Percentile**: The value below which \( P\% \) of the data falls.
  - Example: The 90th percentile (P90) means 90% of data is below that value.
- Percentiles are commonly used in:
  - **Test scores**: To show performance relative to peers.
  - **Descriptive statistics**: Summarizing large datasets.

### **Formula to Find a Percentile**
$$ P_k = \text{Value at position } \frac{k}{100} \times (n + 1) $$
- \( k \): Percentile number (1-100).
- \( n \): Total number of data points.

### **Percentile Example**

#### Dataset:
Sort the dataset first in ascending
$$[5, 10, 15, 20, 25, 30, 35, 40]$$

#### Goal:
Find the **90th percentile (P90)**.

#### Steps:

1. **Sort the dataset (if not already sorted):**
   $$ [5, 10, 15, 20, 25, 30, 35, 40] $$

2. **Calculate the position:**
   $$
   \text{Position} = P \times \frac{(n + 1)}{100}
   $$

   Where:
   - \( P = 90 \) (percentile value)
   - \( n = 8 \) (total number of data points)

   Substituting the values:
   $$
   \text{Position} = 90 \times \frac{(8 + 1)}{100} = 90 \times \frac{9}{100} = 8.1
   $$

3. **Interpolate to find the value:**
   - The position is \( 8.1 \), so we consider the 8th value (40) and interpolate beyond it.
   - The interpolation formula is:
     $$
     P_{90} = \text{Value at Position 8} + (\text{Fractional Part}) \times (\text{Next Value} - \text{Value at Position 8})
     $$

     Since there is no next value beyond 40:
     $$
     P_{90} = 40
     $$

#### Final Result:
The **90th percentile** is:
$$
P_{90} = 40
$$



---

## **Relationship Between Quantiles and Percentiles**
- Percentiles are **quantiles** where \( q = 100 \).
- Quartiles (4 equal parts) are equivalent to:
  - 25th percentile (Q1)
  - 50th percentile (Q2, Median)
  - 75th percentile (Q3)

---

## **How to Calculate Quantiles and Percentiles**
1. **Sort the Dataset**: Arrange data in ascending order.
2. **Determine the Position**:
   - For quantiles: Divide the dataset into $q$ equal parts.
   - For percentiles: Multiply the percentile number $k$ by $\frac{(n + 1)}{100}$.
3. **Locate the Value**:
   - If the position is an integer, take the value at that index.
   - If not, interpolate between the nearest values.

### **Interpolation Formula**
If $P_k$ falls between two indices $i$ and $i+1$:
$$
P_k = \text{Value at } i + (\text{Fractional part}) \times (\text{Value at } i+1 - \text{Value at } i)
$$

---

## **Examples**
### Example 1: Finding the Median (50th Percentile)
**Dataset**: [10, 20, 30, 40, 50]

- Median Position:
  $$
  50\% \times (5 + 1) = 3
  $$
- Median Value: Value at Position 3 = **30**.

---

### Example 2: Finding the 90th Percentile
**Dataset**: [5, 10, 15, 20, 25, 30]

- Position:
  $$
  90\% \times (6 + 1) = 6.3
  $$
- Interpolating between Value at Position 6 and Position 7:
  $$
  P_{90} = 30 + 0.3 \times (35 - 30) = 31.5
  $$
- 90th Percentile = **31.5**.


---

## **Visualizing Quantiles and Percentiles**
- Quantiles are often visualized using:
  - **Box Plots**: Show quartiles (Q1, Median, Q3) and outliers.
  - **Cumulative Distribution Function (CDF)**: Shows percentiles.

# **Five-Number Summary**

The **Five-Number Summary** provides a concise description of a dataset's distribution. It consists of:

1. **Minimum**: The smallest value in the dataset.
2. **First Quartile (Q1)**: The value below which 25% of the data falls.
3. **Median (Q2)**: The middle value of the dataset (50th percentile).
4. **Third Quartile (Q3)**: The value below which 75% of the data falls.
5. **Maximum**: The largest value in the dataset.

![alt text](5-number-summary-explained-3892409429.png)
---

## **Steps to Calculate the Five-Number Summary**

1. **Sort the Dataset**: Arrange the data in ascending order.
2. **Identify the Minimum and Maximum**: Select the smallest and largest values, respectively.
3. **Calculate Q1 (First Quartile)**:
   - Q1 is the median of the lower half (below the overall median) of the dataset.
4. **Calculate Q2 (Median)**:
   - The median is the middle value if the dataset has an odd number of observations.
   - If the dataset has an even number of observations, the median is the average of the two middle values.
5. **Calculate Q3 (Third Quartile)**:
   - Q3 is the median of the upper half (above the overall median) of the dataset.

---

## **Example**

**Dataset**: [7, 15, 36, 39, 40, 41, 42, 43, 46, 49]

1. **Sort the Dataset**: 
   $$ [7, 15, 36, 39, 40, 41, 42, 43, 46, 49] $$

2. **Minimum**: 
   $$ 7 $$

3. **Maximum**: 
   $$ 49 $$

4. **Median (Q2)**:
   - Number of observations \( n = 10 \) (even).
   - Median is the average of the 5th and 6th values:
     $$
     Q2 = \frac{40 + 41}{2} = 40.5
     $$

5. **First Quartile (Q1)**:
   - Lower half: [7, 15, 36, 39, 40]
   - Median of the lower half:
     $$
     Q1 = 36
     $$

6. **Third Quartile (Q3)**:
   - Upper half: [41, 42, 43, 46, 49]
   - Median of the upper half:
     $$
     Q3 = 43
     $$

---

## **Final Five-Number Summary**
- **Minimum**: 7
- **Q1**: 36
- **Median (Q2)**: 40.5
- **Q3**: 43
- **Maximum**: 49

---

## **Applications**
- **Box Plots**: Visualize the Five-Number Summary with whiskers and outliers.
- **Descriptive Statistics**: Summarize the dataset for quick insights.
- **Outlier Detection**: Identify extreme values using interquartile range (IQR).

---

## **Interquartile Range (IQR)**
The interquartile range (IQR) is a measure of variability that is based on the five-number summary of a dataset. Specifically, the IQR is defined as a the difference between the third quartile (Q3) and the first quartile (Q1) of a datase. 

The IQR is the range between the first and third quartiles:
$$
\text{IQR} = Q3 - Q1
$$

For the example dataset:
$$
\text{IQR} = 43 - 36 = 7
$$

Outliers are typically defined as values below:
$$
Q1 - 1.5 \times \text{IQR}
$$
or above:
$$
Q3 + 1.5 \times \text{IQR}
$$

# **Boxplot**

A **boxplot** (or box-and-whisker plot) is a graphical representation of the distribution of a dataset based on the **five-number summary**. It is used to visualize the central tendency, spread, and potential outliers in the data.

---

## **Components of a Boxplot**

1. **Minimum**: The smallest data point within 1.5 times the IQR below Q1.
2. **First Quartile (Q1)**: The lower edge of the box, representing the 25th percentile.
3. **Median (Q2)**: The line inside the box, representing the 50th percentile.
4. **Third Quartile (Q3)**: The upper edge of the box, representing the 75th percentile.
5. **Maximum**: The largest data point within 1.5 times the IQR above Q3.
6. **Whiskers**:
   - Extend from the box to the smallest and largest values within 1.5 times the IQR.
7. **Outliers**:
   - Data points outside the whiskers are marked as individual dots or symbols.

![alt text](1_0MPDTLn8KoLApoFvI0P2vQ-3702459769.png)
---

## Benefits of a Boxplot
- Easy way to see the distribution of data
- Tells about skewness of data
- Can identify outliers
- Compare 2 categories of data



## **How to Create a Boxplot**

1. **Calculate the Five-Number Summary**:
   - Minimum, Q1, Median, Q3, and Maximum.
2. **Calculate the Interquartile Range (IQR)**:
   $$
   \text{IQR} = Q3 - Q1
   $$
3. **Determine the Whisker Bounds**:
   - Lower Bound:
     $$
     Q1 - 1.5 \times \text{IQR}
     $$
   - Upper Bound:
     $$
     Q3 + 1.5 \times \text{IQR}
     $$
4. **Identify Outliers**:
   - Values outside the whisker bounds.

5. **Plot the Box and Whiskers**:
   - The box spans from Q1 to Q3.
   - The line inside the box represents the Median (Q2).
   - Whiskers extend to the minimum and maximum within the whisker bounds.
   - Outliers are plotted as individual points.

---

## **Example**

**Dataset**: [7, 15, 36, 39, 40, 41, 42, 43, 46, 49]

1. **Five-Number Summary**:
   - Minimum: 7
   - Q1: 36
   - Median (Q2): 40.5
   - Q3: 43
   - Maximum: 49

2. **IQR**:
   $$
   \text{IQR} = Q3 - Q1 = 43 - 36 = 7
   $$

3. **Whisker Bounds**:
   - Lower Bound:
     $$
     Q1 - 1.5 \times \text{IQR} = 36 - 1.5 \times 7 = 25.5
     $$
   - Upper Bound:
     $$
     Q3 + 1.5 \times \text{IQR} = 43 + 1.5 \times 7 = 53.5
     $$

4. **Outliers**:
   - Values below 25.5 or above 53.5.
   - No outliers in this dataset.

---

## **Boxplot Summary**
- **Box**: Spans from Q1 (36) to Q3 (43).
- **Median**: A line at 40.5 inside the box.
- **Whiskers**: Extend to 7 (Minimum) and 49 (Maximum).
- **Outliers**: None.

---

## **Applications**
- **Descriptive Statistics**: Summarizing data distribution.
- **Outlier Detection**: Highlight extreme values.
- **Comparative Analysis**: Comparing multiple datasets side by side.

---

## **Visual Representation**

A boxplot visually looks like this:

# **Scatter Plot**

A scatter plot is used to visualize the relationship between two numerical variables. Each point in the plot represents one observation, with its position determined by the values of the two variables.

---

## **Components of a Scatter Plot**

1. **X-Axis**: Represents the independent variable.
2. **Y-Axis**: Represents the dependent variable.
3. **Points**: Each point represents an observation, with its position determined by the values of \( x \) (independent variable) and \( y \) (dependent variable).

---

## **Purpose of a Scatter Plot**

1. **Identify Relationships**:
   - Determine if a relationship exists between two variables (e.g., positive, negative, or no correlation).
2. **Detect Patterns**:
   - Identify trends, clusters, or outliers.
3. **Highlight Correlation**:
   - Visualize the strength and direction of a relationship.

---

## **Steps to Create a Scatter Plot**

1. **Prepare the Data**:
   - Collect two numerical variables for analysis.
2. **Assign Axes**:
   - Plot the independent variable on the \( x \)-axis.
   - Plot the dependent variable on the \( y \)-axis.
3. **Plot Points**:
   - For each observation, position a point at the corresponding \( (x, y) \) coordinates.

---

## **Example**

### Dataset:

| Observation | \( x \) (Hours Studied) | \( y \) (Test Score) |
|-------------|--------------------------|-----------------------|
| 1           | 1                        | 50                    |
| 2           | 2                        | 55                    |
| 3           | 3                        | 65                    |
| 4           | 4                        | 70                    |
| 5           | 5                        | 80                    |

### Scatter Plot Coordinates:
- \( (1, 50) \)
- \( (2, 55) \)
- \( (3, 65) \)
- \( (4, 70) \)
- \( (5, 80) \)

---

## **Interpreting the Scatter Plot**

1. **Positive Correlation**:
   - As \( x \) increases, \( y \) also increases.
2. **Negative Correlation**:
   - As \( x \) increases, \( y \) decreases.
3. **No Correlation**:
   - No apparent relationship between \( x \) and \( y \).

---

# **Covariance**

Covariance is a statistical measure that quantifies the degree to which two random variables change together. It helps determine the **direction** of the relationship between the variables.

---

## **Formula for Covariance**

For two variables, \( X \) and \( Y \), with \( n \) data points:

### **Population Covariance**
$$
\text{Cov}(X, Y) = \frac{\sum_{i=1}^{n} (X_i - \mu_X)(Y_i - \mu_Y)}{n}
$$

### **Sample Covariance**
$$
\text{Cov}(X, Y) = \frac{\sum_{i=1}^{n} (X_i - \bar{X})(Y_i - \bar{Y})}{n - 1}
$$

Where:
- \( X_i \): The \( i \)-th value of \( X \).
- \( Y_i \): The \( i \)-th value of \( Y \).
- \( \mu_X \): Mean of \( X \) (for population).
- \( \mu_Y \): Mean of \( Y \) (for population).
- \( \bar{X} \): Sample mean of \( X \).
- \( \bar{Y} \): Sample mean of \( Y \).
- \( n \): Number of data points.

---

## **Interpreting Covariance**

1. **Positive Covariance**:
   - When \( X \) increases, \( Y \) tends to increase.
   - Indicates a positive linear relationship.

2. **Negative Covariance**:
   - When \( X \) increases, \( Y \) tends to decrease.
   - Indicates a negative linear relationship.

3. **Zero Covariance**:
   - No linear relationship between \( X \) and \( Y \).

---

## **Steps to Calculate Covariance**

1. **Find the Mean** of \( X \) and \( Y \):
   $$
   \bar{X} = \frac{\sum X_i}{n}, \quad \bar{Y} = \frac{\sum Y_i}{n}
   $$

2. **Subtract the Mean** from each data point:
   - Compute \( (X_i - \bar{X}) \) for all \( X \).
   - Compute \( (Y_i - \bar{Y}) \) for all \( Y \).

3. **Multiply the Deviations**:
   - Calculate \( (X_i - \bar{X})(Y_i - \bar{Y}) \) for each pair of \( X \) and \( Y \).

4. **Sum the Products**:
   - Compute \( \sum (X_i - \bar{X})(Y_i - \bar{Y}) \).

5. **Divide by \( n - 1 \)** (for sample) or \( n \) (for population).

---

## **Example**

### Dataset:
| \( X \) | \( Y \) |
|-------|-------|
| 1     | 2     |
| 2     | 4     |
| 3     | 6     |
| 4     | 8     |
| 5     | 10    |

### Step 1: Calculate the Means
$$
\bar{X} = \frac{1 + 2 + 3 + 4 + 5}{5} = 3
$$
$$
\bar{Y} = \frac{2 + 4 + 6 + 8 + 10}{5} = 6
$$

### Step 2: Subtract the Means
| \( X \) | \( Y \) | \( X - \bar{X} \) | \( Y - \bar{Y} \) | \( (X - \bar{X})(Y - \bar{Y}) \) |
|-------|-------|----------------|----------------|--------------------------------|
| 1     | 2     | -2             | -4             | 8                              |
| 2     | 4     | -1             | -2             | 2                              |
| 3     | 6     | 0              | 0              | 0                              |
| 4     | 8     | 1              | 2              | 2                              |
| 5     | 10    | 2              | 4              | 8                              |

### Step 3: Sum the Products
$$
\sum (X - \bar{X})(Y - \bar{Y}) = 8 + 2 + 0 + 2 + 8 = 20
$$

### Step 4: Divide by \( n - 1 \) (Sample Covariance)
$$
\text{Cov}(X, Y) = \frac{20}{5 - 1} = \frac{20}{4} = 5
$$

---

## **Applications**

1. **Statistics**:
   - Understanding relationships between variables.
2. **Portfolio Management**:
   - Measuring how stock prices move together.
3. **Machine Learning**:
   - Feature selection and correlation analysis.

---

## **Limitations**
- Covariance is **not standardized**, making it difficult to interpret its magnitude directly.
- To address this, the **correlation coefficient** is often used:
   $$
   \text{Correlation} = \frac{\text{Cov}(X, Y)}{\sigma_X \cdot \sigma_Y}
   $$
   
Where $$\sigma_X$$ and $$\sigma_Y$$ are the standard deviations of $$X$$ and $$Y$$, respectively.
   
---

Covariance is a foundational concept in understanding relationships between variables and serves as the basis for more advanced techniques like correlation and regression analysis.


