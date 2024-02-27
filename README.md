## North Carolina State Center Birth Statistics Case Study

**Introduction**

This case study analysis will focus on a random sample of 50 births from the available 800 records within the North Caroline Birth Registry dataset.

**Objectives** 

The objective of this analysis is to understand the concept of sampling distributions, compute and interpret confidence intervals for population parameters such as the population mean or proportion and calculate the difference between two sample measures. Using R for this analysis, I will calculate the probability (percentage) for variables sex and smoke and the difference in the proportion (percentage) of low-birth-weight babies between married and non-married mothers. Additionally, I will calculate mean age and weight as well as the difference between the continuous qualitative (gained, tgrams) and qualitative categorical variables (marital, low).

**Data Description of Variables**

![Screenshot 2024-01-26 130924](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/05f9847f-ca03-42cb-8469-b9978bfff1ae)

**Note:** MAGE is a discrete quantitative variable. GAINED and TGRAMS are continuous quantitative variables. SEX, SMOKE, MARITAL and LOW are qualitative categorical value with numerical values (0, 1 OR 2).

**Data**

The data below represents a simple random sample (SRS) of 50 records from the available 800 within the North Carolina Birth Registry dataset NCBIRTH800. 95 percent confidence intervals will be calculated for the file name: **LDS_C02_NCBIRTH800**

![Screenshot 2024-01-26 131042](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/8ed09c6d-d7e7-489d-b0c2-09ab0f241531)

![Screenshot 2024-01-26 131103](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/7cae4639-b6d5-400a-a2bb-b29f18e2579a)

**Results and Discussion**

Using a simple random sample (SRS) of 50, calculate the 95 percent confidence interval for: 

**a)	the proportion (percentage) of male children**

•	An exact binomial test is used when an experiment has two possible outcomes (i.e success/failure) and you have an idea about what the possibility of success is. It is run to see if observed results differ from what was expected.

	Exact binomial test
 
	data:  22 and 50
 
	number of successes = 22, number of trials = 50, p-value = 0.4799
 
	alternative hypothesis: true probability of success is not equal to .5
 
	95 percent confidence interval: 0.2999072 0.5874559

	sample estimates: probability of success 0.44

o	The variable sex is a qualitative categorical value where 1 = male and 2 = female. In the SRS of 50 records, 22 of the births were male. The p value is 0.4799 and the alternative hypothesis states that the true probability of success is not equal to 0.5. The observed proportion of success is the sample estimate, which is approximately 0.44. We are 95% confident that the population proportion p is between 0.2999072 and 0.5874559, because in repeated sampling, about 95 percent of the intervals constructed in the manner of the present single interval would include the true p. On the basis of these results, we would expect with 95 percent confidence, to find somewhere between 29.990% and 58.745% of births to be male. 

**b)	the mean age of a mother giving birth**

  ![Screenshot 2024-02-27 153205](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/9224c74b-46da-4188-8e7d-2fc44302f736)

o	For the SRS of n=50, the mean for variable mage is 25.68, close to the median of 25, and the standard deviation is 5.85. The range is 23 years old (the highest age is 38 and the lowest age is 15 years old).

![image](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/a3310d08-8c66-48ca-8402-5f29dec77b29)

o	SRS is 50. The histogram for variable mage represents a distribution curve with mothers falling within the most frequent age group of 20-25 years old. The age group with the lowest frequency is 35-40 years old. Skew for mage is 0.21 and kurtosis is -0.97 and platykurtic.

![image](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/49cd041d-ba7a-4e65-8ffb-3118a08c1c78)

**Min. | 1st Qu. | Median  | Mean | 3rd Qu. | Max**

15.00 | 21.00 | 25.00  | 25.68  | 30.75  | 38.00

o	SRS is 50. The IQR for variable mage is 9.75. 3rd quartile (30.75) – 1st quartile (21) = IQR (9.75). Lower extreme = 15; Upper extreme = 38; Range = 23

•	A one sample t-test is used to test whether the mean of a population is equal to some value and whether the difference between an SRS is statistically significant to the population.

**One Sample t-test**

