# EXPLORATORY DATA ANALYSIS
![](https://cdn.prod.website-files.com/63119622d2a6edf1d171e0bc/65d3a069871456bd33730869_GC2xT1oWgAA1rAC.jpeg)

### DATATYPES
-  Continuous
-  Discrete
  -  Classification and regression

### VISUALISATION
Data visualization is an important component of Exploratory Data Analysis (EDA) because it allows a data analyst to “look at” their data and get to know the variables and relationships between them. In order to choose and design a data visualization, it is important to consider two things:
<br> 1) The question you want to answer (and how many variables that question involves).
<br> 2) The data that is available. (is it quantitative or categorical?)

#### Quantitative variables
<br> Box plots (or violin plots) and histograms are common choices for visually summarizing a quantitative variable. These plots are useful because they simultaneously communicate information about minimum and maximum values, central location, and spread. Histograms can additionally illuminate patterns that can impact an analysis (eg., skew or multimodality).
<br> ![](https://static-assets.codecademy.com/Paths/data-analyst-career-path/EDA-visualizations/boxplot_rent_blue.svg)

#### Categorical variables
<br> For categorical variables, we can use a bar plot (instead of a histogram) to quickly visualize the frequency (or proportion) of values in each category. For example, suppose we want to know how many apartments are available in each borough. We can visually represent that information as follows:
<br>![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSxOe4UoJwBFEMWnuHHN6sNnUwXdQbBYNGilw&s)

### Matplolib
-  Figures 
-  Axis labels
-  Sub-figures
-  Ticks
### Types of Plots
-  Line plots
      -   Variables: Continuous data with one variable on the x-axis and another on the y-axis.
          <br>Use Case: Used to show trends over time, smooth relationships, or changes in continuous data.

-  Bar charts
      -  Variables: Categorical data on the x-axis and numerical values on the y-axis.
          <br>Use Case: Used to compare discrete categories or groups.
-  Pie charts
      -  Variables: Proportional data, typically percentages summing up to 100%.
          <br>Use Case: Best for showing part-to-whole relationships but less effective with many categories.
-  Histogram
      -  Variables: Numerical data divided into bins (intervals).
          <br>Use Case: Used to visualize the frequency distribution of data.
-  CDF plot
      -   Variables: Sorted numerical data to show the cumulative proportion.
          <br>Use Case: Used to understand the probability or cumulative frequency distribution.
-  KDE plot
      -  Variables: Continuous numerical data.
          <br>Use Case: Used to estimate the probability density function of a variable, smoother than a histogram.
-  Scatter Plot
      -  Variables: Two continuous variables plotted against each other.
          <br>Use Case: Used to identify relationships, patterns, or correlations between two variables.

      -  With color -> Variables: Two continuous variables, with a third variable used to encode color.
                        <br>Use Case: Used when adding an extra dimension to show variation in another attribute.
-  Heatmaps
      -  Variables: Matrix-like data with categories or indices on both axes.
          <br>Use Case: Used to visualize data intensity or density across two categorical dimensions.
-  Box plots
      -  Variables: Numerical data grouped by a categorical variable.
          <br>Use Case: Used to show the distribution, central tendency (median), and variability of data, including outliers.
 <br> *A scatter plot is a great option for investigating the relationship between two quantitative variables. For example, if we want to explore the relationship between rent and size_sqft, we could create a scatter plot*

### Seaborn
<br>   Seaborn is great for quickly creating visually appealing plots with minimal code, while Matplotlib offers more customization options and fine-grained control over every aspect of a plot.

### Feature Extraction and Transformation

### Features and Labels

### Featurization
-  Text Data
    -  BoW
    -  TFIDF
-  Feature Engineering
-  Feature Orthogonality
    -  Meaning features that are orthogonal to each other maybe be more useful when having relationships
-  Cosine Similarity
-  Feature Colinearity
-  Feature Slicing
-  Indicator variable
-  Feature bening
-  Mathematical Transforms  
  -  Logarithms
  -  FFT & STFT


## Seaborn and matplotlib is used to perform data exploration
  - a stage we execute after data cleaning..
     -  Use of correlation- when selecting features to train a  model, if there are 1000 features, instead of training all of them , we can take the correlation data, and using it, select those data that has extreme corr data and train the model using the same- result will be the same.

 It is always better to select those features that have correlation value low with each other. Using orthogonal features will yield better results through the model.

  ### Cosine similarity
 -  Cos sim= u.v/(|u| |v|). If u and v are orthogonal, cos sim will be zero  Check for orthogonality

### Colinearity - features sharing similarity in characteristics - NON Desirable

  Assume f1,f2,f3
    <br>And f2= 1.5*f1
    <br>Ie - f1, 1.5*f1, f3 - HERE there exist colinearity among f1 and f2 and these are non desirable as a training features

 ### Feature Slicing

  Assume Height, weight , haircolor, eyecolor, country of origin as features
  <br>We gotta predict Gender.
  <br>Suppose we have data on only 2 countries with majority india(80%) that arent equally distributed
  <br>We may already have a domain knowledge on this dataset.
  <br>If we were to train directly using this, the model would perform poorly.
  <br>But since we have 2 country, we split the data into india and usa, and train 2 models so that we have 2 models experienced in two categories of prediction.
 <br>Conditions-

   1) We have sufficient data for both models
  
   2) There should exist a disparity among the data . why? Becuz if the 2 categories have 50-50 data distribution then using a single model will more or less give the same prediction rate meaning the error rate for single model will approax the error rate of individual models. 
  <br>When there exist disparity, individual models will show lower error rate compared to single model.
<br>
In data science, horizontal slicing and vertical slicing are two techniques for developing software that differ in their approach and focus: 


#### *Horizontal slicing*
  A traditional approach that focuses on technical tasks and developing software layer-by-layer. It's ideal for features with multiple layers or components. 


 #### *Vertical slicing*
  An agile approach that focuses on delivering thin slices of functionality across all layers of the application stack. It's ideal for projects that require a fully functional system at each stage of development.

 ### Feature Binning
   Assume a column height with values. And u want to categorise the height say values below a value like 150 and above it as 0 and 1. Thus we can add a new column of 1s and 0s under a condition and this variable will be called Indicator variable.
      <br>And if we add more than 1 indicator variable essentially adding more categories, the method will be called Feature Binning.

   ### Mathematical Transforms
  Transformations help bring uniformity and symmetry to the data as symmetric data always performs better in a model - same reason why 50-50 data has minimum error in a d=single model.
<br>Data that are unsymmetric or non uniform will have some disparity one 2 or more dimensions causing  single models to perform poorly.
  
-  Logarithms
      <br>Taking a log of 2 tailed dist will help reduce the tailed dist and provide little more symmetry/ uniformly distributed

-  Box -Cox transformation
  <br>  More complex and precise than log

      
