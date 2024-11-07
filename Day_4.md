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
    A confidence interval has a lower and upper bound that contains the true value of a parameter. A 95% yconfidence level is most commonly used across disciplines, corresponding to a level of significance of 
     α=0.05
    If we sample from a population with an approximate normal distribution, a confidence interval can be calculated as:<br>
              ![](https://github.com/Gauthamnair-Ronin/ICTAK-1/blob/main/equation1.png)<br>
    Where y is the mean of the sample, tn-1, $\alpha$ /2 is the value t from the t-distribution, s is the standard deviation, and n is the number of observations.
  - Standard Deviation-  It calculates the measure of how spread out the values are in relation to the mean (average) value
      ![](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/variation-for-data-comparisons/estimate-probability/images/cb3a31ab266c4db9e116a9cbf60734b2_656-e-37-fb-5341-4-c-5-a-8-daa-ededf-79904-b-8.png)

  - Variance - Variance is a measure of how spread out a set of values is from their average (mean). A higher variance indicates greater variability, while a lower variance suggests less variability.
    <br> ![](https://i.pinimg.com/564x/4e/cb/d0/4ecbd0703254a347f004bdb700f602ac.jpg)
  - Box PLOT
      - Shows median(q2), q1, q3, LB, UB, Outliers
  - Univariate = data related to one variable
  - Scatter Plot (Bivariate Analysis)
      - Visually inspecting Correlation between two Variables
  - Correlation coefficient (-1 to 1)
    
      - Pearsons Correlation Coefficient
          <br> We can use the pearson correlation coefficient to measure the **linear relationship between two variables**.
         -  With a correlation analysis we can determine:
                - How strong the correlation is
                - and in which direction the correlation goes.
              <br> We can read the strength and direction of the correlation in the Pearson correlation coefficient r, whose value varies between -1 and 1.
             ![](https://miro.medium.com/v2/resize:fit:2000/1*H4Ssq7V7mgWRRJhrIGhw7Q.png)
      - Spearman Correlation Coefficient
          The Spearman rank correlation examines the relationship between two variables, being the **non-parametric counterpart** of Pearson's correlation. Therefore, in this case, a normal distribution of the               data is not required.
        <br> Spearman correlation **uses the ranks** of the data rather than the original data, hence the name rank correlation.
  - Probability density function
      A PDF is a function that describes the probability distribution of a continuous random variable. It's used to calculate the likelihood of a random variable falling within a specific range of values. PDFs are a fundamental concept in probability theory and statistics

    A probability distribution function can refer to a PDF, but it can also refer to a cumulative distribution function or a probability mass function (PMF). A PMF is used for discrete random variables, while a PDF is used for continuous random variables.
  - Cumulative Density Function
      - Advantage
  - Scaling can be used to convert two tables of data in two different ranges into a single range data

  