data:  ncb50$mage t = 31.022, df = 49, p-value < 2.2e-16

**alternative hypothesis:** true mean is not equal to 0 95 percent confidence interval: 24.01647 27.34353

**sample estimates:** mean of x 25.68

o	We wish to construct the sampling distribution of the sample mean, x, based on samples of size n=50 drawn from this population. The output tells us that the sample mean is 25.68 and standard deviation is 5.85. 

o	The standard error of the sample mean is where 5.85 is divided by the square root of the sample, 50. The standard error of the mean is 0.827315 or .83.

o	The 95 percent confidence interval falls between 24.016% and 27.343%

**c)	the mean weight gained during pregnancy** 

 ![Screenshot 2024-02-27 153619](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/b7745004-cdcc-4daa-8eaf-3ecef9de9740)

o	For the population of 50, the mean weight gained for women during pregnancy was 26.88, close to the median of 25. The range is 61 with 0 pounds weight gained as the min and 61 pounds gained as the max.

![image](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/52abde73-b515-4c3b-a348-7006aea11c31)

o	SRS is 50. The histogram for variable gained represents a normal curve. The most amount of weight gained falls between 20 to 40 pounds. Weight gain (in pounds) decreases significantly after 40 pounds. Skew for gained is 0.12 and kurtosis is -0.21 and mesokurtic.

![image](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/caff58a7-cd11-4036-b0e3-57a5bc93a254)

**Min. | 1st Qu.  | Median    | Mean  | 3rd Qu. | Max.**

0.00   | 18.25   | 25.00   | 26.88   | 35.00 | 61.00

o	SRS is 50. The IQR for variable gained is 16.75. 3rd quartile (35) – 1st quartile (18.25) = IQR (16.75). Lower extreme = 0; Upper extreme = 61; Range = 61

**One Sample t-test**

data:  ncb50$gained t = 13.385, df = 49, p-value < 2.2e-16

**alternative hypothesis:** true mean is not equal to 0

95 percent confidence interval: 22.84422 30.91578

**sample estimates:** mean of x 26.88 

o	We wish to construct the sampling distribution of the sample mean, x, based on samples of size n=50 drawn from this population. The output tells us that the sample mean is 26.88 and SD is 14.2. 

o	The confidence coefficient is the quantity 1- α, or .95 in this case. The interval  is called a confidence interval for μ, or the mean. When (1- α ) =.95, the interval is called the 95 percent confidence interval for μ.

o	The standard error of the sample mean is calculated as   where 14.2 is divided by the square root of the sample, 50. The standard error of the mean is 2.00818 or 2.01.

o	We wish to construct the sampling distribution of the sample mean, x, based on samples of size n=50 drawn from this population. An approximate 95 percent confidence interval for μ is given by   . The 95 percent confidence interval falls between 22.844% and 30.915%.

**d)	the proportion (percentage) of mothers admitting to smoking during pregnancy**

**Exact binomial test**

	data:  8 and 50, number of successes = 8, number of trials = 50, 
 
	p-value = 1.164e-06

	alternative hypothesis: true probability of success is not equal to .5
 
	95 percent confidence interval:0.07170077 0.29112631
 
	sample estimates: probability of success 0.16 

o	The variable smoke is a qualitative categorical value where 0 = mother did not smoke during pregnancy and 1 = mother did smoke during pregnancy.  In the SRS of 50 records, 8 mothers admitted to smoking during pregnancy. The p value is 1.164e-06 and the alternative hypothesis states that the true probability of success is not equal to 0.5. The observed proportion of success is the sample estimate, which is approximately 0.16. We are 95% confident that the population proportion p is between 0.07170077 and 0.29112631, because in repeated sampling, about 95 percent of the intervals constructed in the manner of the present single interval would include the true p. On the basis of these results, we would expect with 95 percent confidence to find somewhere between 7.170% and 29.112% of mothers that have admitted to smoking during pregnancy.

**e)	the difference in the average weight gained between smoking and nonsmoking mothers**

![Screenshot 2024-02-27 154427](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/26b0fd47-f376-4ffd-b8f9-368afd18216a)

