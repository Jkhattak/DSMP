# Statistics 

Statistics is a branch of mathematics that invovles `collecting, analysing, interpreting, and presenting data`. It provides `tools and methods` to understand and make sense of large amounts of data and to `draw conclusion` and `make decision based on the data`. 


## Type of Statistics

```mermaid 
graph TD
  Statistics --> Descriptive
  Statistics --> Inferential
  Descriptive --> MeasuresOfCentralTendency
  Descriptive --> MeasuresOfDispersion
  Inferential --> HypothesisTesting
  Inferential --> RegressionAnalysis


```

## Descriptive Statistics 

Descriptive Statistics is a branch of statistics that focuses on summarizing and organizing data in a meaningful way. It provides simple summaries about the sample and the measures. This can include measures of central tendency (such as mean, median, and mode) and measures of dispersion (such as range, variance, and standard deviation). Descriptive statistics help in understanding the basic features of the data, offering a quick overview without drawing conclusions or making predictions about the data.

## Infrential Statistics 


- Inferential Statistics is a branch of statistics that allows us to make predictions or inferences about a population based on data collected from a sample. It involves using probability theory to estimate population parameters, test hypotheses, and make decisions or predictions. Inferential statistics go beyond merely describing the data and help determine relationships, assess the reliability of estimates, and draw conclusions that extend beyond the data set at hand. 
  - Examples include hypothesis testing, confidence intervals, regression analysis, and ANOVA.


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

```mermaid
graph TD
    A[Types of data] --> B[Categorical or qualitative data]
    A --> C[Numerical or quantitative data]
    B --> D[Nominal data]
    B --> G[Ordinal data]
    C --> E[Discrete data]
    C --> F[Continous data]
```

- `Types of Data:` Data can be broadly classified into different types based on the characteristics of what is being measured or observed. These types help in selecting appropriate statistical methods for analysis.

- `Categorical or Qualitative Data:` This type of data represents characteristics or attributes that can be used to group or categorize objects but cannot be measured or counted numerically. Examples include gender, religion, and color.

- `Numerical or Quantitative Data:` This type of data represents values or observations that can be measured or counted and expressed numerically. Examples include height, age, and income.

- `Nominal Data:` A subcategory of categorical data, nominal data consists of labels or names used to identify or classify objects, but the order of these labels is not meaningful. Examples include eye color (blue, brown, green) and type of cuisine (Italian, Chinese, Mexican).

- `Ordinal Data:` Another subcategory of categorical data, ordinal data represents categories that have a meaningful order or ranking but the differences between the ranks are not quantifiable. Examples include rankings (1st, 2nd, 3rd) and satisfaction levels (satisfied, neutral, dissatisfied).

- `Discrete Data:` A subcategory of numerical data, discrete data represents countable values or numbers that can only take specific values. There are gaps between these values, such as the number of students in a class or the number of cars in a parking lot.

- `Continuous Data:` Another subcategory of numerical data, continuous data represents values that can take any value within a given range, and there are no gaps between the values. Examples include height, weight, and temperature. Continuous data can be measured to any level of precision, depending on the measurement tool.

## Measure of Central Tendency 

A measure of central tendency is a statistical measure that represents a typical or central value for a dataset. it provides a summary of the data by identifying a single value that is most representative of the dataset as whole. 

```mermaid
graph TD    

    A[Measure of Central Tendency] --> B[Mean]
    A[Measure of Central Tendency] --> C[Median]
    A[Measure of Central Tendency] --> D[Mode]

```

- `Mean:` The average of all values in a dataset, calculated by adding up all the values and dividing by the total number of values. The mean is sensitive to outliers, which can skew the result. 
  - For example, the mean of 2, 3, and 4 is (2+3+4)/3 = 3.

- `Median:` The middle value of a dataset when it is ordered from least to greatest. If there is an even number of values, the median is the average of the two middle numbers. The median is less affected by outliers and is often used when the data distribution is skewed. 
  - For example, the median of 2, 3, and 10 is 3.

- `Mode:` The value that appears most frequently in a dataset. A dataset may have one mode, more than one mode, or no mode at all if no value repeats. It is best use in categorical dataset.
  - For example, in the dataset 1, 2, 2, 3, the mode is 2.

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

### Weighted Mean

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


