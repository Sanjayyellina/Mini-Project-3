# Mini-Project-3


### 📌 Title and Objective

**Title**: *How Does Inflation Affect Different Types of Crime in Los Angeles?*

**Objective**:
This project investigates the relationship between inflation and various categories of crime in the city of Los Angeles(only dataset available with large crime data). The main focus is to determine whether economic stress—measured using the Consumer Price Index (CPI)—leads to increases in certain types of criminal behavior, particularly financially or emotionally driven offenses such as theft, assault, or robbery.

Understanding these relationships is critical to advance the public good. In times of economic instability, vulnerable communities may become more susceptible to engage in or becoming victims of crime. Insights from this study can help policymakers, law enforcement, and community organizations to develop  data-informed interventions to reducde crime during inflationary periods. This may include expanding the social support, improving economic resilience, or increasing law enforcement presence at high-risk areas.



### 📊 Data and Hypothesis Development

1. Data Description

This project draws from two key datasets that together represent crime activity in Los Angeles from 2010 through 2023:

Crime Dataset 1 (2010–2019): Sourced from data.gov and some missing data .
Crime Dataset 2 (2020–2023): sourced from same website data.gov .
Inflation Data: Monthly CPI data from the Bureau of Labor Statistics (2010–2017) used as the main economic indicator.
Supplemental data includes population counts, unemployment statistics, and demographic information such as victim age.

I was drawn to this topic because it felt very real — inflation is something many people worry about, and crime affects communities directly. Combining these both gave me a chance to use my skills on something socially relevant. It also helped me strengthen my data cleaning and merging skills since I was working with different formats and time scales.

#### 2. Summary Statistics

* Observations: 3,117,370
* Key Variables:
* CPI: Mean = 240.47 (SD = 9.29)
* Victim Age: Mean = 30.91 (SD = 21.11)


#### 3. Crime Type Distribution

The top 15 crime categories accounted for 79.2% of all reported crimes. Theft and burglary together represented over 60% of this total, with vehicle-related crimes making up a significant portion. Assault-related incidents (including intimate partner violence) and fraud (primarily identity theft) were also prevalent.

This distribution confirmed the need to analyze inflation's impact on different types of crimes individually, especially those involving financial or emotional motivation.

---

### 🛠️ Analysis

#### 1. Methodology: Simple Linear Regression

Step 1: Preparing the Data

Removed records with incorrect or missing values (like negative victim ages)

Grouped crimes by category and aggregated them monthly

Joined the crime data with monthly CPI data (for the years where both were complete)

Step 2: Regression Analysis

I ran simple linear regressions for each crime type, using CPI as the predictor and monthly crime count as the outcome. This allowed me to compare how inflation might be related to each type of crime.

Step 3: Time Trends and Visualization

Created line charts to compare CPI and crime trends over time

Highlighted important time periods like the COVID lockdown and 2022 inflation peak

Used Tableau to explore how crime varied by location across Los Angeles

#### 2. Visual Time Series Analysis

* **Assault**: Crime levels declined significantly during the COVID-19 pandemic due to lockdowns and decreased social contact, despite inflation peaking. Post-pandemic, assault levels rose again, but inflation did not seem to be the driving factor. Social constraints had more influence than economic variables.

* **Theft**: Showed a strong upward trend post-pandemic, closely mirroring the CPI rise. Financial hardship likely increased theft motivation, suggesting a positive association between inflation and theft.

* **Robbery**: Although there was an increase post-pandemic, robbery rates didn’t show a strong correlation with inflation. The pattern seemed more related to public mobility and enforcement rather than CPI.

* **Burglary**: Rates dropped during the pandemic (likely due to more people staying home) and remained variable afterward. While there was some increase with inflation, other factors like housing security likely had more influence.

* **Fraud**: Spiked during the pandemic, likely due to scams and increased digital transactions. Inflation did not show a strong direct impact.

#### 3. Tableau Visualizations

I also created dashboards in Tableau to examine spatial and categorical crime trends across Los Angeles neighborhoods. These visuals complemented the regression results and made patterns more interpretable for policy applications.

---

### 📈 Regression Results Summary

* **Assault vs CPI**:

  * R² = 0.326
  * β (CPI) = 24.23, p < 0.001
  * Interpretation: As inflation increases, assault incidents also rise significantly.

* **Theft vs CPI**:

  * R² = 0.438
  * β (CPI) = 31.46, p < 0.001
  * Interpretation: Strongest relationship found; theft rises significantly with inflation.

* **Burglary vs CPI**:

  * R² = 0.013, p = 0.267
  * Interpretation: CPI is not a significant predictor of burglary.

* **Robbery vs CPI**:

  * R² = 0.002, p = 0.643
  * Interpretation: No meaningful relationship.

* **Fraud vs CPI**:

  * R² = 0.011, p = 0.299
  * Interpretation: No significant correlation.

These results confirm that inflation has a statistically significant impact on **assault and theft**, while its relationship with other crime categories appears negligible.

###  Key Results

Theft had the clearest relationship with inflation (R² = 0.438, p < 0.001) — it rose alongside CPI

Assault was also significantly related to inflation (R² = 0.326, p < 0.001), though other factors like social restrictions likely influenced it too

Burglary, Robbery, and Fraud didn’t show strong or consistent relationships with CPI

From this, it looks like crimes tied to financial pressure (like theft) are more responsive to inflation than others that may depend more on opportunity or intent.

### 💬 Reflection

This project deepened my understanding of how economic variables like inflation can influence social behavior, including crime. It was interesting to see how certain crimes, particularly those rooted in financial desperation (e.g., theft), rose in direct response to inflation. On the other hand, crimes like robbery or fraud appeared to be more situational or opportunistic and not closely linked to inflation.

A key learning was the value of segmenting crime by type. If I had used only an aggregated crime total, I might have missed these individual patterns. I also saw the benefit of combining statistical models with visual storytelling (e.g., Tableau) to interpret social trends more clearly.

In the future, I would like to explore multivariate models including unemployment, income inequality, or social services availability to better explain the fluctuations. Time-lagged regression could also help evaluate whether inflation impacts crime with a delay.

Overall, this project showed me that economic data isn't just about markets—it can be a lens to understand and improve public safety too.

---