o	The SRS is 50. For variable gained, the mean is 26.88, median is 25, and IQR is 16.75. Range is 61, lower extreme = 0 and upper extreme = 61. Standard deviation is 14.2

![Screenshot 2024-02-27 154535](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/d7381bd5-b269-4a1c-8b81-0d16226d70d1)

o	Descriptive statistics are generated for continuous quantitative variable gained as grouped by qualitative categorical variable smoke. The results show summary statistics between smokers (value = 1) and non-smokers (value = 0) in comparison to the distribution of weight gained. Nonsmokers = 42 and smokers = 8.

**Standard error:** 4.74867224

**95 percent CI:** (27.83-21.88=5.95); 5.95±1.96 (4.748) ; 5.95±9.307 = (-3.357, 15.257)

o	The standard error is 4.7486. We are 95 percent confident that the true difference, μ1 - μ2, is somewhere between -3.357 and 15.257. Since the interval includes zero, we conclude that the population means may be equal.

![image](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/a363e01b-6aec-4cda-8a87-28b705603e78)

o	First box is variable gained, second box is variable smoke (group 0 = non-smokers) and third box is variable smoke (group 1 = smokers). IQR for gained is 16.75 (Q3 as 35 minus Q1 as 18.25), IQR for smoke(0) is 19.5, and IQR for smoke(1) is 16.25.

![image](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/701fe189-b192-4b7c-ba76-0843a2b8e14f)

o	The SRS is 50. The continuous quantitative variable gained is compared against qualitative categorical variable smoke (0 = non-smokers and 1 = smokers)

**Quartiles for smoke = 0**: 19.25; 25; 38.75 

o	For variable smoke, group 0, the 1st quartile is 19.25, middle (2nd) quartile is 25 and 3rd quartile is 38.75. IQR is (38.75 – 19.25) = 19.5.

**Quartiles for smoke = 1**: 14.25; 23.5; 30.5

o	For variable smoke, group 1, the 1st quartile is 14.25, the middle (2nd) quartile is 23.5 and 3rd quartile is 30.5. IQR is (30.5 – 14.25) = 16.25.

•	The Welch two sample t-test compares the means of two independent groups when sample sizes and variances are unequal.

**Welch Two Sample t-test**

data:  subset(ncb50$gained, ncb50$smoke == 0) and subset(ncb50$gained, ncb50$smoke == 1) t = 1.2549, df = 11.437, p-value = 0.2346

**alternative hypothesis**: true difference in means is not equal to 0

95 percent confidence interval: -4.443972 16.360639

**sample estimates**: mean of x 27.83333 mean of y 21.87500 

o	The SRS is 50. We are 95 percent confident that the difference between population means is somewhere between -4.443 and 16.360. If we were to repeat the study many times and compute confidence intervals in the same, about 95 percent of the intervals would include the difference between the population means. Based on the results of the two-sample t-test with a p value of 0.2346, greater than the common significance level of 0.05, we fail to reject the null hypothesis. Since the interval includes zero, we conclude that the population means may be equal. When calculating manually, the 95 percent CI resulted in the range of -3.357 and 15.257 - there is no significant difference in the bounds.

•	A two sample t-test is used to determine whether two population means are equal.

**Two Sample t-test**
data:  subset(ncb50$gained, ncb50$smoke == 0) and subset(ncb50$gained, ncb50$smoke == 1) t = 1.0898, df = 48, p-value = 0.2813

**alternative hypothesis:** true difference in means is not equal to 0

95 percent confidence interval: -5.034951 16.951617

**sample estimates:** mean of x 27.83333 mean of y 21.87500

o	The SRS is 50. We are 95 percent confident that the difference between the population means is somewhere between -5.0349 and 16.9515. By comparing the results of the Welch two-sample t-test and the standard two-sample t-test, we can conclude there is no substantial difference in the conclusions. Since the interval includes zero, we conclude that the population means may be equal. The smoking habit of pregnant women will not have a significant impact on their weight gained during pregnancy.

**f)	the difference in the average birth weight in grams between married and nonmarried mothers**

