# CLT, Hypothesis Testing-1

- Probability of a value occurring after a threshold in a bell curve = integral of the area under that part of curve.
- Probability distribution of a total area is ONE.
- Gaussian distribution 
  - Mean value will be any value 
- Normal distribution is special case of gaussian distribution.
- Sampling of data - Representative sample of small data taken from a large corpus of data as it is more feasible for doing inference. The sample data is supposed to perform and give more or less same results as the large corpus of data.
  - The Entire Data is called  Population
  - A small portion of data taken from population is called Sample
## Central Limit Theorem
When the means of a number of samples taken from a population when population is plotted , it tends to be a normal distribution called Sampling Distribution  and the mean of the SD will approax the mean value of the actual distribution. The higher the number of samples we take, the closer the mean of the SD will be to the mean of the actual distribution.

![](https://miro.medium.com/v2/resize:fit:433/1*LoCtj78Ow6QqdjRaDu53qw.jpeg)

[learn more](https://onlinestatbook.com/stat_sim/sampling_dist/)

- Without using CLT, it is possible to measure the significance of a variable in certain cases.
  -  Significance Level or Alpha value Decided by us
    - usually 2 thresholds - 0.05 or 0.01
    - If the probability of a variable is lower than the alpha value, then that event or variable is a rare event.
    - This is called Z-Test

  - Requirement for Z test = Population mean and population standard deviation
    - **z= (x_cap- pop_mean) / (𝞼 / sqrt(N))** , where N is the size of sample, x_cap is sample mean, 𝞼 is pop_SD
## Hypothesis Testing
- Null hypotheses
  - A hypothesis where the effect of  an experiment is assumed to be null or no existent.
- Alternate Hypotheses
  - Opp of null hypo - the hypothesis that says that the experiment do have significant effect on sample/popualtion.
- Paired Test or T test
  - T test 
    - Degree of freedom df = sample size -1
    - **T = (x_cap - u)/(s /sqrt(n))** where s is sample SD, x_cap is sample mean, u( u alla meu anu) = pop_mean and n is sample size
        <br > S/sqrt(N) is called  Standard Error.
    - <br>![](https://github.com/Gauthamnair-Ronin/ICTAK-1/blob/main/equation%202.png) is  the Sample t-test formula
    - For Independent samples t-test, the formula is
      <br> ![](https://github.com/Gauthamnair-Ronin/ICTAK-1/blob/main/equation%203.png)
      <br> where S1 and s2 are SD of samples 1 and 2. N1 and n2 are the number of cases in sample 1 and sample 2
    - P value
      1.  Two groups are taken . They are mixed up and then split again.
      2. From the 2 new groups, we take the mean weight value  assuming gm1 and gm2.
      3. Then the difference between gm1 and gm2 is calculated called it D1
      4. Then one group say g2 is given a diet. After completion of diet, the weight difference is calculated again, say gm_diet1 and gm_diet2.
      5. Difference between gm_diet1 and gm_diet2 is calculated, say D2.
      6. The difference between D1 and D2 is taken. If the p value from this difference is rare then the diet has an effect.
      7. When it comes to graph, the difference in weights  of samples taken from the 2 groups is plotted and the rarity observed in this graph will decide the significance of the Diet.
      8. If p value is lower than alpha value, then the hypothesis has an effect
    - **T test is performed when population Standard deviation is unavailable.
        <br>When population STD is both assumed/available Z test is performed.**

    - Example :
   
      ![](https://slideplayer.com/slide/14507488/90/images/5/Example+%E2%80%93+Performing+a+Hypothesis+Test.jpg)




