# NYC Dog Bite Incidents Statistical Testing
This personal project analyzes dog bite incidents across NYC to determine if a statistical association exists between dog characteristics and boroughs. The goal of the analysis is to perform hypothesis testing (chi-square test of independence) to extract actionable insights and highlight patterns that could support the Department of Health and Mental Hygiene (DOHMH) in its data-driven decision-making.

# Tools Used
-Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy)

# Key Task
-Conducted data cleaning on a real-world messy dataset, handled missing values, blanks, formatting errors, and numeric conversions. 

-Conducted descriptive statistics to understand and summarize the data, ensuring data quality and identifying patterns in the data.

-Conducted univariate visualization to identify the distributions of the categorical variables.

-Conducted bivariate visualization to visualize the associations between dog characters and boroughs.

-Performed chi-square tests of independence to determine significant statistical associations.

-Calculated Cramer’s V to measure the strength of association between the variables.

# The Process
I started by importing the necessary tools for analysis in Jupyter Notebook. The first step was performing data cleaning since the dataset was messy. I checked for duplicates, missing values, blanks, formatting errors, and numeric conversions.

Missing values and blanks were detected in the dataset. I did not drop those rows or fill them in with imputation because, as I analyzed the dataset, I realized the data was Missing Not At Random (MNAR), which is the most problematic type and can introduce bias if ignored. Due to this, I decided to replace the blanks and missing values with NaN or “Unknown” to prevent bias and avoid introducing assumptions through imputation. 

After data cleaning, I conducted univariate and bivariate visualizations of the variables I will use for my statistical analysis to identify their distributions and visualize their associations before conducting the test.
<img width="762" height="561" alt="Image" src="https://github.com/user-attachments/assets/15c77a33-75e7-480f-b199-cfeeaa0ee15a" />
![Image](https://github.com/user-attachments/assets/5cbca6f6-b6ac-4762-a22f-543939f84c8c)
![Image](https://github.com/user-attachments/assets/5899320b-03c3-4623-bb8a-ab17b660947f)
![Image](https://github.com/user-attachments/assets/9bbfde35-cd90-4635-9c05-29d98b76cd04)
![Image](https://github.com/user-attachments/assets/4e6b0ad9-e292-4ea7-8469-72117ffe82cd)

Since both tests use categorical variables, I conducted the Chi-Square Test of Independence.

For both Chi-Square tests, “Unknown” and “Other” were excluded from the tests. These values were only filled during data cleaning to prevent introducing bias, and including them wouldn’t be relevant to answering the research questions.

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

The p-value is 0 and is less than the significance level of 0.05, meaning we reject the null hypothesis. Cramer’s V is 0.03, indicating a weak association between a dog’s gender and its spay/neuter status. These results show that technically there is an association, but it is weak and meaningless in practice.

Chi-Square Test 2 Results:

![Image](https://github.com/user-attachments/assets/b03fd056-38cd-436c-ae90-183db7a368a2)
![Image](https://github.com/user-attachments/assets/aa5de5f1-463a-47f4-999d-37897a8e3c51)

The p-value is 0 and is less than the significance level of 0.05, meaning we reject the null hypothesis. Cramer’s V is 0.13, indicating a weak association between a dog’s spay/neuter status and the borough where the bite incident occurred. These results show that technically there is an association, but it is weak and meaningless in practice. 

# Course of Action
Based on Chi-Square Test 1, the DOHMH could emphasize the importance of spaying and neutering dogs through their website or social media ads. Even though the association between a dog’s gender and its spay/neuter status is weak, these messages can help raise public awareness among New Yorkers.

Based on Chi-Square Test 2, the DOHMH could focus on conducting public campaign programs in boroughs where more dogs that aren’t spayed/neutered are reported. Even though the association between a dog’s spay/neuter status and the borough where the incident occurred is weak, campaign programs can still help raise public awareness to help prevent dog bite incidents.