![Screenshot 2024-02-27 154915](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/1b7eb626-91fb-46f9-be5d-64a505a7a141)

o	The SRS is 50. For variable tgrams, the mean is 3193.91, median is 3274.43, and IQR is 928.46. The standard deviation is 774.12. The range is 4167.45, with a lower extreme = 453.6 and upper extreme = 4621.05.

**Descriptive statistics by group**

![Screenshot 2024-02-27 155011](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/2da08ceb-b91f-4752-9359-dd4cbcfe9ac6)

o	Descriptive statistics are generated for continuous quantitative variable tgrams as grouped by qualitative categorical variable marital. The results show summary statistics between married (value = 1) and non-married (value = 2) women in comparison to the average birth weight in grams. Married mothers = 30 and nonmarried = 20.

**Standard error:** 233.23059237

**95 percent CI:** (3356.64-2949.82 = 406.82); 406.82±1.96 (233.2305) ; 406.82 ± 457.1317 =         (-50.311, 863.951)

o	The standard error is 233.230. We are 95 percent confident that the true difference, μ1 - μ2, is somewhere between -50.311 and 457.13. Since the interval includes zero, we conclude that the population means may be equal.

![image](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/1ef2615e-f878-4f6f-8007-5d48f31b0db9)

o	First box is variable tgrams, second box is variable marital (group 1 = married) and third box is variable marital (group 2 = not married). IQR for tgrams is 928.46 (Q3 as 3678.4 minus Q1 as 2749.9), IQR for marital(1) is 928.46, and IQR for marital(2) is 793.8.

![image](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/baa5e268-25dd-4d22-8dcf-642a0eca90b0)

o	The SRS is 50. The continuous quantitative variable tgrams is compared against qualitative categorical variable marital, where 1 = mothers who are married and 2 = mothers who are not.

**Quartiles for marital = 1:** 2884.612; 3472.875; 3813.075 

o	For variable marital, group 1, the 1st quartile is 2884.612, middle (2nd) quartile is 3472.875 and 3rd quartile is 3813.075. IQR is (3813.075 – 2884.612) = 928.46, the same IQR as tgrams.

**Quartiles for marital = 2:** 2721.6; 3047.625; 3515.4 

o	For variable marital, group 2, the 1st quartile is 2721.6, the middle (2nd) quartile is 3047.625 and 3rd quartile is 3515.4. IQR is (3515.4 – 2721.6) = 793.8

**Welch Two Sample t-test**

data:  subset(ncb50$tgrams, ncb50$marital == 1) and subset(ncb50$tgrams, ncb50$marital == 2) t = 1.7443, df = 31.586, p-value = 0.09083

**alternative hypothesis:** true difference in means is not equal to 0

95 percent confidence interval: -68.49842 882.14342

**sample estimates:** mean of x 3356.640 mean of y 2949.818 

o	The SRS is 50. We are 95 percent confident that the difference between population means is somewhere between -68.4984 and 882.14342. If we were to repeat the study many times and compute confidence intervals in the same, about 95 percent of the intervals would include the difference between the population means. Based on the results of the two-sample t-test with a p value of 0.09083, greater than the common significance level of 0.05, we fail to reject the null hypothesis. Since the interval includes zero, we conclude that the population means may be equal. When calculating manually, the 95 percent CI resulted in the range of -50.311 and 863.951, there is no significant difference in the bounds. The marital status of the mother does not significantly impact the birth weight of the child.

**g)	the difference in the proportion (percentage) of low-birth-weight babies between married and nonmarried mothers**

