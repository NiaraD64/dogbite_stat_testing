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

Since both tests use categorical variables, I conducted the Chi-Square Test of Independence.
For both Chi-Square tests, “Unknown” and “Other” were excluded from the tests. These values were only filled during data cleaning to prevent introducing bias, and including them wouldn’t be relevant to answering the research questions.

Research Question 1: Is there an association between a dog’s gender and its spay/neuter status in reported bite incidents?

Null Hypothesis: There is no statistically significant association between a dog’s gender and its spay/neuter status in bite incidents.

Alternative Hypothesis: There is a statistically significant association between a dog’s gender and its spay/neuter status in bite incidents.

Research Question 2: Is there an association between a dog’s spay/neuter status and the borough where the bite incident occurred?

Null Hypothesis: There is no statistically significant association between a dog’s spay/neuter status and the borough in which the bite incident occurred.

Alternative Hypothesis: There is a statistically significant association between a dog’s spay/neuter status and the borough in which the bite incident occurred.

# What I Learned
