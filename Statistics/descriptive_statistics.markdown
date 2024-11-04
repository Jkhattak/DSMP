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