![Screenshot 2024-02-27 152937](https://github.com/efejzic/Inferential_Birth_Statistics/assets/119814593/44dbd899-ee05-45ff-beea-9a995f3b11a1)

•	A proportion test (prop test) is used to assess whether the proportions of two independent groups (particularly categorical data) are significantly different from each other.
o	The two independent variables are marital status where 1 = married and 2 = not married, and variable low where 0 = infant was not low birth weight and 1 = infant was low birth weight. The cross table illustrates the levels of each variable and their frequency.

**2-sample test for equality of proportions without continuity correction**

data:  c(t[, 1]) out of c(t[, 1] + t[, 2])

X-squared = 0.99668, df = 1, p-value = 0.3181

**alternative hypothesis:** two.sided

95 percent confidence interval: -0.3055628  0.1055628

**sample estimates:** prop 1 0.1  prop 2 0.2

**Warning message:**

In prop.test(x = c(t[, 1]), n = c(t[, 1] + t[, 2]), conf.level = 0.95,  :

  _Chi-squared approximation may be incorrect_

•	The Chi-squared test is used to test the null hypothesis that the proportions in the two variable groups are equal and relies on the assumption that the sample size is large. The SRS sample for this data is 50.

o	We are 95 percent confident that the true proportion falls between the lower bound – 0.3055628 and upper bound 0.1055628. Based on the results of the test with a p value of 0.3181, greater than the common significance level of 0.05, we fail to reject the null hypothesis. There is not sufficient data to conclude that the proportions are significantly different. Since the interval includes zero, we conclude that the population means may be equal.

•	The Fisher’s exact test is another statistical test used to analyze categorical data and does not rely on a large sample size. Can be used when chi-squared assumptions are not met. I am using Fisher’s test since the Chi-square resulted in warning message that the approximation may be incorrect.

**Fisher's Exact Test for Count Data**

data:  matrix(c(t[, 1], t[, 2]), ncol = 2)

p-value = 0.4161

**alternative hypothesis:** true odds ratio is not equal to 1

95 percent confidence interval: 0.0585276 3.0475027

**sample estimates:** odds ratio 0.4520331

o	The p value for Fisher’s test is 0.4161, greater than the common significance level of 0.05, we fail to reject the null hypothesis for both tests. Both tests suggest there is no significant difference between the birth weights of the two populations.

**Conclusion**

The simple random sample for this analysis includes 50 records. There were 22 male births and 28 female births. The p value for the proportion (percentage) of male children is 0.4799 and the observed proportion of success is the sample estimate, which is approximately 0.44. On the basis of these results, we would expect with 95 percent confidence, to find somewhere between 29.990% and 58.745% of births to be male. The mean age of a mother was 25.68, the max age was 38 years, and the min age was 15 years old. The 95 percent confidence interval for the mean age of the mother falls between 24.016% and 27.343%. The mean weight gained during pregnancy was 26.88 pounds, max was 61 pounds and min was 0 pounds. The 95 percent confidence interval for mean weight falls between 22.844% and 30.915%. In the SRS of 50 records, 8 mothers admitted to smoking during pregnancy and 42 mothers did not. The p value for the proportion (percentage) of mothers admitting to smoking during pregnancy is 1.164e-06 and the observed proportion of success is the sample estimate, which is approximately 0.16. We would expect with 95 percent confidence to find somewhere between 7.170% and 29.112% of mothers that have admitted to smoking during pregnancy. When calculating manually for the difference in the average weight gained between smoking and nonsmoking mothers, the 95 percent CI resulted in the interval range of -3.357 and 15.257 pounds. The Welch two sample t-test resulted in the range of -4.443 and 16.360, and the standard two sample t-test resulted in the range of -5.0349 and 16.9515. By comparing the results of the Welch two-sample t-test and the standard two sample t-test, we can conclude there is no substantial difference in the conclusions. Since the interval includes zero, we conclude that the population means may be equal. The smoking habit of pregnant women will not have a significant impact on their weight gained during pregnancy. Within the SRS of 50, there were 30 married mothers and 20 nonmarried mothers. When calculating manually for the difference in the average birth weight in grams between married and non married mothers, the 95 percent CI resulted in the interval range of -50.311 and 457.13 grams. There is no significant difference when compared with the 95 percent interval range of the Welch two sample t-test, -69.498 and 882.142. Since the interval includes zero, we conclude that the population means may be equal. The marital status of the mother does not significantly impact the birth weight of the baby. The Chi-squared and Fisher’s test conclude that there is no significant difference between the birth weights of the two populations, married and nonmarried mothers.
