# A-B-Testing-Analysis-of-Digital-Marketing-Campaigns

### Summary

In this project, an analysis based on A/B testing will be conducted to evaluate the effectiveness of digital marketing campaigns. We have a dataset where users are assigned to different advertisement groups, and their conversion status is tracked. The data includes information such as the advertisement group the users belong to (test_group), the total number of ad impressions (total_ads), the day with the highest ad impressions (most_ads_day), and the hour with the highest ad impressions (most_ads_hour). The objective is to understand the effects of ad impressions on conversion rates and identify the days and time slots with the highest conversion rates.

### Problem:

To understand how ad impressions impact user conversion rates. To answer this question, various analyses will be conducted. Users are divided into two different test groups (ad and psa), and conversion rates will be compared for each group. Additionally, the relationship between the timing of ad impressions (the day and hour with the highest impressions) and conversion rates will be examined.




In this analysis, the relationship between the most_ads_day variable and the converted variable was examined, and conversion rates (CVR) were calculated for each day. According to the results:

-   The highest conversion rate occurred on Monday (3.28%).
-   Compared to other days, Monday stands out as a more effective day for conversions.
-   This finding suggests that focusing on Monday in marketing strategies could be beneficial for increasing conversion rates.

![bar2](https://github.com/user-attachments/assets/c562cd88-87fc-4661-b9cd-e06d493e612b)
![box1](https://github.com/user-attachments/assets/533c240d-18fd-4a7e-b8f5-cf82e81c676c)
![bar1](https://github.com/user-attachments/assets/2efc0504-d76a-4971-879c-a6d6161f5ded)

The conversion rate is a critical metric that measures the success of an advertising campaign and evaluates the effectiveness of marketing strategies. Since it shows the ratio of ad impressions or interactions that lead to conversions, it plays an important role in the decision-making processes of advertisers, digital marketing teams, and strategists.

![cr](https://github.com/user-attachments/assets/06acf657-40b2-426d-8831-d8db8c691f81)

![bar3](https://github.com/user-attachments/assets/12a1cf8f-8a87-4af0-87c5-e6605f486674)

-   Ad Group (CR = 0.1): This means that 10% of the users in the ad group completed the desired action (e.g., clicking, making a purchase, signing up) after being exposed to the advertisement.

-   PSA Group (CR = 0.07): This means that 7% of the users in the PSA group took the desired action after seeing the content related to the Public Service Announcement (PSA), which typically doesn't include paid ads.


# Statistical Testing:

##### Normality assumption

Many parametric tests are based on the assumption of normal distribution. For these tests to be valid, the data must follow a normal distribution. If the data does not follow a normal distribution, the results may be misleading.

To perform parametric tests, it is important to first check if the data meets the assumption of normality. If the data does not follow a normal distribution, the results of parametric tests may be misleading. To assess whether the data follows a normal distribution, various normality tests can be used. These include:
 - Shapiro-Wilk Test
 - Kolmogorov-Smirnov Test:
 - Anderson-Darling Test: 
 
Since our dataset contains more than 5,000 observations, it is not possible to apply the Shapiro-Wilk test. Therefore, we will use the Kolmogorov-Smirnov test.

##### Kolmogorov-Smirnov test

ad_group:
Null Hypothesis (H₀): : The distribution of the data is normal. (The data follows a normal distribution.)

Alternative Hypothesis (H₁): The distribution of the data is not normal. (The data does not follow a normal distribution.)


psa_group:

Null Hypothesis (H₀):  The distribution of the data is normal. 
Alternative Hypothesis (H₁): The distribution of the data is not normal.

Asymptotic one-sample Kolmogorov-Smirnov test

data:  ad_group
D = 0.53877, p-value < 0.00000000000000022
alternative hypothesis: two-sided


	Asymptotic one-sample Kolmogorov-Smirnov test

data:  psa_group
D = 0.53577, p-value < 0.00000000000000022
alternative hypothesis: two-sided


Both ad_group and psa_group do not follow a normal distribution according to the Kolmogorov-Smirnov test. Since the data fails the normality test, parametric tests that assume normality (such as t-tests or ANOVA) would not be appropriate for analyzing these data. Instead, non-parametric tests, which do not assume normality, should be considered for further analysis.


##### Mann-Whitney U test


Null Hypothesis (H₀): There is no significant difference in conversion rates (converted) between the "ad" and "psa" groups. 

Alternative Hypothesis (H₁): There is a significant difference in conversion rates between the "ad" and "psa" groups. 

data:  converted by test_group
W = 6691636830, p-value = 0.0000000000001705
alternative hypothesis: true location shift is not equal to 0


The Mann-Whitney U test tests the median differences between groups. Since the p-value is very small, the null hypothesis is rejected, and it is concluded that there is a significant difference in conversion rates between the "ad" and "psa" groups.



# Results

According to the results of the A/B test, the conversion rate of the advertising group (10%) is higher, meaning that users exposed to ads have a significantly higher conversion rate compared to the group that did not see ads. It was concluded that ad impressions have a significant impact on conversion rates, and marketing strategies can be shaped accordingly. It was suggested that focusing on Monday, the day with the highest conversion rate, could be more effective in marketing strategies. In this process, non-parametric tests were used instead of parametric tests to obtain accurate and reliable results.

















