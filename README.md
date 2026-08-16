# NYC Dog Bite Incidents Statistical Testing
This personal project analyzes dog bite incidents across NYC to determine if a statistical association exists between dog characteristics and boroughs. The goal of the analysis is to perform hypothesis testing (chi-square test of independence) to extract actionable insights and highlight patterns that could support the Department of Health and Mental Hygiene (DOHMH) in its data-driven decision-making.

# Tools Used
-Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy)

# Key Task
-Conducted data cleaning on a real-world messy dataset, handled missing values, blanks, formatting errors, and numeric conversions. 

-Conducted descriptive statistics to understand and summarize the data, ensuring data quality and identifying patterns in the data.

-Conducted univariate visualizations to identify the distributions of the categorical variables.

-Conducted bivariate visualizations to visualize the associations between dog characters and boroughs.

-Performed chi-square tests of independence to determine significant statistical associations.

-Calculated Cramer’s V to measure the strength of association between the variables.

# The Process
I started by importing the necessary tools for analysis in Jupyter Notebook. The first step was performing data cleaning since the dataset was messy. I checked for duplicates, missing values, blanks, formatting errors, and numeric conversions.

Missing values and blanks were detected in the dataset. I did not drop those rows or fill them in with an estimated value. First, I converted the blanks to NaN so they would be recognized as missing values during analysis. As I looked into the pattern of missingness, I realized the data was Missing Not At Random (MNAR), meaning the missingness was related to the value itself, not just random chance. Because filling it in with an estimated value, such as the mean or mode, would have introduced an assumption about what the value likely was and hidden that pattern, I labeled the missing categorical values as "Unknown" instead, so the missingness remained visible as its own category rather than being guessed at.

After data cleaning, I conducted univariate and bivariate visualizations of the variables I will use for my statistical analysis to identify their distributions and visualize their associations before conducting the test.
<img width="762" height="561" alt="Image" src="https://github.com/user-attachments/assets/15c77a33-75e7-480f-b199-cfeeaa0ee15a" />
![Image](https://github.com/user-attachments/assets/5cbca6f6-b6ac-4762-a22f-543939f84c8c)
![Image](https://github.com/user-attachments/assets/5899320b-03c3-4623-bb8a-ab17b660947f)
![Image](https://github.com/user-attachments/assets/9bbfde35-cd90-4635-9c05-29d98b76cd04)
![Image](https://github.com/user-attachments/assets/4e6b0ad9-e292-4ea7-8469-72117ffe82cd)

Since both tests use categorical variables, I conducted the Chi-Square Test of Independence.

For both Chi-Square tests, "Unknown" and "Other" were excluded. These values were assigned during data cleaning to preserve missingness without guessing at an estimated value, and including them wouldn't be relevant to answering the research questions.


Research Question 1: Is there an association between a dog’s gender and its spay/neuter status in reported bite incidents?

Null Hypothesis: There is no statistically significant association between a dog’s gender and its spay/neuter status in bite incidents.

Alternative Hypothesis: There is a statistically significant association between a dog’s gender and its spay/neuter status in bite incidents.


Research Question 2: Is there an association between a dog’s spay/neuter status and the borough where the bite incident occurred?

Null Hypothesis: There is no statistically significant association between a dog’s spay/neuter status and the borough in which the bite incident occurred.

Alternative Hypothesis: There is a statistically significant association between a dog’s spay/neuter status and the borough in which the bite incident occurred.

# What I Learned
Chi-Square Test 1 Results:

![Image](https://github.com/user-attachments/assets/dcd112ca-840f-452d-bea3-dc80cddde650)
![Image](https://github.com/user-attachments/assets/31d9db5b-5cfd-4832-b824-e6b7ed0f42fd)

The p-value is less than .001, which is below the significance level of 0.05, so we reject the null hypothesis. Cramér's V is 0.038, indicating a negligible association between a dog's gender and its spay/neuter status. Although the association is statistically significant, it is too weak to be meaningful in practice.

Chi-Square Test 2 Results:

![Image](https://github.com/user-attachments/assets/b03fd056-38cd-436c-ae90-183db7a368a2)
![Image](https://github.com/user-attachments/assets/aa5de5f1-463a-47f4-999d-37897a8e3c51)

The p-value is less than .001, which is below the significance level of 0.05, so we reject the null hypothesis. Cramér's V is 0.130. Given this table has 4 degrees of freedom, that value falls close to the threshold for a moderate association rather than a negligible one. This suggests spay/neuter status and borough have a more meaningful relationship than the gender comparison above, even though both results are statistically significant.

# Future Considerations
-Since gender showed a negligible association with spay/neuter status, outreach efforts are unlikely to benefit from being tailored by gender based on this analysis.

-The moderate association between spay/neuter status and borough suggests unspayed/unneutered dogs are more frequently involved in reported bite incidents in certain boroughs (e.g., Bronx, Queens) than others, which may be worth further investigation by DOHMH.

-Because this analysis only includes reported bite incidents rather than a comparison to the general dog population, it cannot confirm that spay/neuter status increases bite risk, only that the two are associated within this dataset. Comparing bite-incident data to borough-level spay/neuter registration rates would help clarify whether this reflects an actual risk pattern or differences in dog population/reporting across boroughs.

-These findings could serve as a starting point for identifying where spay/neuter awareness efforts might be worth prioritizing, pending further validation with population-level data.
