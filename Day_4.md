# Statistics
![](https://stats4nr.com/Figs/stats_hypothesis.png)
- Best used for calculating (Science of )causal relationship
- Inferential and descriptive Statistics
  ## Central Tendency
   **A summary measure that attempts to describe a whole set of data with a single value that represents the middle or centre of its distribution.**
    - Mean,median,mode,minimum value, maximum value
    - Percentile.
      - Median is 50th percentile. 
      - Arrange in an order, count no: of elements, 20% of elements = 20th percentile.
      - 25th and 75th percentile is more popular. Represents Bell curve in Distribution.
      - ![](https://www.allmath.com/storage/2023/Nov/quartiles_82.png)
      - Symmetric distribution cases will have same mean and median values. Only Median is used in unsymmetric cases.
      - Percentile is useful selecting a fixed value from x number of values. Eg: 90th percentile of 100 is 10 but for 200, 95th percentile is 10.
      - Outlier = labelled on that data that is significantly far away from the trend of other data
      - Inter Quartile Range = 75th - 25th percentile after removing duplicates q1= 25th, q2= 50th, q3= 75th
        <br>
        IQR= q3-q1 <br>
        Lower bound LB= q1- 1.5xIQR <br>
        Upper bound UB= q3+ 1.5xIQR

      - Points above UB and Below LB are Outliers
  ## DISPERSION
  **Measurement of Variability**
  - Dispersion parameters are a measure of how much a sample fluctuates around a mean value.
  - Range - can be used to showcase spread of data
  - Z-Score (used for standarisation)
    <br> (x-u)/𝞼 where 𝝈- stdev, x=mean
      <br >Standarisation = can convert range of a graph to range from 0 to 1 without disrupting shape of graph
  - Confidence Interval
    A confidence interval has a lower and upper bound that contains the true value of a parameter. A 95% yconfidence level is most commonly used across disciplines, corresponding to a level of significance of α=0.05
    If we sample from a population with an approximate normal distribution, a confidence interval can be calculated as:
              
    Where y is the mean of the sample, tn-1,/2 is the value t from the t-distribution, s is the standard deviation, and n is the number of observations.

